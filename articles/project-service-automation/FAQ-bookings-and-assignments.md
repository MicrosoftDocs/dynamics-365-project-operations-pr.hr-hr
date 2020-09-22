---
title: Rezervacije resursa i kako su povezane s dodjelama zadataka
description: Ova tema pruža informacije o upravljanju imenovanim resursima, rezervacijama resursa i dodjelama zadataka te načinu na koji su međusobno povezani.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 700eb78a-31ff-4e3b-8c38-3944c74f3413
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74369753fba4b5d29e5b49f5b6a6593f902d1133
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750067"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Rezervacije resursa i kako su povezane s dodjelama zadataka


Postoje dva načina na koji se imenovani resursi mogu rezervirati za projektni tim i mogu im biti dodijeljeni projektni zadaci:

- Resurs se može izravno rezervirati za projekt, a zatim dodijeliti projektnim zadacima.
- Zadaci se mogu dodijeliti generičkom resursu koji se zatim koristi za pronalaženje i zamjenu generičkog imenovanim resursom. 

U oba slučaja čin rezerviranja resursa rezervira kapacitet resursa.

Voditelj projekta koji planira projekt posjeduje projektni plan i raspored. Koristeći generički resurs za zadatak, a zatim generirajući zahtjev resursa iz njega, voditelj projekta može rezervirati resurse za projekt s konturama navedenim u projektnom planu. On može rezervirati resurse za projekt, a zatim ih dodijeliti zadacima, ali nema načina da uskladi konture rezervacije s konturama zadataka. Rezervacije ne utječu na raspored projekta.

Zamislite složeni projekat s više preklapajućih zadataka za koji više resursa iste vrste mora raditi istovremeno. Ako je resursu data kontura koja je različita od konture agregata njihovih dodjela, tada je teško izmijeniti zadatke da bi se uklopili u konturu rezervacija za njihove pojedinačne zadatke i izvorne konture.

U primjeru ispod ukupni rad istog resursa iz skupa četiri zadatka je 62 sata tijekom razdoblja od dva tjedna i postoji određena kontura. Ako je resurs Bob rezerviran na 62 sati tijekom ista dva tjedna, ali s različitom konturom, preduvjet i rezervacije su usklađeni.

| **Konture zadatka**    | **Ukupan broj sati** | Pon 4.6. | Uto 5.6. | Sri 6.6. | Čet 7.6. | Pet 8.6. | Sub 9.6. | Nedj 10.6. | Pon 11.6. | Uto 12.6. | Sri 13.6. | Čet 14.6. | Pet 15.6. |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Zadatak 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Zadatak 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Zadatak 3               | 1,0              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Zadatak 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Zbrojevi**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bobova dostupnost
| **Rezervacija   resursa** | **Ukupan broj sati** | Pon 4.6. | Uto 5.6. | Sri 6.6. | Čet 7.6. | Pet 8.6. | Sub 9.6. | Nedj 10.6. | Pon 11.6. | Uto 12.6. | Sri 13.6. | Čet 14.6. | Pet 15.6. |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Međutim, ne postoji sustavan način dodijeljivanja konture rezerviranih sati zadacima po dnevnoj osnovi. Ako je voditelj projekta spreman izmijeniti projektni raspored da bi ispuio dostupnost resursa, morat će ukloniti dodjelu i revidirati sve zadatke da bi bili u skladu s konturama rezervacije.

U slučaju kada organizacija dodijeli zadatak projektnog planiranja i voditelju projekta i upravitelju resursa, voditelj projekta treba postaviti raspored, što uključuje konturiranje potrebnog rada. Upravitelj resursa ne bi smio moći utjecati na raspored bez znanja voditelja projekta, odnosno mijenjati konture rada rezervacijom pravih resursa. Ako upravitelj resursa ispunjava nešto što voditelj projekta nije zatražio, oni se trebaju dogovoriti u vezi potrebnih promjena u projektnom rasporedu.

Budući da rezervacije i dodjele nisu usko povezane, moguće je rezervirati konture koje su različite od kontura zadatka ili izmijeniti zadatke što rezultira situacijom u kojoj rezervacije i zadaci nisu usklađeni.

**Prikaz usklađivanja** omogućuje voditelju projekta pregled rezervacija i zadataka za svakog člana projektnog tima. Ovaj prikaz koristi boje i sjene za prikaz neusklađenosti između rezervacija i dodjela člana tima. Na temelju ove informacije voditelj projekta može poduzeti odgovarajuće korake da produži rezervacije resursa u slučajevima kada postoje dodjele a ne postoje rezervacije ili da otkaže rezervacije kada su resursi rezervirani ali ne postoje dodjele.

> [!NOTE]
> Ako premjestite zadatak koji ste sami konturirali, te konture neće ostati. Konture se regeneriraju prema projektnom kalendaru i prilagođavaju se promjenama u radnim satima i odmorima. Ovako je prema zadanim postavkama jer sustav ne može znati namjeru izvorne konture i ne može odrediti ima li smisla zadržati određenu konturu za novo vremensko razdoblje. Budući da rezervacije i zadaci nisu povezani, rezervacije zadržavaju izvorne rezervacijske konture. U tom slučaju morat ćete otkazati i ponovno rezervirati novu konturu dodjele.

