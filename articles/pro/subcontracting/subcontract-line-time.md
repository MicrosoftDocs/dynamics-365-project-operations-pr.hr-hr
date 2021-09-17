---
title: Redci podugovora za vrijeme
description: U ovoj temi objašnjava se način bilježenja redaka podugovora za vrijeme i kupnje vremena od dobavljača.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323857"
---
# <a name="subcontract-lines-for-time"></a>Redci podugovora za vrijeme

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Podugovor u aplikaciji Dynamics 365 Project Operations može imati redak podugovora za vrijeme. Redci podugovora za vrijeme omogućuju voditelju projekta da kupi vrijeme resursa dobavljača kako bi angažirao osoblje za projektne zadatke i zahtjeve za resurse.

Kako biste stvorili redak podugovora za vrijeme u aplikaciji Project Operations, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovori** i otvorite podugovor.
2. Na kartici **Retci podugovora** odaberite **Novi** kako biste stvorili novi redak podugovora.
3. Na stranici **Brzo stvaranje**, u polju **Klasa transakcije**, odaberite **Vrijeme**.
4. Unesite preostale podatke o polju, a zatim odaberite **Spremi**.

  U tablici u nastavku nalaze se podaci o poljima na stranicama **Redak podugovora** i **Brzo stvaranje**.

| **Polje** | **Opis** |
| --- | --- |
| Ime/naziv | Naziv retka podugovora. |
| Opis | Kratak opis usluga koje se kupuju na retku podugovora. | 
| Vrsta retka | Ovo je polje zadana vrijednost.  |
| Način naplate | Odaberite način naplate. Na temelju načina naplate referentnog retka podugovora, raspored faktura koji se temelji na kontrolnim točkama dostupan je za način naplate s fiksnom cijenom. |
| Razred transakcije | Ovo je polje zadana vrijednost koja označava upotrebljava li se redak podugovora za bilježenje kupnje vremena podizvođača. |
| Uloga | Uloga resursa podugovora čije se vrijeme kupuje. Uloga dodijeljena resursima podugovora određuje cijenu kupnje. |
| Zatraženi početak | Datum kada je potrebno da resursi podizvođača započnu rad. Traženi početak upotrebljava se za odabir cjenika projekta iz cjenika projekta priloženih podugovoru. Cijena uloge na retku podugovora tada se zadaje iz tog cjenika. |
| Zatraženi završetak | Datum kada završava zadatak resursa podizvođača. Ovaj se datum upotrebljava za prikaz upozorenja kada voditelj projekta crpi ovaj kapacitet za potrebe resursa koje se javljaju nakon tog datuma. |
| Naručena količina | Broj sati uloge koji se kupuju od dobavljača. Vrijednost se upotrebljava za prikaz upozorenja kada voditelj projekta prekomjerno crpi ovaj kapacitet za potrebe resursa. |
| Grupa jedinica | Ova vrijednost polja zadana je za grupu jedinica Vrijeme i ne može se promijeniti.  |
| Jedinica | Ovo je polje zadano za osnovnu jedinicu sata iz grupe jedinica za vrijeme. Ovu vrijednost možete promijeniti kako biste kupili bilo koju jedinicu grupe jedinica vremena, kao što je dan ili tjedan. Kombinacija Uloge i Jedinice upotrebljava se za izračun jedinične cijene retka podugovora. |
| Jedinična cijena | Jedinična cijena zadana je iz kombinacije Uloge i Jedinice iz cjenika projekta koja se primjenjuje na traženi datum početka retka podugovora. Kada je u mjerodavnom cjeniku projekta cijena postavljena u drugoj jedinici različitoj od jedinice na retku podugovora, sustav upotrebljava pretvaranje jedinice za izračun jedinične cijene. |
| Podzbroj | Ovo je polje samo za čitanje koje se automatski izračunava kao **Količina x Jedinična cijena**, ako su unesene vrijednosti i količine i jedinične cijene. Ako su količina, jedinična cijena ili oboje prazni, možete unijeti vrijednost u polje. |
| Porez na promet |  Unesite iznos poreza na prodaju. |
| Ukupni iznos | Ukupni iznos retka podugovora nakon poreza uključen je. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
