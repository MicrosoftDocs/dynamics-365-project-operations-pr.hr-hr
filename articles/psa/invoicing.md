---
title: Fakturiranje u sustavu Project Service Automation
description: U ovom se članku navode informacije o fakturiranju.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: fa036dda6514449b04e1416bde2cd9c21fc558b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926813"
---
# <a name="invoicing-in-project-service-automation"></a>Fakturiranje u sustavu Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fakturiranje u sustavu Dynamics 365 Project Service Automation korisno je jer upraviteljima projekata pruža drugu razinu odobrenja prije nego što stvore fakture za klijente. Prva razina odobrenja završena je kada se odobre unosi vremena i troškova koje pošalju članovi projektnog tima.

PSA nije osmišljen za generiranje faktura namijenjenih klijentima, iz sljedećih razloga:

- Ne sadrži porezne informacije.
- Ne može pretvoriti druge valute u valutu fakture pomoću ispravno konfiguriranih tečajeva.
- Ne može ispravno oblikovati fakture tako da se mogu ispisati.

Umjesto toga, možete koristiti financijski ili računovodstveni sustav za stvaranje faktura namijenjenih klijentima koje koriste podatke iz prijedloga faktura koji su generirani u PSA-u.

## <a name="creating-project-invoices-in-psa"></a>Stvaranje faktura projekta u PSA-u

Istodobno možete stvoriti jednu fakturu projekta ili više njih. Možete ih stvoriti ručno ili ih konfigurirati tako da se generiraju prilikom automatskog pokretanja.

### <a name="manually-create-project-invoices-in-psa"></a>Ručno stvaranje faktura projekta u PSA-u

Na stranici popisa **Projektni ugovori** možete stvoriti fakture projekta zasebno za svaki ugovor projekta ili možete skupno stvoriti fakture za više ugovora projekta.

Poduzmite ovaj korak da biste stvorili fakturu za određeni ugovor projekta.

- Na stranici popisa **Ugovori projekta** otvorite ugovor o projektu, a zatim odaberite **Stvori fakturu.**

    ![Stvaranje faktura projekta za određeni ugovor projekta.](media/CreateProjectInvoicesOneByOne.png)

    Faktura se generira za sve transakcije za odabrani ugovor projekta koje imaju status **Spremno za fakturiranje**. Te transakcije uključuju vrijeme, troškove, kontrolne točke i retke ugovora temeljene na proizvodu.

Poduzmite ove korake da biste skupno stvorili fakture.

1. Na stranici popisa **Ugovori projekta** odaberite jedan ili više ugovora projekta za koje morate stvoriti fakturu, a zatim odaberite **Stvori fakture projekta**.

    ![Skupno stvaranje faktura projekta.](media/CreateProjectInvoicesBulk.png)

    Poruka upozorenja obavještava vas da je moguća odgoda prije stvaranja faktura. Prikazan je i postupak.

2. Odaberite **U redu** da biste zatvorili okvir poruke.

    Generira se faktura za sve transakcije u retku ugovora koje imaju status **Spremno za fakturiranje**. Te transakcije uključuju vrijeme, troškove, kontrolne točke i retke ugovora temeljene na proizvodu.

3. Da biste vidjeli generirane fakture, idite na **Prodaja** \> **Naplata** \> **Fakture**. Vidjet ćete jednu fakturu za svaki ugovor projekta.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Postavljanje automatskog stvaranja faktura projekta u PSA-u

Poduzmite ove korake za konfiguriranje automatskog pokretanja faktura u PSA-u.

1. Idite na **Project Service** \> **Postavke** \> **Skupni poslovi**.
2. Stvorite skupni posao i dodijelite mu naziv **PSA – stvaranje faktura**. Naziv skupnog posla mora sadržavati pojam "Stvaranje faktura".
3. U polju **Vrsta posla** odaberite **Ništa**. Prema zadanim postavkama mogućnosti **Dnevna učestalost** i **Aktivno** postavljene su na **Da**.
4. Odaberite **Pokreni tijek rada**. U dijaloškom okviru **Pretraživanje zapisa** vidjet ćete tri tijeka rada:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Odaberite **ProcessRunCaller**, a zatim **Dodaj**.
6. U sljedećem dijaloškom okviru odaberite **U redu**. Nakon tijeka rada **Sleep** slijedi tijek rada **Process**.

    U petom koraku možete odabrati i **ProcessRunner**. Zatim, kada odaberete **U redu**, nakon tijeka rada **Process** slijedi tijek rada **Sleep**.

Tijekovi rada **ProcessRunCaller** i **ProcessRunner** stvaraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** jest tijek rada koji stvara fakture. Prolazi kroz sve retke ugovora za koje je potrebno stvoriti fakture i stvara fakture za te retke. Da bi se odredili reci ugovora za koje je potrebno stvoriti fakture, posao traži datume stvaranja faktura za retke ugovora. Ako reci ugovora koji pripadaju jednom ugovoru imaju isti datum stvaranja fakture, transakcije se kombiniraju u jednu fakturu koja ima dva retka fakture. Ako nema transakcija za stvaranje faktura, posao preskače stvaranje faktura.

Nakon pokretanja funkcije **ProcessRunner** poziva se **ProcessRunCaller**, navodi se vrijeme završetka i funkcija se zatvara. **ProcessRunCaller** zatim pokreće mjerač vremena koji se izvodi 24 sata od navedenog vremena završetka. Po završetku izvođenja mjerača vremena funkcija **ProcessRunCaller** zatvara se.

Skupni postupak stvaranja faktura ponavljajući je posao. Ako se taj skupni postupak izvodi više puta, stvaraju se višestruke instance posla koje uzrokuju pogreške. Stoga biste trebali pokrenuti skupni postupak samo jednom i ponovno ga pokrenuti samo ako se prestane izvoditi.

> [!NOTE]
> Paketno fakturiranje na usluzi Project Service Automation pokreće se samo za retke projektnih ugovora koji su konfigurirani rasporedima faktura. Ugovorni redci s načinom naplate fiksne cijene moraju imati konfigurirane prekretnice. Redak projektnog ugovora s vremenskim i materijalnim načinom naplate treba imati postavku rasporeda računa na temelju datuma. Informacije o postavljanju učestalosti fakturiranja u kontekstu projekta koji se temelji na retku ponude navedene su u članku [Ponude i redci ponude](basic-quote-lines.md#invoice-schedule). Isto se odnosi i na redak ugovora koji se temelji na projektu.      
 
### <a name="edit-a-draft-psa-invoice"></a>Uređivanje skice PSA fakture

Kada stvorite skicu fakture projekta, sve nenaplaćene prodajne transakcije stvorene kada su unosi vremena i troška odobreni dohvaćaju se u fakturu. Dok je faktura još u fazi skice, možete napraviti sljedeće prilagodbe:

- Izbrišite ili uredite pojedinosti retka fakture.
- Uredite i prilagodite količinu i vrstu naplate.
- Izravno dodajte vrijeme, trošak i naknade kao transakcije u fakturi. Ovu značajku možete koristiti ako je redak fakture mapiran na redak ugovora koji omogućuje navedene klase transakcija.

Odaberite **Potvrdi** da biste potvrdili fakturu. Radnja potvrde jednosmjerna je radnja. Kada odaberete **Potvrdi**, sustav postavlja fakturu samo za čitanje i stvara naplaćene stvarne podatke o prodaji na temelju svake pojedinosti retka fakture za svaki redak fakture. Ako se pojedinost retka fakture poziva na nenaplaćeni stvarni podatak o prodaji, sustav također poništava nenaplaćeni stvarni podatak o prodaji. (Sve pojedinosti retka fakture stvorene na temelju unosa vremena ili troška pozivaju se na nenaplaćeni stvarni podatak o prodaji.) Sustavi integracije glavne knjige mogu koristiti to poništavanje za promjenu rada projekta u tijeku (WIP) u računovodstvene svrhe.

### <a name="correct-a-confirmed-psa-invoice"></a>Ispravak potvrđene PSA fakture

Potvrđene PSA fakture mogu se urediti (ispraviti). Kada ispravite potvrđenu fakturu, stvara se nova skica ispravljene fakture. Budući da se pretpostavlja da želite poništiti sve transakcije i količine iz izvorne fakture, ta ispravljena faktura uključuje sve transakcije iz izvorne fakture, a sve količine navedene u njoj iznose 0 (nula).

Ako transakcije ne zahtijevaju ispravak, možete ih ukloniti iz skice ispravljene fakture. Ako želite poništiti ili vratiti samo djelomičnu količinu, polje **Količina** možete urediti u pojedinosti retka. Ako otvorite pojedinost retka fakture, možete vidjeti izvornu količinu fakture. Zatim možete urediti trenutačnu količinu fakture tako da je manja ili veća od izvorne količine fakture.

Kada potvrdite ispravljenu fakturu, izvorni naplaćeni stvarni podatak o prodaji mijenja se i stvara se novi naplaćeni stvarni podatak o prodaji. Ako je količina manja, razlika će dovesti i do stvaranja novog nenaplaćenog stvarnog podatka o prodaji. Na primjer, ako je izvorna naplaćena prodaja obuhvaćala osam sati, a pojedinost retka ispravljene fakture sadrži manju količinu od šest sati, PSA mijenja izvorni redak naplaćene prodaje i stvara dva nova stvarna podatka:

- Naplaćeni stvarni podatak o prodaji za šest sati.
- Nenaplaćeni stvarni podatak o prodaji za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, ovisno o pregovorima s klijentom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
