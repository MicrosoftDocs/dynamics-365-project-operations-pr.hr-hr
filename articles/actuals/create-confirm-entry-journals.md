---
title: Stvaranje i potvrđivanje dnevnika unosa
description: U ovom se članku nalaze informacije o stvaranju i potvrđivanju dnevnika unosa u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912323"
---
# <a name="create-and-confirm-entry-journals"></a>Stvaranje i potvrđivanje dnevnika unosa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Temeljnice stavki koristite da biste zapisivali stvarne podatke izravno u Microsoftu Dynamics 365 Project Operations. Kada koristite temeljnice stavki, u projektne operacije ne morate unositi zapisnike o vremenu, troškovima i korištenju materijala.

Jedna temeljnica stavki omogućuje kreiranje više redaka temeljnice. Kada je temeljnica potvrđena, redak temeljnice stavki bilježi stvarno za sljedeće detalje:

- Trošak ili prihod, ovisno o odabranoj vrsti transakcije.
- Odabrana klasa transakcija. Dostupne klase su **Vrijeme**, Trošak **,** **Materijal**, Držač **,** **Prekretnica** i **Porez**.
- Projekt i/ili zadatak odabran u retku temeljnice.

Slijedite ove korake da biste stvorili temeljnicu stavki u operacijama projekta.

1. Otvorite Temeljnice **prodajnih** \> **·**\> transakcija.**·**
2. **Na stranici Popis temeljnica unosa** u oknu akcije odaberite **Novo** da biste stvorili temeljnicu.
3. **Na stranici Nova temeljnica** **u polje Opis** unesite opis temeljnice.
4. Provjerite je li polje Vrsta **temeljnice** postavljeno na **Stavka**, a zatim odaberite **Spremi**. Nakon spremanja nove temeljnice stavki na stranici temeljnice **trebala bi se pojaviti kartica Reci** temeljnice.
5. Na kartici Reci temeljnice **na** alatnoj traci iznad rešetke odaberite **Novo** da biste stvorili redak temeljnice unosa.
6. **U dijaloškom okviru Brzo kreiranje** za stvaranje retka temeljnice unosa postavite polja kako je opisano u sljedećoj tablici.

    | Polje | Opis | Funkcionalni utjecaj |
    | --- | --- | --- |
    | Razred transakcije | Redak temeljnice može se svrstati u jednu od šest klasa transakcija: **Vrijeme**, **Trošak**, **Materijal**, **Akontacija,** Ključna **etapa** ili **Porez**. | Klasa **poreznih** transakcija zastarjela je u projektnim operacijama. <br> Ako kreirate klasu **poreznih** transakcija, ona se neće obraditi fakturiranjem ili izračunima troškova ili prihoda. **Prekretnica** je klasa transakcija samo prihoda. <br>Klasa **transakcija Retainer** predstavlja predujam koji je primljen od kupca. Uvijek ga treba kreirati kao par naplaćenih redaka prodajne i nenaplaćene temeljnice prodaje. |
    | Vrsta transakcije | Za bilježenje troška trebale bi se koristiti vrste transakcija troškova **troškova**, **interorg prodaje** i **resourcing jediničnog troška**.<br> Vrste **transakcija Neplaćena prodaja** i **Naplaćena prodaja** trebale bi se koristiti za bilježenje prihoda. | Klasa **transakcija Retainer** radi samo s **vrstama transakcija Neplaćena prodaja** i **Naplaćena prodaja**.<br> Klasa **transakcija Prekretnica** funkcionira samo s vrstom transakcije naplaćena **prodaja**. <br>Vrste transakcija jediničnih troškova **prodaje** i **resursa Interorg primjenjuju** se samo **na klasu transakcija s vremenom** i one se mogu koristiti samo u ulaznim časopisima u scneariju implementacije Lite, a ne pri implementaciji projektnih operacija u scenarijima resursa / bez zaliha. |
    | Odabir proizvoda | Kada je odabrana **klasa transakcija Materijal**, ovo polje omogućuje vam da navedete je li transakcija materijala za koju kreirate redak temeljnice postojeći proizvod ili dopisani proizvod. | Ako odaberete **Dopisani proizvod**, možete unijeti naziv proizvoda. |
    | Proizvod | Referenca na proizvod iz kataloga. | |
    | Opis | Opis retka temeljnice koji olakšava prepoznavanje. | Za retke temeljnice prodaje vrijednost će se koristiti kao opis prilikom kreiranja detalja retka fakture. |
    | Vanjski opis | Opis retka temeljnice koji se može koristiti za zajedničko korištenje s vanjskim dionicima. | Za retke temeljnice prodaje vrijednost će se koristiti kao vanjski opis prilikom kreiranja detalja retka fakture. Može se pojaviti i na fakturi koja se šalje kupcu. |
    | Vrsta naplate | Vrijednost koja pokazuje hoće li se redak temeljnice računati kao komponenta za naplatu, besplatnu ili nenaplativu komponentu na projektu. | U tipičnom tijeku vrsta naplate izvedena je iz dogovorenih uvjeta koji su postavljeni na ugovor. Međutim, kada bilježite redak temeljnice, u ovo polje možete unijeti vrijednost. |
    | Datum dokumenta | Koristite datum kada se transakcija dogodila. | |
    | Datum početka | Koristite datum kada se transakcija dogodila. | Ovo se polje koristi za usporedbu s datumom kreiranja fakture za transakcije vrste Nenaplaćena **prodaja**. Ova usporedba pomoći će vam da odlučite je li transakcija datirana budućnošću ili datirana. Na fakturu će biti dodane samo transakcije s prošlim datumom. |
    | Datum završetka | Koristite datum kada se transakcija dogodila. | |
    | Datum računovodstva | Koristite datum kada će se zabilježiti računovodstveni učinak. | |
    | Kupac retka ugovora | Prema zadanim postavkama, ako redak ugovora ima samo jednog kupca, ovo je polje postavljeno na kupca u retku ugovora prilikom spremanja retka temeljnice. Ako redak ugovora ima više kupaca, odaberite ispravnog kupca u retku ugovora. | Ako sustav ne može odrediti kupca retka ugovora u retku temeljnice i ako je prazan u odnosu na stvarnu vrstu Nebilarna prodaja **kreiranu iz retka temeljnice**, stvarni se neće fakturirati. |
    | Project | Odaberite projekt na koji želite zabilježiti stvarno. | Na temelju odabranog projekta, klase transakcije i zadatka, sustav će pokušati odrediti kupca ugovora, retka ugovora i retka ugovora. |
    | Zadatak | Odaberite zadatak na koji želite zabilježiti stvarno. | Ako ste zadatke povezali s recima ugovora tijekom postavljanja ugovora, sustav će koristiti odabrani zadatak, zajedno s projektom i klasom transakcija, da bi odredio kupca u retku ugovora, retku ugovora i retku ugovora. |
    | Kategorija transakcije | Odaberite kategoriju transakcije na koju želite zabilježiti stvarno. | Za troškove odabrana kategorija transakcije određuje zadanu cijenu koja će se prilikom spremanja unijeti u redak temeljnice. |
    | Uloga | Ovo je polje relevantno za retke temeljnice vremena. Odaberite ulogu resursa koji je proveo vrijeme na projektu i/ili zadatku. | Za retke temeljnice vremena, ako koristite gotovu konfiguraciju za unos zadanih troškova resursa i stopa računa, odabrana uloga koristi se zajedno s jedinicom resursa za određivanje zadane cijene koja će se unijeti u redak temeljnice prilikom spremanja. Ako za unos zadanih cijena koristite prilagođenu konfiguraciju, pregledajte tu konfiguraciju **da biste utvrdili koristi li se polje Uloga** za unos zadanih vrijednosti cijena. |
    | Podugovor | Ako redak temeljnice predstavlja kapacitet kooperacije ili troškove ili materijale kooperanta, odaberite odgovarajući kooperant. | Kada se bilježe reci temeljnice troškova, odabrani kooperant odredit će cjenik koji se koristi za unos zadanog jediničnog troška. |
    | Redak kooperacije | Ako redak temeljnice predstavlja kapacitet kooperacije ili troškove ili materijale kooperanta, odaberite odgovarajući redak podugovaranja. | Kada se zabilježe reci temeljnice troškova, odabrani redak podugovaratelja osigurat će ispravno izračunavanje dostupnih izračuna kapaciteta u retku kooperanta. |
    | Način izračuna iznosa | Po zadanome, ovo je polje postavljeno na **Množi količinu po cijeni**. Kada se ova metoda koristi, iznos će se izračunati kao *Količina* × *cijeni*. Druga podržana metoda je **Fiksna cijena**. Kada se ova metoda koristi, cijena će biti postavljena na iznos, a količina se neće koristiti u izračunu. | |
    | Raspored jedinica i jedinica | Jedinični raspored i jedinica zajedno identificiraju jedinicu količine. | Kombinacija jedinice i kategorije transakcije koristi se za unos zadanih cijena troškova. U zadanoj konfiguraciji operacija projekta kombinacija jedinice, uloge i jedinice resursa koristi se za unos zadanih cijena za vrijeme. Ako imate prilagođenu konfiguraciju za unos zadanih cijena, ona će se koristiti zajedno s jedinicom. Kombinacija proizvoda i jedinice koristi se za unos zadanih cijena materijala. |
    | Količina | Unesite količinu. | |
    | Cijena | Ako cijena ostane prazna prilikom kreiranja retka temeljnice, odgovarajuće vrijednosti koristit će se za unos zadanih cijena, ovisno o klasi transakcije. Ako se prilikom kreiranja retka temeljnice unese cijena, koristit će se ta cijena. | |
    | Porez | Unesite bilo koji iznos poreza. | Ovisno o unesenom iznosu poreza, prošireni iznos izračunat će se kao *porez na* + *iznos*. |

## <a name="confirm-an-entry-journal"></a>Potvrda dnevnika stavki

Nakon što unesete sve retke temeljnice u temeljnicu stavki, možete potvrditi temeljnicu. Ovaj proces bilježit će svaki redak temeljnice kao stvarne na odgovarajućim projektima.

Nakon potvrde temeljnice više je ne možete uređivati ni bilo koji njezin redak.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Stvarne vrijednosti kreirane potvrdom temeljnice stavki

Postoji nekoliko ključnih razlika između stvarnih vrijednosti kreiranih potvrdom temeljnice stavki i stvarnih vrijednosti kreiranih tijekom odobravanja zapisnika o vremenu, troškovima i korištenju materijala te potvrde fakture u operacijama projekta:

- Temeljnice stavki ne koriste transakcijske veze da bi povezale stvarni trošak sa stvarnim iznosom neplaćene prodaje. Stvarne vrijednosti koje se kreiraju kada su odobreni zapisnici o korištenju vremena, rashoda i materijala uvijek koriste transakcijske veze za povezivanje troškova i neplaćenih iznosa prodaje.
- Temeljnice stavki ne koriste podrijetlo transakcija da bi povezale stvarne troškove i neplaćene iznose prodaje s bilo kojim izvornim zapisom. Stvarne vrijednosti koje se kreiraju kada se odobre zapisnici o korištenju vremena, troškova i materijala uvijek koriste podrijetlo transakcije za povezivanje troškova i neplaćenih iznosa prodaje s izvornom stavkom vremena.
- Kada se fakturiraju neograničeni iznosi prodaje kreirani potvrdom temeljnice stavke, naplaćene vrijednosti prodaje kreirane tijekom potvrde fakture povezane su s neplaćenim vrijednostima prodaje, na sličan način kao i neplaćene količine prodaje kreirane kada se odobre zapisi o vremenu, rashodima i korištenju materijala.
- Reci temeljnice stavki kreirani za vrijeme koje unose resursi međuorganizacije ne uzrokuju automatsko kreiranje stvarnih jediničnih troškova **izvora** i **vrsta interorg prodaje**. Te stvarne stvari moraju biti ručno kreirane. Takvo se ponašanje razlikuje od ponašanja unosa vremena koje bilježe međuorganizacijski resursi. U tom slučaju, kada je vrijeme odobreno, aplikacija automatski stvara stvarne podatke **vrste troška** na projektu i stvarne vrijednosti jediničnog **troška** resourcinga i **interorg prodaje** u odjelu vlasništva zaposlenika. Zatim koristi transakcijske veze za povezivanje tih stvarnosti i porijekla transakcija kako bi ih povezao s izvornom stavkom vremena.
- Kada se potvrde temeljnice stavki, one kreiraju stvarne. Međutim, temeljnice ispravaka ne mogu se koristiti za ispravljanje tih stvarnih vrijednosti. Takvo se ponašanje razlikuje od ponašanja stvarnih elemenata stvorenih kada se odobre zapisnici o vremenu, troškovima i korištenju materijala. U tom slučaju aplikacija vam omogućuje korištenje temeljnica ispravaka za ispravljanje stvarnih vrijednosti za ispravljanje bilo kakvih pogrešaka, pod uvjetom da te stvarne vrijednosti još nisu fakturirane. Ako su već fakturirane, i dalje možete ispraviti stvarnu ako kupcu obradite puni kredit tog stvarnog iznosa.

> [!NOTE]
> Temeljnice unosa ne provode stroga zadana pravila. Stoga koristite ove dnevnike unosa što je manje moguće te budite oprezni i oprezni kako biste osigurali da ne stvarate oštećene financijske podatke u svom sustavu. Kad god možete, za kreiranje stvarnih vrijednosti koristite zapisnike o vremenu, troškovima i korištenju materijala, postavu ključne etape i akontacije na ugovorima o projektu te postupak potvrde fakture projekta umjesto temeljnica stavki.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
