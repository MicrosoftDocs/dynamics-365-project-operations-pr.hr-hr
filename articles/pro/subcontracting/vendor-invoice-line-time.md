---
title: Redci za vrijeme u fakturi dobavljača
description: Ovaj članak objašnjava kako zabilježiti retke faktura dobavljača za vremenske troškove koje podizvođači unesu.
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

Faktura dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations može imati retke fakture dobavljača za vrijeme. Voditelji projekata mogu koristiti retke fakture dobavljača za vrijeme kako bi zabilježili troškove vremena podizvođača na projektima.

Redci fakture dobavljača za vrijeme mogu, ali ne moraju upućivati na redak podugovora za vrijeme. Ako redak fakture dobavljača za vrijeme upućuje na podugovor, voditelji projekata moći će usporediti i provjeriti vrijeme koje fakturira redak fakture dobavljača s vremenom koje su zabilježili podizvođači i odobrili voditelji projekata na projektu.

Tablica u nastavku pruža informacije o poljima u recima fakture dobavljača za vrijeme.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv retka fakture dobavljača za pomoć pri identifikaciji. | Taj naziv prikazivat će se kao prvi stupac u svim pretraživanjima koja se temelje na recima fakture dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturira u retku fakture dobavljača. | Nijedno |
| Podugovor | Podugovor na temelju kojeg su usluge izvorno naručene. | Kada se za fakturu dobavljača odabere podugovor, svi reci na fakturi dobavljača naslijedit će taj odabir. Faktura dobavljača ne može sadržavati retke fakture dobavljača koji upućuju na različite podugovore. |
| Redak podugovora | Redak podugovora na temelju kojeg su usluge naručene. Popis redaka podugovora koje je moguće odabrati ograničen je na retke na odabranom podugovoru. | Kada je redak podugovora odabran na retku fakture dobavljača za vrijeme, zadane vrijednosti za polja **Projekt**, **Uloga** i **Resurs koji se može rezervirati** unose se iz odgovarajućih polja u retku podugovora. Ako odabrani redak podugovora ima vrijednosti u poljima **Projekt**, **Uloga** i **Može se rezervirati**, vrijednosti odgovarajućih polja u retku fakture dobavljača ne mogu se razlikovati od tih vrijednosti. |
| Datum transakcije | Datum kada će stvarni trošak retka fakture dobavljača biti zabilježen u projektu. | Nijedno |
| Razred transakcije | Zadana vrijednost je **Vrijeme**. | Vrijednost **Vrijeme** označava da se redak fakture dobavljača koristi za bilježenje iznosa fakture za vrijeme podizvođača. |
| Project | Naziv projekta u kojem su korištene usluge koje se fakturiraju. | To je polje obavezno i ne smije se ostaviti prazno. |
| Zadatak | Naziv projektnog zadatka u kojem su korištene usluge koje se fakturiraju. To polje dostupno je samo ako je odabran projekt. Odabir projektnog zadatka nije obavezan. | Ako se to polje ostavi praznim, voditelj projekta može povezati redak fakture dobavljača s vremenom koje zabilježe resursi podizvođača u bilo kojem zadatku projekta. Ako redak fakture dobavljača ne upućuje na redak podugovora, a to polje je ostavljeno prazno, stvarni trošak koji je kreirao redak fakture dobavljača neće biti povezan ni s kojom nenaplaćenom stvarnom prodajom. U tom slučaju, ako je postavljena naplata na temelju zadataka, troškovi se možda neće moći fakturirati krajnjem kupcu. |
| Uloga | Uloga resursa podugovora čije se vrijeme fakturira. | Ovo polje specificira ulogu koju obavljaju resursi podugovora čije je vrijeme fakturirano na fakturi dobavljača. |
| Resurs koji je moguće rezervirati | Ime podizvođača čije se vrijeme fakturira. Odabir resursa koji se može rezervirati nije obavezan. | Ako se to polje ostavi praznim, voditelj projekta može povezati redak fakture dobavljača s vremenom koje zabilježi bilo koji resurs koji pripada dobavljaču u bilo kojem retku fakture dobavljača. |
| Količina | Unesite broj sati vremena koje dobavljač fakturira u retku fakture. |Nijedno |
| Grupa jedinica | Zadana vrijednost je **Grupa vremenskih jedinica** i ne može se promijeniti. | Nijedno |
| Jedinica | Zadana vrijednost je osnovna jedinica sati iz grupe jedinica za vrijeme. Ovu vrijednost možete promijeniti kako biste kupili bilo koju jedinicu grupe jedinica vremena, kao što je dan ili tjedan. | Kombinacija vrijednosti **Uloga** i **Jedinica** upotrebljavat će se kao zadana ili izračunana vrijednost za polje **Jedinična cijena** u retku fakture dobavljača. |
| Jedinična cijena | Zadana jedinična cijena koristi kombinaciju vrijednosti **Uloga** i **Jedinica** iz cjenika projekta koja je primjenjiva na datum transakcije retka fakture dobavljača. | Ako je cijena za primjenjivi cjenik projekta postavljena u drugoj jedinici različitoj od jedinice u retku fakture dobavljača, sustav upotrebljava pretvaranje jedinice za izračun jedinične cijene. |
| Podzbroj | To je polje samo za čitanje koje se izračunava kao *Količina* &times; *Jedinična cijena* ako su unesene vrijednosti u polja **Količina** i **Jedinična cijena**. Ako su jedno ili oba polja prazna, možete unijeti vrijednost u to polje. | Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. | Nijedno |
| Ukupni iznos | Ukupni iznos retka fakture dobavljača, uključujući porez. To polje izračunava se kao *Međuzbroj* + *Porez na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
