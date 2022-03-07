---
title: Parametri upravljanja troškovima
description: Sljedeći parametri nadziru ponašanje u upravljanju troškovima.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ef48f844656ff5197ae1731fb3f9bdf91a1a906b16f35bb2124469743a9e954
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991342"
---
# <a name="expense-management-parameters"></a>Parametri upravljanja troškovima


Parametri nadziru općenito ponašanje u upravljanju troškovima.

### <a name="general"></a>Općenito

| **Polje**                                                | **Opis**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardna cijena kilometraže**                             | Unesite cijenu naknade za troškove kilometraže. Cijena će se množiti s kilometražom koja se unosi za trošak kako bi se izračunao iznos koji se nadoknađuje za putni trošak.                       |
|**Osobni troškovi koje plaća**                             | Odaberite tko je odgovoran za plaćanje iznosa transakcija kreditnom karticom koji su kategorizirani kao osobni.                                                                                                     |
|**Prikažite cijelo izvješće o troškovima kroz razine unatrag**               | Odaberite ovu mogućnost kako biste prikazali sve troškove za izvješće o troškovima kada se pregledavaju pojedinosti izvornog dokumenta za određeni kupon koji je generiran kada je knjiženo izvješće o troškovima.              |
|**Prethodna je autorizacija putovanja obvezna**                 | Odaberite ovu mogućnost kako biste zahtijevali da se putni nalog pošalje i odobri prije nego što zaposlenik može poslati izvješće o troškovima.                                                                    |
|**Dozvoli uređivanje raspodjela prije knjiženja**            | Odaberite hoće li se raspodjele izvješća o troškovima moći uređivati prije knjiženja.                                                                                                                 |
|**Procjena pravila za upravljanja troškovima**                     | Odaberite kada će se troškovi procjenjivati kako biste utvrdili jesu li kršena pravila o troškovima. Provjera kršenja pravila o troškovima može se izvršiti kada se unese i spremi unos troška ili kada se trošak pošalje na odobrenje. Propisi pravilnika za potrebne fakture provjerit će se kad se spremi redak troška.                   |
|**Omogući retke troškova među tvrtkama**                         | Odaberite hoćete li dozvoliti unos troškova za ostale pravne osobe unutar izvješća o troškovima.                                                                                                          |
|**Dozvoli uređivanje tečaja za troškove kreditne kartice** | Odaberite ovu mogućnost kako biste korisniku omogućili uređivanje tečaja za uvezene troškove kreditne kartice.                                                                        |
|**Polja višerazinske hijerarhije za prikaz**                  | Odaberite koja će se polja odobravatelja prikazivati kada je vrsta dodjele tijeka rada postavljena na hijerarhiju, a odabir hijerarhije postavljen tako da upotrebljava hijerarhiju višerazinskog odobrenje troškova. Kada se za tijek rada upotrebljava hijerarhija višerazinskog odobrenja, odabrana polja prikazat će se u izvješću o troškovima i mogu se uređivati. |
|**Unos broja kreditne kartice zaposlenika (ažuriranje za lipanj 2017.)**     | Odaberite hoće li se u polje **ID kartice** na stranici **Kreditne kartice** za zaposlenika moći unijeti i spremiti broj s 15 ili 16 znakova.                                                                          |

### <a name="financial"></a>Financije

| **Polje**                                                            | **Opis**     |
|----------------------------------------------------------------------|------------------------------------|
|**Naziv dnevne temeljnice glavne knjige**                                         | Odaberite naziv temeljnice glavne knjige u koji se knjiže odobrena izvješća o troškovima.            |
|**Omogućivanje povrata PDV-a iz troškova**                                  | Odaberite ovu mogućnost kako biste omogućili povrat PDV-a za prihvatljive troškove. Ova se mogućnost ne može omogućiti ako su omogućena pravila SAD-a o porezu na promet i porezu na uporabu.      |
|**Gotovinske predujmove knjižite odmah**                                     | Odaberite ovu mogućnost za knjiženje odobrenog gotovinskog predujma kada je postupak plaćanja i prijenosa završen. Ako ova mogućnost nije odabrana, postupak plaćanja i prijenosa generirat će opću temeljnicu koja nije knjižena. |
|**Ispravljanje datuma knjiženja tijekom knjiženja**                             | Odaberite ovu mogućnost kako biste ažurirali datum knjiženja kada se knjiže troškovi, ako je tekuće razdoblje na čekanju ili je zatvoreno. Datum knjiženja postavit će se na sljedeće otvoreno razdoblje.   |
|**Omogući grupiranje transakcija na temelju računa za poravnanje navedenog u načinu plaćanja**      | Odaberite ovu mogućnost kako biste saželi transakcije troškova za izvješće o troškovima, na temelju računa za poravnanje navedenog u načinu plaćanja troškova.   
|**PDV uključen**                                                   | Odaberite ovu mogućnost kako biste prema zadanim postavkama u iznos troškova uključili PDV.             |
|**Oslobađanje opterećenja pri zatvaranju putnih naloga**            | Odaberite ovu mogućnost za oslobađanje opterećenih sredstava kada se odobreni putni nalog zatvori.                                                                                   |
|**Dozvoli slanja putnog naloga koji je prekoračio proračun registru proračuna i proračunu projekta** | Odaberite ovu mogućnost kako biste zaposlenicima omogućili slanje putnog naloga na odobrenje iako premašuju ili dozvoljeni proračun koji je postavljen u registru proračuna ili dozvoljeni proračun za projekt.            |
|**Dozvoli slanje izvješća o troškovima koji su prekoračili proračun registru proračuna i proračunu projekta**    | Odaberite ovu mogućnost kako biste zaposlenicima omogućili slanje izvješća o troškovima na odobrenje, iako premašuju ili dozvoljeni proračun koji je postavljen u registru proračuna ili dozvoljeni proračun za projekt.                |
|**Dozvoli odobrenje izvješća o troškovima koji su prekoračili proračun samo registru proračuna**                | Odaberite ovu mogućnost kako biste odobravateljima dozvolili da odobre izvješća o troškovima koja premašuju dozvoljeni proračun postavljen u registru proračuna.                                                                       |

### <a name="per-diem"></a>Po danu

| **Polje**                             | **Opis**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimalni sati za dnevnice**           | Unesite zadani minimalni broj sati koje zaposlenik mora odraditi u jednom danu kako bi imao pravo na dnevnicu za putne troškove.  Ova se vrijednost upotrebljava samo kao zadana vrijednost za polje Minimalni sati za razine dnevnica.                                                                                      |
|**Postotak za obrok**                          | Unesite zadani postotak dnevnice za obroke koji se upotrebljavaju prvog i zadnjeg dana putnih troškova kada je polje **Izračunajte smanjenje obroka za** postavljeno bilo na mogućnost **Vrsta obroka dnevno** ili **Broj obroka dnevno**. Radni dan prvog i zadnjeg dana može biti kraći od standardnog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je postotak postavljen na 0 (nula), tada će smanjenja za prvi i zadnji dan biti 0,00. |
|**Postotak za hotel**                        | Unesite zadani postotak dnevnice za hotele koji se koriste prvog i zadnjeg dana putnih troškova. Radni dan prvog i zadnjeg dana može biti kraći od standardnog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je postotak postavljen na 0 (nula), tada će smanjenja za prvi i zadnji dan biti 0,00.                                              |
|**Ostali postoci**                        | Unesite zadani postotak dnevnice za razne troškove koji se koriste prvog i zadnjeg dana putnih troškova. Radni dan prvog i zadnjeg dana može biti kraći od standardnog radnog dana. Stoga bi se iznos dnevnice tih dana mogao razlikovati od standardnog iznosa. Ako je postotak postavljen na 0 (nula), tada će smanjenja za prvi i zadnji dan biti 0,00.                                                                                                     |
|**Postotno smanjenje za doručak** | Unesite iznos za koji se umanjuje dnevnica za doručak. Primjerice, ako zaposlenik dobije besplatan doručak, možda ćete htjeti smanjiti iznos dnevnice za 10 posto.                               |
|**Postotno smanjenje za ručak**    | Unesite iznos za koji se umanjuje dnevnica za ručak. Primjerice, ako zaposlenik dobije besplatan ručak, možda ćete htjeti smanjiti iznos dnevnice za 15 posto.                                       |
|**Postotno smanjenje za večeru**   | Unesite iznos za koji se umanjuje dnevnica za večeru. Primjerice, ako zaposlenik dobije besplatnu večeru, možda ćete htjeti smanjiti iznos dnevnice za 25 posto.                                     |
|**Izračunaj smanjenje obroka za**         | Odaberite način na koji sustav treba izračunati smanjenje dnevnice za obrok odabirom temelji li se smanjenje na vrsti obroka po putovanju ili po danu ili se smanjenje temelji na dozvoljenom broju obroka dnevno.|
|**Zaokruživanje dnevnica**                  | Odaberite vrstu zaokruživanja koja se upotrebljava za troškove dnevnice. Ako odaberete uobičajeno zaokruživanje, svi troškovi dnevnice koji imaju iznos od 0,50 zaokružuju se na 1,00, a svi troškovi dnevnice koji imaju iznos manji od 0,50 zaokružuju se na 0,00.                                                                                              |
|**Izračun osnovne dnevnice na**         | Odaberite hoće li se iznos dnevnice temeljiti na kalendarskom danu ili razdoblju od 24 sata.       |

### <a name="fax-cover-pages"></a>Naslovne stranice telefaksa

| **Polje**                      | **Opis**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Upute**                   | Unesite upute kojih se zaposlenici moraju pridržavati kada stvaraju naslovnu stranicu telefaksa koji se upotrebljava za slanje računa povezanih s izvješćem o troškovima. Za unos teksta specifičnog za jezik koji će se prikazivati na temelju jezika korisnika kliknite mogućnost **Prijevodi**. |
|**ID korisnika (podaci crtičnog koda)** | Odaberite ovu mogućnost kako biste jedinstveni identifikator zaposlenika spremili u crtični kod koji se upotrebljava na naslovnoj stranici telefaksa.                 |
|**Crtični kod**                      | Odaberite crtični kod koji se upotrebljava na naslovnoj stranici telefaksa. U upravljanju troškovima podržani su crtični kodovi 39 i 128.               |

### <a name="anti-corruption"></a>Suzbijanje korupcije

|                 <strong>Polje</strong>                 |                                                                                                                                                                                            <strong>Opis</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Prikaži potvrdu o suzbijanju korupcije</strong>  | Odaberite ovu mogućnost kako biste tijekom stvaranja novog izvješća o troškovima prikazali tekst o suzbijanju korupcije. Tada se mogu omogućiti određene kategorije troškova zbog kojih će se u izvješću o troškovima odabrati potvrda o suzbijanju korupcije. Na primjer, kategorija poklona koja se odnosi na trošak državnog službenika može zahtijevati da zaposlenik potvrdi da je trošak u skladu s pravilima tvrtke koja se odnose na državne službenike. |
| <strong>Poruka o suzbijanju korupcije za podnositelja prijave</strong> |                                                                                             Unesite tekst koji će se prikazati zaposleniku tijekom izrade novog izvješća o troškovima. Za unos teksta specifičnog za jezik koji će se prikazivati na temelju jezika korisnika kliknite mogućnost <strong>Prijevodi</strong>.                                                                                             |
| <strong>Poruka o suzbijanju korupcije za odobravatelja</strong>  |                                                                                             Unesite tekst koji će se prikazati odobravatelju tijekom izrade novog izvješća o troškovima. Za unos teksta specifičnog za jezik koji će se prikazivati na temelju jezika korisnika kliknite mogućnost <strong>Prijevodi</strong>.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]