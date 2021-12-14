---
title: Aplikacija Trošak za mobilni uređaj
description: U ovoj se temi nalaze informacije o mobilnom radnom prostoru za upravljanje troškovima.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5ab5959fa5c9c5463826a9a792112a93e469de5f
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818174"
---
# <a name="mobile-expense-app"></a>Aplikacija Trošak za mobilni uređaj

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U ovoj se temi nalaze informacije o mobilnom radnom prostoru **Upravljanje troškovima**. Ovaj radni prostor omogućuje korisnicima dohvaćanje i prijenos računa, kako bi ga kasnije mogli priložiti izvješću o troškovima. Korisnici također mogu brzo stvoriti redak troška s pomoću priloženog računa te stvoriti i upravljati svojim izvješćima o troškovima. Osim toga, odobravatelji mogu upotrebljavati mobilni radni prostor **Upravljanje troškovima** za pregled izvješća o troškovima koji su im dodijeljeni i ta izvješća odobriti ili odbiti.

Ovaj mobilni radni prostor namijenjen je uporabi s mobilnom aplikacijom Dynamics 365 Unified Ops.

Mnoge tvrtke ili ustanove traže da se uz izvješće o troškovima povezanim s putovanjem ili poslom, koje zaposlenik podnosi za nadoknadu, priloži kopija računa. Mobilni radni prostor **Upravljanje troškovima** omogućuje korisnicima brzo stvaranje novih redaka troškova na mobilnom uređaju po vlastitu odabiru s pomoću priložene fotografije računa. Alternativno, korisnici mogu snimiti fotografiju računa, a zatim je kasnije priložiti izvješću o troškovima. Zaposlenici također mogu stvoriti i upravljati svojim izvješćima o troškovima, a zatim ih podnijeti na odobrenje i nadoknadu s pomoću svog mobilnog uređaja.

Konkretno, mobilni radni prostor **Upravljanje troškovima** omogućuje korisnicima izvršavanje ovih zadataka:

- Fotografiranje računa. Učitavanje fotografije računa i njeno kasnije prilaganje izvješću o troškovima.
- Prijenos snimljenog računa kao datoteke. Kasnije tu datoteku možete priložiti izvješću o troškovima.
- Stvaranje novog retka troška s pomoću priloženog računa. Kasnije možete dodati stavku retka u izvješće o troškovima i poslati je na odobrenje i nadoknadu.

Ove značajke možete upotrebljavati i za sljedeće:

- Stvaranje novog izvješća o troškovima.
- Prilaganje transakcija kreditnom karticom i ostalih prethodno stvorenih troškova izvješću o troškovima.
- Stvaranje novih troškova za izvješće o troškovima.
- Prilaganje računa za svaki trošak uz izvješće o troškovima, fotografiranjem računa ili prijenosom snimljenog računa u obliku datoteke.
- Ovisno o pravilima koja se odnose na troškove tvrtke, trošku dodajte popis gostiju.
- Ovisno o pravilima koja se odnose na troškove tvrtke, specificirajte troškove.
- Podnošenje izvješća o troškovima na odobrenje i nadoknadu.
- Odobravanje ili odbijanje izvješća o troškovima kojima ste dodijeljeni kao odobritelj.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Preduvjeti ako koristite Dynamics 365 Finance

Ako su Financije postavljene za vašu tvrtku ili ustanovu, administrator sustava mora objaviti mobilni radni prostor **Upravljanje troškovima**. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Preuzimanje i instaliranje mobilne aplikacije Dynamics 365 Unified Ops
Preuzimanje i instaliranje mobilne aplikacije Dynamics 365 Unified Ops:

- [Za Android telefone](https://go.microsoft.com/fwlink/?linkid=850662)
- [Za iPhon uređaje](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prijava u mobilnu aplikaciju
1. Pokrenite aplikaciju na mobilnom uređaju.
2. Unesite URL-adresu svojeg sustava Dynamics 365.
4. Kad se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite vjerodajnice.
5. Nakon što se prijavite, prikazuju se dostupni radni prostori za vašu tvrtku. Morat ćete osvježiti popis mobilnih radnih prostora ako vaš administrator sustava kasnije objavi novi radni prostor.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Snimanje računa s pomoću mobilnog radnog prostora Upravljanje troškovima

1. Na mobilnom uređaju otvorite radni prostor **Upravljanje troškovima**.
2. Odaberite **Snimanje računa**.
3. Odaberite **Fotografiraj** ili **Odaberi sliku**.
4. Slijedite jedan od ovih koraka:

    - Ako ste odabrali **Fotografiraj**, slijedite ove korake:

        1. Preusmjereni ste na kameru svojeg mobilnog uređaja kako biste mogli fotografirati račun. 
        2. Kada završite s fotografiranjem, odaberite **U redu** kako biste prihvatili fotografiju.
        3. Neobvezno: Unesite naziv fotografije i sve bilješke.

    - Ako ste odabrali mogućnost **Odaberi sliku**, slijedite ove korake:

        1. Odaberite sliku s popisa.
        2. Neobvezno: Unesite naziv slike i sve bilješke.

5. Odaberite **Gotovo**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Brzi unos troškova s pomoću mobilnog radnog prostora Upravljanje troškovima

1. Na mobilnom uređaju otvorite radni prostor **Upravljanje troškovima**.
2. Odaberite **Brzi unos troškova**.
3. Odaberite kategoriju troška. Prikazuje se popis kategorija troškova koji su preneseni u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Razvojni inženjeri bi dodatne informacije trebali potražiti u članku [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ako vaša kategorija nije na popisu, odaberite **Pretraži** kako biste pretražili na mreži. Pretražujte po kategoriji troška ili se prebacite na pretraživanje po vrsti troška.
4. Unesite datum transakcije troškova.
5. Neobvezno: Unesite trgovca radi troškova.
6. Unesite iznos troška.
7. Odaberite valutu troška. Prikazuje se popis šifri valuta koje su prenesene u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama prenosi se 400 valuta, ali razvojni inženjer može promijeniti taj broj. Razvojni inženjeri bi dodatne informacije trebali potražiti u članku [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ako vaša valuta nije na popisu, odaberite **Pretraži** kako biste pretražili na mreži. Pretražujte po valuti ili se prebacite na pretraživanje po nazivu.
8. Odaberite **Fotografiraj** ili **Odaberi sliku**.
9. Slijedite jedan od ovih koraka:

    - Ako ste odabrali **Fotografiraj**, preusmjereni ste na kameru svojeg mobilnog uređaja kako biste mogli fotografirati račun. Kada završite s fotografiranjem, odaberite **U redu** kako biste prihvatili fotografiju.
    - Ako ste odabrali **Odaberi sliku**, odaberite sliku s popisa.

10. Odaberite **Gotovo**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Odobravanje izvješća o troškovima pomoću mobilnog radnog prostora za upravljanje troškovima

1. Na mobilnom uređaju otvorite radni prostor **Upravljanje troškovima**.
2. Mogućnost **Odobrenja troškova** prikazuje broj izvješća o troškovima koja su vam dodijeljena na odobrenje. Broj se ažurira otprilike svakih 30 minuta. Odaberite **Odobrenja troškova**.

    Prikazuje se popis izvješća o troškovima koja su vam dodijeljena na odobrenje.

3. Odaberite izvješće o troškovima kako biste vidjeli pojedinosti o troškovima.
4. Odaberite trošak kako biste vidjeli njegove pojedinosti. Podaci koji se prikazuju za trošak obuhvaćaju sve pojedinosti o računu, gostu i specifikaciji.
5. Povratkom na stranicu **Izvješće o troškovima** odaberite odobravate li ili odbacujete izvješće o troškovima.
6. Unesite komentare za radnju odobrenja.
7. Odaberite **Gotovo**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Stvaranje novog izvješća o troškovima i slanje na odobrenje pomoću mobilnog radnog prostora za upravljanje troškovima

1. Na mobilnom uređaju otvorite radni prostor **Upravljanje troškovima**.
2. Odaberite **Unos troškova**.
3. Odaberite **Novo izvješće** ili s popisa odaberite postojeće izvješće o troškovima.
4. Za nova izvješća o troškovima unesite svrhu i sve dostupne dodatne podatke. Ovi se podaci razlikuju, ovisno o načinu na koji je upravljanje troškovima konfigurirano za vašu tvrtku.
5. Odaberite **Gotovo**.
6. Kako biste u izvješće o troškovima dodali postojeće troškove, poput transakcija kreditnom karticom, odaberite **Dodaj privitak**.
7. Na popisu odaberite jedan trošak ili više njih.
8. Odaberite **Gotovo**.
9. Kako biste dodali novi trošak u izvješće o troškovima, odaberite **Novi trošak**.
10. Odaberite kategoriju troška. Prikazuje se popis kategorija troškova koji su preneseni u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Razvojni inženjeri bi dodatne informacije trebali potražiti u članku [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ako vaša kategorija nije na popisu, odaberite **Pretraži** kako biste pretražili na mreži. Pretražujte po kategoriji troška ili se prebacite na pretraživanje po vrsti troška.
11. Neobvezno: Unesite trgovca radi troškova.
12. Unesite datum transakcije troškova.
13. Unesite iznos troška.
14. Odaberite valutu troška. Prikazuje se popis šifri valuta koje su prenesene u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama prenosi se 400 valuta, ali razvojni inženjer može promijeniti taj broj. Razvojni inženjeri bi dodatne informacije trebali potražiti u članku [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ako vaša valuta nije na popisu, odaberite **Pretraži** kako biste pretražili na mreži. Pretražujte po valuti ili se prebacite na pretraživanje po nazivu.
15. Odaberite **Gotovo**.
16. Kako biste trošku dodali više pojedinosti, odaberite **Dodaj više pojedinosti**. Dostupna polja ovise o konfiguraciji upravljanja troškovima za vašu tvrtku.
17. Ako je prema pravilima tvrtke potreban račun o trošku, odaberite **Računi**, a zatim slijedite ove korake:

    1. Odaberite **Dohvati račun** ili **Priloži račun**.
    2. Slijedite jedan od ovih koraka:

        - Ako ste odabrali mogućnost **Dohvati račun**, slijedite ove korake:

            1. Odaberite **Fotografiraj** ili **Odaberi sliku**.
            2. Slijedite jedan od ovih koraka:

                - Ako ste odabrali **Fotografiraj**, slijedite ove korake:

                    1. Preusmjereni ste na kameru svojeg mobilnog uređaja kako biste mogli fotografirati račun. Kada završite s fotografiranjem, odaberite **U redu** kako biste prihvatili fotografiju.
                    2. Neobvezno: Unesite naziv fotografije i sve bilješke.

                - Ako ste odabrali mogućnost **Odaberi sliku**, slijedite ove korake:

                    1. Odaberite sliku s popisa.
                    2. Neobvezno: Unesite naziv slike i sve bilješke.

            3. Odaberite **Gotovo**.

        - Ako ste odabrali mogućnost **Priloži račun**, slijedite ove korake:

            1. Na popisu odaberite jednu sliku ili više njih.
            2. Odaberite **Gotovo**.

    3. Odaberite gumb **Povratak** za povratak na pojedinosti o troškovima.

18. Ako su prema pravilima tvrtke za trošak potrebni gosti, odaberite **Gosti**, a zatim slijedite ove korake:

    1. Odaberite **Gost**, **Prethodni gosti** ili **Suradnici**.
    2. Slijedite jedan od ovih koraka:

        - Ako ste odabrali mogućnost **Gost**, slijedite ove korake:

            1. Unesite naziv gosta.
            2. Neobvezno: Unesite organizaciju i/ili državu gosta.
            3. Neobavezno: Unesite stručni naslov gosta.
            4. Odaberite **Gotovo**.

        - Ako ste odabrali mogućnost **Prethodni gosti**, slijedite ove korake:

            1. Na popisu odaberite jednog prethodnog gosta ili više njih. Prikazuje se popis prethodnih gostiju koje ste dodali u prethodna izvješća o troškovima koja su prenesena u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Razvojni inženjeri bi dodatne informacije trebali potražiti u članku [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ako vaš prethodni gost nije na popisu, odaberite **Pretraži** kako biste pretražili na mreži. Pretražujte po imenu ili se prebacite na pretraživanje po tvrtki ili ustanovi, državi ili stručnom naslovu.
            2. Odaberite **Gotovo**.

        - Ako ste odabrali mogućnost **Suradnici**, slijedite ove korake:

            1. Na popisu odaberite jednog suradnika ili više njih. Prikazuje se popis suradnika koji su preneseni u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Razvojni inženjeri bi dodatne informacije trebali potražiti u članku [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ako vaši suradnici nisu na popisu, odaberite **Pretraži** kako biste pretražili na mreži. Pretražujte po imenu ili se prebacite na pretraživanje po tvrtki ili stručnom naslovu.
            2. Odaberite **Gotovo**.

    3. Odaberite gumb **Povratak** za povratak na pojedinosti o troškovima.

19. Ako je prema pravilima tvrtke potrebna specifikacija troška, odaberite **Specificiraj**, a zatim slijedite ove korake:

    1. Odaberite prvi datum za specifikaciju.
    2. Odaberite **Dodaj specifikaciju**.
    3. Odaberite potkategoriju specifikacije troška. Prikazuje se popis potkategorija troškova koji su preneseni u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Razvojni inženjeri bi dodatne informacije trebali potražiti u članku [Mobilna platforma](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Ako vaša potkategorija nije na popisu, odaberite **Pretraži** kako biste pretražili na mreži. Pretražite po nazivu potkategorije troška.
    4. Unesite iznos transakcije za specifikaciju.
    5. Uredite datum transakcije, ako je to potrebno.
    6. Odaberite **Gotovo**.
    7. Ponavljajte prethodne korake dok ne završite s dodavanjem svih specifikacija za odabrani datum.
    8. Za dodatne dane možete odabrati **Kopiraj na sljedeći dan** za kopiranje specifikacija na sljedeći dan. Alternativno, možete odabrati datum za izradu specifikacije, a zatim dodati specifikaciju kao što ste to učinili za prvi datum.
    9. Nakon što završite sa specifikacijom troškova, odaberite gumb **Povratak** za povratak na pojedinosti o troškovima.

20. Odaberite gumb **Natrag** za povratak na stranicu **Izvješće o troškovima**.
21. Ponavljajte prethodne korake dok ne završite s dodavanjem svih troškova.
22. Odaberite **Šalji**.
23. Unesite komentare za odobravatelja.
24. Odaberite **Gotovo**.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Zašto mobilna aplikacija Trošak ne ulazi u način plaćanja prema zadanim postavkama?

Organizacije mogu prilagoditi **zadanu postavku načina plaćanja** za svaku kategoriju troška prilikom stvaranja. Uz to, kada postavljate načine plaćanja, polje Zadani način plaćanja možete **postaviti** samo na **Uvoz**.

Kada **je samo uvoz omogućen za način** plaćanja, način plaćanja ne unosi se prema zadanim postavkama. Bit će prazan u kategorijama troškova u kojima je postavljen ovaj način plaćanja. Takvo je ponašanje dosljedno i u web iskustvu i u mobilnom iskustvu.
    
Ako **samo uvoz nije omogućen za način** plaćanja, zadana vrijednost unosi se prema zadanim postavkama za kategorije troškova u kojima je postavljen ovaj način plaćanja. Međutim, postoji poznati problem u kojem zadana vrijednost nije unesena u mobilnu aplikaciju Trošak. Da biste zaobišli taj problem, prije spremanja izvješća o troškovima ručno odaberite način plaćanja. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Zašto ne mogu dodati ili urediti financijske dimenzije u mobilnoj aplikaciji Trošak?

Unos dimenzija i distribucija nije podržan. Da biste zaobišli to ograničenje, ta polja možete postaviti prema zadanim postavkama u mobilnoj aplikaciji postavljanjem zadanih financijskih dimenzija po projektu ili zaposleniku.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Zašto se u mobilnoj aplikaciji Trošak ponekad pojavljuje pogreška pri sinkronizaciji?

Ako reci troškova ne zadovoljavaju zahtjeve pravila, a korisnik pošalje izvješće o troškovima bez adresiranja upozorenja o pravilima, mobilni podaci se ne sinkroniziraju s poslužiteljem i dolazi do pogreške pri sinkronizaciji. Sva izvješća o troškovima koja se šalju nakon neuspjeha sinkronizacije ostat će u neuspjelom stanju i uzrokovati više neuspjeha sinkronizacije. Jedini način da popravite ovu situaciju je ručno brisanje obavijesti o sinkronizaciji. Taj je problem riješen zaustavljanjem slanja izvješća o troškovima kada upozorenja o pravilima nisu riješena, tako da se izbjegnu pogreške pri sinkronizaciji.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Zašto se provjera valjanosti projekta i kategorije ne odražava ispravno u mobilnoj aplikaciji Trošak?

Ova provjera valjanosti trenutno nije podržana. Međutim, potpora bi mogla biti dodana u budućnosti. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Koje su vrste dokumenata podržane u mobilnoj aplikaciji Trošak?

Mobilna aplikacija Trošak podržava samo slike. Trenutno ne podržava PDF-ove ili druge dokumente.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
