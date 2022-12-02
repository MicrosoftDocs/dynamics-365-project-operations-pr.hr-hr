---
title: Stvaranje i potvrđivanje dnevnika unosa
description: U ovom se članku navode informacije o tome kako izraditi i potvrditi temeljnice u aplikaciji Microsoft Dynamics 365 Project Operations.
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

Temeljnice upotrebljavajte za evidentiranje stvarnih podataka izravno u aplikaciji Microsoft Dynamics 365 Project Operations. Kada se koristite temeljnicama, ne morate unositi zapisnike Vrijeme, Troškovi i Korištenje materijala u aplikaciji Project Operations.

Jednom temeljnicom možete izraditi više redaka u dnevniku. Kada se dnevnik potvrdi, redak temeljnice evidentira stvarne podatke za sljedeće pojedinosti:

- Trošak ili prihod, ovisno o vrsti transakcije koja je odabrana.
- Odabranu klasu transakcije. Dostupne klase su **Vrijeme**, **Trošak**, **Materijal**, **Akontacija**, **Kontrolna točka** i **Porez**.
- Projekt i/ili zadatak koji je odabran na retku u dnevniku.

Slijedite ove upute za izradu temeljnice u aplikaciji Project Operations.

1. Idite na **Prodaja** \> **Transakcije** \> **Dnevnici**.
2. U oknu Radnje na stranici popisa **Temeljnice** odaberite **Novo** da biste izradili dnevnik.
3. Na stranici **Novi dnevnik**, u polje **Opis** unesite opis dnevnika.
4. Provjerite je li polje **Vrsta dnevnika** postavljeno na **Unos**, a zatim odaberite **Spremi**. Nakon što se nova temeljnica spremi, na stranici dnevnika trebala bi se pojaviti kartica **Retci u dnevniku**.
5. Na alatnoj traci iznad rešetke na kartici **Retci u dnevniku** odaberite **Novo** da biste izradili redak temeljnice.
6. U dijaloškom okviru **Brza izrada** koji se upotrebljava za izradu retka temeljnice postavite polja kako je opisano u sljedećoj tablici.

    | Polje | Opis | Funkcionalni utjecaj |
    | --- | --- | --- |
    | Razred transakcije | Redak u dnevniku može se klasificirati u jednu od šest klasa transakcija: **Vrijeme**, **Trošak**, **Materijal**, **Akontacija**, **Kontrolna točka** ili **Porez**. | Razred transakcije **Porez** zastario je u aplikaciji Project Operations. <br> Ako izradite razred transakcije **Porez**, neće se obraditi fakturiranjem ili u izračunima troškova ili prihoda. **Kontrolna točka** je razred transakcije samo za prihod. <br>Razred transakcije **Akontacija** predstavlja predujam koji je primljen od klijenta. Uvijek se treba izraditi kao par kao par plaćenih i neplaćenih redaka iz dnevnika prodaje. |
    | Vrsta transakcije | Vrste transakcija **Trošak**, **Međuorganizacijska prodaja** i **Jedinična cijena resursa** trebaju se upotrebljavati za bilježenje troškova.<br> Vrste transakcije **Nenaplaćena prodaja** i **Naplaćena prodaja** trebaju se upotrebljavati za bilježenje prihoda. | Razred transakcije **Akontacija** radi samo s vrstama transakcije **Nenaplaćena prodaja** i **Naplaćena prodaja**.<br> Razred transakcije **Kontrolna točka** radi samo s vrstom transakcije **Naplaćena prodaja**. <br>Vrste transakcije **Međuorganizacijska prodaja** i **Jedinična cijena resursa** primjenjive su samo na razred transakcije **Vrijeme** i dostupne su samo u temeljnicama u scenariju Osnovne implementacije, a ne kada se aplikacija Project Operations implementira u scenarijima Resurs / Bez zaliha. |
    | Odabir proizvoda | Kada se odabere razred transakcije **Materijal**, to polje omogućuje vam odrediti je li transakcija materijala za koju izrađujete redak u dnevniku postojeći proizvod ili upisani proizvod. | Ako odaberite **Upisani proizvod**, možete unijeti naziv proizvoda. |
    | Proizvod | Referenca na proizvod iz kataloga. | |
    | Opis | Opis retka u dnevniku koji olakšava prepoznavanje. | Za nenaplaćene retke iz dnevnika prodaje vrijednost će se upotrebljavati kao opis prilikom izrade pojedinosti retka fakture. |
    | Vanjski opis | Opis retka u dnevniku koji se može upotrebljavati za dijeljenje s vanjskim zainteresiranim stranama. | Za nenaplaćene retke iz dnevnika prodaje vrijednost će se upotrebljavati kao vanjski opis prilikom izrade pojedinosti retka fakture. Može se pojaviti i na fakturi koja se šalje klijentu. |
    | Vrsta naplate | Vrijednost koja pokazuje hoće li se redak u dnevniku računati kao naplativa, besplatna ili nenaplativa komponenta projekta. | U tipičnom toku, vrsta naplate izvedena je iz dogovorenih uvjeta koji su postavljeni u ugovoru. Međutim, kada bilježite redak u dnevniku, možete unijeti vrijednost u to polje. |
    | Datum dokumenta | Upotrijebite datum kada se transakcija dogodila. | |
    | Datum početka | Upotrijebite datum na koji se transakcija dogodila. | To polje se koristi za usporedbu s datumom izrade fakture za transakcije vrste **Nenaplaćena prodaja**. Ta usporedba pomoći će vam da odlučite ima li transakcija budući ili prošli datum. Na fakturu će se dodati samo transakcije s prošlim datumom. |
    | Datum završetka | Upotrijebite datum na koji se transakcija dogodila. | |
    | Datum računovodstva | Upotrebljavajte datum pri bilježenju računovodstvenog utjecaja. | |
    | Klijent retka ugovora | Prema zadanim postavkama, ako redak ugovora ima samo jednog klijenta, ovo je polje postavljeno na klijenta u retku ugovora kada se redak u dnevniku spremi. Ako redak ugovora ima više klijenata, odaberite ispravnog klijenta u retku ugovora. | Ako sustav ne može odrediti klijenta retka ugovora u retku u dnevniku i ako je prazan na stvarnom podatku vrste **Nenaplaćena prodaja** izrađenom iz retka iz dnevnika, stvarni se podatak neće fakturirati. |
    | Project | Odaberite projekt za bilježenje stvarnog projekta. | Sustav će na temelju odabranog projekta, razreda transakcije i zadatka pokušati odrediti ugovor, redak ugovora i klijenta retka ugovora. |
    | Zadatak | Odaberite zadatak na kojem će se zabilježiti stvarni podatak. | Ako ste tijekom postavljanja ugovora povezali zadatke s retcima ugovora, sustav će upotrijebiti odabrani zadatak zajedno s projektom i razredom transakcije za određivanje ugovora, retka ugovora i klijenta retka ugovora. |
    | Kategorija transakcije | Odaberite kategoriju transakcije na kojoj će se zabilježiti stvarni podatak. | Za troškove, odabrana kategorija transakcije određuje zadanu cijenu koja će se unijeti u redak u dnevniku kada se spremi. |
    | Uloga | To je polje relevantno za retke u dnevniku Vrijeme. Odaberite ulogu resursa koji je proveo vrijeme na projektu i/ili zadatku. | Za retke u dnevniku Vrijeme, ako upotrebljavate gotovu konfiguraciju za unos zadanih troškova resursa i stopa naplate, odabrana uloga upotrebljava se zajedno s jedinicom resursa za određivanje zadane cijene koja će se unijeti u redak u dnevniku kada se spremi. Ako upotrebljavate prilagođenu konfiguraciju za unos zadanih cijena, trebali biste pregledati tu konfiguraciju da biste utvrdili upotrebljava li se polje **Uloga** za unos vrijednosti zadane cijene. |
    | Podugovor | Ako redak u dnevniku predstavlja podugovoreni kapacitet ili podugovorene troškove ili materijale, odaberite relevantni podugovor. | Kada se zabilježe redci u dnevniku Trošak, cjenik koji se upotrebljava za unos zadanog jediničnog troška određuje se prema odabranom podugovoru. |
    | Redak podugovora | Ako redak u dnevniku predstavlja podugovoreni kapacitet ili podugovorene troškove ili materijale, odaberite relevantni redak podugovora. | Kada se zabilježe redci u dnevniku Trošak, odabranim retkom podugovora osigurat će se da su dostupni izračuni kapaciteta u retku podugovora točno izračunati. |
    | Način izračuna iznosa | To polje je prema zadanim postavkama postavljeno na vrijednost **Množi količinu cijenom**. Kada se upotrebljava ta metoda, iznos će se izračunati kao *Količina* × *Cijena*. Druga podržana metoda je **Fiksna cijena**. Kada se upotrebljava ta metoda, cijena će se postaviti na iznos, a količina se neće upotrebljavati u izračunu. | |
    | Raspored jedinica i Jedinica | Raspored jedinica i jedinica zajedno identificiraju jedinicu količine. | Kombinacija jedinice i kategorije transakcije upotrebljava se za unos zadanih cijena za troškove. U zadanoj konfiguraciji aplikacije Project Operations, kombinacija jedinice, uloge i jedinice resursa upotrebljava se za unos zadanih cijena za vrijeme. Ako imate prilagođenu konfiguraciju za unos zadanih cijena, ona će se upotrebljavati zajedno s jedinicom. Kombinacija proizvoda i jedinice upotrebljava se za unos zadanih cijena za materijale. |
    | Količina | Unesite količinu. | |
    | Cijena | Ako se cijena ostavi praznom prilikom izrade retka u dnevniku, relevantne vrijednosti upotrebljavat će se za unos zadanih cijena, ovisno o razredu transakcije. Ako se cijena unese prilikom izrade retka u dnevniku, upotrebljavat će se ta cijena. | |
    | Porez | Unesite bilo koji iznos poreza. | Ovisno o unesenom iznosu poreza, dodatni iznos izračunat će se kao *Iznos* + *Porez*. |

## <a name="confirm-an-entry-journal"></a>Potvrđivanje temeljnice

Nakon što ste unijeli sve retke u dnevniku u temeljnici, možete potvrditi dnevnik. Tim će se procesom svi redci dnevnika zabilježiti kao stvarni podaci na odgovarajućim projektima.

Nakon što se dnevnik potvrdi, više ga ne možete uređivati dnevnik niti bilo koje njegove retke.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Stvarni podaci izrađeni potvrdom temeljnice

Postoji nekoliko ključnih razlika između stvarnih podataka koji se izrađuju potvrdom temeljnice i stvarnih podataka koji se izrađuju tijekom odobrenja zapisnika Vrijeme, Troškovi i Korištenje materijala te potvrde fakture u aplikaciji Project Operations:

- Temeljnice ne upotrebljavaju veze transakcije za povezivanje stvarnog podatka troška sa stvarnim podatkom nenaplaćene prodaje. Stvarni podaci koji se izrađuju kada se odobre zapisnici Vrijeme, Trošak i Korištenje materijala uvijek upotrebljavaju veze transakcije za povezivanje stvarnih podataka troškova i nenaplaćene prodaje.
- Temeljnice ne upotrebljavaju izvore transakcije za povezivanje stvarnih podataka troška i stvarnih podataka nenaplaćene prodaje s izvornim zapisom. Stvarni podaci koji se izrađuju kada se odobre zapisnici Vrijeme, Trošak i Korištenje materijala uvijek upotrebljavaju izvore transakcije za povezivanje stvarnih podataka troška i stvarnih podataka nenaplaćene prodaje s izvornim unosom vremena.
- Kada se fakturiraju stvarni podaci nenaplaćene prodaje koji su stvoreni potvrdom temeljnice, stvarni podaci naplaćene prodaje koji se izrađuju tijekom potvrde fakture povezuju se sa stvarnim podacima nenaplaćenih prodaja na sličan način kao stvarni podaci nenaplaćene prodaje koji se izrađuju kada se odobre zapisi Vrijeme, Trošak i Korištenje materijala.
- Redci temeljnice koji su izrađeni za vrijeme koje su unijeli međuorganizacijski resursi ne uzrokuju automatsku izradu stvarnih podataka vrsta **Jedinična cijena resursa** i **Međuorganizacijska prodaja**. Ti stvarni podaci moraju se izraditi ručno. To se ponašanje razlikuje od ponašanja za unose vremena koje bilježe međuorganizacijski resursi. U tom slučaju, kada se vrijeme odobri, aplikacija automatski izrađuje stvarne podatke vrste **Trošak** u projektu i stvarne podatke vrsta **Jedinična cijena resursa** i **Međuorganizacijska prodaja** za odjelu kojem zaposlenici pripadaju. Zatim upotrebljava veze transakcije za povezivanje tih stvarnih podataka i izvora transakcije te za njihovo povezivanje s izvornim vremenskim unosom.
- Kada se temeljnice potvrde, one izrađuju stvarne podatke. Međutim, dnevnike ispravaka nije moguće upotrijebiti za ispravljanje tih stvarnih podataka. To se ponašanje razlikuje od ponašanja stvarnih podataka koji se izrađuju kada se odobre zapisnici Vrijeme, Trošak i Korištenje materijala. U tom slučaju, aplikacija vam omogućuje upotrebu dnevnika ispravaka za ispravljanje stvarnih podataka radi ispravljanja grešaka, pod uvjetom da ti stvarni podaci još nisu fakturirani. Ako su već fakturirani, još uvijek možete ispraviti stvarni podatak ako obradite cjelokupni kredit tog stvarnog podatka klijentu.

> [!NOTE]
> Temeljnice nemaju stroga pravila za zadane vrijednosti. Stoga upotrebljavajte te temeljnice što je manje moguće i budite oprezni kako ne biste izradili neispravne financijske podatke u svom sustavu. Kad god možete, upotrebljavajte zapise Vrijeme, Trošak i Korištenje materijala, postavke kontrolne točke i akontacije u ugovorima o projektu i postupak potvrde fakture za projekt umjesto temeljnica za izradu stvarnih podataka.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
