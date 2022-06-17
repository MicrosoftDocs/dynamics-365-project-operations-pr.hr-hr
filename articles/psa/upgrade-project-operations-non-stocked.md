---
title: Nadogradnja s automatizacije projektnih usluga na projektne operacije
description: U ovom se članku daje pregled procesa nadogradnje s Microsoft Dynamics 365 Project Service Automation na Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 30eb02240de6617d4c550ce59db2a454eee36f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912967"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadogradnja s automatizacije projektnih usluga na projektne operacije

Uzbuđeni smo što možemo najaviti prvu od tri faze nadogradnje od Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations. Ovaj članak pruža pregled za kupce koji kreću na ovo uzbudljivo putovanje. Budući članci uključivat će razmatranja razvojnih programera i detalje o poboljšanjima značajki. Oni ne samo da će pružiti smjernice koje će vam pomoći da se pripremite za nadogradnju na projektne operacije, već će objasniti i što možete očekivati nakon nadogradnje.

Program isporuke nadogradnje podijelit će se u tri faze.

| Isporuka nadogradnje | 1. faza (siječanj 2022.) | Faza 2 (travanjski val 2022.) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nema ovisnosti o strukturi raščlambe rada (WBS) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS u trenutno podržanim granicama projektnih operacija | | :heavy_check_mark: | :heavy_check_mark: |
| WBS izvan trenutno podržanih ograničenja projektnih operacija, uključujući podršku za klijent za stolna računala project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Značajke procesa nadogradnje 

Kao dio postupka nadogradnje dodali smo zapisnike nadogradnje na kartu web-mjesta kako bi administratori mogli lakše dijagnosticirati neuspjehe. Osim novog sučelja, dodat će se i nova pravila provjere valjanosti kako bi se osigurao integritet podataka nakon nadogradnje. U postupak nadogradnje bit će dodane sljedeće provjere valjanosti.

| Provjere valjanosti | 1. faza (siječanj 2022.) | Faza 2 (travanjski val 2022.) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS će biti potvrđen u odnosu na uobičajena kršenja integriteta podataka (na primjer, dodjele resursa koje su povezane s istim nadređenim zadatkom, ali imaju različite nadređene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će biti potvrđen u odnosu na [poznata ograničenja projekta za web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će biti potvrđen u odnosu na poznata ograničenja project desktop klijenta. | |  | :heavy_check_mark: |
| Resursi i kalendari projekata koji se mogu rezervirati vrednovat će se u odnosu na uobičajene nekompatibilne iznimke pravila kalendara. | | :heavy_check_mark: | :heavy_check_mark: |

U fazi 2 korisnicima koji nadograđuju na Projektne operacije postojeći projekti bit će nadograđeni na iskustvo samo za čitanje za planiranje projekata. U ovom iskustvu samo za čitanje, cijeli WBS bit će vidljiv u mreži za praćenje. Da biste uredili WBS, voditelji projekata mogu odabrati **Pretvori** na glavnoj **stranici Projekti**. Pozadinski proces zatim će ažurirati projekt tako da podržava novo iskustvo zakazivanja projekata iz programa Project for the Web. Ova faza je prikladna za korisnike koji imaju projekte koji se uklapaju u [poznate granice programa Project za web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

U trećoj fazi dodat će se podrška za klijent za stolna računala Project u korist korisnika koji žele nastaviti uređivati svoje projekte iz te aplikacije. Međutim, ako se postojeći projekti pretvore u novi projekt za web-iskustvo, pristup dodatku bit će onemogućen za svaki pretvoreni projekt.

## <a name="prerequisites"></a>Preduvjeti

Da bi ispunjavao uvjete za nadogradnju prve faze, kupac mora ispuniti sljedeće kriterije:

- Ciljno okruženje ne smije sadržavati zapise u entitetu **msdyn_projecttask**.
- Valjane licence za project operations moraju se dodijeliti svim aktivnim korisnicima klijenta. 
- Kupac mora provjeriti valjanost postupka nadogradnje u barem jednom neproizvodnom okruženju koje ima reprezentativni skup podataka koji je usklađen s podacima o proizvodnji.
- Ciljno okruženje mora se ažurirati na 41 (3.10.62.162 za ažuriranje automatizacije usluge projekta Project Service ili novije.

Preduvjeti za 2. i 3. fazu ažurirat će se kako se budu približavali opći datumi dostupnosti.

## <a name="licensing"></a>Licenciranje

Ako imate aktivne licence za automatizaciju usluga projekta, možete instalirati i koristiti Project Operations, što uključuje sve mogućnosti automatizacije project usluga i još mnogo toga. Na taj način možete testirati mogućnosti projektnih operacija dok nastavljate koristiti automatizaciju projektnih usluga u proizvodnji. Nakon isteka licenci za automatizaciju usluga projekta morat ćete prijeći na projektne operacije. Kada planirate taj prijelaz, morate uzeti u obzir činjenicu da licenca za Project Operations ne uključuje licencu za automatizaciju usluga projekta.

## <a name="testing-and-refactoring-customizations"></a>Testiranje i refaktoriranje prilagodbi

Kao polazište, uvezite sve prilagodbe u čisto okruženje project operations (lite) kako biste potvrdili da je uvoz uspješan i da se poslovne operacije ponašaju prema očekivanjima.

Evo nekoliko stvari na koje treba pripaziti:

- Uvoz možda neće uspjeti zbog nedostataka ovisnosti. Drugim riječima, prilagodbe se odnose na polja ili druge komponente uklonjene u operacijama projekta. U tom slučaju uklonite te ovisnosti iz razvojnog okruženja.
- Ako neupravljana i upravljana rješenja obuhvaćaju komponente koje nisu prilagođene, uklonite te komponente iz rješenja. Na primer, kada prilagodite **entitet Projekt**, u rešenje dodajte samo zaglavlje entiteta. Nemojte dodavati sva polja. Ako ste prethodno dodali sve podkomponente, možda ćete morati ručno stvoriti novo rješenje i dodati mu relevantne komponente.
- Obrasci i prikazi možda se neće pojaviti na očekivani način. U nekim okolnostima, ako ste prilagodili bilo koji od gotovih obrazaca ili prikaza, prilagodbe mogu spriječiti stupanje na snagu novih ažuriranja u operacijama projekta. Da biste identificirali te probleme, preporučujemo da napravite usporedni pregled čiste instalacije projektnih operacija i instalacije projektnih operacija koja uključuje vaše prilagodbe. Usporedite najčešće korištene obrasce u svojoj tvrtki kako biste potvrdili da vaša verzija obrasca još uvijek ima smisla i da joj nešto ne nedostaje iz čiste verzije obrasca. Učinite istu vrstu usporednog pregleda za sve prikaze koje ste prilagodili.
- Poslovna logika možda neće uspjeti u vrijeme izvođenja. Budući da reference na polja u dodacima nisu provjerene u trenutku uvoza, poslovna logika možda neće uspjeti zbog referenci na polja koja više ne postoje i možda ćete dobiti poruku o pogrešci koja nalikuje sljedećem primjeru: "Entitet "Projekt" ne sadrži atribut s nazivom = 'msdyn_plannedhours' i NameMapping = 'Logical'." U tom slučaju izmijenite prilagodbe tako da koriste nova polja. Ako u logici dodatka koristite automatski generirane proxy klase i jake reference tipa, razmislite o regeneraciji tih proxyja iz čiste instalacije. Na taj način možete lako identificirati sva mjesta na kojima vaši dodaci ovise o zastarjelim poljima.

Nakon što ažurirate prilagodbe da biste čisto uvezli projektne operacije, prijeđite na sljedeće korake.

## <a name="end-to-end-testing-in-development-environments"></a>End-to-end testiranje u razvojnim okruženjima

### <a name="initiate-upgrade"></a>Pokreni nadogradnju 

1. U centru za administratore Power Platform pronađite i odaberite svoje okruženje. Zatim u aplikacijama pronađite i odaberite **Dynamics 365 Project Operations**.
2. Odaberite **Instaliraj** da biste pokrenuli nadogradnju. Centar za administratore Power Platform predstavit će ovu instalaciju kao novu instalaciju. Međutim, otkrit će se prisutnost starije verzije automatizacije usluga projekta, a postojeća instalacija će biti nadograđena.

    Nakon dovršetka nadogradnje okruženje bi trebalo pokazati da su projektne operacije instalirane i da automatizacija projektnih usluga nije instalirana.

    > [!NOTE]
    > Ovisno o količini podataka u okruženju, nadogradnja može potrajati nekoliko sati. Temeljni tim koji upravlja nadogradnjom trebao bi planirati u skladu s tim i pokrenuti nadogradnju tijekom neradnog vremena. U nekim slučajevima, ako je količina podataka velika, nadogradnja bi se trebala izvoditi tijekom vikenda. Odluka o rasporedu trebala bi se temeljiti na rezultatima testiranja u nižim okruženjima.

3. Prema potrebi nadogradite prilagođena rješenja. U ovom trenutku implementirajte sve promjene koje ste napravili na prilagodbama u [odjeljku Testiranje i refaktoriranje prilagodbi](#testing-and-refactoring-customizations) ovog članka.
4. Otvorite **Rješenja postavki** \> **i** odaberite da biste deinstalirali **rješenje Komponente zastarjele** za operacije projekta.

    Ovo rješenje je privremeno rješenje koje sadrži postojeći podatkovni model i komponente koje su prisutne tijekom nadogradnje. Uklanjanjem ovog rješenja uklanjate sva polja i komponente koje se više ne koriste. Na taj način pomažete pojednostaviti sučelje i olakšati integraciju i proširenje.
    
### <a name="validate-common-scenarios"></a>Provjera valjanosti uobičajenih scenarija

Kada potvrdite valjanost određenih prilagodbi, preporučujemo da pregledate i poslovne procese koji su podržani u svim aplikacijama. Ti poslovni procesi uključuju, ali nisu ograničeni na, stvaranje prodajnih subjekata kao što su citati i ugovori te stvaranje projekata koji uključuju WBI-ove i odobravanje stvarnih.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Velike promjene između automatizacije projektnih usluga i operacija projekta

U ovom se odjeljku nalazi sažetak glavnih promjena koje možete očekivati između automatizacije projektnih usluga i operacija projekta.

### <a name="project-planning"></a>Planiranje projekta

Mogućnosti planiranja projekta u operacijama projekta više se ne oslanjaju na kombiniranu logiku na strani klijenta i logiku na strani poslužitelja. Umjesto toga, Project Operations koristi Project za web kao mehanizam za zakazivanje. Ova promjena mogućnosti zakazivanja omogućuje nekoliko novih značajki, kao što su prikazi ploča i Gantt, planiranje temeljeno na resursima, [stavke kontrolnog popisa zadataka](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) i načini zakazivanja projekata. Nove mogućnosti zakazivanja podržane su i bogatim skupom novih [sučelja za programiranje aplikacija (API-jevi)](../project-management/schedule-api-preview.md). Ovi API-ji namijenjeni su osiguravanju da nijedna programska operacija za stvaranje, ažuriranje ili brisanje entiteta u WBS-u ne ošteti izračunata polja u rasporedu.

## <a name="billing-and-pricing"></a>Naplata i određivanje cijene

U sklopu kontinuiranih ulaganja u projektne operacije dostupno je nekoliko novih mogućnosti u naplati i određivanju cijena. Evo nekoliko primjera:

- [Bilježenje upotrebe materijala na projektima i projektnim zadacima](../material/material-usage-log.md)
- [Upravljanje kooperantima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Predujmovi i ugovori koji e temelje na povremenim plaćanjima](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status i provjere valjanosti ugovora koje ne premašuju](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Naplata temeljena na zadacima

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Koje su vrste implementacije trenutno podržane za nadogradnju?

| Izvor                                                 | Cilj                                                    | Stanje                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementacija Lite za projektne operacije                        | Podržano               |
| Dynamics 365 Finance upravljanje projektima i računovodstvo | Implementacija Lite za projektne operacije                        | Trenutno nije podržano |
| Upravljanje financijskim projektima i računovodstvo              | Project Operations za scenarije temeljene na resursima / bez zaliha     | Trenutno nije podržano |
| Automatizacija usluge projekta 3.x                         | Project Operations za scenarije temeljene na resursima / bez zaliha     | Trenutno nije podržano |
| Projekt za web (namjensko okruženje)            | Implementacija Lite za projektne operacije                        | Trenutno nije podržano |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako instalirati Project Operations prije nego što alat za nadogradnju bude dostupan?

Prije dostupnosti alata za nadogradnju postoje dvije mogućnosti za instalaciju operacija programa Project Operations:

- Dodijelite novo okruženje.
- Zasebno implementirajte projektne operacije u bilo kojoj prodajnoj organizaciji u kojoj automatizacija project usluga nije prisutna.

> [!NOTE]
> Ako je automatizacija project servisa instalirana u tvrtki ili ustanovi, ali nije korištena, može se deinstalirati. Nakon što u potpunosti uklonite automatizaciju usluge projekta, Project Operations mogu se instalirati u istu organizaciju.
