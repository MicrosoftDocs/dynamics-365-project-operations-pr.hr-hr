---
title: Redci podugovora za proizvode
description: U ovoj temi objašnjava se način bilježenja redaka podugovora za proizvode i uporabe različitih polja za bilježenje kupnje proizvoda od dobavljača.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71e4a48c3d29d7ea5b015f6c6797da60001fccff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579064"
---
# <a name="subcontract-lines-for-products"></a>Redci podugovora za proizvode

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Podugovor u aplikaciji Dynamics 365 Project Operations može imati redak podugovora za proizvode. Ovi redci omogućuju voditelju projekta da kupuje proizvode od dobavljača koje zatim mogu upotrebljavati za projektne zadatke.

Kako biste stvorili redak podugovora za proizvode u aplikaciji Project Operations, poduzmite sljedeće korake.

1. Na stranici navigacije odaberite **Podugovori** i zatim otvorite podugovor na kojem želite raditi. 
2. Na kartici **Retci podugovora** odaberite **+ Novi** kako biste stvorili novi redak podugovora.
3. Na stranici **Brzo stvaranje**, u polju **Klasa transakcije**, odaberite **Materijal** i unesite ili odaberite obvezne podatke o polju. 
4. Odaberite **Spremi**.

U tablici u nastavku nalaze se podaci o poljima na stranicama **Pojedinosti retka podugovora** i **Brzo stvaranje**, budući da su relevantna za kupnju.

| Polje | Opis | Funkcionalni utjecaj|
| ----- | ----------- | ----------- |
| Ime/naziv | Naziv retka podugovora za pomoć pri identifikaciji. |To će se prikazati kao prvi stupac u svim pretraživanjima koja se temelje na redcima podugovara.
| Opis | Kratak opis proizvoda koje se naručuje na retku podugovora. | Nijedno |
| Vrsta retka | Ovo polje ima zadanu vrijednost stavke **Na temelju količine**. |Nijedno |
| Način naplate | Ovo je skup mogućnosti koji predstavlja dva glavna modela ugovaranja podržana aplikacijom Project Operations: **Fiksna cijena** i **Vrijeme i materijal**. | Na temelju odabranog načina naplate, raspored faktura koji se temelji na kontrolnim točkama dostupan je za retke podugovora koji imaju način naplate s fiksnom cijenom. |
| Razred transakcije |Ovo polje ima zadanu vrijednost stavke **Vrijeme**. Kako biste stvorili retke podugovora za kupnju proizvoda, postavite polje **Klasa transakcije** na **Materijal**.  | To ukazuje da se redak podugovora upotrebljava za evidentiranje kupnje proizvoda koji će se upotrebljavati za projekte. |
| Odabir proizvoda | Odaberite ako se proizvod koji se kupuje nalazi u katalogu proizvoda ili je upisani proizvod. |Nijedno |
| Proizvod | Odaberite aktivan proizvod iz kataloga. Ovo je polje dostupno samo kada je stavka **Odaberi proizvod** postavljena na **Postojeći**. |Kombinacija **Proizvod** i **Jedinica** upotrebljavat će se kao zadana vrijednost ili će se izračunati za jediničnu cijenu retka podugovora.
| Upisani proizvod | Unesite naziv upisanog proizvoda. Ovo je polje dostupno samo kada je stavka **Odaberi proizvod** postavljena na **Upisan**.  |Nabavna cijena neće se automatski popuniti za dopisane proizvode.|
| Zatraženi datum isporuke | Unesite željeni datum isporuke proizvoda.| Ovaj se datum također upotrebljava za odabir cjenika projekta iz cjenika projekta priloženih podugovoru. Cijena proizvoda na retku podugovora tada se zadaje iz tog cjenika. |
| Ugovoreni datum isporuke | Unesite datum kada je ugovorom predviđena isporuka proizvoda.  |Nijedno|
| Naručena količina | Unesite količinu proizvoda koji se kupuje od dobavljača.| To će se upotrebljavati za prikaz upozorenja kada voditelj projekta previše crpi tu količinu.|
| Grupa jedinica | Ova je vrijednost zadana samo za kataloške proizvode. |Nakon odabira stavki **Proizvod** i **Traženi datum isporuke** sustav bira primjenjivi cjenik na temelju datuma isporuke. Povezane stavke cjenika potrebne su za odgovarajući proizvod. Vrijednosti jedinice i grupe jedinica zadane su iz postavki u zapisu stavke cjenika. |
| Jedinica | Ova je vrijednost zadana za postavku jedinice u zapisu stavke cjenika. Po potrebi ovo možete promijeniti u drugu jedinicu.| Kombinacija proizvoda i jedinice upotrebljava se za zadavanje jedinične cijene u retku podugovora za postojeće kataloške proizvode. |
| Jedinična cijena | Jedinična cijena zadana je s pomoću kombinacije proizvoda i jedinice iz stavki cjenika povezanih s cjenikom za projekt koji se primjenjuje na traženi datum isporuke retka podugovora.  |Nijedno |
| Podzbroj | Ovo polje samo za čitanje izračunava se kao Količina x Jedinična cijena ako oba polja imaju unesene vrijednosti. Ako su polja **Količina**, **Jedinična cijena** ili oba prazna, u polje možete unijeti vrijednost.  |Nijedno |
| Porez na promet | Unesite vrijednost poreza na promet. |Nijedno |
| Ukupni iznos | Ovo izračunano polje prikazuje ukupni iznos retka podugovora nakon uključivanja poreza. Vrijednost u ovom polju izračunava se kao međuzbroj + porez. |Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
