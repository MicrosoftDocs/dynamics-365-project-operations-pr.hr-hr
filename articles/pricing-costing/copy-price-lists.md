---
title: Kopiranje cjenika
description: U ovoj temi nalaze se informacije o načinu kopiranja cjenika u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67a69d521ac0a5632371138bd4fbb9dd00fe34ee
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181488"
---
# <a name="copy-price-lists"></a>Kopiranje cjenika

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Kopije cjenika možete stvoriti u aplikaciji Dynamics 365 Project Operations. Na primjer, možete stvoriti cjenike za predstojeću godinu s pomoću cjenika iz tekuće godine.  Ili možete kopirati cjenik za cijene naplate i prodajne cijene iz cjenika troškova. 

Kako biste kopirali cjenik, poduzmite sljedeće korake.

1. Otvorite cjenik kojeg želite kopirati i odaberite **Kopiraj**.
2. Unesite sve potrebne podatke za kopiranje cjenika. Sljedeća tablica prikazuje razmatranja koja treba imati na umu pri unosu podataka.

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| Ime | Naziv izvornog cjenika s dodanom riječju **-kopija**. | Cjenik uključuje ovu vrijednost na svim stranicama popisa i padajućim mogućnostima. |
| Kontekst | Unesite kontekst koji želite za ciljani cjenik. | Cjenik s kontekstom postavljenim na **Trošak** upotrebljava se za traženje cijene za procjene troškova i stvarne troškove. Cjenik s kontekstom postavljenim na **Prodaja** upotrebljava se za traženje cijene za procjene prodaje i stvarne podatke o prodaji. Samo cjenici s kontekstom postavljenim na **Prodaja** mogu se priložiti cjeniku projekta za klijenta, ponude ili ugovor. |
| Datum početka | Datum početka razdoblja u kojem je cjenik na snazi. | Zajedno s mogućnosti **Datum završetka** ovo se polje upotrebljava za određivanje cjenika mjerodavnog za određeni redak procjene ili stvarnog podatka. |
| Datum završetka | Datum završetka razdoblja u kojem je cjenik na snazi. | Zajedno s mogućnosti **Datum početka** ovo se polje upotrebljava za određivanje cjenika mjerodavnog za određeni redak procjene ili stvarnog podatka. |
| Valuta | Valuta izvornog cjenika. To se može promijeniti. | Kada se to promijeni, svi nastali redci cijene radne snage, troškove i stavke kataloga proizvoda pretvaraju se tijekom kopiranja u valutu ciljanog cjenika. |
| Jedinica vremena | Valuta izvornog cjenika. To se može promijeniti. | Kada se to promijeni, svi nastali redci cijene za stavke radne snage pretvaraju se tijekom kopiranja u jedinicu ciljanog cjenika. Upotrebljava se pretvorba iz postavke jedinice za vremensku jedinicu izvornog cjenika i vremensku jedinicu ciljanog cjenika. |
| Opis | Opis izvornog cjenika s dodanom riječju **-kopija**. Ovo je tekstno polje i omogućuje vam da imate opis cjenika u više redaka. | Ovo se polje prikazuje u prikazu **Pridružen** na cjeniku različitih entiteta koji imaju povezane cjenike. |

3. Spremite cjenik. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Ažuriranje cjenika primjenom marže na sve cijene

1. Na karticama cjenika **Uloga**, **Kategorija** i **Stavka cjenika** možete odabrati **Ažuriraj cijene** kako biste primijenili maržu na sve cijene u podrešetki. 
2. Otvara se dijaloška stranica na kojoj unesite maržu. Također možete unijeti postotak negativne marže kako biste smanjili cijene za određeni postotak. 
3. Odaberite **U redu** na dijaloškoj stranici, a zatim provjerite podudaraju li se cijene u podrešetki s promjenama koje ste napravili.
