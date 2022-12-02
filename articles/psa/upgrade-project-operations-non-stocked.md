---
title: Nadogradnja s aplikacije Project Service Automation na aplikaciju Project Operations
description: Ovaj članak daje pregled postupka nadogradnje iz sustava Microsoft Dynamics 365 Project Service Automation u Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736657"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadogradnja s aplikacije Project Service Automation na aplikaciju Project Operations

Uzbuđeni smo što možemo najaviti drugu od tri faze nadogradnje iz sustava Microsoft Dynamics 365 Project Service Automation u Microsoft Dynamics 365 Project Operations. Ovaj članak daje pregled klijentima koji kreću na ovo uzbudljivo putovanje. 

Program isporuke nadogradnje bit će podijeljen u tri faze.

| Dostava nadogradnje | Faza 1 (siječanj 2022.) | Faza 2 (studeni 2022.) | Faza 3 (travanjski val 2023.)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nema ovisnosti o strukturnoj analizi rada za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| SAR unutar trenutačno podržanih ograničenja aplikacije Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| SAR izvan trenutačno podržanih ograničenja aplikacije Project Operations, uključujući podršku za Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Značajke postupka nadogradnje 

Kao dio postupka nadogradnje, dodali smo zapisnike nadogradnje na kartu web-mjesta kako bismo administratorima omogućili jednostavnije dijagnosticiranje kvarova. Uz novo sučelje, dodat će se nova pravila provjere valjanosti kako bi se osigurao integritet podataka nakon nadogradnje. Sljedeće provjere valjanosti bit će dodane postupku nadogradnje.

| Provjere valjanosti | Faza 1 (siječanj 2022.) | Faza 2 (studeni 2022.) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| SAR će biti provjeren prema uobičajenim povredama integriteta podataka (na primjer, dodjele resursa koji su povezani s istim nadređenim zadatkom, ali imaju različite nadređene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| SAR će biti potvrđen prema [poznatim ograničenjima aplikacije Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| SAR će biti potvrđen prema poznatim ograničenjima aplikacije Project desktop client. | |  | :heavy_check_mark: |
| Resursi koji se mogu rezervirati i projektni kalendari procijenit će se u odnosu na uobičajene iznimke pravila nekompatibilnog kalendara. | | :heavy_check_mark: | :heavy_check_mark: |

U fazi 2 klijentiima koji nadograde na Project Operations će njihovi postojeći projekti biti nadograđeni na iskustvo samo za čitanje za planiranje projekta. U ovom iskustvu samo za čitanje, puni SAR bit će vidljiv na rešetki za praćenje. Kako bi uredili SAR, voditelji projekta mogu odabrati [**Pretvori**](/PSA-Upgrade-Project-Conversion.md) na glavnoj stranici projekta. Pozadinski postupak zatim ažurira projekt tako da podržava novo iskustvo planiranja projekta iz aplikacije Project for the Web. Ova faza prikladna je za klijente koji imaju projekte koji odgovaraju [poznatim ograničenjima aplikacije Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

U fazi 3 bit će dodana podrška za Project desktop client, za dobrobit klijenta koji žele nastaviti uređivati svoje projekte iz te aplikacije. Međutim, ako se postojeći projekti pretvore u novo iskustvo aplikacije Project for the Web, pristup dodatku bit će onemogućen za svaki pretvoreni projekt.

## <a name="prerequisites"></a>Preduvjeti

Da biste ispunili uvjete za nadogradnju faze 1, morate zadovoljiti sljedeće kriterije:

- Ciljno okruženje ne smije sadržavati nikakve zapise u entitetu **msdyn_projecttask**.
- Važeće licence za Project Operations moraju se dodijeliti svim aktivnim korisnicima. 
- Morate potvrditi postupak nadogradnje u barem jednom neradnom okruženju koje sadrži reprezentativni skup podataka koji je usklađen s vašim radnim okruženjem.
- Ciljno okruženje mora se ažurirati na izdanje ažuriranja 37 aplikacije Project Service Automation (V3.10.58.120) ili na noviju verziju.

Da biste ispunili uvjete za nadogradnju faze 2, morate zadovoljiti sljedeće kriterije:

- Važeće licence za Project Operations moraju se dodijeliti svim aktivnim korisnicima. 
- Morate potvrditi postupak nadogradnje u barem jednom neradnom okruženju koje sadrži reprezentativni skup podataka koji je usklađen s vašim radnim okruženjem.
- Ciljno okruženje mora se ažurirati na izdanje ažuriranja 37 aplikacije Project Service Automation (V3.10.58.120) ili na noviju verziju.
- Okruženja koja sadrže zadatke (msdyn_projecttask) podržana su samo ako je ukupan broj zadataka po projektu 500 ili manji.

Preduvjeti za fazu 3 ažurirat će se kako se približava datum opće dostupnosti.

## <a name="licensing"></a>Licenciranje

Ako imate aktivne licence za Project Service Automation, možete instalirati i upotrebljavati Project Operations, koji uključuje sve mogućnosti aplikacije Project Service Automationa i više. Na ovaj način možete testirati mogućnosti aplikacije Project Operations dok nastavljate upotrebljavati Project Service Automation u proizvodnji. Nakon što vaše licence za Project Service Automation isteknu, morat ćete prijeći na Project Operations. Kada planirate ovaj prijelaz, morate uzeti u obzir činjenicu da licenca za Project Operations ne uključuje licencu za Project Service Automation. Klijenti koji imaju scenarije u kojima su uveli Project Service Automation i trebaju nastaviti upotrebljavati ili povećati svoje licence za PSA dok planiraju prijeći na Project Operations, mogu zatražiti privremene licence za PSA na temelju kupljenih licenci za Project Operations. Jedna licenca za Project Service Automation bit će izdana za jednu licencu za Project Operations. Privremene licence za PSA mogu se zatražiti na sljedećoj vezi: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Testiranje i refaktoriranje prilagođavanja

Za početak, uvezite sve prilagodbe u čisto okruženje Project Operations (Lite) kako biste potvrdili da je uvoz uspješan i da se poslovne operacije ponašaju prema očekivanjima.

Evo nekih stvari na koje treba pripaziti:

- Uvoz možda neće uspjeti jer nedostaju ovisnosti. Drugim riječima, referentna polja prilagodbe ili druge komponente koje su uklonjene u aplikaciji Project Operations. U tom slučaju uklonite te ovisnosti iz razvojnog okruženja.
- Ako vaša neupravljana i upravljana rješenja uključuju komponente koje nisu prilagođene, uklonite te komponente iz rješenja. Na primjer, kada prilagodite entitet **Projekt**, svom rješenju dodajte samo zaglavlje entiteta. Nemojte dodavati sva polja. Ako ste prethodno dodali sve podkomponente, možda ćete morati ručno izraditi novo rješenje i dodati mu relevantne komponente.
- Obrasci i prikazi možda se neće prikazati kako se očekuje. U nekim okolnostima, ako ste prilagodili bilo koji od gotovih obrazaca ili prikaza, prilagodbe mogu spriječiti da nova ažuriranja u aplikaciji Project Operations stupe na snagu. Da biste identificirali te probleme, preporučujemo da usporedno pregledate čistu instalaciju aplikacije Project Operations i instalaciju aplikacije Project Operations koja uključuje vaše prilagodbe. Usporedite obrasce koji se najčešće upotrebljavaju u vašem poslovanju kako biste potvrdili da vaša verzija obrasca još uvijek ima smisla i da joj ne nedostaje nešto od čiste verzije obrasca. Napravite istu vrstu usporednog pregleda za sve prikaze koje ste prilagodili.
- Poslovna logika može zakazati tijekom izvođenja. Budući da reference na polja u vašim dodacima nisu potvrđene u trenutku uvoza, poslovna logika može biti neuspješna zbog referenci na polja koja više ne postoje i mogli biste primiti poruku o pogrešci koja sliči sljedećem primjeru: Entitet "'Projekt' ne sadrži atribut s nazivom Name = 'msdyn_plannedhours' i NameMapping = 'Logical'." U tom slučaju promijenite svoje prilagodbe tako da upotrebljavaju nova polja. Ako upotrebljavate automatski generirane proxy razrede i jake reference tipa u svojoj logici dodatka, razmislite o ponovnom generiranju tih proxyja iz čiste instalacije. Na ovaj način možete jednostavno identificirati sva mjesta na kojima vaši dodaci ovise o zastarjelim poljima.

Nakon što ažurirate svoje prilagodbe za čisti uvoz aplikacije Project Operations, prijeđite na sljedeće korake.

## <a name="end-to-end-testing-in-development-environments"></a>Sveobuhvatno testiranje u razvojnim okruženjima

### <a name="initiate-upgrade"></a>Pokretanje nadogradnje 

1. U centru za administratore usluge Power Platform nađite i odaberite svoje okruženje. Zatim u aplikacijama nađite i odaberite **Dynamics 365 Project Operations**.
2. Odaberite **Instaliraj** kako biste započeli nadogradnju. Centar za administratore usluge Power Platform predstavit će ovu instalaciju kao novu instalaciju. Međutim, otkrit će se prisutnost ranije verzije aplikacije Project Service Automation, a postojeća instalacija će se nadograditi.

    Nakon dovršetka nadogradnje, okruženje bi trebalo pokazati da je aplikacija Project Operations instalirana, a da aplikacija Project Service Automation nije instalirana.

    Nadogradnja može potrajati nekoliko sati ovisno o količini podataka u okruženju. Glavni tim koji upravlja nadogradnjom trebao bi planirati u skladu s tim i pokrenuti nadogradnju izvan radnog vremena. U nekim slučajevima, ako je količina podataka velika, nadogradnju treba pokrenuti tijekom vikenda. Odluka o rasporedu trebala bi se temeljiti na rezultatima testiranja u nižim okruženjima.

3. Prilagođena rješenja prilagodite prema potrebi. U ovom trenutku uvedite sve promjene koje ste napravili u svojim prilagodbama u odjeljku [Testiranje i refaktoriranje prilagodbi](#testing-and-refactoring-customizations) ovog članka.
4. Otvorite **make.powerapps.com**, s padajućeg izbornika u gornjem desnom dijelu portala odaberite svoje okruženje, odaberite **Rješenja** u lijevom izborniku odaberite rješenje **Zastarjele komponente aplikacije Project Operations** i **Deinstaliraj**.

    Ovo je rješenje privremeno rješenje koje zadržava postojeći podatkovni model i komponente koje su prisutne tijekom nadogradnje. Uklanjanjem ovog rješenja uklanjate sva polja i komponente koje se više ne upotrebljavaju. Na taj način pomažete pojednostaviti sučelje i olakšavate integraciju i proširenje.
    
### <a name="upgrade-to-project-operations-lite"></a>Nadogradnja na aplikacije Project Operations Lite

Sljedeći koraci opisuju postupak nadogradnje i povezano bilježenje pogrešaka:

1. **Provjera verzije PSA:** Da biste instalirali Project Operations, morate imati V3.10.58.120 ili noviji.
1. **Prethodna provjera valjanosti:** Kada administrator pokrene nadogradnju, sustav pokreće operaciju prethodne provjere valjanosti na svakom entitetu koji je srž rješenja Project Operations. Ovaj korak provjerava jesu li sve reference entiteta valjane i osigurava da su podaci koji se odnose na WBS unutar objavljenih ograničenja aplikacije Project for the Web.
1. **Nadogradnja metapodataka:** Nakon uspješne prethodne provjere valjanosti sustav pokreće promjene sheme i stvara rješenje zastarjelih komponenata. Ovo zastarjelo rješenje možete ukloniti nakon što dovršite svo potrebno refaktoriranje prilagodbi. Ovaj je korak najduži dio postupka nadogradnje i može trajati do četiri sata.
1. **Nadogradnja podataka:** Nakon što su sve potrebne promjene sheme dovršene u koraku nadogradnje metapodataka, vaši se podaci premještaju u novu shemu, a sve potrebne zadane postavke i ponovni izračun su izvršeni.
1. **Ažuriranje modula rasporeda projekta:** Nakon uspješne nadogradnje podataka kartica **Raspored** na glavnoj stranici mijenja oznaku u **Zadaci**. Kada korisnik odabere ovu karticu nakon nadogradnje, usmjerava se na navigaciju do rešetke za praćenje kako bi pogledao verziju aplikacije WBS samo za čitanje. Da bi uredili WBS, moraju pokrenuti [postupak konverzije](/PSA-Upgrade-Project-Conversion.md) rasporeda. Svi projekti bez prethodno postojeće aplikacije WBS mogu izravno upotrijebiti novo iskustvo zakazivanja, bez pretvorbe.
 
### <a name="validate-common-scenarios"></a>Provjera valjanosti uobičajenih scenarija

Kada potvrdite valjanost svojih specifičnih prilagodbi, preporučujemo da također pregledate poslovne procese koji su podržani u svim aplikacijama. Ovi poslovni procesi uključuju, ali nisu ograničeni na, stvaranje prodajnih entiteta, kao što su ponude i ugovori, i stvaranje projekata koji uključuju aplikacije WBS i odobrenje stvarnih podataka.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Glavne promjene u aplikacijama Project Service Automation i Project Operations

Ovaj odjeljak daje sažetak glavnih promjena koje možete očekivati u aplikacijama Project Service Automation i Project Operations.

### <a name="project-planning"></a>Planiranje projekta

Mogućnosti planiranja projekta u aplikaciji Project Operations više se ne oslanjaju na kombinaciju logike na strani klijenta i logike na strani poslužitelja. Umjesto toga, Project Operations upotrebljava Project for the Web kao modul za planiranje. Ova promjena u mogućnostima zakazivanja omogućuje nekoliko novih značajki, kao što su prikazi ploče i Gantt, planiranje temeljeno na resursima [stavke popisa zadataka](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) i načini zakazivanja projekta. Nove mogućnosti zakazivanja također su podržane bogatim skupom novih [sučelja za programiranje aplikacija (API)](../project-management/schedule-api-preview.md). Ovi API-ji pomažu osigurati da nijedna programska operacija za stvaranje, ažuriranje ili brisanje entiteta u aplikaciji WBS ne pokvari izračunata polja u rasporedu.

### <a name="billing-and-pricing"></a>Naplata i određivanje cijene

Kao dio stalnih ulaganja u Project Operations, dostupno je nekoliko novih mogućnosti u naplati i cijenama. Evo nekoliko primjera:

- [Zapis utrošenog materijala na projektima i projektnim zadacima](../material/material-usage-log.md)
- [Upravljanje podugovorima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Predujmovi i ugovori koji e temelje na povremenim plaćanjima](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Ugovor sa statusom koji se ne smije premašiti i provjerama valjanosti](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Naplata na temelju zadataka

### <a name="resource-management"></a>Upravljanje resursima

Project Operations pruža neobaveznu podršku za ploču i pomoćnika za raspored Universal Resource Scheduling (URS). Ovo novo iskustvo postat će obavezno u valu iz travnja 2023.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Koje su vrste uvođenja trenutačno podržane za nadogradnju?

| Izvor                                                 | Cilj                                                    | Stanje                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Uvođenje aplikacije Project Operations Lite                        | Podržano               |
| Upravljanje projektima i računovodstvo u aplikaciji Dynamics 365 Finance | Uvođenje aplikacije Project Operations Lite                        | Trenutačno nije podržano |
| Upravljanje projektom i računovodstvo u aplikaciji Finance              | Project Operations za scenarije temeljene na resursima / bez zaliha     | Trenutačno nije podržano |
| Project Service Automation 3.x                         | Project Operations za scenarije temeljene na resursima / bez zaliha     | Trenutačno nije podržano |
| Project for the Web (namjensko okruženje)            | Uvođenje aplikacije Project Operations Lite                        | Trenutačno nije podržano |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako mogu instalirati Project Operations prije nego što alat za nadogradnju bude dostupan?

Postoje dvije opcije za instaliranje aplikacije Project Operations prije nego što alat za nadogradnju postane dostupan:

- Dodjela novog okruženja.
- Zasebno uvedite Project Operations u bilo koji prodajni odjel gdje aplikacija Project Service Automation nije prisutna.

Ako je aplikacija Project Service Automation instalirana u tvrtki ili usluzi, ali nije upotrebljena, može se deinstalirati. Nakon što potpuno uklonite Project Service Automation, Project Operations može se instalirati u istoj tvrtki i usluzi.
