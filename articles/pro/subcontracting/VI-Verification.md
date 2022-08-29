---
title: Provjera faktura dobavljača s odobrenim stvarnim podacima
description: U ovom se članku objašnjava kako voditelji projekata Microsoft Dynamics 365 Project Operations let's provjeravaju fakture dobavljača sa stvarnim vrijednostima koje su odobrene kao izvođači radova i zabilježenim vremenom te troškovima i materijalima koje su koristili članovi projektnog tima.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ab9f69e36aa58bfe3a2f8e3455db66b6bceea968
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261737"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Provjera faktura dobavljača s odobrenim stvarnim podacima

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Microsoftovi Dynamics 365 Project Operations voditelji projekata provjeravaju retke fakture dobavljača na sljedeće načine:

- Koristite polje Status **provjere u** recima fakture dobavljača.
- Ako se reci fakture dobavljača odnose na redak kooperacije, povežite stvarne troškove iz aktivnosti kooperanta s recima fakture dobavljača. Veza se kreira podudaranjem iznosa troškova s recima fakture dobavljača.

    > [!NOTE]
    > Iako se status provjere može pratiti za retke fakture dobavljača koji se ne odnose na kooperant, stvarni troškovi ne mogu se povezati s tim recima fakture dobavljača.

## <a name="verification-status"></a>Stanje provjere

Polje **Status** provjere u retku fakture dobavljača pokazuje taj status provjere. Podržani su sljedeći statusi:

1. Nije pokrenuto
2. U tijeku
3. Dovršeno

Reci fakture dobavljača koji imaju status provjere nije pokrenut **može** se uređivati.

Reci fakture dobavljača koji imaju status **provjere U tijeku** više se ne mogu uređivati. Za redak fakture dobavljača koji upućuje na podugovaranje, status provjere automatski se postavlja na **U tijeku** čim se stvarni trošak uskladi s retkom fakture dobavljača.

Reci fakture dobavljača koji imaju status **provjere Dovršeno** više se ne mogu uređivati. Kada svi reci na fakturi dobavljača imaju taj status provjere, faktura dobavljača može se potvrditi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Uskladite stvarne troškove s recima fakture dobavljača

Podudaranje stvarnih troškova pomaže u postupku provjere u retku fakture dobavljača. Da biste usporedili stvarne troškove s retkom fakture dobavljača, slijedite ove korake.

1. Otvorite redak fakture dobavljača i odaberite karticu **Neupareni iznosi** troška. Rešetka prikazuje popis stvarnih troškova koji se odnose na isti redak kooperanta kao i redak fakture dobavljača.
2. Odaberite jednu ili više stvarnih troškova, a zatim na alatnoj traci iznad rešetke odaberite **Podudaranje**. Sustav provjerava mogu li se odabrane stvarne vrijednosti troškova uskladiti. Nakon što je provjera valjanosti proslijeđena, stvarni troškovi povezuju se s retkom fakture dobavljača.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteriji provjere valjanosti koji se koriste za povezivanje stvarnog troška s recima fakture dobavljača

Tijekom postupka podudaranja veza između stvarnog troška i retka fakture dobavljača može se uspostaviti samo ako su ispunjena oba sljedeća uvjeta:

- Polje Status **prilagođavanja** za svaki odabrani iznos troška mora biti prazno. Drugim riječima, stvarni troškovi ne smiju se zamijeniti drugim stvarnim troškovima tijekom postupka opoziva, otkazivanja odobrenja ili postupka temeljnice ispravaka.
- Vrijednosti sljedećih polja podudaraju se između retka fakture dobavljača i stvarnog odabranog troška. Ako nijedno polje nije postavljeno u retku fakture dobavljača, ne smatra se podudarnim.

    - Ugovor o projektu
    - Redak ugovora o projektu
    - Razred transakcije
    - Project
    - Zadatak
    - Kategorija resursa
    - Kategorija transakcije
    - Proizvod
    - Redak kooperacije
    - Resurs koji je moguće rezervirati

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Poništavanje prikaza iznosa troškova iz retka fakture dobavljača

Neprilagođenost stvarnih troškova također može pomoći u postupku provjere na fakturi dobavljača omogućavanjem uklanjanja prethodno uspostavljenih veza. Stvarne vrijednosti troškova mogu se poništiti samo iz redaka fakture dobavljača koji imaju status **provjere u tijeku**. Da biste uklonili stvarne troškove iz retka fakture dobavljača, slijedite ove korake.

1. Otvorite redak fakture dobavljača i odaberite karticu **Uskladi s stvarnim troškovima** . Rešetka prikazuje popis iznosa troškova koji se odnose na redak fakture dobavljača.
2. Odaberite jednu ili više stvarnih troškova, a zatim na alatnoj traci iznad rešetke odaberite **Neusporedivo**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
