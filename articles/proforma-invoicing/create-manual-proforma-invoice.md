---
title: Stvaranje ručnog predračuna
description: U ovoj temi nalaze se informacije o stvaranju predračuna.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ad85262482f782391eca85f46ca0e63a887c89f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896092"
---
# <a name="create-a-manual-proforma-invoice"></a>Stvaranje ručnog predračuna

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Fakturiranje upraviteljima projekata pruža drugu razinu odobrenja prije nego što stvore fakture za klijente. Prva razina odobrenja završena je kada se odobre unosi vremena i troškova koje pošalju članovi projektnog tima.

Dynamics 365 Project Operations nije osmišljen za generiranje faktura namijenjenih klijentima, iz sljedećih razloga:

- Ne sadrži porezne informacije.
- Ne može pretvoriti druge valute u valutu fakture pomoću ispravno konfiguriranih tečajeva.
- Ne može ispravno oblikovati fakture tako da se mogu ispisati.

Umjesto toga, za stvaranje faktura namijenjenih klijentima možete upotrijebiti financijski ili računovodstveni sustav koji upotrebljava podatke iz generiranih prijedloga faktura.

## <a name="creating-project-invoices"></a>Stvaranje faktura za projekt

Istodobno možete stvoriti jednu fakturu projekta ili više njih. Možete ih stvoriti ručno ili ih konfigurirati tako da se generiraju prilikom automatskog pokretanja.

### <a name="manually-create-project-invoices"></a>Ručno stvaranje faktura za projekt 

Na stranici popisa **Projektni ugovori** možete stvoriti fakture projekta zasebno za svaki ugovor projekta ili možete skupno stvoriti fakture za više ugovora projekta.

Poduzmite ovaj korak da biste stvorili fakturu za određeni ugovor projekta.

- Na stranici popisa **Ugovori projekta** otvorite ugovor o projektu, a zatim odaberite **Stvori fakturu.**

    Faktura se generira za sve transakcije za odabrani ugovor projekta koje imaju status **Spremno za fakturiranje**. Te transakcije uključuju vrijeme, troškove, kontrolne točke i retke ugovora temeljene na proizvodu.

Poduzmite ove korake da biste skupno stvorili fakture.

1. Na stranici popisa **Ugovori projekta** odaberite jedan ili više ugovora projekta za koje morate stvoriti fakturu, a zatim odaberite **Stvori fakture projekta**.

    Poruka upozorenja obavještava vas da je moguća odgoda prije stvaranja faktura. Prikazan je i postupak.

2. Odaberite **U redu** da biste zatvorili okvir poruke.

    Generira se faktura za sve transakcije u retku ugovora koje imaju status **Spremno za fakturiranje**. Te transakcije uključuju vrijeme, troškove, kontrolne točke i retke ugovora temeljene na proizvodu.

3. Da biste vidjeli generirane fakture, idite na **Prodaja** \> **Naplata** \> **Fakture**. Vidjet ćete jednu fakturu za svaki ugovor projekta.

### <a name="set-up-automated-creation-of-project-invoices"></a>Postavljanje automatskog stvaranja faktura za projekt 

Slijedite ove korake za konfiguraciju automatskog pokretanja faktura.

1. Idite u **Postavke** \> **Skupni poslovi**.
2. Stvorite skupni posao i dodijelite mu naziv **Stvaranje faktura aplikacije Project Operations**. Naziv skupnog posla mora sadržavati pojam "Stvaranje faktura".
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
> Skupno fakturiranje izvršava se samo za retke ugovora o projektu koji su konfigurirani prema rasporedu faktura. Ugovorni redci s načinom naplate fiksne cijene moraju imati konfigurirane prekretnice. Redak projektnog ugovora s vremenskim i materijalnim načinom naplate treba imati postavku rasporeda računa na temelju datuma. Isto se odnosi i na redak ugovora koji se temelji na projektu.      
 
### <a name="edit-a-draft-invoice"></a>Uređivanje skice fakture

Kada stvorite skicu fakture projekta, sve nenaplaćene prodajne transakcije stvorene kada su unosi vremena i troška odobreni dohvaćaju se u fakturu. Dok je faktura još u fazi skice, možete napraviti sljedeće prilagodbe:

- Izbrišite ili uredite pojedinosti retka fakture.
- Uredite i prilagodite količinu i vrstu naplate.
- Izravno dodajte vrijeme, trošak i naknade kao transakcije u fakturi. Ovu značajku možete koristiti ako je redak fakture mapiran na redak ugovora koji omogućuje navedene klase transakcija.

Odaberite **Potvrdi** da biste potvrdili fakturu. Radnja potvrde jednosmjerna je radnja. Kada odaberete **Potvrdi**, sustav postavlja fakturu samo za čitanje i stvara naplaćene stvarne podatke o prodaji na temelju svake pojedinosti retka fakture za svaki redak fakture. Ako se pojedinost retka fakture poziva na nenaplaćeni stvarni podatak o prodaji, sustav također poništava nenaplaćeni stvarni podatak o prodaji. (Sve pojedinosti retka fakture stvorene na temelju unosa vremena ili troška pozivaju se na nenaplaćeni stvarni podatak o prodaji.) Sustavi integracije glavne knjige mogu koristiti to poništavanje za promjenu rada projekta u tijeku (WIP) u računovodstvene svrhe.

### <a name="correct-a-confirmed-invoice"></a>Ispravak potvrđene fakture

Potvrđene fakture mogu se urediti (ispraviti). Kada ispravite potvrđenu fakturu, stvara se nova skica ispravljene fakture. Budući da se pretpostavlja da želite poništiti sve transakcije i količine iz izvorne fakture, ta ispravljena faktura uključuje sve transakcije iz izvorne fakture, a sve količine navedene u njoj iznose 0 (nula).

Ako transakcije ne zahtijevaju ispravak, možete ih ukloniti iz skice ispravljene fakture. Ako želite poništiti ili vratiti samo djelomičnu količinu, polje **Količina** možete urediti u pojedinosti retka. Ako otvorite pojedinost retka fakture, možete vidjeti izvornu količinu fakture. Zatim možete urediti trenutačnu količinu fakture tako da je manja ili veća od izvorne količine fakture.

Kada potvrdite ispravljenu fakturu, izvorni naplaćeni stvarni podatak o prodaji mijenja se i stvara se novi naplaćeni stvarni podatak o prodaji. Ako je količina manja, razlika će dovesti i do stvaranja novog nenaplaćenog stvarnog podatka o prodaji. Na primjer, ako je izvorna naplaćena prodaja obuhvaćala osam sati, a pojedinost retka ispravljene fakture sadrži manju količinu od šest sati, vraća se izvorni redak naplaćene prodaje i stvaraju se dva nova stvarna podatka:

- Naplaćeni stvarni podatak o prodaji za šest sati.
- Nenaplaćeni stvarni podatak o prodaji za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, ovisno o pregovorima s klijentom.
