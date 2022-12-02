---
title: Provjera faktura dobavljača s odobrenim stvarnim podacima
description: Ovaj članak objašnjava kako Microsoft Dynamics 365 Project Operations omogućuje voditeljima projekata da provjere fakture dobavljača sa stvarnim podacima koji su odobreni jer su izvođači obavili radove i zabilježili vrijeme te troškove i materijale koje su koristili članovi projektnog tima.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522934"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Provjera faktura dobavljača s odobrenim stvarnim podacima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Microsoft Dynamics 365 Project Operations omogućuje voditeljima projekata da provjere retke fakture dobavljača na sljedeće načine:

- Koristite polje **Status provjere** u recima fakture dobavljača.
- Ako reci fakture dobavljača upućuju na redak podugovora, povežite stvarne troškove iz aktivnosti podugovarača s tim recima fakture dobavljača. Veza se stvara uspoređivanjem stvarnih troškova s recima fakture dobavljača.

    > [!NOTE]
    > Iako se status provjere može pratiti za retke fakture dobavljača koji ne upućuju na podugovor, stvarni troškovi ne mogu se povezati s tim recima fakture dobavljača.

## <a name="verification-status"></a>Stanje provjere

Polje **Status provjere** u retku fakture dobavljača označava taj status provjere. Podržani su sljedeći statusi:

1. Nije pokrenuto
2. U tijeku
3. Dovršeno

Reci fakture dobavljača koji imaju status provjere **Nije započeto** mogu se urediti.

Reci fakture dobavljača koji imaju status provjere **U tijeku** više se ne mogu urediti. Za redak fakture dobavljača koji upućuje na podugovor, status provjere automatski se postavlja na **U tijeku** čim se prvi stvarni trošak uskladi s retkom fakture dobavljača.

Reci fakture dobavljača koji imaju status provjere **Završeno** više se ne mogu urediti. Kada svi reci na fakturi dobavljača imaju taj status provjere, faktura dobavljača može se potvrditi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Uskladi stvarne troškove s recima fakture dobavljača

Usklađivanje stvarnih troškova pomaže u postupku provjere u retku fakture dobavljača. Za usklađivanje stvarnih troškova s retkom fakture dobavljača slijedite ove korake.

1. Otvorite redak fakture dobavljača i odaberite karticu **Neusklađeni stvarni troškovi**. Rešetka prikazuje popis stvarnih troškova koji upućuju na isti redak podugovora kao redak fakture dobavljača.
2. Odaberite jedan ili više stvarnih troškova, a zatim odaberite **Uskladi** na alatnoj traci iznad rešetke. Sustav potvrđuje da se odabrani stvarni troškovi mogu uskladiti. Nakon što prođe provjera valjanosti, stvarni troškovi povezuju se s retkom fakture dobavljača.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteriji provjere valjanosti koji se koriste za povezivanje stvarnih troškova s recima fakture dobavljača

Tijekom postupka usklađivanja veza između stvarnog troška i retka fakture dobavljača može se uspostaviti samo ako su ispunjena oba sljedeća uvjeta:

- Polje **Status prilagodbe** za svaki odabrani stvarni trošak mora biti prazno. Drugim riječima, stvarni troškovi ne smiju biti zamijenjeni drugim stvarnim troškovima tijekom postupka opoziva, otkazivanja odobrenja ili dnevnika ispravaka.
- Vrijednosti sljedećih polja usklađuju se između retka fakture dobavljača i odabranog stvarnog troška. Ako neko polje nije postavljeno u retku fakture dobavljača, ne uzima se u obzir za usklađivanje.

    - Ugovor o projektu
    - Redak ugovora o projektu
    - Razred transakcije
    - Project
    - Zadatak
    - Kategorija resursa
    - Kategorija transakcije
    - Proizvod
    - Redak podugovora
    - Resurs koji je moguće rezervirati

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Stvarni troškovi neusklađeni s retkom fakture dobavljača

Neusklađivanje stvarnih troškova također može pomoći u procesu provjere na fakturi dobavljača omogućavanjem uklanjanja prethodno uspostavljenih veza. Usklađivanje stvarnih troškova može se poništiti samo u recima fakture dobavljača koji imaju status provjere **U tijeku**. Za poništenje usklađivanja stvarnih troškova u retku fakture dobavljača slijedite ove korake.

1. Otvorite redak fakture dobavljača i odaberite karticu **Usklađeni stvarni troškovi**. Rešetka prikazuje popis stvarnih troškova koji upućuju na redak fakture dobavljača.
2. Odaberite jedan ili više stvarnih troškova, a zatim odaberite **Poništi usklađivanje** na alatnoj traci iznad rešetke.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
