---
title: Redci za proizvode u fakturi dobavljača
description: U ovom članku objašnjava se način bilježenja redaka fakture dobavljača za proizvode i uporabe različitih polja za bilježenje kupnje proizvoda od dobavljača.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261549"
---
# <a name="vendor-invoice-lines-for-products"></a>Redci za proizvode u fakturi dobavljača

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Faktura dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations može imati retke fakture dobavljača za proizvode (koji se također nazivaju materijalima). Voditelji projekata mogu koristiti retke fakture dobavljača za proizvode kako bi zabilježili troškove proizvoda koji su nabavljeni u projektima.

Reci fakture dobavljača za proizvode mogu, ali ne moraju upućivati na redak podugovora za materijale. Ako redak fakture dobavljača za proizvode upućuje na podugovor, voditelji projekata moći će usporediti i provjeriti proizvode koje fakturira redak fakture dobavljača s upotrebom kupljenih proizvoda koje su zabilježili i odobrili voditelji projekata.

Tablica u nastavku pruža informacije o poljima u recima fakture dobavljača za proizvode.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj naziv prikazivat će se kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis proizvoda koje dobavljač fakturira u retku fakture dobavljača. | Nijedno |
| Podugovor | Podugovor na temelju kojeg su proizvodi izvorno naručeni. | Kada se za fakturu dobavljača odabere podugovor, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može sadržavati retke fakture dobavljača koji upućuju na različite podugovore. |
| Redak podugovora | Redak podugovora na temelju kojeg su proizvodi naručeni. Popis redaka podugovora koje je moguće odabrati ograničen je na retke na odabranom podugovoru. | Kada je redak podugovora odabran u retku fakture dobavljača za proizvode, zadane vrijednosti za polja **Projekt**, **Zadatak** i **Proizvod** unose se iz odgovarajućih polja u retku podugovora. Ako odabrani redak podugovora ima vrijednosti u poljima **Projekt**, **Zadatak** i **Proizvod**, vrijednosti odgovarajućih polja u retku fakture dobavljača ne mogu se razlikovati od tih vrijednosti. |
| Datum transakcije | Datum kada će stvarni trošak retka fakture dobavljača biti zabilježen u projektu. | Nijedno|
| Razred transakcije | Kada se proizvodi fakturiraju, ovo polje treba postaviti na **Materijal**. | Vrijednost **Materijal** označava da se redak fakture dobavljača koristi za bilježenje iznosa fakture za materijale koji su nabavljeni. |
| Project | Naziv projekta u kojem su korišteni proizvodi koji se fakturiraju. | To je polje obavezno i ne smije se ostaviti prazno. |
| Zadatak | Naziv projektnog zadatka u kojem su korišteni proizvodi koji se fakturiraju. To polje dostupno je samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako se to polje ostavi praznim, voditelj projekta može povezati redak fakture dobavljača s nabavljenim proizvodom koji se koristi u bilo kojem zadatku projekta. Ako redak fakture dobavljača ne upućuje na redak podugovora, a to polje je ostavljeno prazno, stvarni trošak koji je kreirao redak fakture dobavljača neće biti povezan ni s kojom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se neće moći fakturirati krajnjem kupcu. |
| Odaberi proizvod | Odaberite je li proizvod koji se fakturira postojeći proizvod u katalogu ili dopisani proizvod. | Zadana vrijednost unosi se iz retka podugovora kada se odabere redak podugovora. |
| Proizvod | Odaberite proizvod iz kataloga Unesite proizvod dopisan, unesite naziv prizvoda. | Ovo polje koristi se za unos zadanih nabavnih cijena za postojeće proizvode. |
| Količina | Unesite količinu koju dobavljač fakturira u ovom retku fakture. | Nijedno |
| Grupa jedinica | Odaberite grupu jedinica jedinice u kojoj je izražena količina koja se fakturira. | Nijedno |
| Jedinica | Zadana vrijednost je osnovna jedinica odabrane grupe jedinica. Tu vrijednost možete promijeniti za kupnju u bilo kojoj jedinici odabrane grupe jedinica. | Kombinacija vrijednosti **Proizvod** i **Jedinica** upotrebljavat će se kao zadana ili izračunana vrijednost za polje **Jedinična cijena** u retku fakture dobavljača. |
| Jedinična cijena | Zadana jedinična cijena koristi kombinaciju vrijednosti **Proizvod** i **Jedinica** iz cjenika projekta koja je primjenjiva na datum transakcije retka fakture dobavljača. | Nijedno |
| Podzbroj | To je polje samo za čitanje koje se izračunava kao *Količina* &times; *Jedinična cijena* ako su unesene vrijednosti u polja **Količina** i **Jedinična cijena**. Ako su jedno ili oba polja prazna, možete unijeti vrijednost u to polje. | Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupni iznos | Ukupni iznos retka fakture dobavljača, uključujući porez. To polje izračunava se kao *Međuzbroj* + *Porez na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
