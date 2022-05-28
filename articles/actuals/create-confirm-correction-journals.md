---
title: Stvaranje i potvrda dnevnika ispravaka
description: U ovoj se temi nalaze informacije o načinu izrade i potvrde dnevnika ispravaka.
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
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582794"
---
# <a name="create-and-confirm-correction-journals"></a>Stvaranje i potvrda dnevnika ispravaka

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Povremeno se unos vremena ili troškova može pogrešno unijeti. Na primjer, konzultant može odabrati pogrešan datum kada kreira stavku vremena ili može odabrati pogrešan projekt prilikom unosa troška. Ako konzultant ne može ažurirati poslane unose, pozadinski administrator može izravno ispraviti stvarne podatke za projekt.

## <a name="correct-approved-time-entries"></a>Ispravljanje odobrenih vremenskih unosa     

Izvršite sljedeće korake kako biste ispravili pojedinačne ili višestruke vremenske unose za projekt.

1. U području mogućnosti **Prodaja**, odaberite stavku **Transakcije**, a zatim odaberite mogućnost **Odobreno vrijeme**, 

2. U popisu **Odobreno vrijeme** pronađite i odaberite jedan ili više odobrenih vremenskih unosa koje želite ispraviti. Možete upotrijebiti filtar za pronalaženje povezanih unosa. Na primjer, možete filtrirati po ID-u projekta i odabrati sve odobrene vremenske unose s tim ID-om projekta.

3. Odaberite mogućnost **Ispravi unose**. Automatski se stvara novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak vremena**. Unosi koje ste odabrali dodaju se u dnevnik. 

4. Na stranicu **Novi dnevnik** unesite **Opis** za svoj dnevnik ispravaka, a zatim odaberite karticu **Ispravci vremenskih unosa**.  

5. U odjeljku **Nove vrijednosti za vremenske unose**, po potrebi, polja ažurirajte ispravnim podacima. Na primjer, možete promijeniti dodijeljeni projekt ili resurs koji se može rezervirati.

6. Odaberite mogućnost **Pretpregled**. U dijaloškom okviru odaberite mogućnost **U redu**. Na kartici **Redci dnevnika** možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim vremenskim unosima koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni. Ako je potrebno izvršiti dodatne ispravke, ponovite korake 5 i 6. 

    > [!NOTE]
    > Svi ispravljeni stvarni podaci imat će iste vrijednosti koje ste odabrali u odjeljku **Nove vrijednosti za vremenske unose**.

7. Ako se ispravci prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**. U dijaloškom okviru odaberite mogućnost **U redu**.

8. Vratite se na područje **Prodaja**, odaberite stavku **Projekti** i otvorite projekt za koji ste upravo ažurirali vremenske unose. 

9. Na stranici **Projekti**, kartici **Stvarni podaci**, pogledajte promjene koje ste napravili. 

    > [!NOTE]
    > Ako kartica **Stvarni podaci** nije vidljiva, odaberite mogućnost **Povezani** > **Stvarni podaci**.  

10. Na popisu **Stvarni pridruženi prikaz** možete vidjeti da se izvorni vremenski unosi koji su poništeni i dalje navode, kao i odgovarajući ispravljeni vremenski unosi. 

 
## <a name="correct-approved-expense-entries"></a>Ispravljanje odobrenih unosa troškova

Izvršite sljedeće korake za ispravljanje jednog ili više unosa troškova. 

1. U lijevom navigacijskom oknu područja **Prodaja**, ispod stavke **Transakcije**, odaberite mogućnost **Odobreni troškovi**.

2. Na popisu **Odobreni troškovi** odaberite projekt koji želite ispraviti i zatim odaberite mogućnost **Ispravni unosi**. Automatski će se stvoriti novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak troška**. 

3. Na stranici **Novi dnevnik** unesite **Opis** za ispravak, a na kartici **Ispravljanje troškova**, u odjeljku **Nove vrijednosti za rashode**, odaberite polja podataka koja želite ispraviti za odabrane retke troškova. Na primjer, trošak možete dodijeliti drugom **Projektu** ili ispraviti stavke **Kategorija troškova**, **Datum troška** ili **Resurs koji se može rezervirati**.

4. Odaberite mogućnost **Pretpregled**. U dijaloškom okviru odaberite mogućnost **U redu**. 

5. Na kartici **Redci dnevnika** provjerite ispravke. Možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim unosima troškova koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni.

6. Ako se ispravljene vrijednosti prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**. U dijaloškom okviru odaberite mogućnost **U redu**. Ako se vrijednosti ne prikazuju onako kako ste očekivali, odaberite mogućnost **Otkaži** kako biste se vratili na popis **Odobreni troškovi**. Ponovite korake 2 do 5. 

7. Nakon što potvrdite temeljnicu ispravaka, vratite se projektu ili projektima koje ste ažurirali da biste vidjeli promjene.

8. Na stranici projekta na **kartici Stvarne** vrijednosti pregledajte **popis Stvarni pridruženi prikaz**. Navedeni su izvorni i ispravljeni unosi.


## <a name="correct-approved-material-usage-logs"></a>Ispravljanje odobrenih zapisnika korištenja materijala

Da biste ispravili jednu ili više stavki evidencije korištenja materijala, dovršite sljedeće korake.

1. **U području Prodaja** u lijevom navigacijskom oknu u odjeljku **Transakcije** odaberite **Stvarne**.

2. **Na popisu Stvarne** vrijednosti pomoću filtara stupaca odaberite klasu **transakcija materijalom**, tako da se prikazuju samo stvarne vrijednosti za materijale. Koristite druge filtre stupaca da biste dodatno ograničili prikazane stvarne vrijednosti. Kada pronađete željeni skup stvarnih vrijednosti, odaberite stvarne, a zatim odaberite **Ispravne stavke**. Automatski se kreira nova temeljnica ispravaka i **dodjeljuje se vrsta ispravka** materijala.

3. **Na stranici Nova temeljnica** **u polje Opis** unesite opis ispravka. Zatim na **kartici Ispravak** materijala u **odjeljku Nove vrijednosti za materijale** odaberite podatkovna polja koja želite ispraviti za odabrane retke materijala. Na primjer, materijal možete dodijeliti drugom projektu ili ispraviti proizvod, datum materijala ili podugovor.

4. Odaberite mogućnost **Pretpregled**. Zatim u dijaloškom okviru odaberite **U redu**.

5. Na kartici **Reci** temeljnice provjerite ispravke. Možete pregledati popis izvornih stvarnih vrijednosti povezanih s odabranim stavkama materijala koje su stornirane i kreiranim ispravljenim odgovarajućim recima.

6. Ako se ispravljene vrijednosti prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**. Zatim u dijaloškom okviru odaberite **U redu**. Ako vrijednosti nisu okrenute prema očekivanjima, odaberite **Odustani** da biste se vratili na **popis Stvarne** vrijednosti. Zatim ponovite korake od 2 do 5.

7. Nakon što potvrdite temeljnicu ispravaka, vratite se projektu ili projektima koje ste ažurirali da biste vidjeli promjene.

8. Na stranici projekta na **kartici Stvarne** vrijednosti pregledajte **popis Stvarni pridruženi prikaz**. Navedeni su izvorni i ispravljeni unosi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
