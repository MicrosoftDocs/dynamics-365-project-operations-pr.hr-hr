---
title: Pregled strukturnih analiza rada
description: Strukturna analiza rada (WBS) opis je posla koji će se izvršiti na projektu. To je hijerarhija zadataka koja predstavlja način na koji projektni tim shvaća ustrojstvo rada te veličinu, trošak i trajanje svake komponente ili zadatka.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 093f9901aec0db1fa8f920533c0084f877f26445fd07159e8e1ae0cf53849641
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998812"
---
# <a name="work-breakdown-structures-overview"></a>Pregled strukturnih analiza rada

[!include [banner](../includes/banner.md)]

Strukturna analiza rada (WBS) opis je posla koji će se izvršiti na projektu. To je hijerarhija zadataka koja predstavlja način na koji projektni tim shvaća ustrojstvo rada te veličinu, trošak i trajanje svake komponente ili zadatka. WBS ima tri glavne svrhe:

-   Opišite analizu ili ustrojstvo posla u zadacima.
-   Rasporedite rad na projektu.
-   Procijenite trošak svakog zadatka.

Stupanj pojedinosti u WBS-u ovisi o razini preciznosti koja je potrebna u procjenama i razini praćenja koja je potrebna u odnosu na te procjene. Za projekte koji imaju vrlo nisku toleranciju na klizanje rasporeda ili troška obično treba podrobniji WBS i ustrajno praćenje napretka posla i troškova u odnosu na WBS. Ova vrsta projekta uobičajena je u građevinskoj i inženjerskoj industriji. 

Suprotno tome, projekti u industrijama poput medija i oglašavanja, softvera i IT infrastrukture imaju tendenciju da budu jedinstveni, a produktivnost je u odnosu s iskustvom i kompetencijom pojedinca koji izvršava zadatak. Stoga ove industrije upotrebljavaju WBS kako bi dobile približnu veličinu projekta, a ne da bi podrobno pratile napredak tog projekta. 

Izgradnja WBS-a intenzivan je postupak koji se obično radi tijekom dugog razdoblja i koji zahtijeva suradnju i podatke od širokog spektra ljudi. U ovoj se temi opisuje način uporabe poboljšanja WBS-a kako biste zadovoljili svoje zahtjeve za procjene i praćenje.

## <a name="prerequisites-for-creating-a-wbs"></a>Preduvjeti za stvaranje WBS-a
Kako biste stvorili WBS, morate biti u mogućnosti stvoriti raspored rada i procijeniti trošak rada.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Preduvjeti za stvaranje rasporeda rada

Kako biste upotrijebili sve mogućnosti planiranja značajki WBS-a, dovršite sljedeće postavljanje:

1.  Postavite zadani kalendar i kalendar projekta:
    1.  Kliknite **Upravljanje projektima i računovodstvo** &gt; **Postavljanje** &gt; **Parametri za upravljanje projektom i računovodstveni parametri** &gt; **Planiranje**. U polju **Zadani radni kalendar** navedite zadani kalendar. To će biti zadani radni kalendar za svaki novostvoreni projekt.
    2.  Zadani kalendar za određeni projekt možete promijeniti. Kliknite stranicu s pojedinostima o projektu, a zatim na Brzoj kartici **Projektni tim i planiranje** ažurirajte polje **Kalendar za planiranje** odabirom drugog kalendara.

2.  Postavite standardne radne dane i radno vrijeme. Kalendar koji ste postavili kao radni kalendar za svoj projekt upotrebljavat će se u WBS-u za određivanje sljedećih podataka:

-   Radnih dana i praznika
-   Broja radnih sati u danu

Kako biste postavili radne dane i radne sate za kalendar ili stvorili novi kalendar, kliknite **Administracija organizacije** &gt; **Uobičajeno** &gt; **Kalendari**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Preduvjeti za procjenu troška rada

Kako biste upotrijebili ukupne mogućnosti procjene troškova WBS-a, trebali biste postaviti troškove i prodajne cijene za radnike, kategorije rada, izdatke, naknade i artikle.

-   Kako biste postavili trošak i kategorije prodajne cijene rada, izdataka i naknada kliknite **Upravljanje projektima i računovodstvo** &gt; **Postavljanje** &gt; **Cijene**.
-   Za postavljanje troška i prodajne cijene artikla upotrebljavajte stranicu **Trgovinski ugovori** za svaku stavku na stranici popisa **Pušteni proizvodi** u mogućnosti Upravljanje podacima o proizvodu.

## <a name="creating-a-wbs"></a>Stvaranje WBS
Stvaranje WBS-a uključuje tri aktivnosti:

1.  **Raščlamba posla** – Stvorite raščlambu posla na upravljačke dijelove ili zadatke.
2.  **Raspored rada** – Procijenite vrijeme potrebno za izvršavanje zadatka, postavite međuovisnost zadatka i odaberite datume početka i završetka zadataka.
3.  **Procjena troška** – Procijenite troškove svakog zadatka.

U sljedeći odjeljcima raspravlja se o načinu na koji mogućnosti WBS-a mogu pomoći u svakoj od ovih aktivnosti.

### <a name="work-decomposition"></a>Raščlamba posla

Stvaranje analize ili raščlamba posla obično je prvi korak u procesu stvaranja WBS-a. Funkcija WBS-a podržava sljedeće osnovne konstrukcije za analizu ili raščlambu posla. 

**Temeljni zadatak projekta** Temeljni zadatak projekta sumarni je projektni zadatak najviše razine. Svi drugi projektni zadaci stvaraju se ispod njega. Naziv temeljnog zadatka uvijek se postavlja u naziv projekta. Rad, datumi i trajanje temeljnog čvora sažimaju vrijednosti zadataka ispod temeljnog zadatka. Ne možete mijenjati svojstva temeljnog čvora ili ih izbrisati.

**Sumarni zadaci ili zadaci spremnika** Sumarni zadatak je onaj koji ispod sebe ima pod-zadatke ili sastavne zadatke. Sumarni zadatak ne sadrži vlastiti rad ili trošak. Umjesto toga, radni napor i trošak sumarnog zadatka zbroj su radnog napora i troška njegovih sastavnih zadataka. Najraniji datum početka sastavnih zadataka upotrebljava se kao datum početka sumarnog zadatka, a najnoviji datum završetka sastavnih zadataka upotrebljava se kao datum završetka. Naziv sumarnog zadatka možete mijenjati, no ne i svojstva planiranja rada, datuma i trajanja. Ako izbrišete sumarni zadatak, izbrisat ćete i sve njegove sastavne zadatke. 

**Zadaci lisnog čvora** Zadatak lisnog čvora predstavlja najopširniji radni paket na projektu. Lisni čvor sadrži procijenjeni rad, planirani broj resursa, planirane početne i završne datume te trajanje. 

Možete dovršiti sljedeće hijerarhijske operacije kako biste omogućili stvaranje radne hijerarhije ili raščlambu projekta. 

**Novi zadatak** Svaki novi zadatak koji izradite automatski se dodaje pod temeljni čvor i zadatku se automatski dodjeljuje WBS broj. WBS broj predstavlja razinu zadatka u hijerarhiji. Za zadatke na prvoj razini ispod temeljnog zadatka projekta upotrebljava se shema numeriranja od 1, 2, 3 itd. Za zadatke koji su ispod prve razine upotrebljava se shema numeriranja od 1.1, 1.2, 1.3 itd. Za svaku razinu koja se dodaje pod prethodnu razinu dodaje se novi niz brojeva s točkom. 

Trenutačno ne možete prilagoditi WBS numeriranje. 

**Uvučeni zadatak** Kada uvučete zadatak, on postaje podređen zadatku koji mu prethodi. WBS broj novog podređenog zadatka automatski se preračunava na temelju WBS broja njegovog novog nadređenog zadatka. Nadređeni zadatak sada je sumarni zadatak ili zadatak spremnika i stoga postaje skup svojih sastavnih zadataka. 

> [!NOTE] 
> Kada uvlačite zadatke u zadatak koji je prije uvlačenja bio lisni čvor, novostvoreni sumarni zadatak gubi vlastite datume, rad i broj resursa. Sada upotrebljava zbroj vrijednosti svojih novih sastavnih zadataka. 

**Izvučeni zadatak** Kada izvučete zadatak, on više nije sastavni zadatak svojeg nadređenog zadatka. WBS broj ovog zadatka automatski se preračunava kako bi odražavao novu razinu zadatka u hijerarhiji. Rad, trošak i datumi prethodno nadređenog zadatka ponovno se izračunavaju tako da ne uključuju taj zadatak. 

**Pomakni se gore i Pomakni se dolje** Kad kliknete mogućnosti **Pomakni se gore** i **Pomakni se dolje**, mijenjate položaj zadatka unutar hijerarhije njegovog nadređenog zadatka. Položaj zadatka ne utječe na rad, trošak, datume ili trajanje zadatka. No, WBS broj ovog zadatka automatski se preračunava kako bi odražavao novi položaj zadatka.

### <a name="schedule-estimation"></a>Procjena rasporeda

Procjena rasporeda obično je drugi korak pri stvaranju WBS-a. Kao najbolju praksu, trebali biste dovršiti procjenu rasporeda nakon što stvorite zadatke. Stranica **Strukturna analiza rada** u Financijama ima dva odjeljka. Gornje okno namijenjeno je procjeni rasporeda, a donje uključuje karticu **Procijenjeni troškovi i prihodi** koju možete upotrebljavati za procjenu troška. 
**Ovisnosti zadatka** U WBS-u možete stvoriti odnos prethodnika između zadataka. Kada zadatku dodjeljujete zadatke prethodnika, taj zadatak može započeti tek nakon dovršetka svih njegovih zadataka prethodnika. Planirani datum početka zadatka automatski se postavlja na najnoviji datum svih njegovih prethodnika. 

**Planiranje zadataka** Sljedeći čimbenici određuju planiranje zadataka lisnih čvorova:

-   Prethodnici
-   Mogućnost rada
-   Broj resursa
-   datumi početka i završetka

Početni datum zadatka lisnog čvora koji nema prethodnike automatski se postavlja na početni datum planiranja projekta. Trajanje zadatka lisnog čvora uvijek se izračunava kao broj radnih dana između njegovog početnog i završnog datuma. 

*<strong><em>Pravila planiranja</em></strong>* Kad je uključena pomoć za automatsko planiranje, sljedeća se pravila primjenjuju na planiranje zadataka za zadatke lisnih čvorova:

-   Datumi početka i završetka zadatka uvijek moraju biti radni dani prema kalendaru planiranja projekta.
-   Početni datum zadatka koji ima prethodnike automatski se postavlja na najnoviji završni datum prethodnika.
-   Rad na zadatku automatski se izračunava na sljedeći način:

Broj osoba × trajanje × broj sati u standardnom radnom danu kalendara projekta. 

U nekim slučajevima možda ćete željeti zaobići ta pravila. Možete isključiti automatsko planiranje kako biste spriječili da Financije automatski postavljaju ili ispravljaju neko svojstvo zadataka lisnih čvorova. Kada unesete podatke za zadatak koji uzrokuje kršenje pravila planiranja, za zadatak se prikazuje ikona pogreške planiranja. Ako ne želite da se prikazuju pogreške planiranja, kliknite **Pogreške planiranja se prikazuju** kako biste isključili značajku. 

> [!NOTE] 
> Vrijednosti sumarnog zadatka ili zadatka spremnika i dalje se izračunavaju kao zbroj vrijednosti sastavnih zadataka, bez obzira na to je li pomoć za automatsko raspoređivanje uključena ili isključena. 

**Ispravljanje pogrešaka planiranja** Kad je uključena pomoć za automatsko planiranje, vjerojatno do pogrešaka planiranja neće doći. Međutim, ako isključite pomoć za automatsko planiranje, a zatim je ponovno uključite kasnije, ikone pogrešaka planiranja mogu se pojaviti na WBS-u. 

**Ispravljanje pogrešaka planiranja po zadatku** Kada dvaput kliknete ikonu pogreške rasporeda za određeni zadatak, dijaloški okvir prikazuje sve pogreške planiranja za taj zadatak. Možete odlučiti koje ćete pogreške planiranja popraviti za zadatak. 

**Ispravljanje svih pogrešaka planiranja** Ako želite da Financije poprave sve pogreške planiranja na WBS-u, u oknu radnji kliknite **Ispravi sva odstupanja planiranja**. 

> [!NOTE] 
> Ova značajka može prouzročiti značajne izmjene WBS-a. Pogreške se ispravljaju sljedećim redoslijedom:

1.  Procijenjeni rad na svim zadacima izmijenjen je tako da je jednak kapacitetu definiranom u kalendaru projekta.
2.  Datum početka svakog zadatka mijenja se tako da zadatak započinje nakon dovršetka svih zadataka prethodnika.
3.  Datum početka svakog zadatka mijenja se kako bi se uklonile razlike u datumima početka prethodnih zadataka.

### <a name="cost-estimation"></a>Procjena troškova

Kao što je ranije spomenuto u ovom dokumentu, procjenu troškova za svaki zadatak lisnog čvora unosite s pomoću kartice **Procijenjeni troškovi i prihodi** u donjem oknu stranice **Strukturna analiza rada**. 

> [!NOTE] 
> Ne možete izmijeniti procjenu troška za sumarni zadatak ili zadatak spremnika. Procjena troška za sumarni zadatak jednaka je zbroju procjene troška njegovih zadataka lisnog čvora. Procijenjeni ukupni trošak za svaki zadatak izračunava se kao zbroj procijenjenih iznosa troška za sljedeće vrste transakcija:

-   Rad
-   Artikl ili materijal
-   Troškovi

Vrsta transakcije **Naknada** upotrebljava se za procjenu prihoda od naknada. Ova vrsta transakcije nema komponentu troška i stoga se ne uzima u obzir prilikom procjene troškova. 

Vrsta transakcije **Djelomično** upotrebljava se za bilježenje ugovorene vrijednosti prodaje u projektu s fiksnom vrijednošću. Ova vrsta transakcije također se ne uzima u obzir prilikom procjene troškova. 

Kada procjenjujete troškove rada, materijala i izdataka za svaki zadatak, procijenjenom trošku morate dodijeliti kategoriju projekta. 

**Procjena troškova rada** Za svaki zadatak lisnog čvora dodjeljujete radni u satima i zadanu kategoriju. Stoga, kada postavite raspored za zadatak, procjena troška rada za taj zadatak automatski se dodaje u zadanu kategoriju za rad. Ova procjena troška prikazuje se na kartici **Procijenjeni troškovi i prihodi** u rešetki **Pojedinosti o retku** za taj zadatak. Ako vam je potrebno više procjena troška rada, možete ih dodati na ovu karticu. Ako povećate ili smanjite sate na procjeni troška rada, raspored za zadatak automatski se preračunava. 

**Procjena izdatka i materijalnih troškova** Kartica **Procijenjeni troškovi i prihod** također vam omogućuje procjenu izdatka i materijalnih troškova za zadatak ako su vam potrebne procjene. 

Trošak i prodajna cijena za svaki redak procjene rada ili izdatka temelje se na postavci koja je definirana za svaku kategoriju u tablicama cijena pod stavkom **Upravljanje projektima i računovodstvo** &gt; **Postavi** &gt; **Određivanje cijene**. Za artikle se trošak i prodajna cijena dodaju prema zadanim postavkama iz ugovora o artiklima ili trgovinskim ugovorima na stranici s popisom **Pušteni proizvodi** u mogućnosti Upravljanje informacijama o proizvodu.

## <a name="tracking-progress-on-the-wbs"></a>Praćenje napretka na WBS-u
Neke industrije prate napredak projekta prema WBS-u na razini sitnih poslova, dok druge prate napredak na višoj razini WBS-a. U ovom se odjeljku opisuje način na koji možete upotrebljavati WBS praćenje za potrebe svojeg projekta. 

U Financijama postoje tri prikaza WBS projekta: prikaz planiranja, prikaz praćenja rada i prikaz praćenja troška.

### <a name="planning-view"></a>Prikaz planiranja

Prikaz planiranja prikazuje planiranu ili osnovnu procjenu podataka o rasporedu i trošku. Iako ne postoje značajke za praćenje verzije i osnove WBS projekta, vrijednosti u ovom prikazu namijenjene su predstavljanju osnovne verzije. U odjeljcima ove teme, Procjena rasporeda i Procjena troškova, opisuje se ovaj prikaz i način njegove uporabe za stvaranje WBS-a.

### <a name="effort-tracking-view"></a>Motrište praćenja rada

Prikaz Praćenje rada pokazuje praćenje napretka zadataka u WBS-u. Uspoređuje akumulirane stvarne radne sate na zadatku s planiranim radnim satima. Sljedeće formule osiguravaju vrijednosti u prikazu praćenja rada:

-   Postotak napretka = stvarni rad do danas ÷ planirani rad za zadatak
-   Preostali rad (poznat i kao Procjena rada za dovršetak projekta \[ETC\]) = Planirani rad - Stvarni rad do danas
-   Procjena ukupnog rada na završenom projektu (EAC, Estimate at complete) = preostali rad + stvarni rad do danas
-   Predviđeno odstupanje rada = planirani rad – EAC

Prikaz praćenja rada pokazuje predviđanje odstupanja rada za zadatak na temelju toga je li EAC veći ili manji od planiranog rada:

-   Ako je EAC veći od planiranog rada, predviđa se da će zadatak potrajati dulje nego što je prvotno planirano i da zaostaje za rasporedom.
-   Ako je EAC manji od planiranog rada, predviđa se da će zadatak potrajati kraće nego što je prvotno planirano i da je ispred roka.

**Ponovno predviđanje voditelja projekta o radu** Povremeno će voditelj projekta ili druga osoba koja prati napredak projekta morati revidirati prvotne procjene koje se odnose na zadatak. Zadatak se može kretati brže ili sporije nego što se prvotno očekivalo iz različitih razloga. Primjerice, opseg je smanjen ili radnici imaju manje iskustva od prvotno planiranog. Predviđanja proizlaze iz percepcije upravitelja projekta o procjeni na temelju trenutačnog stanja projekta. Općenito, ne biste trebali mijenjati osnovne brojeve, jer osnova predstavlja objavljeni dokument o procjeni rasporeda projekta i troška s kojim su se sve zainteresirane strane složile. 

Postoje dva načina na koja upravitelji projekta mogu izmijeniti rad na zadacima:

-   Izmijenite preostali rad koji se automatski postavlja za ažuriranje stvarnog preostalog rada na zadatku.
-   Izmijenite postotak napretka koji se automatski postavlja za ažuriranje stvarnog napretka na zadatku.

Oba ova pristupa uzrokuju ponovno izračunavanje ETC-a, EAC-a i postotka napretka zadatka te predviđena odstupanja rada na zadatku. EAC, ETC i postotak napretka na sumarnim zadacima također se ponovno izračunavaju i ažurira se predviđanje odstupanja rada. 

**Izmijenjeni rad na sumarnim zadacima** Možete izmijeniti rad na sumarnim zadacima ili zadacima spremnika. Bez obzira na to jeste li izmijenili te vrijednosti s pomoću preostalog rada ili postotka napretka na sumarnim zadacima, izračuni se odvijaju automatski sljedećim redoslijedom:

1.  Izračunačava se EAC, ETC i postotak napretka na zadatku.
2.  Novi se EAC raspodjeljuje na podređene zadatke u istom omjeru kao prvotni iznos EAC-a.
3.  Izračunava se novi EAC za svaki zadatak lisnog čvora.
4.  Preostali rad i postotak napretka preračunavaju se za sve pogođene podređene zadatke, na temelju nove vrijednosti EAC-a. Također se preračunava odstupanje rada na zadacima.
5.  EAC sumarnih zadataka također se preračunava iz lisnih čvorova.

Kliknite stavku **Proširi do razine** u prikazu praćenja rada kako biste postavili razinu na kojoj ćete pratiti i održavati svoj WBS. WBS se automatski širi na tu razinu u prikazu praćenja rada kad god ga otvorite.

### <a name="cost-tracking-view"></a>Prikaz praćenja troškova

Prikaz praćenja troška pokazuje praćenje troška za zadatak. U ovom se prikazu stvarni trošak koji je do danas potrošen na zadatak uspoređuje s planiranim troškom za zadatak. Sljedeće formule osiguravaju vrijednosti u prikazu praćenja troška:

-   Postotak učinjenog troška = stvarni trošak do danas ÷ planirani trošak za zadatak
-   Trošak za dovršetak (CTC,Cost to complete) = planirani trošak – stvarni trošak do danas
-   Procjena ukupnog troška (EAC, Estimate at complete) = CTC + stvarni trošak do danas
-   Predviđeno odstupanje troškova = planirani trošak – EAC

Prikaz praćenja troška pokazuje predviđanje odstupanja troška za zadatak na temelju toga je li EAC veći ili manji od planiranog troška:

-   Ako je EAC veći od planiranog troška, predviđa se da će zadatak koštati više novca nego što je prvotno planirano i da premašuje proračun.
-   Ako je EAC manji od planiranog troška, predviđa se da će zadatak koštati manje novca nego što je prvotno planirano i da je ispod proračuna.

**Ponovno predviđanje voditelja projekta o trošku** Voditelji projekata moraju upotrebljavati CTC za revidiranje prvotne procjene troška za zadatak. Voditelj projekta može izmijeniti vrijednost CTC-a prema trošku koji je potreban za dovršenje zadatka. Ako izmijenite CTC vrijednost, preračunavaju se CTC zadatka, EAC i postotak učinjenog troška te predviđeno odstupanje troška za zadatak. EAC, ETC i postotak učinjenog troška na sumarnim zadacima također se ponovno izračunavaju i ažurira se predviđanje odstupanja troška. 

> [!NOTE] 
> Kada revidirate rad za WBS zadatak u prikazu praćenja rada, CTC, EAC, postotak učinjenog troška i predviđeno odstupanje troška preračunavaju se u prikazu praćenja troška. Međutim, revidiranja troška ne utječu na vrijednosti u prikazu praćenja rada jer se troškovi prema vrsti transakcije (rad, materijal ili izdatak) ili kategoriji projekta ne revidiraju. 

**Predviđanje revizije troška na sumarnim zadacima** Možete revidirati troškove sumarnog zadatka i izračuni se odvijaju automatski sljedećim redoslijedom:

1.  Preračunavaju se EAC, CTC i postotak troška učinjenog na zadatku.
2.  Novi EAC raspoređuje se na podređene zadatke u istom omjeru kao izvorni EAC na zadatke.
3.  Izračunava se novi EAC za svaki zadatak.
4.  CTS i postotak učinjenih troškova preračunavaju se za pogođene podređene zadatke na temelju vrijednosti EAC-a. Također se preračunava odstupanje troška na zadacima.
5.  EAC za sve sumarne zadatke ponovno se izračunava na temelju ove promjene.

Kliknite stavku **Proširi do razine** u prikazu praćenja troška kako biste postavili razinu na kojoj ćete pratiti i održavati svoj WBS. WBS se širi na tu razinu u prikazu praćenja troška kad god ga otvorite.

### <a name="earned-value-management"></a>Upravljanje zarađenom vrijednosti

Za praćenje napretka projekta možete upotrijebiti način zarađene vrijednosti (EVM, earned value method). Mjerne podatke o zarađenoj vrijednosti možete pregledati u Centru uloga voditelja projekta. Komponenta grafikona zarađene vrijednosti prikazuje vrijednosti po vremenskim fazama planirane vrijednosti i stvarnog troška. Zarađena vrijednost na tekućem datumu prikazuje se kao točka. Podaci vremenske faze za zarađenu vrijednost trenutačno nisu dostupni. 

Vremenska faza na grafikonu zarađene vrijednosti prikazana je po tjednima ili mjesecima. U ovom se odjeljku opisuju tri stupa EVM-a: planirana vrijednost, ostvarena vrijednost i stvarni trošak. 

**Planirana vrijednost** Teorija EVM-a govori da prikaz planirane vrijednosti predstavlja stopu po kojoj je projektni tim planirao zaraditi vrijednost na projektu. 

Financije upotrebljavaju pravilo zarade 0 : 100 kada ucrtavaju planiranu vrijednost. Prema ovom pravilu, vrijednost zadatka knjiži se u zadatak od datuma završetka. Dok se zadatak 100 posto ne izvrši, vrijednost se ne objavljuje. 

U Upravljanje projektima i računovodstvo unosite datum završetka lisnih čvorova i planirani trošak za to. Kada se grafikon planirane vrijednosti prikaže po tjednima, planirana vrijednost zbraja se po tjednima za sve zadatke lisnih čvorova za vrijeme trajanja projekta. 

**Zarađena vrijednost** Teorija EVM-a govori da prikaz zarađene vrijednosti predstavlja stopu po kojoj projektni tim stvarno zarađuje vrijednost na projektu. 

Financije upotrebljavaju pravilo zarade 0 : 100 kada ucrtavaju zarađenu vrijednost. Prema ovom pravilu, vrijednost zadatka knjiži se u zadatak od datuma završetka. Dok se zadatak 100 posto ne izvrši, vrijednost se ne objavljuje. 

Pri izračunavanju zarađena vrijednosti uzima se u obzir postotak napretka svakog zadatka. Prema pravilu zarade 0 : 100, za izračun zarađene vrijednosti na kraju tog razdoblja uzimaju se u obzir samo zadaci koji su izvršeni u određenom razdoblju. Zarađena vrijednost na projektu izračunava se za sve zadatke koji su dovršeni tijekom izrade grafikona. 

> [!NOTE] 
> Trenutačno sustav za praćenje WBS-a nema podatkovne strukture za pohranu povijesnih postotaka napretka za svaki zadatak. Stoga se zarađena vrijednost može prijaviti samo od trenutka obrade kocke. Redovito obrađujte kocku kako biste ažurirali podatke o zarađenoj vrijednosti koji su prikazani u centru uloga. 

**Stvarni trošak** Teorija EVM govori kako prikaz stvarnog troška predstavlja stopu po kojoj se novac troši na projekt. 

Transakcije koje se knjiže za projekt upotrebljavaju se za prikaz stvarnog retka troška. Troškovi su sažeti po datumima. Ti se podaci zatim upotrebljavaju za grafički prikaz stvarnih troškova po tjednu ili mjesecu na grafikonu zarađenih vrijednosti.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Način uporabe koncepata planirane i zarađene vrijednosti te stvarnog troška

**Odstupanje rasporeda** Tijekom planiranja, na vremenskoj traci stvarate predviđanje rada. Stoga je planirana vrijednost cijena po kojoj bi se, po mišljenju planera projekta, mogao obaviti posao za dovršenje projekta. Nakon tijeka napredovanja projekta, posao se završi i projekt donosi vrijednost. Usporedbom planirane s ostvarenom vrijednosti možete vidjeti kako napreduje posao na projektu. Rezultat ove usporedbe naziva se odstupanjem rasporeda. 

Ako je planirana vrijednost za razdoblje veća od zarađene vrijednosti, količina posla koji je obavljen na projektu manja je od planirane. Stoga projekt kasni s rokom. Budući da su planirana i zarađena vrijednost izraženi u novčanim vrijednostima, vrijeme kašnjenja projekta dobiva i novčanu vrijednost. 

Ako je planirana vrijednost za razdoblje manja od zarađene vrijednosti, količina posla koji je obavljen na projektu veća je od planirane. Stoga se projekt izvršava prije roka. Ovo vrijeme izvedbe također dobiva novčanu vrijednost.

**Odstupanje troška** Budući da zarađena vrijednost upotrebljava cijenu koštanja kao multiplikator, zarađena vrijednost označava trošak posla koji je obavljen na projektu. Kako projekt napreduje, zapisnik transakcija daje evidenciju novca koji se stvarno troši na tom projektu. Usporedbom zarađene vrijednosti sa stvarnim troškom možete vidjeti količinu novca koji se troši u odnosu na zarađenu vrijednost. Rezultat ove usporedbe naziva se odstupanjem troška. 

Ako je stvarni trošak potrošen u razdoblju veći od zarađene vrijednosti, potrošeno je više novca nego što je zarađeno. Stoga je projekt premašio proračun. 

Ako je stvarni trošak potrošen u razdoblju manji od zarađene vrijednosti, više je novca zarađeno nego što je potrošeno. Stoga je projekt u okvirima proračuna.

## <a name="wbs-templates"></a>WBS predlošci
Funkcionalnost WBS predložaka možete upotrebljavati za izradu standardnih predložaka za projekte. Ako projekti koje nudi vaša tvrtka obuhvaćaju puno poslova koji se ponavljaju, trebali biste razmisliti o stvaranju WBS predloška. 

WBS predložak možete stvoriti iz WBS-a postojećeg projekta, tako da se znanje i najbolje prakse koje ste prikupili tijekom planiranja tog projekta mogu ponovno upotrebljavati na sličnim projektima u budućnosti. Međutim, ponekad možda nema smisla spremiti cijeli WBS kao predložak. Stoga za projekt možete i izraditi predloške iz dijelova WBS-a.

### <a name="saving-a-projects-wbs-as-a-template"></a>Spremanje WBS-a projekta kao predloška

Nakon što stvorite predložak, možete ga uvesti u WBS novog projekta pod temeljnim čvorom ili pod neki zadatak u WBS-u projekta.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Uvoz WBS predloška u WBS projekta

Kada uvozite zadatke, oni se u predlošku organiziraju na temelju datuma početka zadatka pod kojim se uvoze. Tijekom uvoza, odnosi prethodnika na zadacima predloška upotrebljavaju se za izračunavanje datuma početka uvezenih zadataka. Standardni radni kalendar odredišnog projekta primjenjuje se za izračunavanje datuma završetka uvezenih zadataka, tako da se zadržavaju radni dani i standardno radni sati definirani u radnom kalendaru trenutačnog projekta. 

Iznosi troška i prodajne cijene u recima procjene primjenjuju se kako bi se zajamčilo da cijene specifične za projekt ili ugovor o projektu imaju valjane datume.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Razlike između WBS-a projekta i WBS predloška

-   Zadaci u WBS predlošcima nemaju datume početka i završetka.

Radni i neradni dani za WBS predloške nisu postavljeni.

-   WBS predlošci uvijek upotrebljavaju kalendar planiranja koji je postavljen kao zadani kalendar za sve projekte.

Zadani kalendar planiranja upotrebljava se samo za pronalaženje radnih sati u standardnom radnom danu.

-   Odnosi prethodnika nisu kopirani u WBS predložak.

Budući da WBS predlošci nemaju datume, logika datuma početka koja se temelji na datumu završetka prethodnika nije potrebna.

-   Redak procjene troška rada automatski se stvara kada se u WBS predlošku stvara zadatak. Prodajna cijena i iznos troška kopiraju se od odabranog radnika.

Izdaci i troškovi stavki mogu se stvarati ručno, baš kao što se mogu i na WBS-u projekta.

-   Pogreške u planiranju prikazuju se kada postoje odstupanja od sljedeće formule:

Rad = Broj resursa × trajanje × broj sati u standardnom radnom danu 

Sve pogreške u planiranju možete ispraviti istodobno klikom na mogućnost **Ispravi sve pogreške u planiranju**. 

Alternativno, pogreške u planiranju možete ispraviti i pojedinačno klikom na ikonu upozorenja za svaki zadatak.





[!INCLUDE[footer-include](../includes/footer-banner.md)]