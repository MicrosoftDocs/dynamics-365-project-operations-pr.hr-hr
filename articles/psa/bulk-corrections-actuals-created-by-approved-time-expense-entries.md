---
title: Skupne korekcije stvarnih podataka stvorene odobrenim unosima vremena i rashoda
description: U ovoj temi objašnjava se kako administrator može izvršiti pojedinačne ili skupne ispravke prethodno odobrenih unosa vremena i rashoda ako naplata nije dovršena.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073564"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Skupne korekcije stvarnih podataka stvorene odobrenim unosima vremena i rashoda

Povremeno se mogu pogrešno unijeti unosi vremena ili troškova. Na primjer, tijekom stvaranja vremenskog unosa savjetnik može odabrati pogrešan datum ili tijekom unosa troškova zamijeniti redoslijed brojeva. Ako savjetnik ne može izvršiti ažuriranja poslanih unosa, administrator može izravno ispraviti unos za projekt.

Kako biste dovršili postupke u ovoj temi, trebat će vam dopuštenja administratora.

## <a name="correct-approved-time-entries"></a>Ispravljanje odobrenih vremenskih unosa     

Izvršite sljedeće korake kako biste ispravili pojedinačne ili višestruke vremenske unose za projekt.

1. U području mogućnosti **Prodaja** , odaberite stavku **Transakcije** , a zatim odaberite mogućnost **Odobreno vrijeme** , 

2. U popisu **Odobreno vrijeme** pronađite i odaberite jedan ili više odobrenih vremenskih unosa koje želite ispraviti. Možete upotrijebiti filtar za pronalaženje povezanih unosa. Na primjer, možete filtrirati po ID-u projekta i odabrati sve odobrene vremenske unose s tim ID-om projekta.

3. Odaberite mogućnost **Ispravi unose**. Automatski se stvara novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak vremena**. Unosi koje ste odabrali dodaju se u dnevnik. 

4. Na stranicu **Novi dnevnik** unesite **Opis** za svoj dnevnik ispravaka, a zatim odaberite karticu **Ispravci vremenskih unosa**.  
5. U odjeljku **Nove vrijednosti za vremenske unose** , po potrebi, polja ažurirajte ispravnim podacima. Na primjer, možete promijeniti dodijeljeni projekt ili resurs koji se može rezervirati.

6. Odaberite mogućnost **Pretpregled**. U dijaloškom okviru odaberite mogućnost **U redu**. Na kartici **Redci dnevnika** možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim vremenskim unosima koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni. Ako je potrebno izvršiti dodatne ispravke, ponovite korake 5 i 6. 

> [!NOTE]
> Svi ispravljeni stvarni podaci imat će iste vrijednosti koje ste odabrali u odjeljku **Nove vrijednosti za vremenske unose**.

7. Ako se ispravci prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**. U dijaloškom okviru odaberite mogućnost **U redu**.

8. Vratite se na područje **Prodaja** , odaberite stavku **Projekti** i otvorite projekt za koji ste upravo ažurirali vremenske unose. 

9. Na stranici **Projekti** , kartici **Stvarni podaci** , pogledajte promjene koje ste napravili. 

> [!NOTE]
> Ako kartica **Stvarni podaci** nije vidljiva, odaberite mogućnost **Povezani** > **Stvarni podaci**.  

10. Na popisu **Stvarni pridruženi prikaz** možete vidjeti da se izvorni vremenski unosi koji su poništeni i dalje navode, kao i odgovarajući ispravljeni vremenski unosi. 

Na primjer, na sljedećoj slici postoje dvije stavke retka s količinom od 8,00 koje imaju zaduženja navedena u stupcu Iznos. Uz to, postoje dvije stavke retka s količinom od -8,00, koje prikazuju kreditirane iznose u stupcu Iznos. Ovim se korekcijama količina svodi na nulu.

![Popis pridruženog prikaza stvarnih podataka](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Ispravljanje odobrenih unosa troškova

Izvršite sljedeće korake za ispravljanje jednog ili više unosa troškova. 

1. U lijevom navigacijskom oknu područja **Prodaja** , ispod stavke **Transakcije** , odaberite mogućnost **Odobreni troškovi**.

2. Na popisu **Odobreni troškovi** odaberite projekt koji želite ispraviti i zatim odaberite mogućnost **Ispravni unosi**. Automatski će se stvoriti novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak troška**. 

3. Na stranici **Novi dnevnik** unesite **Opis** za ispravak, a na kartici **Ispravljanje troškova** , u odjeljku **Nove vrijednosti za rashode** , odaberite polja podataka koja želite ispraviti za odabrane retke troškova. Na primjer, trošak možete dodijeliti drugom **Projektu** ili ispraviti stavke **Kategorija troškova** , **Datum troška** ili **Resurs koji se može rezervirati**.

4. Odaberite mogućnost **Pretpregled**. U dijaloškom okviru odaberite mogućnost **U redu**. 

5. Na kartici **Redci dnevnika** provjerite ispravke. Možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim unosima troškova koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni.

6. Ako se ispravljene vrijednosti prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**. U dijaloškom okviru odaberite mogućnost **U redu**. Ako se vrijednosti ne prikazuju onako kako ste očekivali, odaberite mogućnost **Otkaži** kako biste se vratili na popis **Odobreni troškovi**. Ponovite korake 2 do 5. 

> [!NOTE]
> Ispravljeni stvarni podaci imat će iste vrijednosti koje ste odabrali u odjeljku **Nove vrijednosti za troškove**.

7. Nakon što potvrdite dnevnik ispravaka, vratite se na projekt ili projekte koje ste ažurirali kako biste pogledali promjene.  

8. Na stranici projekta, na kartici **Stvarni podaci** , pregledajte mogućnost **Stvarni pridruženi prikaz**. Navedeni su izvorni i ispravljeni unosi. Sljedeća slika prikazuje unose izvornih iznosa troškova i odgovarajuće ispravljene iznose unosa troškova. 

![Stvarni podaci o troškovima](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
