---
title: Konfiguriranje parametara upravljanja troškom
description: U ovoj temi opisani su parametri koji kontroliraju opće ponašanje u upravljanju troškovima.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1cabb0be624f7f6c12761e4fb6d5a095396a5940a37616bb3a304798e1f97808
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007767"
---
# <a name="configure-expense-management-parameters"></a>Konfiguriranje parametara upravljanja troškom

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi opisani su parametri kontrole općeg ponašanja u upravljanju troškovima.

## <a name="general"></a>Općenito

| Polje                                                    | Opis |
|----------------------------------------------------------|-------------|
| Standardna cijena kilometraže                                 | Unesite cijenu naknade za troškove kilometraže. Ova se cijena množi s kilometražom koja se unosi za trošak kako bi se izračunao iznos koji se nadoknađuje za putni trošak. |
| Provjera valjanosti svrhe troška                                 | Uključite ovu mogućnost kako biste ograničili korisnike na postojeći skup vrijednosti koji je konfiguriran u polju **Svrha izvješća o troškovima** kada stvaraju izvješća o troškovima. |
| Osobni troškovi koje plaća                                | Odaberite tko je odgovoran za plaćanje iznosa transakcija kreditnom karticom koji su kategorizirani kao osobni. |
| Prikažite cijelo izvješće o troškovima kroz razine unatrag               | Odaberite ovu mogućnost kako biste prikazali sve troškove za izvješće o troškovima kada se pregledavaju pojedinosti izvornog dokumenta za određeni kupon koji je generiran kada je knjiženo izvješće o troškovima. |
| Prethodna je autorizacija putovanja obvezna                 | Odaberite ovu mogućnost kako biste zahtijevali da se putni nalog pošalje i odobri prije nego što zaposlenik može poslati izvješće o troškovima. |
| Dozvoli uređivanje raspodjela prije knjiženja            | Odaberite hoće li se raspodjele izvješća o troškovima moći uređivati prije knjiženja. |
| Procjena pravila za upravljanja troškovima                     | Odaberite kada će se troškovi procjenjivati kako biste utvrdili jesu li kršena pravila o troškovima. Procjena kršenja pravila o troškovima može se izvršiti kada se unese i spremi unos troška ili kada se trošak pošalje na odobrenje. Propisi pravilnika za potrebne račune procijenit će se kad se spremi redak troška. |
| Omogući retke troškova među tvrtkama                         | Odaberite mogu li se troškovi za ostale pravne osobe unijeti u izvješće o troškovima. |
| Dozvoli uređivanje tečaja za troškove kreditne kartice | Odaberite ovu mogućnost kako biste korisniku omogućili uređivanje tečaja za uvezene troškove kreditne kartice. |
| Polja višerazinske hijerarhije za prikaz                  | Odaberite koja će se polja odobravatelja prikazivati kada je vrsta dodjele tijeka rada postavljena na hijerarhiju, a odabir **Hijerarhija** postavljen je tako da upotrebljava hijerarhiju odobrenja, višerazinsko odobrenje troškova. Kada se za tijek rada upotrebljava hijerarhija višerazinskog odobrenja, odabrana polja prikazat će se u izvješću o troškovima i mogu se uređivati. |
| Unos broja kreditne kartice zaposlenika                        | Odaberite hoće li se u polje **ID kartice** na stranici **Kreditne kartice** za zaposlenika moći unijeti i spremiti broj s 15 ili 16 znakova. |
| Provjera valjanosti svrhe putnog naloga                      | Uključite ovu mogućnost kako biste ograničili korisnike na postojeći skup vrijednosti koji je konfiguriran u polju **Svrha izvješća o troškovima** kada stvaraju putne naloge. |

## <a name="financial"></a>Financije

| Polje                                                                                    | Opis |
|------------------------------------------------------------------------------------------|-------------|
| Naziv dnevne temeljnice glavne knjige                                                                | Odaberite naziv temeljnice glavne knjige u koji se knjiže odobrena izvješća o troškovima. |
| Omogućivanje povrata PDV-a iz troškova                                                        | Odaberite ovu mogućnost kako biste omogućili povrat PDV-a za prihvatljive troškove. Ova se mogućnost ne može odabrati ako su omogućena pravila SAD-a o porezu na promet i porezu na uporabu. |
| Gotovinske predujmove knjižite odmah                                                           | Odaberite ovu mogućnost za knjiženje odobrenog gotovinskog predujma kada je postupak plaćanja i prijenosa završen. Ako ova mogućnost nije odabrana, postupak plaćanja i prijenosa generira opću temeljnicu koja nije knjižena. |
| Ispravljanje datuma knjiženja tijekom knjiženja                                                   | Odaberite ovu mogućnost kako biste ažurirali datum knjiženja kada se knjiže troškovi, ako je tekuće razdoblje na čekanju ili je zatvoreno. Datum knjiženja postavit će se na sljedeće otvoreno razdoblje. |
| Omogući grupiranje transakcija na temelju računa za poravnanje navedenog u načinu plaćanja       | Odaberite ovu mogućnost kako biste saželi transakcije troškova za izvješće o troškovima, na temelju računa za poravnanje koji je naveden u načinu plaćanja troškova. |
| PDV uključen                                                                             | Odaberite ovu mogućnost kako biste prema zadanim postavkama u iznos troškova uključili PDV. |
| Oslobađanje opterećenja pri zatvaranju putnih naloga                                      | Odaberite ovu mogućnost za oslobađanje opterećenih sredstava kada se odobreni putni nalog zatvori. |
| Dozvoli slanja putnog naloga koji je prekoračio proračun registru proračuna i proračunu projekta | Odaberite ovu mogućnost kako biste zaposlenicima omogućili podnošenje putnog naloga na odobrenje, iako premašuju ili dozvoljeni proračun koji je postavljen u registru proračuna ili dozvoljeni proračun za projekt. |
| Dozvoli slanje izvješća o troškovima koji su prekoračili proračun registru proračuna i proračunu projekta     | Odaberite ovu mogućnost kako biste zaposlenicima omogućili slanje izvješća o troškovima na odobrenje, iako premašuju ili dozvoljeni proračun koji je postavljen u registru proračuna ili dozvoljeni proračun za projekt. |
| Dozvoli odobrenje izvješća o troškovima koji su prekoračili proračun samo registru proračuna                 | Odaberite ovu mogućnost kako biste odobravateljima dozvolili da odobre izvješća o troškovima koja premašuju dozvoljeni proračun postavljen u registru proračuna. |

## <a name="per-diem"></a>Po danu

| Polje                                 | Opis |
|---------------------------------------|-------------|
| Minimalni sati za dnevnice            | Unesite zadani minimalni broj sati koje zaposlenik mora odraditi u jednom danu kako bi imao pravo na dnevnicu za putne troškove. Ova se vrijednost upotrebljava kao zadana vrijednost samo za polje **Minimalni sati** za razine dnevnica. |
| Postotak za obrok                          | Unesite zadani postotak dnevnice za obroke koji se upotrebljavaju prvog i zadnjeg dana putnih troškova kada je polje **Izračunajte smanjenje obroka za** postavljeno bilo na mogućnost **Vrsta obroka dnevno** ili **Broj obroka dnevno**. Radni dan prvog i zadnjeg dana može biti kraći od standardnog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je postotak postavljen na **0** (nula), smanjenja za prvi i zadnji dan bit će 0,00. |
| Postotak za hotel                         | Unesite zadani postotak dnevnice za hotele koji se koriste prvog i zadnjeg dana putnih troškova. Radni dan prvog i zadnjeg dana može biti kraći od standardnog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je postotak postavljen na **0** (nula), smanjenja za prvi i zadnji dan bit će 0,00. |
| Ostali postoci                         | Unesite zadani postotak dnevnice za razne troškove koji se koriste prvog i zadnjeg dana putnih troškova. Radni dan prvog i zadnjeg dana može biti kraći od standardnog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je postotak postavljen na **0** (nula), smanjenja za prvi i zadnji dan bit će 0,00. |
| Postotno smanjenje za doručak | Unesite iznos za koji se umanjuje dnevnica za doručak. Primjerice, ako zaposlenik dobije besplatan doručak, možda ćete htjeti smanjiti iznos dnevnice za 10 posto. |
| Postotno smanjenje za ručak     | Unesite iznos za koji se umanjuje dnevnica za ručak. Primjerice, ako zaposlenik dobije besplatan ručak, možda ćete htjeti smanjiti iznos dnevnice za 15 posto. |
| Postotno smanjenje za večeru    | Unesite iznos za koji se umanjuje dnevnica za večeru. Primjerice, ako zaposlenik dobije besplatnu večeru, možda ćete htjeti smanjiti iznos dnevnice za 25 posto. |
| Izračunaj smanjenje obroka za           | Navedite kako sustav treba izračunati smanjenje dnevnice za obrok odabirom temelji li se smanjenje na vrsti obroka po putovanju ili po danu ili se temelji na dozvoljenom broju obroka dnevno. |
| Zaokruživanje dnevnica                     | Odaberite vrstu zaokruživanja koja se upotrebljava za troškove dnevnice. Ako odaberete uobičajeno zaokruživanje, svi troškovi dnevnice koji imaju iznos od 0,50 zaokružuju se na 1,00, a svi troškovi dnevnice koji imaju iznos manji od 0,50 zaokružuju se na 0,00. |
| Izračun osnovne dnevnice na          | Odaberite hoće li se iznos dnevnice temeljiti na kalendarskom danu ili razdoblju od 24 sata. |

## <a name="fax-cover-pages"></a>Naslovne stranice telefaksa

| Polje                          | Opis |
|--------------------------------|-------------|
| Upute                   | Unesite upute kojih se zaposlenici moraju pridržavati kada stvaraju naslovnu stranicu telefaksa koji se upotrebljava za slanje računa povezanih s izvješćem o troškovima. Za unos teksta specifičnog za jezik koji će se prikazivati na temelju jezika korisnika odaberite mogućnost **Prijevodi**. |
| ID korisnika (podaci crtičnog koda) | Odaberite ovu mogućnost kako biste jedinstveni identifikator zaposlenika spremili u crtični kod koji se upotrebljava na naslovnoj stranici telefaksa. |
| Crtični kod                       | Odaberite crtični kod koji se upotrebljava na naslovnoj stranici telefaksa. U upravljanju troškovima podržani su crtični kodovi 39 i 128. |

## <a name="anti-corruption"></a>Suzbijanje korupcije

| Polje                                 | Opis |
|---------------------------------------|-------------|
| Prikaži potvrdu o suzbijanju korupcije   | Odaberite ovu mogućnost kako biste tijekom stvaranja izvješća o troškovima prikazali tekst o suzbijanju korupcije. Tada se mogu omogućiti određene kategorije troškova zbog kojih će se u izvješću o troškovima odabrati potvrda o suzbijanju korupcije. Na primjer, kategorija poklona koja se odnosi na trošak državnog službenika može zahtijevati da zaposlenik potvrdi da je trošak u skladu s pravilima tvrtke koja se odnose na državne službenike. |
| Poruka o suzbijanju korupcije za podnositelja prijave | Unesite tekst koji bi trebao biti prikazan zaposleniku koji stvara izvješće o troškovima. Za unos teksta specifičnog za jezik koji će se prikazivati na temelju jezika korisnika odaberite mogućnost **Prijevodi**. |
| Poruka o suzbijanju korupcije za odobravatelja  | Unesite tekst koji bi trebao biti prikazan odobravatelju tijekom stvaranja izvješća o troškovima. Za unos teksta specifičnog za jezik koji će se prikazivati na temelju jezika korisnika odaberite mogućnost **Prijevodi**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]