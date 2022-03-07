---
title: Nadogradnja s automatizacije projektnih servisa na projektne operacije
description: Ovaj tema pruža pregled procesa nadogradnje iz Microsoft Dynamics 365 Project Service Automation sustava u Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954289"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadogradnja s automatizacije projektnih servisa na projektne operacije

Uzbuđeni smo što možemo najaviti prvu od tri faze nadogradnje od Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations. Ovaj tema pruža pregled za kupce koji kreću na ovo uzbudljivo putovanje. Buduće teme uključivat će razmatranja razvojnih programera i pojedinosti o poboljšanjima značajki. Oni ne samo da će vam pružiti smjernice koje će vam pomoći da se pripremite za nadogradnju na projektne operacije, već će vam i objasniti što možete očekivati nakon nadogradnje.

Program isporuke nadogradnje bit će podijeljen u tri faze.

| Nadogradnja isporuke | Faza 1 (siječanj 2022.) | Faza 2 (travanjski val 2022.) | Faza 3 (travanjski val 2022.) |
|------------------|------------------------|---------------------------|---------------------------|
| Nema ovisnosti o strukturi raščlambe rada (WBS) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS u trenutačno podržanim granicama projektnih operacija | | :heavy_check_mark: | :heavy_check_mark: |
| WBS izvan trenutno podržanih ograničenja projektnih operacija, uključujući podršku za klijent projekta za stolna računala | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Značajke procesa nadogradnje 

Kao dio postupka nadogradnje, dodali smo zapisnike nadogradnje na kartu web-mjesta kako bi administratori lakše dijagnosticirali kvarove. Osim novog sučelja, dodat će se i nova pravila provjere valjanosti kako bi se osigurao integritet podataka nakon nadogradnje. U postupak nadogradnje dodat će se sljedeće provjere valjanosti.

| Provjere valjanosti | Faza 1 (siječanj 2022.) | Faza 2 (travanjski val 2022.) | Faza 3 (travanjski val 2022.) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS će se provjeriti u odnosu na uobičajena kršenja integriteta podataka (na primjer, dodjele resursa koje su povezane s istim nadređenim zadatkom, ali imaju različite nadređene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će biti provjeren u odnosu na [poznata ograničenja projekta za web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će se provjeriti u odnosu na poznata ograničenja klijenta programa Project za stolna računala. | | :heavy_check_mark: | :heavy_check_mark: |
| Resursi koje je moguće rezervirati i kalendari projekata vrednovat će se u odnosu na uobičajene nespojive iznimke pravila kalendara. | | :heavy_check_mark: | :heavy_check_mark: |

U fazi 2, korisnici koji nadograde na Project Operations nadogradit će svoje postojeće projekte na iskustvo samo za čitanje za planiranje projekata. U ovom iskustvu samo za čitanje, puni WBS bit će vidljiv u rešetki za praćenje. Da bi uredili WBS, voditelji projekata mogu **odabrati Pretvori** na **glavnoj** stranici Projekti. Pozadinski proces zatim će ažurirati projekt tako da podržava novo iskustvo zakazivanja projekta iz programa Project za web. Ova faza je prikladna za klijente koji imaju projekte koji se uklapaju u [poznate granice Projekta za web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

U trećoj fazi dodat će se podrška za klijenta projekta za stolna računala u korist korisnika koji žele nastaviti uređivati svoje projekte iz te aplikacije. Međutim, ako se postojeći projekti pretvore u novi projekt za web-sučelje, pristup dodatku bit će onemogućen za svaki pretvoreni projekt.

## <a name="prerequisites"></a>Preduvjeti

Da bi ispunjavao uvjete za nadogradnju prve faze, korisnik mora zadovoljiti sljedeće kriterije:

- Ciljno okruženje ne smije sadržavati zapise u **entitetu** msdyn_projecttask.
- Valjane licence za operacije projekta moraju biti dodijeljene svim aktivnim korisnicima klijenta. 
- Kupac mora provjeriti valjanost postupka nadogradnje u najmanje jednom neproizvodnom okruženju koje ima reprezentativni skup podataka koji je usklađen s proizvodnim podacima.
- Ciljno okruženje mora se ažurirati na Project Service Automation Update Release 38 ili noviji.

Preduvjeti za fazu 2 i fazu 3 ažurirat će se kako se približavaju datumi opće dostupnosti.

## <a name="licensing"></a>Licenciranje

Ako imate aktivne licence za automatizaciju servisa Project Service Automation, možete instalirati i koristiti Operacije projekta, što uključuje sve mogućnosti automatizacije project service i još mnogo toga. Na taj način možete testirati mogućnosti projektnih operacija dok nastavite koristiti automatizaciju usluga projekta u proizvodnji. Nakon isteka licenci za automatizaciju servisa project service morat ćete prijeći na projektne operacije. Kada planirate ovaj prijelaz, morate uzeti u obzir činjenicu da licenca za operacije projekta ne uključuje licencu za automatizaciju servisa Project.

## <a name="testing-and-refactoring-customizations"></a>Testiranje i refaktoriranje prilagodbi

Kao početnu točku, uvezite sve prilagodbe u čisto okruženje projektnih operacija (lite) kako biste potvrdili da je uvoz uspješan i da se poslovne operacije ponašaju prema očekivanjima.

Evo nekoliko stvari na koje treba paziti:

- Uvoz možda neće uspjeti zbog nedostajućih ovisnosti. Drugim riječima, prilagodbe upućuju na polja ili druge komponente koje su uklonjene u projektnim operacijama. U tom slučaju uklonite te ovisnosti iz razvojnog okruženja.
- Ako neupravljana i upravljana rješenja sadrže komponente koje nisu prilagođene, uklonite te komponente iz rješenja. Na primer, kada prilagodite **entitet** "Projekt", u rešenje dodajte samo zaglavlje entiteta. Nemojte dodavati sva polja. Ako ste prethodno dodali sve potkomponente, možda ćete morati ručno stvoriti novo rješenje i dodati mu relevantne komponente.
- Obrasci i prikazi možda neće izgledati neočekivano. U nekim okolnostima, ako ste prilagodili neki od gotovih obrazaca ili prikaza, prilagodbe mogu spriječiti stupanje na snagu novih ažuriranja u projektnim operacijama. Da biste utvrdili te probleme, preporučujemo da usporedno pregledate čistu instalaciju operacija programa Project i instalaciju operacija programa Project koja uključuje vaše prilagodbe. Usporedite najčešće korištene obrasce u tvrtki da biste potvrdili da vaša verzija obrasca još uvijek ima smisla i da ne nedostaje nešto iz čiste verzije obrasca. Napravite istu vrstu usporednog pregleda za sve prikaze koje ste prilagodili.
- Poslovna logika možda neće uspjeti tijekom izvođenja. Budući da se reference na polja u dodacima ne provjeravaju u trenutku uvoza, poslovna logika možda neće uspjeti zbog referenci na polja koja više ne postoje i možda ćete primiti poruku o pogrešci sličnu sljedećem primjeru: "Entitet "Projekt" ne sadrži atribut s nazivom = 'msdyn_plannedhours' i NameMapping = 'Logical'." U tom slučaju izmijenite prilagodbe tako da koriste nova polja. Ako koristite automatski generirane proxy klase i jake reference tipa u svojoj logici dodatka, razmislite o regeneraciji tih proxyja iz čiste instalacije. Na taj način možete jednostavno identificirati sva mjesta na kojima dodaci ovise o zastarjelim poljima.

Kada ažurirate prilagodbe da biste čisto uvezli projektne operacije, prijeđite na sljedeće korake.

## <a name="end-to-end-testing-in-lower-environments"></a>End-to-end testiranje u nižim okruženjima

### <a name="run-the-upgrade-in-production"></a>Pokretanje nadogradnje u proizvodnji

1. U Power Platform centru za administratore pronađite i odaberite okruženje. Zatim u aplikacijama pronađite i odaberite **Dynamics 365 Project Operations**.
2. Odaberite **Instaliraj** da biste pokrenuli nadogradnju. Power Platform Centar za administratore predstavit će ovu instalaciju kao novu instalaciju. Međutim, otkrit će se prisutnost starije verzije automatizacije servisa Project Service i nadograditi postojeća instalacija.

    Nakon dovršetka nadogradnje okruženje bi trebalo pokazati da su projektne operacije instalirane i da automatizacija servisa Project Service nije instalirana.

    > [!NOTE]
    > Ovisno o količini podataka u okruženju, nadogradnja može potrajati nekoliko sati. Osnovni tim koji upravlja nadogradnjom trebao bi planirati u skladu s tim i pokrenuti nadogradnju tijekom neradnog radnog vremena. U nekim slučajevima, ako je količina podataka velika, nadogradnja bi se trebala pokrenuti tijekom vikenda. Odluka o rasporedu trebala bi se temeljiti na rezultatima ispitivanja u nižim okruženjima.

3. Prema potrebi nadogradite prilagođena rješenja. U ovom trenutku implementirajte sve promjene koje ste napravili na prilagodbama u [odjeljku Testiranje i refaktoriranje prilagodbi](#testing-and-refactoring-customizations) ovog tema.
4. Idite na **Rješenja postavki** \> **i** odaberite deinstalaciju **rješenja Zastarjele komponente operacija** projekta.

    Ovo rješenje je privremeno rješenje koje sadrži postojeći podatkovni model i komponente koje su prisutne tijekom nadogradnje. Uklanjanjem ovog rješenja uklanjate sva polja i komponente koje se više ne koriste. Na taj način pojednostavljujete sučelje i olakšavate integraciju i proširenje.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Velike promjene između automatizacije projektnih servisa i projektnih operacija

Ovaj odjeljak sadrži sažetak glavnih promjena koje možete očekivati između automatizacije usluga projekta i operacija projekta.

### <a name="project-planning"></a>Planiranje projekta

Mogućnosti planiranja projekta u operacijama projekta više se ne oslanjaju na kombiniranu logiku na strani klijenta i logiku na strani poslužitelja. Umjesto toga, Projektne operacije koriste Project za web kao modul za zakazivanje. Ova promjena u mogućnostima zakazivanja omogućuje nekoliko novih značajki, kao što su prikazi ploča i gantoteka, planiranje temeljeno na [resursima, stavke kontrolnog popisa](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) zadataka i načini zakazivanja projekata. Nove mogućnosti zakazivanja podržava i bogat skup novih [sučelja za programiranje aplikacija (API-jeva).](../project-management/schedule-api-preview.md) Ovi API-jeji namijenjeni su osiguravanju da nijedna programska operacija za stvaranje, ažuriranje ili brisanje entiteta u WBS-u ne oštećuje izračunata polja u rasporedu.

## <a name="billing-and-pricing"></a>Naplata i određivanje cijene

Kao dio kontinuiranih ulaganja u projektne operacije, dostupno je nekoliko novih mogućnosti u naplati i određivanju cijena. Evo nekoliko primjera:

- [Bilježenje korištenja materijala na projektima i projektnim zadacima](../material/material-usage-log.md)
- [Upravljanje kooperantima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Predujmovi i ugovori koji e temelje na povremenim plaćanjima](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status i provjere valjanosti ugovora koji ne premašuju](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Naplata na temelju zadataka

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Koje su vrste implementacije trenutno podržane za nadogradnju?

| Izvor                                                 | Cilj                                                    | Stanje                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementacija operacija projekta Lite                        | Podržano               |
| Dynamics 365 Finance Upravljanje projektima i računovodstvo | Implementacija operacija projekta Lite                        | Trenutno nije podržano |
| Upravljanje financijskim projektima i računovodstvo              | Project Operations za scenarije temeljene na resursima / bez zaliha     | Trenutno nije podržano |
| Upravljanje financijskim projektima i računovodstvo              | Project Operations za scenarije temeljene na zalihama / radnim nalozima | Trenutno nije podržano |
| Automatizacija servisa projekta 3.x                         | Project Operations za scenarije temeljene na resursima / bez zaliha     | Trenutno nije podržano |
| Projekt za web (namjensko okruženje)            | Implementacija operacija projekta Lite                        | Trenutno nije podržano |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako instalirati operacije programa Project prije nego što alat za nadogradnju postane dostupan?

Postoje dvije mogućnosti instalacije operacija programa Project prije nego što alat za nadogradnju postane dostupan:

- Dodjela novog okruženja.
- Zasebno implementirajte operacije projekta u bilo kojoj prodajnoj organizaciji u kojoj nije prisutna automatizacija servisa projekta.

> [!NOTE]
> Ako je automatizacija servisa Project instalirana u tvrtki ili ustanovi, ali nije korištena, može se deinstalirati. Nakon što u potpunosti uklonite automatizaciju usluga projekta, operacije projekta mogu se instalirati u istu tvrtku ili ustanovu.
