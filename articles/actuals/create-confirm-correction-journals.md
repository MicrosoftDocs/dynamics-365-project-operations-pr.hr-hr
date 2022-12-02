---
title: Stvaranje i potvrda dnevnika ispravaka
description: U ovom se članku navode informacije o načinu izrade i potvrde dnevnika ispravaka.
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
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928055"
---
# <a name="create-and-confirm-correction-journals"></a>Stvaranje i potvrda dnevnika ispravaka

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Povremeno se mogu pogrešno unijeti unosi vremena ili troškova. Na primjer, tijekom izrade unosa vremena savjetnik može odabrati pogrešan datum ili pak odabrati pogrešan projekt tijekom unosa određenog troška. Ako savjetnik ne može ažurirati poslane unose, pozadinski administrator može izravno ispraviti stvarni podatak za projekt.

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

7. Nakon što potvrdite dnevnik ispravaka, vratite se na projekt ili projekte koje ste ažurirali da biste vidjeli izmjene.

8. Na stranici projekta, na kartici **Stvarni podaci**, pregledajte popis **Pridruženi prikaz stvarnih podataka**. Navedeni su izvorni i ispravljeni unosi.


## <a name="correct-approved-material-usage-logs"></a>Ispravite odobrene dnevnike upotrebe materijala

Izvršite sljedeće korake za ispravljanje jednog ili više unosa upotrebe materijala.

1. U lijevom navigacijskom oknu područja **Prodaja**, ispod stavke **Transakcije**, odaberite mogućnost **Stvarni podaci**.

2. Na popisu **Stvarni podaci** upotrijebite filtre stupaca za odabir klase transakcije **Materijal** kako bi se prikazivale samo stvarne vrijednosti za materijale. Ostale filtre stupaca možete upotrijebiti da biste dodatno ograničili koji se stvarni podaci prikazuju. Nakon što možete pronaći željeni skup stvarnih podataka, odaberite ih i zatim odaberite **Ispravi unose**. Automatski se izrađuje novi dnevnik ispravljanja te se dodjeljuje vrsta **Ispravak materijala**.

3. Na stranici **Novi dnevnik** unesite opis ispravka u polje **Opis**. Potom na kartici **Ispravak materijala** u odjeljku **Nove vrijednosti za materijale** odaberite polja podatka koja će se ispraviti za odabrane retke materijala. Na primjer, možete dodijeliti materijal drugom projektu ili ispraviti proizvod, datum materijala ili podugovor.

4. Odaberite mogućnost **Pretpregled**. Potom, u dijaloškom okviru odaberite **U redu**.

5. Na kartici **Redci dnevnika** potvrdite ispravke. Možete pregledati popis izvornih stvarnih podataka povezanih s odabranim unosima materijala koji su stornirani i odgovarajuće ispravljene retke koji su izrađeni.

6. Ako se ispravljene vrijednosti prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**. Potom, u dijaloškom okviru odaberite **U redu**. Ako vrijednosti nisu one koje ste očekivali, odaberite **Otkaži** da biste se vratili na popis **Stvarni podaci**. Potom ponovite korake od 2 do 5.

7. Nakon što potvrdite dnevnik ispravaka, vratite se na projekt ili projekte koje ste ažurirali da biste vidjeli izmjene.

8. Na stranici projekta, na kartici **Stvarni podaci**, pregledajte popis **Pridruženi prikaz stvarnih podataka**. Navedeni su izvorni i ispravljeni unosi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
