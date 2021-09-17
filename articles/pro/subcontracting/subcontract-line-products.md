---
title: Redci podugovora za proizvode
description: U ovoj temi objašnjava se način bilježenja redaka podugovora za proizvode i uporabe različitih polja za bilježenje kupnje proizvoda od dobavljača.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323677"
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

| Polje | Opis |
| ----- | ----------- |
| Ime/naziv | Naziv retka podugovora. |
| Opis | Kratak opis proizvoda koje se naručuje na retku podugovora. |
| Vrsta retka | Ova vrijednost polja zadana je na vrijednost **Na temelju količine**. |
| Način naplate |  Način naplate retka podugovora. Raspored faktura koje se temelje na kontrolnim točkama dostupan je za retke podugovora s fiksnom cijenom. |
| Razred transakcije | Ova vrijednost polja zadana je na vrijednost **Vrijeme**. Za stvaranje redaka podugovora za kupnju proizvoda, u polju **Klasa transakcije** odaberite **Materijal**. Ovaj odabir označava da se redak podugovora koristi za bilježenje kupnje proizvoda koji će se upotrebljavati na projektima. |
| Odabir proizvoda | Odaberite ako se proizvod koji se kupuje nalazi u katalogu proizvoda ili je upisani proizvod. |
| Proizvod | Odaberite aktivan proizvod iz kataloga. Ovo je polje dostupno samo kada je stavka **Odaberi proizvod** postavljena na **Postojeći**. |
| Upisani proizvod | Unesite naziv upisanog proizvoda. Ovo je polje dostupno samo kada je stavka **Odaberi proizvod** postavljena na **Upisan**.  |
| Zatraženi datum isporuke | Odaberite željeni datum isporuke proizvoda. Ovaj se datum također upotrebljava za odabir cjenika projekta iz cjenika projekta priloženih podugovoru. Cijena proizvoda na retku podugovora tada se zadaje iz tog cjenika. |
| Ugovoreni datum isporuke | Odaberite datum kada je ugovorom utanačena isporuka proizvoda.  |
| Naručena količina | Unesite količinu proizvoda koji se kupuje od dobavljača. Ako voditelj projekta prekorači ovu količinu, prikazat će se upozorenje. |
| Grupa jedinica | Ova je vrijednost zadana samo za kataloške proizvode. Nakon odabira stavki **Proizvod** i **Traženi datum isporuke** sustav bira primjenjivi cjenik na temelju datuma isporuke. Povezane stavke cjenika potrebne su za odgovarajući proizvod. Vrijednosti jedinice i grupe jedinica zadane su iz postavki u zapisu stavke cjenika. |
| Jedinica | Ova je vrijednost zadana postavkama jedinice u zapisu stavke cjenika. Po potrebi ovo možete promijeniti u drugu jedinicu. Kombinacija proizvoda i jedinice upotrebljava se za zadavanje jedinične cijene u retku podugovora za postojeće kataloške proizvode. |
| Jedinična cijena | Jedinična cijena zadana je s pomoću kombinacije proizvoda i jedinice iz stavki cjenika povezanih s cjenikom za projekt koji se primjenjuje na traženi datum isporuke retka podugovora.  |
| Podzbroj | Ovo polje samo za čitanje izračunava se kao Količina x Jedinična cijena ako oba polja imaju unesene vrijednosti. Ako su polja **Količina**, **Jedinična cijena** ili oba prazna, u polje možete unijeti vrijednost.  |
| Porez na promet | Unesite vrijednost poreza na promet. |
| Ukupni iznos | Ovo izračunano polje prikazuje ukupni iznos retka podugovora nakon uključivanja poreza. Vrijednost u ovom polju izračunava se kao međuzbroj + porez. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
