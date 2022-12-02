---
title: Redci za kategorije troška u fakturi dobavljača
description: Ovaj članak objašnjava kako zabilježiti retke fakture dobavljača za kategorije troškova.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261671"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Redci za kategorije troška u fakturi dobavljača

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Faktura dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations može imati retke fakture dobavljača za kategorije troškova. Voditelji projekata mogu koristiti retke faktura dobavljača za kategorije troškova kako bi zabilježili troškove usluga koje se nabavljaju kao kategorije troškova.

Reci fakture dobavljača za kategorije troškova mogu, ali ne moraju upućivati na redak podugovora za kategorije troškova. Ako redak fakture dobavljača za kategorije troškova upućuje na podugovor, voditelji projekata moći će usporediti i provjeriti troškove koje fakturira redak fakture dobavljača s troškovima koji su zabilježeni u tim kategorijama troškova i koje su odobrili voditelji projekata na projektu.

Tablica u nastavku pruža informacije o poljima u recima fakture dobavljača za kategorije troškova.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj naziv prikazivat će se kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturira u retku fakture dobavljača. | Nijedno |
| Podugovor | Podugovor na temelju kojeg su usluge izvorno naručene. | Kada se za fakturu dobavljača odabere podugovor, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može sadržavati retke fakture dobavljača koji upućuju na različite podugovore. |
| Redak podugovora | Redak podugovora na temelju kojeg su usluge naručene. Popis redaka podugovora koje je moguće odabrati ograničen je na retke na odabranom podugovoru. | Kada je redak podugovora odabran na retku fakture dobavljača za kategorije troškova, zadane vrijednosti za polja **Projekt**, **Zadatak** i **Kategorija transakcije** unose se iz odgovarajućih polja u retku podugovora. Ako odabrani redak podugovora ima vrijednosti u poljima **Projekt**, **Projektni zadatak** i **Kategorija transakcije**, vrijednosti odgovarajućih polja u retku fakture dobavljača ne mogu se razlikovati od tih vrijednosti. |
| Datum transakcije | Datum kada će stvarni trošak retka fakture dobavljača biti zabilježen u projektu. |Nijedno |
| Razred transakcije | Odaberite **Trošak** za bilježenje fakture dobavljača za kategoriju troškova. | Vrijednost **Trošak** označava da se redak fakture dobavljača koristi za bilježenje iznosa fakture za usluge koje su nabavljene kao kategorije troškova. |
| Project | Naziv projekta u kojem su korištene usluge koje se fakturiraju. | To je polje obavezno i ne smije se ostaviti prazno. |
| Zadatak | Naziv projektnog zadatka u kojem su korištene usluge koje se fakturiraju. To polje dostupno je samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako se to polje ostavi praznim, voditelj projekta može povezati redak fakture dobavljača s troškovima koji su zabilježeni u bilo kojem zadatku projekta. Ako redak fakture dobavljača ne upućuje na redak podugovora, a to polje je ostavljeno prazno, stvarni trošak koji je kreirao redak fakture dobavljača neće biti povezan ni s kojom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se možda neće moći fakturirati krajnjem kupcu. |
| Kategorija transakcije | Kategorija transakcije koja se fakturira. Za odabranu kategoriju transakcije mora se kreirati odgovarajuća kategorija troška. | Kombinacija vrijednosti **Kategorija transakcije** i **Jedinica** upotrebljavat će se kao zadana ili izračunana vrijednost za polje **Jedinična cijena** u retku fakture dobavljača. |
| Količina | Unesite količinu koju dobavljač fakturira u retku fakture. |Nijedno|
| Grupa jedinica | Zadana vrijednost unosi se na temelju grupe jedinica odabrane kategorije transakcije. | Nijedno |
| Jedinica | Zadana vrijednost je osnovna jedinica odabrane grupe jedinica. Tu vrijednost možete promijeniti za kupnju u bilo kojoj jedinici grupe jedinica. | Kombinacija vrijednosti **Kategorija transakcije** i **Jedinica** upotrebljavat će se kao zadana ili izračunana vrijednost za polje **Jedinična cijena** u retku fakture dobavljača. |
| Jedinična cijena | Zadana jedinična cijena koristi kombinaciju vrijednosti **Kategorija transakcije** i **Jedinica** iz cjenika projekta koja je primjenjiva na datum transakcije retka fakture dobavljača. | Ako je cijena za primjenjivi cjenik projekta postavljena u drugoj jedinici različitoj od jedinice u retku fakture dobavljača, sustav upotrebljava pretvaranje jedinice za izračun jedinične cijene. |
| Podzbroj | To je polje samo za čitanje koje se izračunava kao *Količina* &times; *Jedinična cijena* ako su unesene vrijednosti u polja **Količina** i **Jedinična cijena**. Ako su jedno ili oba polja prazna, možete unijeti vrijednost u to polje.| Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupni iznos | Ukupni iznos retka fakture dobavljača, uključujući porez. To polje izračunava se kao *Međuzbroj* + *Porez na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
