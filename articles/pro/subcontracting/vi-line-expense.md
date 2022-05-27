---
title: Reci fakture dobavljača za kategorije troškova
description: Ova tema objašnjava kako zabilježiti retke fakture dobavljača za kategorije troškova.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579527"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Reci fakture dobavljača za kategorije troškova

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Faktura dobavljača u Microsoftu Dynamics 365 Project Operations može imati retke fakture dobavljača za kategorije troškova. Voditelji projekata mogu koristiti retke fakture dobavljača za kategorije troškova da bi zabilježili troškove usluga koje se nabavljaju kao kategorije troškova.

Reci fakture dobavljača za kategorije troškova mogu se, ali i ne moraju odnositi na redak kooperanta za kategorije troškova. Ako redak fakture dobavljača za kategorije troškova upućuje na podugovaranje, voditelji projekata moći će uskladiti i provjeriti troškove koje redak fakture dobavljača fakturira s troškovima koji su zabilježeni u tim kategorijama troškova i koje su odobrili voditelji projekata na projektu.

Sljedeća tablica sadrži informacije o poljima u recima fakture dobavljača za kategorije troškova.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj će naziv biti prikazan kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturira u retku fakturiranja dobavljača. | Nijedno |
| Podugovor | Kooperant na kojem su usluge izvorno naručene. | Kada je za fakturu dobavljača odabran kooperant, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može imati retke fakture dobavljača koji se odnose na različite kooperante. |
| Redak kooperacije | Linija podugovaranja na kojoj su usluge naručene. Popis redaka kooperanta koji se mogu odabrati ograničen je na retke na odabranom kooperantu. | Kada je redak kooperanta odabran u retku fakture dobavljača za kategorije troškova, zadane vrijednosti za **polja Kategorija** projekta **·**, Zadatka **i** Transakcije unose se iz odgovarajućih polja u retku kooperanta. Ako odabrani redak kooperanta ima vrijednosti u poljima Projekt, Zadatak projekta i **Kategorija** transakcije, vrijednosti odgovarajućih polja u **retku fakture dobavljača ne mogu se razlikovati od tih vrijednosti.** **·** |
| Datum transakcije | Datum kada će se na projektu zabilježiti stvarni trošak retka fakture dobavljača. |Nijedno |
| Razred transakcije | Odaberite **Trošak** da biste zabilježili fakturu dobavljača za kategoriju troškova. | Vrijednost **Trošak** označava da se redak fakture dobavljača koristi za bilježenje iznosa fakture za usluge koje su nabavljene kao kategorije troškova. |
| Project | Naziv projekta na kojem su korištene usluge koje se fakturiraju. | Ovo je polje obavezno i ne može se ostaviti praznim. |
| Zadatak | Naziv projektnog zadatka na kojem su korištene usluge koje se fakturiraju. Ovo je polje dostupno samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako ovo polje ostane prazno, voditelj projekta može uskladiti redak fakture dobavljača s troškovima koji su zabilježeni na bilo kojem zadatku projekta. Ako se redak fakture dobavljača ne odnosi na redak kooperanta, a to polje ostaje prazno, stvarni trošak kreiran retkom fakture dobavljača neće biti povezan ni s jednom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se možda neće moći fakturirati krajnjem kupcu. |
| Kategorija transakcije | Kategorija transakcije koja se fakturira. Za odabranu kategoriju transakcije potrebno je kreirati odgovarajuću kategoriju troškova. | Kombinacija vrijednosti Kategorije **transakcije i** Jedinice **koristit će se kao zadana** ili izračunata vrijednost za **polje Jedinična cijena** u retku fakture dobavljača. |
| Količina | Unesite količinu koju dobavljač fakturira u redak fakture. |Nijedno|
| Grupa jedinica | Zadana vrijednost unosi se na temelju grupe jedinica odabrane kategorije transakcije. | Nijedno |
| Jedinica | Zadana vrijednost je osnovna jedinica odabrane grupe jedinica. Tu vrijednost možete promijeniti tako da biste je kupili u bilo kojoj jedinici grupe jedinica. | Kombinacija vrijednosti Kategorije **transakcije i** Jedinice **koristit će se kao zadana** ili izračunata vrijednost za **polje Jedinična cijena** u retku fakture dobavljača. |
| Jedinična cijena | Zadana jedinična cijena koristi kombinaciju kategorije **transakcije** i **vrijednosti Jedinica** iz cjenika projekta koja se primjenjuje na datum transakcije retka fakture dobavljača. | Ako je cijena primjenjivog cjenika projekta postavljena u jedinici koja se razlikuje od jedinice u retku fakture dobavljača, sustav koristi jediničnu konverziju za izračun cijene po jedinici. |
| Podzbroj | Ovo polje samo za čitanje izračunava se kao *Jedinična cijena* količine&times;*ako* su vrijednosti unesene **i u polje Količina** i u polje Jedinična **cijena.** Ako su jedno ili oba polja prazna, u ovo polje možete unijeti vrijednost.| Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupan iznos | Ukupan iznos retka fakture dobavljača, uključujući poreze. Ovo se polje izračunava kao *porez na promet podzbroja* + *·*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
