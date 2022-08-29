---
title: Redci za vrijeme u fakturi dobavljača
description: U ovom se članku objašnjava kako zabilježiti retke fakture dobavljača za vremenske troškove koje su stavili kooperanti.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262003"
---
# <a name="vendor-invoice-lines-for-time"></a>Redci za vrijeme u fakturi dobavljača

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Faktura dobavljača u Microsoftu Dynamics 365 Project Operations može imati retke fakture dobavljača za vrijeme. Voditelji projekata mogu koristiti retke fakture dobavljača za vrijeme bilježenja troškova vremena kooperanta na projektima.

Reci fakture dobavljača za vrijeme mogu se, ali i ne moraju odnositi na redak kooperanta za vrijeme. Ako redak fakture dobavljača za vrijeme upućuje na podugovaranje, voditelji projekata moći će uskladiti i provjeriti vrijeme koje redak fakture dobavljača fakturira s vremenom koje su zabilježili podizvođači i odobrili voditelji projekata na projektu.

Sljedeća tablica sadrži podatke o poljima u recima fakture dobavljača za vrijeme.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj će naziv biti prikazan kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturira u retku fakturiranja dobavljača. | Nijedno |
| Podugovor | Kooperant na kojem su usluge izvorno naručene. | Kada je za fakturu dobavljača odabran kooperant, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može imati retke fakture dobavljača koji se odnose na različite kooperante. |
| Redak kooperacije | Linija podugovaranja na kojoj su usluge naručene. Popis redaka kooperanta koji se mogu odabrati ograničen je na retke na odabranom kooperantu. | Kada je redak kooperanta odabran u retku fakture dobavljača za vrijeme, zadane vrijednosti za **polja Resursi** Projekt **,** Uloga **i** Raspoloživost za rezervaciju unose se iz odgovarajućih polja u retku kooperanta. Ako odabrani redak kooperanta ima vrijednosti u poljima Projekt **,** Uloga **i** Moguće **rezervirati, vrijednosti odgovarajućih polja u** retku fakture dobavljača ne mogu se razlikovati od tih vrijednosti. |
| Datum transakcije | Datum kada će se na projektu zabilježiti stvarni trošak retka fakture dobavljača. | Nijedno |
| Razred transakcije | Zadana vrijednost je **Vrijeme**. | **Vrijednost Vrijeme** označava da se redak fakture dobavljača koristi za bilježenje iznosa fakture vremena kooperanta. |
| Project | Naziv projekta na kojem su korištene usluge koje se fakturiraju. | Ovo je polje obavezno i ne može se ostaviti praznim. |
| Zadatak | Naziv projektnog zadatka na kojem su korištene usluge koje se fakturiraju. Ovo je polje dostupno samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako ovo polje ostane prazno, voditelj projekta može uskladiti redak fakture dobavljača s vremenom koje su zabilježili resursi kooperanta na bilo kojem zadatku projekta. Ako se redak fakture dobavljača ne odnosi na redak kooperanta, a to polje ostaje prazno, stvarni trošak kreiran retkom fakture dobavljača neće biti povezan ni s jednom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se možda neće moći fakturirati krajnjem kupcu. |
| Uloga | Uloga resursa kooperanta čije se vrijeme fakturira. | Ovo polje navodi ulogu koju obavljaju resursi kooperanta čije je vrijeme fakturirano na fakturi dobavljača. |
| Resurs koji je moguće rezervirati | Ime podizvođača čije se vrijeme fakturira. Odabir resursa koji se može rezervirati nije obavezan. | Ako ovo polje ostane prazno, voditelj projekta može uskladiti redak fakture dobavljača s vremenom koje bilježi bilo koji resurs koji pripada dobavljaču u retku fakture dobavljača. |
| Količina | Unesite broj sati koje dobavljač fakturira u retku fakture. |Nijedno |
| Grupa jedinica | Zadana vrijednost je **grupa** Jedinica vremena i ne može se mijenjati. | Nijedno |
| Jedinica | Zadana vrijednost je osnovna jedinica sati iz grupe jedinica vremena. Tu vrijednost možete promijeniti tako da biste je kupili u bilo kojoj jedinici grupe vremenskih jedinica, kao što su dan ili tjedan. | Kombinacija vrijednosti Uloga **i** Jedinica **koristit će se kao zadana ili izračunata vrijednost za** polje Jedinična **cijena** u retku fakture dobavljača. |
| Jedinična cijena | Zadana jedinična **cijena koristi kombinaciju vrijednosti Uloga** i **Jedinica** iz cjenika projekta koja se primjenjuje na datum transakcije retka fakture dobavljača. | Ako je cijena primjenjivog cjenika projekta postavljena u jedinici koja se razlikuje od jedinice u retku fakture dobavljača, sustav koristi jediničnu konverziju za izračun cijene po jedinici. |
| Podzbroj | Ovo polje samo za čitanje izračunava se kao *Jedinična cijena* količine&times;*ako* su vrijednosti unesene **i u polje Količina** i u polje Jedinična **cijena.** Ako su jedno ili oba polja prazna, u ovo polje možete unijeti vrijednost. | Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupan iznos | Ukupan iznos retka fakture dobavljača, uključujući poreze. Ovo se polje izračunava kao *porez na promet podzbroja* + *·*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
