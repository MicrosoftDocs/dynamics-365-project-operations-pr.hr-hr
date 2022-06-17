---
title: Predračuni za projekt
description: U ovom se članku nalaze informacije o proforma fakturama projekta u operacijama projekta.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934541"
---
# <a name="proforma-project-invoices"></a>Predračuni za projekt

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Upraviteljima projekata predračuni daju drugu razinu odobrenja prije nego što stvore fakture za klijente. Prva razina odobrenja završena je kada se odobre unosi vremena, troškova i materijala koje pošalju članovi projektnog tima.

Implementacija osnovne aplikacije Dynamics 365 Project Operations nije dizajnirana za generiranje faktura za klijente. Popis u nastavku pokazuje zašto se fakture ne mogu generirati:

- Ne sadrži porezne informacije.
- Nije moguće pretvoriti druge valute u valutu fakturiranja.
- Nije moguće pravilno oblikovati fakture za ispis.

Umjesto toga, možete upotrebljavati financijski ili računovodstveni sustav za stvaranje faktura namijenjenih klijentima koje upotrebljavaju podatke u generiranim ponudama faktura.

## <a name="creating-project-invoices"></a>Stvaranje faktura za projekt

Istodobno možete stvoriti jednu fakturu projekta ili više njih. Možete ih stvoriti ručno ili ih konfigurirati tako da se generiraju prilikom automatskog pokretanja.

### <a name="manually-create-project-invoices"></a>Ručno stvaranje faktura za projekt 

Na stranici popisa **Projektni ugovori** možete stvoriti fakture projekta zasebno za svaki ugovor projekta ili možete skupno stvoriti fakture za više ugovora projekta.

   - Kako biste stvorili fakturu za određeni ugovor o projektu, na stranici s popisom **Ugovori projekta** otvorite ugovor o projektu, a zatim odaberite **Stvori fakturu**.

   Faktura se generira za sve transakcije za odabrani ugovor projekta koje imaju status **Spremno za fakturiranje**. Te transakcije obuhvaćaju vrijeme, troškove, materijale, kontrolne točke, retke ugovora koji se temelje na proizvodima i ostale nefakturirane retke dnevnika prodaje koji su možda potvrđeni.

Za stvaranje skupnih faktura:

1. Na stranici popisa **Ugovori projekta** odaberite jedan ili više ugovora o projektu za koje stvarate fakturu, a zatim odaberite **Stvori fakture projekta**.
2. Poruka upozorenja obavještava vas da je moguća odgoda prije stvaranja faktura. Prikazan je i postupak. Odaberite **U redu** da biste zatvorili okvir poruke.

   Generira se faktura za sve transakcije u retku ugovora koje imaju status **Spremno za fakturiranje**. Te transakcije obuhvaćaju vrijeme, troškove, materijale, kontrolne točke, retke ugovora koji se temelje na proizvodima i ostale nefakturirane retke dnevnika prodaje koji su možda potvrđeni.

3. Prikažite generirane fakture tako da odete na **Prodaja** \> **Naplata** \> **Fakture**. Vidjet ćete jednu fakturu za svaki ugovor projekta.

### <a name="set-up-automated-creation-of-project-invoices"></a>Postavljanje automatskog stvaranja faktura za projekt 

Slijedite ove korake za konfiguraciju automatskog pokretanja faktura.

1. Idite u **Postavke** \> **Skupni poslovi**.
2. Stvorite skupni posao i dodijelite mu naziv **Stvaranje faktura aplikacije Project Operations**. Naziv skupnog posla mora sadržavati pojam "Stvaranje faktura".
3. U polju **Vrsta posla** odaberite **Ništa**. Prema zadanim postavkama mogućnosti **Dnevna učestalost** i **Aktivno** postavljene su na **Da**.
4. Odaberite **Pokreni tijek rada**. U dijaloškom okviru **Pretraživanje zapisa** vidjet ćete sljedeće tijekove rada:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Odaberite **ProcessRunCaller**, a zatim **Dodaj**.
6. U sljedećem dijaloškom okviru odaberite **U redu**. Nakon tijeka rada **Sleep** slijedi tijek rada **Process**.

    U petom koraku možete odabrati i **ProcessRunner**. Zatim, kada odaberete **U redu**, nakon tijeka rada **Process** slijedi tijek rada **Sleep**.

Tijekovi rada **ProcessRunCaller** i **ProcessRunner** stvaraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** jest tijek rada koji stvara fakture. Taj tijek rada prolazi kroz sve retke ugovora za koje je potrebno stvoriti fakture i stvara fakture. Da bi se odredili reci ugovora za koje je potrebno stvoriti fakture, tijek rada traži datume stvaranja faktura za retke ugovora. Ako reci ugovora koji pripadaju jednom ugovoru imaju isti datum stvaranja fakture, transakcije se kombiniraju u jednu fakturu koja ima dva retka fakture. Ako nema transakcija za koje treba stvoriti fakture, fakture se ne stvaraju.

Nakon pokretanja funkcije **ProcessRunner** poziva se **ProcessRunCaller**, navodi se vrijeme završetka i funkcija se zatvara. **ProcessRunCaller** zatim pokreće mjerač vremena koji se izvodi 24 sata od navedenog vremena završetka. Po završetku izvođenja mjerača vremena funkcija **ProcessRunCaller** zatvara se.

Skupni postupak stvaranja faktura ponavljajući je posao. Ako se taj skupni postupak izvodi više puta, stvaraju se višestruke instance posla koje mogu uzrokovati pogreške. Kako biste zaobišli ovaj problem. pokrenite skupni postupak samo jednom i ponovno ga pokrenite samo ako se prestane izvršavati.

> [!NOTE]
> Skupno fakturiranje izvršava se samo za retke ugovora o projektu koji su konfigurirani prema rasporedu faktura. Ugovorni redci s načinom naplate fiksne cijene moraju imati konfigurirane prekretnice. Redak projektnog ugovora s vremenskim i materijalnim načinom naplate treba imati postavku rasporeda računa na temelju datuma. Isto se odnosi i na redak ugovora koji se temelji na projektu.      
 
### <a name="edit-a-draft-invoice"></a>Uređivanje skice fakture

Kada stvorite skicu fakture projekta, sve nenaplaćene prodajne transakcije stvorene kada su unosi vremena i troška odobreni dohvaćaju se u fakturu. Dok je faktura još u fazi skice, možete napraviti sljedeće prilagodbe:

- Izbrišite ili uredite pojedinosti retka fakture.
- Uredite i prilagodite količinu i vrstu naplate.
- Izravno dodajte vrijeme, trošak, materijal i naknade kao transakcije u fakturi. Ovu značajku možete koristiti ako je redak fakture mapiran na redak ugovora koji omogućuje navedene klase transakcija.

Odaberite **Potvrdi** da biste potvrdili fakturu. Ova je radnja jednosmjerna. Kada odaberete **Potvrdi**, sustav postaje samo za čitanje i stvara naplaćene stvarne podatke o prodaji na temelju svake pojedinosti retka fakture za svaki redak fakture. Ako se pojedinost retka fakture poziva na nenaplaćeni stvarni podatak o prodaji, stornira se nenaplaćeni stvarni podatak o prodaji. Svaka pojedinost retka fakture koja je stvorena na temelju unosa vremena, troškova ili utroška materijala odnosit će se na stvarnu nenaplaćenu prodaju. Sustavi integracije Glavne knjige ovaj storno mogu upotrebljavati za preokretanje nedovršenog rada na projektu (WIP, work in progress) u računovodstvene svrhe.

### <a name="correct-a-confirmed-invoice"></a>Ispravak potvrđene fakture

Potvrđene fakture mogu se urediti. Kada ispravite potvrđenu fakturu, stvara se nova skica ispravljene fakture. Budući da se pretpostavlja da želite poništiti sve transakcije i količine iz izvorne fakture, ta ispravljena faktura uključuje sve transakcije iz izvorne fakture, a sve količine navedene u njoj jesu nula.

Ako postoje transakcije koje ne trebaju ispravak, možete ih ukloniti iz skice ispravljene fakture. Ako želite poništiti ili vratiti samo djelomičnu količinu, polje **Količina** možete urediti u pojedinosti retka. Ako otvorite pojedinost retka fakture, možete vidjeti izvornu količinu fakture. Zatim možete urediti trenutačnu količinu fakture tako da je manja ili veća od izvorne količine fakture.

Kada potvrdite ispravljenu fakturu, izvorni naplaćeni stvarni podatak o prodaji mijenja se i stvara se novi naplaćeni stvarni podatak o prodaji. Ako je količina manja, razlika će dovesti do stvaranja novog nenaplaćenog stvarnog podatka o prodaji. Na primjer, ako je izvorna naplaćena prodaja obuhvaćala osam sati, a pojedinost retka ispravljene fakture sadrži manju količinu od šest sati, vraća se izvorni redak naplaćene prodaje i stvaraju se dva nova stvarna podatka:

- Naplaćeni stvarni podatak o prodaji za šest sati.
- Nenaplaćeni stvarni podatak o prodaji za preostala dva sata. Ova transakcija može biti ili naplaćena kasnije ili označena kao nenaplativa, ovisno o pregovorima s klijentom.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
