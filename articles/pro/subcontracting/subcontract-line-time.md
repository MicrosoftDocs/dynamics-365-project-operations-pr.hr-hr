---
title: Redci podugovora za vrijeme
description: U ovom se članku objašnjava kako zabilježiti retke kooperanta za vrijeme i zabilježiti nabavu vremena od dobavljača.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522223"
---
# <a name="subcontract-lines-for-time"></a>Redci podugovora za vrijeme

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Podugovor u aplikaciji Dynamics 365 Project Operations može imati redak podugovora za vrijeme. Redci podugovora za vrijeme omogućuju voditelju projekta da kupi vrijeme resursa dobavljača kako bi angažirao osoblje za projektne zadatke i zahtjeve za resurse.

Kako biste stvorili redak podugovora za vrijeme u aplikaciji Project Operations, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovori** i otvorite podugovor.
2. Na kartici **Retci podugovora** odaberite **Novi** kako biste stvorili novi redak podugovora.
3. Na stranici **Brzo stvaranje**, u polju **Klasa transakcije**, odaberite **Vrijeme**.
4. Unesite preostale podatke o polju, a zatim odaberite **Spremi**.

  U tablici u nastavku nalaze se podaci o poljima na stranicama **Redak podugovora** i **Brzo stvaranje**.

| **Polje** | **Opis** | **Funkcionalni utjecaj** |
| --- | --- | --- |
| Ime/naziv | Naziv retka podugovora za pomoć pri identifikaciji. | To će se prikazati kao prvi stupac u svim pretraživanjima koja se temelje na redcima podugovara. |
| Opis | Kratak opis usluga koje se kupuju na retku podugovora. |Nijedno |
| Vrsta retka |   Ovo polje ima zadanu vrijednost stavke **Na temelju količine**.| Nijedno |
| Način naplate | Ovo je skup mogućnosti koji predstavlja dva glavna modela ugovaranja podržana aplikacijom Project Operations: **Fiksna cijena** i **Vrijeme i materijal**. | Na temelju odabranog načina naplate, raspored faktura koji se temelji na kontrolnim točkama dostupan je za retke podugovora koji imaju način naplate s fiksnom cijenom. |
| Razred transakcije | Zadana vrijednost je **Vrijeme**. | To ukazuje da se redak podugovora upotrebljava za evidentiranje kupnje vremena podizvođača. |
| Uloga | Odaberite ulogu resursa podugovora čije se vrijeme kupuje. | Uloga koju obavljaju resursi podugovora određuje cijenu kupnje. |
| Zatraženi početak | Unesite datum kada resursi podugovora trebaju početi raditi. | To se upotrebljava za odabir cjenika projekta iz cjenika projekta priloženog podugovoru. Trošak uloge na retku podugovora dolazi iz tog cjenika. |
| Traženi završetak | Unesite datum završetka zadatka resursa podizvođača. | To će se upotrebljavati za prikazivanje upozorenja kada voditelj projekta crpi kapacitete za zahtjeve za resurse koji se javljaju nakon tog datuma. |
| Naručena količina | Unesite broj sati uloge koja se kupuje od dobavljača. | To će se upotrebljavati za prikazivanje upozorenja kada voditelj projekta prekomjerno crpi taj kapacitet za zahtjeve za resurse. |
| Grupa jedinica | Zadana vrijednost je **Grupa vremenskih jedinica**, koja se ne može promijeniti. | Nijedno|
| Jedinica | Zadana vrijednost za ovo polje osnovna je jedinica sata od stavke **Grupa vremenske jedinice**. Ovu vrijednost možete promijeniti kako biste kupili bilo koju jedinicu **Grupe jedinica vremena**, kao što je dan ili tjedan. | Kombinacija **Uloga** i **Jedinica** upotrebljavat će se kao zadana vrijednost ili će se izračunati za jediničnu cijenu retka podugovora. |
| Jedinična cijena | Zadana cijena jedinice upotrebljava kombinaciju **Uloga** i **Jedinica** iz cjenika projekta koji se primjenjuje za datum **Traženi početak** retka podugovora. | Kada je u mjerodavnom cjeniku projekta cijena postavljena u drugoj jedinici različitoj od jedinice na retku podugovora, sustav upotrebljava pretvaranje jedinice za izračun jedinične cijene. |
| Podzbroj |    Ovo je polje samo za čitanje koje se izračunava kao Količina x Jedinična cijena, ako se unesu vrijednosti i količine i jedinične cijene. Ako su količina, jedinična cijena ili oboje prazni, možete unijeti vrijednost u polje. | Nijedno|
| Porez na promet |   Unesite iznos poreza na prodaju. |Nijedno |
| Ukupni iznos | Ukupni iznos retka podugovora, uključujući porez. Ovo polje izračunava se kao međuzbroj + porez na promet.|Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
