---
title: Redci za kontrolne točke u fakturi dobavljača
description: Ovaj članak objašnjava kako stvoriti retke fakture dobavljača za kontrolne točke na podugovoru.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9260986"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Redci za kontrolne točke u fakturi dobavljača

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Faktura dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations može imati retke fakture dobavljača za kontrolne točke koje su definirane u retku podugovora. Voditelji projekata mogu koristiti retke faktura dobavljača za kontrolne točke za bilježenje troškova usluga koje su nabavljene kao troškova temeljenih na kontrolnim točkama koji nastaju na uslugama ili proizvodima koji su nabavljeni za projekt.

Reci fakture dobavljača za kontrolne točke uvijek moraju upućivati na redak podugovora koji ima metodu naplate po fiksnoj cijeni. Kada redak fakture dobavljača za kontrolne točke upućuje na redak podugovora, voditelji projekata moći će uskladiti i provjeriti temeljne troškove vremena, troškova ili materijala koji upućuju na taj redak podugovora u odnosu na kontrolnu točku koju fakturira dobavljač.

Tablica u nastavku pruža informacije o poljima u recima fakture dobavljača za kontrolne točke.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj naziv prikazivat će se kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturira u retku fakture dobavljača. | Nijedno |
| Podugovor | Podugovor na temelju kojeg su usluge izvorno naručene. | Kada se za fakturu dobavljača odabere podugovor, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može sadržavati retke fakture dobavljača koji upućuju na različite podugovore. |
| Redak podugovora | Redak podugovora na temelju kojeg su usluge naručene. Popis redaka podugovora koje je moguće odabrati ograničen je na retke na odabranom podugovoru. | Kada je redak podugovora odabran u retku fakture dobavljača za kontrolne točke, polja **Uloga** i **Kategorija transakcije** i polja povezana s proizvodom nevažna su i nisu dostupna. Polja **Količina**, **Jedinica** i **Grupa jedinica** također nisu važna za retke fakture dobavljača temeljene na kontrolnoj točki. |
| Datum transakcije | Datum kada će stvarni trošak retka fakture dobavljača biti zabilježen u projektu. | Nijedno |
| Razred transakcije | Odaberite **Kontrolna točka** za bilježenje fakture dobavljača za dovršenu kontrolnu točka koja je definirana u retku podugovora. | Nijedno |
| Kontrolna točka | Odaberite kontrolnu točku koja je definirana u povezanom retku podugovora koji je označen kao **Spremno za fakturiranje**. | Kontrolne točke retka podugovora koje imaju status **Spremno za fakturiranje** mogu se odabrati u retku fakture dobavljača. |
| Project | Naziv projekta u kojem su korištene usluge koje se fakturiraju. | To je polje obavezno i ne smije se ostaviti prazno. |
| Zadatak | Naziv projektnog zadatka u kojem su korištene usluge koje se fakturiraju. To polje dostupno je samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako se ovo polje ostavi praznim, voditelj projekata može uskladiti redak fakture dobavljača s klasom transakcija u povezanom retku podugovora koji je zabilježen u bilo kojem zadatku projekta. Ako redak fakture dobavljača ne upućuje na redak podugovora, a to polje je ostavljeno prazno, stvarni trošak koji je kreirao redak fakture dobavljača neće biti povezan ni s kojom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se možda neće moći fakturirati krajnjem kupcu. |
| Iznos kontrolne točke | Unesite vrijednost kontrolne točke koja je definirana u retku podugovora koji je spreman za fakturiranje. | Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupni iznos | Ukupni iznos retka fakture dobavljača, uključujući porez. Ovo polje izračunava se kao *Iznos kontrolne točke* + *Porez na promet*. | Nijedno |

> [!NOTE]
> Kada se stvori redak fakture dobavljača koji upućuje na kontrolnu točku retka podugovora, status kontrolne točke podugovora ažurira se na **Faktura dobavljača izrađena**. Zatim, kada se ta faktura dobavljača potvrdi, status kontrolne točke retka podugovora ažurira se na **Faktura dobavljača potvrđena**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
