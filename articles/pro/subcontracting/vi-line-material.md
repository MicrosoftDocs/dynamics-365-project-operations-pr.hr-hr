---
title: Redci za proizvode u fakturi dobavljača
description: U ovom se članku objašnjava kako zabilježiti retke fakture dobavljača za proizvode i koristiti različita polja za bilježenje nabave proizvoda od dobavljača.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931367"
---
# <a name="vendor-invoice-lines-for-products"></a>Redci za proizvode u fakturi dobavljača

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Faktura dobavljača u Microsoftu Dynamics 365 Project Operations može imati retke fakture dobavljača za proizvode (koji se nazivaju i materijalima). Voditelji projekata mogu koristiti retke fakture dobavljača za proizvode da bi zabilježili troškove proizvoda kupljenih na projektima.

Reci fakture dobavljača za proizvode mogu se, ali i ne moraju odnositi na redak kooperanta za materijale. Ako se redak fakture dobavljača za proizvode poziva na podugovaranje, voditelji projekata moći će uskladiti i provjeriti proizvode koje fakturira redak fakture dobavljača u odnosu na upotrebu kupljenih proizvoda koje bilježe i odobravaju voditelji projekata.

Sljedeća tablica sadrži informacije o poljima u recima fakture dobavljača za proizvode.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj će naziv biti prikazan kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis proizvoda koje dobavljač fakturira u retku fakture dobavljača. | Nijedno |
| Podugovor | Podugovor na kojem su proizvodi izvorno naručeni. | Kada je za fakturu dobavljača odabran kooperant, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može imati retke fakture dobavljača koji se odnose na različite kooperante. |
| Redak kooperacije | Linija podugovaranja na kojoj su proizvodi naručeni. Popis redaka kooperanta koji se mogu odabrati ograničen je na retke na odabranom kooperantu. | Kada je redak kooperanta odabran u retku fakture dobavljača za proizvode, zadane vrijednosti za **polja Projekt**, **Zadatak** i **Proizvod** unose se iz odgovarajućih polja u retku kooperanta. Ako odabrani redak kooperanta ima vrijednosti u poljima Projekt **,** Zadatak **i** Proizvod **, vrijednosti odgovarajućih polja u** retku fakture dobavljača ne mogu se razlikovati od tih vrijednosti. |
| Datum transakcije | Datum kada će se na projektu zabilježiti stvarni trošak retka fakture dobavljača. | Nijedno|
| Razred transakcije | Kada se proizvodi fakturiraju, ovo bi polje trebalo postaviti na **Materijal**. | Vrijednost **Materijal** pokazuje da se redak fakture dobavljača koristi za bilježenje iznosa fakture za kupljene materijale. |
| Project | Naziv projekta na kojem su korišteni proizvodi koji se fakturiraju. | Ovo je polje obavezno i ne može se ostaviti praznim. |
| Zadatak | Naziv projektnog zadatka na kojem su korišteni proizvodi koji se fakturiraju. Ovo je polje dostupno samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako ovo polje ostane prazno, voditelj projekta može uskladiti redak fakture dobavljača s kupljenim proizvodom koji se koristi za bilo koji zadatak projekta. Ako se redak fakture dobavljača ne odnosi na redak kooperanta, a to polje ostaje prazno, stvarni trošak kreiran retkom fakture dobavljača neće biti povezan ni s jednom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se neće moći fakturirati krajnjem kupcu. |
| Odaberi proizvod | Odaberite je li proizvod koji se fakturira postojeći proizvod iz kataloga ili dopisani proizvod. | Zadana vrijednost unosi se iz retka kooperanta kada je odabran redak kooperanta. |
| Proizvod | Odaberite proizvod iz kataloga. Ako je proizvod dopisani proizvod, unesite naziv proizvoda. | Ovo se polje koristi za unos zadanih nabavnih cijena za postojeće proizvode. |
| Količina | Unesite količinu materijala koju dobavljač fakturira u ovom retku fakture. | Nijedno |
| Grupa jedinica | Odaberite grupu jedinica u kojoj je izražena količina koja se fakturira. | Nijedno |
| Jedinica | Zadana vrijednost je osnovna jedinica odabrane grupe jedinica. Tu vrijednost možete promijeniti tako da plati u bilo kojoj jedinici odabrane grupe jedinica. | Kombinacija vrijednosti Proizvoda i Jedinice koristit će se kao zadana **ili izračunata vrijednost za** polje Jedinična cijena **u retku fakture dobavljača.** **·** |
| Jedinična cijena | Zadana jedinična **cijena koristi kombinaciju vrijednosti Proizvoda** i **Jedinice** iz cjenika projekta koja se primjenjuje na datum transakcije retka fakture dobavljača. | Nijedno |
| Podzbroj | Ovo polje samo za čitanje izračunava se kao *Jedinična cijena* količine&times;*ako* su vrijednosti unesene **i u polje Količina** i u polje Jedinična **cijena.** Ako su jedno ili oba polja prazna, u ovo polje možete unijeti vrijednost. | Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupan iznos | Ukupan iznos retka fakture dobavljača, uključujući poreze. Ovo se polje izračunava kao *porez na promet podzbroja* + *·*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
