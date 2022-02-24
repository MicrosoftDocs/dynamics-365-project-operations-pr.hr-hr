---
title: Što je novo ili promijenjeno u aplikaciji Project Service Automation, verzija 3
description: Ova tema pruža informacije o tome što je novo i promijenjeno u verziji 3 aplikacije Project Service Automation.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ce4c549b04716d466efa262dbc6a4abf28ea9eb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150659"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Što je novo ili promijenjeno u aplikaciji Project Service Automation, verzija 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ova tema pruža informacije o promjenama korisničkog sučelja (UI), funkcionalnosti i terminologije u aplikaciji Project Service Automation između verzije 2 ili verzije 1 i verzije 3.

## <a name="project-scheduling"></a>Planiranje projekta
Raspored projekta, koji je u prethodnim verzijama bio poznat kao strukturna analiza rada (WBS), preimenovan je u Raspored i pristupa mu se klikom na karticu **Raspored**. 

![Raspored projekta](media/psa-schedule-01.png)

Raspored sada ima novu površinu za interakciju koja je i moderna i pristupačna. Međutim, osnovni modul za planiranje aplikacije Project Service Automation nije se promijenio. Kontrolni gumbi u vrpci rešetke rasporeda omogućuju vam interakciju s rasporedom slično kao u prethodnoj verziji aplikacije Project Service Automation. Dodatne promjene rasporeda uključuju:

- **Ganttov grafikon** – Ganttov grafikon više nije prisutan. Novi vizualni prikaz Ganntova grafikona vratit će se u budućem ažuriranju.
- **Zaglavlja stupaca** – možete sakriti zaglavlja stupaca u rešetki klikom na pokazatelj prema dolje pored naslova stupca. 
- **Stupci** – možete prikazati skrivene stupce klikom na **Dodaj stupac**. 
- **Kategorija transakcije** – pretraživanje **Kategorije transakcije** dodano je u rešetku rasporeda i prikazuje se prema zadanim postavkama. 
 
## <a name="project-templates"></a>Predlošci projekta
Sljedeće su promjene napravljene za funkcionalnost predloška projekta.

### <a name="create-a-project-template"></a>Izradi predložak projekta 
U verziji 3 možete stvoriti predložak projekta slično kao u prethodnim verzijama aplikacije Project Service Automation. Predložak može sadržavati samo raspored, a raspored može uključivati zadatke, ali oni nisu potrebni. Ako raspored ima zadatke, oni mogu biti samo za generičke resurse. Možete generirati preduvjete za resurse za generičke resurse, ali ne mogu se rezervirati sa stvarnim resursima u predlošku. U predlošku ne možete rezervirati stvarni resurs za tim. 

### <a name="create-a-template-from-an-existing-template"></a>Stvaranje predloška iz postojećega predloška
Kada stvorite novi predložak projekta iz postojećeg predloška u verziji 3 aplikacije Project Service Automation, događa se sljedeće: 

- Raspored izvornog projekta kopira se u predložak. 
- Generički se resursi kopiraju u tim i svi se zadaci generičkih resursa kopiraju. Zahtjevi za generičke resurse se ne kopiraju. 

### <a name="create-a-template-from-an-existing-project"></a>Stvaranje predloška iz postojećega projekta
Kada stvorite novi predložak projekta iz postojećeg projekta u verziji 3 aplikacije PSA, događa se sljedeće: 

- Raspored izvornog projekta kopira se u predložak. 
- Generički se resursi kopiraju u tim i svi se zadaci generičkih resursa zadržavaju. Zahtjevi za generičke resurse se ne kopiraju.    
- Imenovani resursi, dodijeljeni ili nedodijeljeni, uklanjaju se iz tima i zamjenjuju generičkim resursima.
- Ako je prisutna, informacija o klijentu se uklanja. 
- Ako su prisutne, uklanjaju se reference na ponude i ugovore. 

### <a name="create-a-project-from-a-template"></a>Stvaranje projekta iz predloška
Kada u verziji 3 aplikacije Project Service Automation stvorite novi projekt iz predloška, događa se sljedeće:

- Raspored, tim i zadaci kopiraju se u novi projekt.   
- Datum je početka datum kopiranja ili datum koji korisnik odabere.   
- Za bilo koje generičke članove tima sa zahtjevima resursa u predlošku, zahtjevi se ne kopiraju ili automatski generiraju. Morat ćete ih generirati. 

## <a name="copy-a-project"></a>Kopiranje projekta
Kada u verziji 3 aplikacije Project Service Automation kopirate projekt, događa se sljedeće: 

- Procijenjeni se datum početka kopira, ali se može promijeniti.  
- Raspored i zadaci projekta se kopiraju. 
- Generički resursi i njihovi zadaci se kopiraju. Zahtjevi za resurse za generičke resurse se ne kopiraju. Morat ćete ih ponovno generirati. 
- Stvarni resursi i njihovi zadaci se ne kopiraju. Umjesto toga se zamjenjuju generičkim resursima. 
- Stvarni se podaci ne kopiraju u novi projekt. 

## <a name="move-a-scheduled-project"></a>Premještanje planiranog projekta
Kada premjestite raspored postojećeg projekta prema naprijed, događa se sljedeće: 

- Datumi zadatka automatski se premještaju kako bi odgovarali razdoblju premještanja. 
- Dodijeljeni generički resursi ostaju dodijeljeni.   
- Ako su generirani prije nego što je projekt premješten, zahtjevi za generički resurs ostaju isti i ne generiraju se ponovno automatski. Morat ćete ih ponovno generirati kako bi odražavali nove zadatke zbog premještanja zadatka. 
- Dodjele na stvarnim resursima mijenjaju se kako bi odgovarale premještanju datuma zadatka. Rezervacije na stvarnim resursima se ne mijenjaju. Morat ćete izmijeniti rezervacije pomoću prikaza usklađivanja. 
- Ne mijenjaju se resursi tima s rezervacijama bez zadataka. 
- Stvarni se podaci ne premještaju. 

## <a name="estimates"></a>Procjene
Procjene su podijeljene na dvije kartice: **Dodjela resursa** i **Procjene**. Kartica **Dodjela resursa** sadrži procjene truda i prikazuje dodjele resursa za zadatke u prikazu vremenske faze. Procjene možete uređivati na temelju onoga što je generirao modul planiranja.

![Kartica dodjela resursa prikazuje procjene truda i dodjele resursa za zadatke](media/resource-assignments-tab-02.png)

Kartica **Procjene** prikazuje iznose troška i prodaje za dodjele resursa. Iznosi su samo za čitanje. Obračun troškova i određivanje cijena prodaje sada se pokreće dodjeljivanjem članova tima u rasporedu. To znači da ako imate zadatak bez ikakve dodjele, zadatak će se prikazati ispod nedodijeljene grupe. To također znači da bez **uloge**, koja je zadana dimenzija određivanja cijena, neće biti procijenjenog troška ili prodaje ako imate klijenta ili ugovor/ponudu povezane s projektom. 

![Kartica procjene prikazuje iznose troška i prodaje](media/estimates-tab-03.png)
  
Kategorija je također podržana na zadacima u prikazu rasporeda. Grupiranje po kategoriji na prikazu procjena vremenske faze pružit će bolji doživljaj, posebno kada u projektu imate i procjene troškova. Procjene troškova unose se pomoću rešetke na pojedinačnoj kartici. 

Procjene troškova mogu se unijeti u rešetku na kartici **Procjene troškova**. 

![Kartica procjene troškova prikazuje rešetku procjene troškova](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Upravljanje resursima
U verziji 3 aplikacije Project Service Automation s novim objedinjenim klijentskim korisničkim sučeljem i promjenama u odnosu između rezervacija i dodjela, dodjeljivanje članova projektu generičkim ili stvarnim resursima dramatično se promijenilo u odnosu na verziju 2 i verziju 1. Međutim, koncepti resursa koji se mogu rezervirati, **stvarnih** i **generičkih** ostaju isti, kao i koncepti članova tima, zahtjeva, dodjela i rezervacija.   

![Korištenje birača resursa](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Dodjela stvarnog resursa koji se može rezervirati 
U verziji 3 aplikacije Project Service Automation rezervacije i dodjele zadataka nisu tako čvrsto isprepletene kao u prethodnim verzijama aplikacije Project Service Automation. Možete koristiti rešetku tima da biste rezervirali **stvarnog** člana tima, slično kao na tržištu.

Pomoću birača resursa u rasporedu možete odabrati člana tima koji je stvoren u prikazu tima, a zatim ih dodijeliti zadacima. Možete im nastaviti dodjeljivati zadatke, čak i uz njihove rezervacije. Koristite karticu **Usklađivanje** da biste uskladili članove tima koji imaju razlike u rezervacijama i dodjelama.

Birač resursa pokazat će članovima tima za projekt. Birača resursa možete koristiti i da biste pretražili i prikazali druge resurse koji se mogu rezervirati, a koji još nisu dio projektnog tima. Možete ih dodijeliti zadatku i postat će dio projektnog tima. Morat ćete ih rezervirati pomoću **Ploče s rasporedom** ili kartice **Usklađivanje**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Dodjela generičkog resursa koji se može rezervirati za zadatak i projektni tim, a zatim ispunjavanje stvarnim resursima pomoću Ploče s rasporedom 
U verziji 3 aplikacije Project Service Automation funkcionalnost generiranja tima ne koristi se za generičke resurse. Umjesto toga možete stvoriti i izravno dodijeliti generički resurs iz rasporeda upisivanjem naziva položaja generičkog resursa u ćeliju resursa u rasporedu. Ili možete odabrati ikonu resursa u ćeliji, a zatim pomoću birača resursa unesite naziv generičkog resursa koji želite stvoriti. Otvorit će se panel za brzo stvaranje koji vam omogućuje da postavite ulogu i jedinicu tvrtke ili ustanove člana tima generičkog resursa. Nakon što ste stvorili resurs, dodijeljen je zadatku i možete nastaviti dodjeljivati taj generički resurs drugim zadacima u rasporedu.    
 
Kada ste resurs dodijelili svim odgovarajućim zadacima, možete generirati zahtjev za resursom, a zatim ga ispuniti izravnom rezervacijom pomoću **Ploče s rasporedom** ili slanjem zahtjeva za resursom. Generičke resurse možete dodati i izravno u rešetku člana tima. 

Generički resursi dodaju se projektnom timu bez zahtjeva za resursom i s datumima početka/završetka projekta dok se ne generira zahtjev za resursom. Da biste generirali zahtjev, odaberite generički resurs i kliknite **Generiraj**. Veza sa zahtjevom sada se prikazuje, a potrebni sati bit će popunjeni dodijeljenim satima. Možete kliknuti vezu da biste otvorili i ažurirali zahtjev.
  
Kada je rezervacija dovršena i imenovani ju je resurs u potpunosti ispunio, generički se resurs zamjenjuje imenovanim resursom i dodjela u rasporedu ažurira se imenovanim resursom. 

Predloženi resursi za zahtjeve sada se pohranjuju na kartici umjesto u pojedinačnom odjeljku.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Nekoliko imenovanih resursa ispunjava generički resurs
Kada se zahtjev ispuni s nekoliko resursa, generički resurs ostaje u timu i dodijeljen je zadatku. Imenovani članovi tima koji su rezervirani nisu dodijeljeni kao dio položaja. Ako je potrebno, voditelj projekta može dodijeliti rad stvarnim resursima.  Prikaz **Usklađivanje** pruža analizu rezervacija preko nekoliko resursa do nekoliko dodjela zadataka. To se ne radi automatski jer u bilo kojem složenijem scenariju, kao u onome u kojem je komplet zadataka koji čine zahtjev, namjera kako upravitelj projekta želi dodjeljivati, mora biti pretpostavljena. Budući da sustav ne može razumjeti namjeru, pretpostavke će se vjerojatno razlikovati od namjere i pojavit će se netočan ili nepredvidljiv rezultat. Predvidljiv je ishod da generički resurs ostaje dodijeljen dok voditelj projekta namjerno ne dodijeli resurse pomoću prikaza **Usklađivanje**.

### <a name="reconciliation"></a>Usklađivanje
Kartica **Usklađivanje** prikazuje rezervacije i sve dodjele za svakog člana projektnog tima. Prikazuje sate u ćelijama koje mogu predstavljati vremenske točke od mjeseci do dana. Taj prikaz omogućuje voditeljima projekta usklađivanje rezervacija člana tima i njihovih zadataka za njihov projektni tim. To je korisno jer rezervacije i dodjele zadataka nisu čvrsto povezani što omogućuje veću fleksibilnost prilikom planiranja projekta. 

![Kartica Usklađivanje prikazuje rezervacije i dodjele za članove projektnog tima](media/resource-reconciliation-tab-06.png)

Za svaki resurs prikaz pokazuje razliku između rezervacija članova tima i skupne vrijednosti njihovih dodjela zadataka te prikazuje sljedeće dvije razlike koje se mogu pojaviti s rezervacijama i dodjelama u projektu: 

- **Nedostatak rezervacija** – nedostatak rezervacija pojavljuje se kada resurs ima više dodjela nego rezervacija. Budući da taj kapacitet nije rezerviran, voditelj projekta može ovo ispraviti produljivanjem rezervacija resursa kako bi se pokrio manjak. 
- **Previše rezervacija** – previše se rezervacija pojavljuje kada je resurs rezerviran za projekt, ali nije dodijeljen zadacima.  To može biti prihvatljiva pojava, na primjer, ako je resurs bio rezerviran prije dodjele zadatka. Međutim, u drugim slučajevima, resurs se možda neće planirati dodijeliti, a voditelj projekta trebao bi razmotriti otkazivanje rezervacija resursa kako bi se omogućilo korištenje kapaciteta za drugi projekt. 

Kada imate dodjele zadataka za resurs bez rezervacija (nedostatak rezervacija), možete odabrati zbirni nedostatak rezervacija i kliknuti na **Proširi rezervaciju**. Odavde možete prikazati rezervaciju koja je potrebna za rješavanje nedostatka resursa i njihove dostupnosti. 
 
## <a name="time-and-expense"></a>Vrijeme i trošak
Ovaj odjeljak pruža informacije o promjenama u vremenu, trošku i odobrenju u verziji 3 aplikacije Project Service Automation. Kao dio rješenja Dynamics 365 Project Service Automation osvježila se značajka **Unos vremena** za iskorištavanje okvira objedinjenog sučelja. To donosi dosljedno, objedinjeno korisničko sučelje koje slijedi načela responzivnog dizajna za optimalan prikaz na bilo kojoj veličini zaslona ili bilo kojem uređaju. 

### <a name="landing-page"></a>Odredišna stranica
Neproširivi prilagođeni doživljaj unosa vremena zastario je u verziji 3. Umjesto toga, sada je tu proširiv i dostupan doživljaj izvorne rešetke. Možete pristupiti funkcionalnosti unosa vremena pomoću karte web-mjesta na lijevoj strani. Uz ovu promjenu više nećete moći odjednom unositi vrijeme za jedan tjedan. Umjesto toga ćete morati stvoriti Unos vremena za svaki dan u rešetki. Nakon što se stvori nekoliko vremenskih unosa, korisnici mogu skupno stvarati vremenske unose s funkcijom **Kopiraj** koja će biti objašnjena kasnije u ovoj temi. 

![Odredišna stranica za Unos vremena](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Stvaranje novog unosa vremena 
Kliknite **Novo** na vrpci da biste otvorili stranicu za brzo stvaranje za Unos vremena gdje unosite trajanje u minutama, satima ili danima. Da biste to učinili, samo počnite upisivati h, m ili d zajedno s količinom.  

![Brzo stvaranje unosa vremena](media/quick-create-time-entry-08.png)

Sistemski prikazi podržavaju polja za pretraživanje. Na primjer, nakon što unesete informacije o projektu, polje **Projektni zadatak** prema zadanim je postavkama postavljeno na prikaz **Moji otvoreni projektni zadaci**. Da biste stvorili vremenske unose za zadatke koji nisu dodijeljeni korisniku, kliknite na prikaz **Promijeni** u pretraživanju, a zatim odaberite **Svi aktivni projektni zadaci**. Nakon što je Unos vremena stvoren i prikazuje se u rešetki, možete urediti bilo koje vrijednosti retka izravno u rešetki.  

### <a name="bulk-createcopy"></a>Skupno stvaranje/kopiranje 
Nakon što ste stvorili nekoliko vremenskih unosa, možete koristiti funkcionalnost kopiranja za skupno stvaranje dodatnih vremenskih unosa. Kliknite **Kopiraj** da biste otvorili dijalog **Kopiraj**. U **Iz razdoblja: datum početka** postavite raspon datuma od kojeg se vremenska razdoblja moraju kopirati. U **Do razdoblja: datum početka** navedite datum za koji se moraju stvarati Unos vremenai. Kliknite **Kopiraj** da biste kopirali vremenske unose u odgovarajući dan u tjednu naznačen u **Do razdoblja**. Na primjer, Unos vremena za ponedjeljak od prošlog tjedna kopirat će se u ponedjeljak za tjedan koji je naznačen u **Do razdoblja**. 

![Kopiranje vremenskih unosa u kompletu](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Uvoz podataka 
Dodjele i zamjena slijede isti uzorak korisničkog sučelja koji korisniku omogućuje navođenje raspona datuma od kada je potrebno uvesti rezervacije. Zatim morate izričito odabrati rezervacije koje treba kopirati u vremenske unose **Skica**. U verziji 3 više ne možete vidjeti uzorak vremenskih unosa **Predloženo** na rešetki i kalendaru.  

### <a name="change-in-calendar-control"></a>Promjena u kontroli kalendara
U verziji 3 odmaknuli smo se od prilagođene kontrole kalendara i sada koristimo UC kalendar za prikaz vremenskih unosa za tjedan dana. S ovim kalendarom možete prikazati dan, tjedan i mjesec. 

> [!NOTE]
> Ograničenje je kalendara to da ova kontrola ne podržava radnje na pojedinačnim stavkama kalendara. Na primjer, nećete moći odabrati jednu ili više stavki kalendara i slati ili brisati te stavke. Klikom na stavku kalendara otvorit će se stranica **Unos vremena** za dodatne radnje. 

### <a name="extensibility"></a>Proširivost
**Snimanje podataka u prilagođenim poljima samo u entitetima unosa vremena i unosa troška** – Unos vremena koristi rešetku koja se može uređivati, rešetku samo za čitanje i kontrole kalendara s platforme. Sve su to izvorne kontrole i stoga će podržavati prilagođavanja. U verziji 3 aplikacije Project Service Automation možete dodati dodatna prilagođena polja, postaviti polja za pretraživanje i stvoriti sigurnosnu kopiju s prilagođenim prikazima. Možete postaviti i prilagođenu poslovnu logiku na temelju odabranih vrijednosti u prilagođenim poljima.  

**Snimanje podataka u prilagođenim poljima u vremenskom unosu i unosu troška i prijenos putem entiteta koji podržavaju slanje i tijek odobravanja** – tipična obrada vremenskih unosa prikazana je na sljedećem dijagramu.

![Tijek obrade vremenskih unosa](media/process-time-entries-10.png)

Ako poslovni preduvjeti propisuju da entiteti vremena i troška moraju snimiti prilagođene dimenzije određivanja cijena i prenijeti vrijednosti koje su postavljene u resursu za vrijeme i unos u prilagođenoj dimenziji određivanja cijena kroz sve entitete u prethodnoj grafici, pogledajte članak [Postavljanje prilagođenih polja kao dimenzija određivanja cijena](set-up-pricing-dimensions.md)

Da biste podržali poslovne preduvjete u kojima entiteti vremena i troškova moraju snimiti prilagođene dimenzije koje ne određuju cijene i prenijeti vrijednosti, možete koristiti postavljanje dimenzija određivanja cijena i izraziti prilagođene dimenzije kao dimenzije određivanja cijena bez troška ili stope naplate. Drugi je scenarij dodavanje prilagođenog polja svakom entitetu pomoću istog naziva polja u svim entitetima. Prilagođeni dodaci mogu se stvoriti za povezivanje zapisa u entitetima koji sudjeluju u tijeku slanja/odobravanja pomoću entiteta izvora transakcija i povezivanja transakcija.  

### <a name="delegate-time-and-expense-entry"></a>Delegiranje unosa vremena i unosa troškova
Platforma Common Data Service ne podržava međusobno oponašanje korisnika, što znači da u verziji 3 aplikacije Project Service Automation ne postoji podrška za delegirane vremenske unose i unose troškova. Međutim, partneri i klijenti iskorištavali su zaobilazno rješenje da bi omogućili podršku za doživljaj delegiranih vremenskih unosa u verziji 3. To je samo zaobilazno rješenje, a ne potpuno rješenje, tako da je važno razumjeti ograničenja i koristiti taj pristup samo ako su ograničenja prihvatljiva. 

> [!IMPORTANT]
> Ove bi se informacije trebale smatrati predloženim smjernicama za prilagođenu implementaciju na strani partnera/klijenta. Tim proizvoda neće ponuditi službenu podršku za tu funkcionalnost putem bilo kojeg od naših kanala za podršku.

### <a name="customization-details"></a>Pojedinosti prilagođavanja 
Prilagođavanje vam omogućuje dodavanje **Resursa koji se može rezervirati** za doživljaje stvaranja i uređivanja, što će korisniku omogućiti da djeluje kao delegat promjenom polja **Resurs za rezervacije** na drugog korisnika za kojeg su Unos vremenai i unosi troška trebali biti snimljeni. Sljedeći koraci pokrivaju delegiranje vremenskih unosa. Ista se informacija primjenjuje za delegiranje unosa troškova. 
 
1.  Provjerite ima li delegirani korisnik ima globalni sigurnosni pristup na projektima i projektnim zadacima. 
1.  Budući da **Resurs koji se može rezervirati**, što je polje na entitetu **Unos vremena**, nije izložen na stranici **Brzo stvaranje** morate ga dodati.

    -ili-

    Stvorite prilagođeni prikaz koji obuhvaća stupac **Resurs koji se može rezervirati** kako biste pregledali samo vremenske unose koji su stvoreni za resurs. Objavite prilagođavanja na dizajneru modula aplikacija da bi se ovaj prikaz pojavio pod stavkom **Birač prikaza** na stranici **Unos vremenai**. Postoje dva dodatka koja obrađuju postavljanje voditelja za vremenske unose izvan projekta:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Stvorite novi dodatak da biste prebrisali polje **Voditelj** za voditelja korisnika dodijeljenog u polju **Resurs koji se može rezervirati**. Koristite istu **Fazu izvršavanja** kao izvankanalni (OOB) dodatak (prethodna provjera valjanosti) i koristite **Redoslijed izvršavanja** koji je veći od dodataka OOB (veći od 1). To će osigurati da se prilagođeni dodatak izvrši nakon dodataka OOB.  
 
### <a name="end-user-experience"></a>Doživljaj krajnjeg korisnika
1.  Kada stvorite Unos vremena na stranici za brzo stvaranje, unesite pojedinosti projekta i projektnog zadatka, a zatim odaberite korisnika u **Resurs koji se može rezervirati** za kojeg je potrebno zabilježiti vremenske unose. 
2.  Prema zadanim postavkama, ovo je polje zadano za prijavljenog korisnika, međutim, s obzirom na to da je korisnik nadjačao ovo polje, sada se stvara Unos vremena za odabrani **Resurs koji se može rezervirati**.
3.  Kada pošaljete vremenske unose koje ste stvorili za te zapise, unosi će biti u redu čekanja za odobravatelja u projektu kao što je očekivano. 
4.  Kada opozovete vremenske unose stvorene za drugog korisnika, vremenski će unosi biti vraćeni u stanje **Skica** s poljem **Resurs koji se može rezervirati** postavljenim na drugog korisnika. 
5.  Neobavezno se možete prebaciti na prilagođeni prikaz da biste filtrirali vremenske unose stvorene za drugog korisnika. 
 
### <a name="limitations"></a>Ograničenja
Funkcionalnosti **Kopiraj** i **Uvezi** rade samo u kontekstu prijavljenog korisnika. To znači da nije moguće kopirati ili importirati vremenske unose koji su stvoreni za korisnika koji je prijavljen kao resurs koji se može rezervirati.

Unos vremenai koji nisu za projekt bit će usmjereni na odobravanje voditelju resursa koji se može rezervirati samo ako je korak 4 u gornjem odjeljku **Pojedinosti o prilagođavanju** dovršen. U suprotnome će se vremenske stavke izvan projekta za drugog korisnika nepravilno usmjeriti na voditelja prijavljenog korisnika. 

### <a name="other-changes"></a>Ostale promjene 
Uklonjena je funkcionalnost **Rezervacije i zadaci**. 

## <a name="multidimensional-pricing"></a>Višedimenzionalno određivanje cijena
Da biste povećali fleksibilnost i ispunili različite poslovne preduvjete, verzija 3 aplikacije Project Service Automation podržava diskretnu primjenu dimenzija određivanja cijena postavljenih na troškovima i stopama naplate. Vrijednosti dimenzija mogu se postaviti kao zadane, a zatim se prenijeti u postupku obračuna troškova i određivanja cijena od profiliranja resursa do vremenskih unosa u stvarne podatke projekta. Konfiguracija i izmjena ili proširenje za određene korisnike iskorištava standardnu infrastrukturu za prilagođavanje.

Aplikacija Project Service Automation dolazi sa zadanim skupom dimenzija određivanja cijena i uloga i jedinica resursa te omogućuje postavljanje cijena i troškova za svaku kombinaciju uloga i jedinica tvrtke ili ustanove.

Za klijente aplikacije Project Service Automation koji žele nastaviti koristiti ova unaprijed pripremljena polja kao dimenzije određivanja cijena u verziji 3, neće biti nikakve vidljive promjene. Možete nastaviti uobičajeno koristiti aplikaciju Project Service Automation. Međutim, ako morate odrediti cijenu ili trošak za svoje resurse pomoću drugih dodatnih atributa, verzija 3 omogućuje dodavanje vlastitih prilagođenih dimenzija za određivanje cijena u aplikaciji Project Service Automation. Proširenje prilagođenih dimenzija za određivanje cijena složen je doživljaj konfiguracije. 

## <a name="quotes-and-contracts"></a>Ponude i ugovori
U verziji 3 aplikacije Project Service Automation promijenili su se aspekti postavljanja i upravljanja za ponude i ugovore. Sljedeći odjeljci pružaju detaljnije informacije.

### <a name="set-up-chargeability-options"></a>Postavljanje opcija za mogućnost naplate
U verzijama 1 i 2 postavljanje mogućnosti naplate za uloge i kategorije za određene ponude i ugovore učinjeno je pomoću prikaza **Mogućnost naplate** koji je bio u gornjoj navigaciji retka ponude ili retka ugovora. To je također bilo mjesto gdje ste mogli postaviti cijene za te uloge i kategorije troškova.

Od verzije 3 postavljanje opcija naplate po ulozi i kategoriji troška bit će učinjeno na razini retka ponude ili retka ugovora. Postavljanje određivanja cijena odvojeno je od postavljanja mogućnosti naplate. Moći ćete pronaći **Naplative uloge** i **Naplative kategorije** kao kartice na stranicama **Redak ponude** i **Redak ugovora** bez korištenja gornje navigacije.

![Naplative uloge](media/chargeable-12.png)
 
Postavljanje Naplativih uloga i Naplativih kategorija također iskorištava gotovu rešetkastu kontrolu koja se može uređivati. Za svaku ulogu i kategoriju podržane opcije vrste naplate tijekom faze izrade ponude i ugovaranja ostaju nepromijenjene u odnosu na prethodne verzije kao **Naplativo** i **Nenaplativo**. **Besplatno** nije podržana vrsta tijekom faze izrade ponude ili ugovaranja. **Besplatno** je podržano samo tijekom odobravanja vremena ili troška.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Stvaranje i uređivanje prilagođenog određivanja cijena za ponudu i ugovor o projektu u aplikaciji Project Service Automation
U verzijama 1 i 2 korištenje prilagođenog cjenika za određene ponude i ugovore učinjeno je pomoću **Uredi cijene** u prikazu **Mogućnost naplate**. Prikaz **Mogućnost naplate** nalazio se u gornjoj navigaciji retka ponude ili retka ugovora. To je također bilo mjesto gdje ste mogli postaviti opcije mogućnosti naplate za uloge ili kategorije troškova.

Od verzije 3 aplikacije Project Service Automation stvaranje i uporaba prilagođenog cjenika projekta u ponudi i ugovoru o projektu odvojeni su od postavljanja mogućnosti naplate. Ponuda i ugovori o projektu u aplikaciji Project Service Automation sadrže novu karticu pod nazivom **Cjenici za projekt**. Ova kartica prikazuje pridruženi prikaz svih Cjenika za projekt koji su dodani ponudi ili ugovoru o projektu u aplikaciji Project Service Automation. Za stvaranje prilagođenog cjenika iz postojećeg cjenika koji je već pridružen ponudi za projekt ili ugovoru kliknite **Stvori prilagođeno određivanje cijena**. To će napraviti kopiju svih pridruženih cjenika i dodati ih ponudi ili ugovoru. Sada možete otvoriti cjenik i uređivati ulogu ili cijenu kategorije troška da bi se te promjene određivanja cijena primjenjivale samo na tu ponudu ili ugovor. 
  
Sljedeća je grafika prije stvaranja prilagođenih cjenika.

![Prije prilagođenih cjenika](media/before-custom-price-lists-13.png)

Sljedeća je grafika nakon stvaranja prilagođenih cjenika.

![Nakon prilagođenih cjenika](media/after-custom-price-lists-14.png)

> [!NOTE]
> Može se pojaviti kratko vrijeme odgode između vremena kada kliknete **Stvori prilagođeno određivanje cijena** i vremena kada će se stvoriti prilagođeni cjenik. Preporučujemo osvježavanje rešetke umjesto višestrukog klikanja. Prilagođeni je cjenik stvoren ako naziv pridruženog cjenika ima naziv ponude ili naziv ugovora o projektu koji mu se dodaje.
