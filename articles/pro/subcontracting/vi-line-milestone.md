---
title: Redci za kontrolne točke u fakturi dobavljača
description: U ovom se članku objašnjava kako kreirati retke fakture dobavljača za ključne etape na podugovaratelju.
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

Faktura dobavljača u Microsoftu Dynamics 365 Project Operations može imati retke fakture dobavljača za ključne etape definirane u retku kooperanta. Voditelji projekata mogu koristiti retke fakture dobavljača za ključne etape kako bi zabilježili troškove usluga koji se nabavljaju kao troškove temeljene na ključnim etapama koji nastaju na uslugama ili proizvodima koji se nabavljaju za projekt.

Reci fakture dobavljača za ključne etape uvijek se moraju odnositi na redak kooperanta koji ima fiksni način naplate cijena. Kada se redak fakture dobavljača za ključne etape poziva na redak podugovaranja, voditelji projekata moći će uskladiti i provjeriti temeljne troškove vremena, troškova ili materijala koji se odnose na taj redak podugovaranja u odnosu na prekretnicu koju fakturira dobavljač.

Sljedeća tablica sadrži informacije o poljima u recima fakture dobavljača za ključne etape.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj će naziv biti prikazan kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturira u retku fakture dobavljača. | Nijedno |
| Podugovor | Kooperant na kojem su usluge izvorno naručene. | Kada je za fakturu dobavljača odabran kooperant, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može imati retke fakture dobavljača koji se odnose na različite kooperante. |
| Redak kooperacije | Linija podugovaranja na kojoj su usluge naručene. Popis redaka kooperanta koji se mogu odabrati ograničen je na retke na odabranom kooperantu. | Kada je redak kooperanta odabran u retku fakture dobavljača za ključne etape, **polja kategorija** Uloga **i** transakcija te polja povezana s proizvodom nisu relevantna i nisu dostupna. Polja **Grupa Količina**, **Jedinica** i **Jedinica** također nisu relevantna za retke fakture dobavljača koji se temelje na ključnoj etapi. |
| Datum transakcije | Datum kada će se na projektu zabilježiti stvarni trošak retka fakture dobavljača. | Nijedno |
| Razred transakcije | Odaberite **Prekretnica** da biste zabilježili fakturu dobavljača za dovršenu prekretnicu definiranu u retku kooperanta. | Nijedno |
| Kontrolna točka | Odaberite prekretnicu definiranu u povezanom retku kooperanta koji je označen kao **Spreman za fakturiranje**. | Ključne etape redaka kooperanta koje imaju status Spremno **za fakturiranje** mogu se odabrati u retku fakture dobavljača. |
| Project | Naziv projekta na kojem su korištene usluge koje se fakturiraju. | Ovo je polje obavezno i ne može se ostaviti praznim. |
| Zadatak | Naziv projektnog zadatka na kojem su korištene usluge koje se fakturiraju. Ovo je polje dostupno samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako ovo polje ostane prazno, voditelj projekta može uskladiti redak fakture dobavljača s klasom transakcija u povezanom retku kooperanta koja je zabilježena na bilo kojem zadatku projekta. Ako se redak fakture dobavljača ne odnosi na redak kooperanta, a to polje ostaje prazno, stvarni trošak kreiran retkom fakture dobavljača neće biti povezan ni s jednom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se možda neće moći fakturirati krajnjem kupcu. |
| Iznos kontrolne točke | Unesite vrijednost prekretnice definirane u retku kooperanta koji je spreman za fakturiranje. | Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupan iznos | Ukupan iznos retka fakture dobavljača, uključujući poreze. Ovo se polje izračunava kao *iznos* + *prekretnice Porez na* promet. | Nijedno |

> [!NOTE]
> Kada se kreira redak fakture dobavljača koji upućuje na prekretnicu retka kooperanta, status prekretnice kooperanta obnavlja se u **kreiranu** fakturu Dobavljača. Zatim, kada se ta faktura dobavljača potvrdi, status prekretnice retka kooperanta ažurira se u **Potvrđena** faktura Dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
