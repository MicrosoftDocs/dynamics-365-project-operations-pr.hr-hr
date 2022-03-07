---
title: Upravljanje cjenikom dobavljača i nabave u aplikaciji Project Operations
description: U ovoj temi nalaze se informacije koje će vam pomoći pri stvaranju i održavanju podataka o dobavljačima i nabavnim cjenicima za podugovaranje.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994132"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Upravljanje cjenikom dobavljača i nabave u aplikaciji Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

## <a name="vendors-in-project-operations"></a>Dobavljači u aplikaciji Project Operations

Računi dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations imaju vrstu odnosa **Dobavljač** ili **Isporučitelj**. Možete odabrati samo zapis računa koji ima jednu od ovih vrsta odnosa kao dobavljača na podugovoru.

Možete povezati jedan ili više nabavnih cjenika sa zapisom o dobavljaču. Međutim, svaki nabavni cjenik koji je povezan sa zapisom o dobavljaču trebao bi imati različito razdoblje primjene. Project Operations ne podržava preklapanje razdoblja primjene nabavnih cjenika.

Prema zadanim postavkama, sljedeća polja i koncepti u zapisu o dobavljaču upotrebljavaju se za sve podugovore koji su stvoreni za dobavljača:

- Uvjeti plaćanja
- Kontakt za naplatu
- Primarni kontakt

    > [!NOTE]
    > Prema zadanim postavkama, primarni kontakt dobavljača upotrebljava se kao upravitelj računa dobavljača podugovora.

- Valuta
- Trenutačni nabavni cjenici

## <a name="purchase-price-lists-in-project-operations"></a>Nabavni cjenik u rješenju Project Operations

Cjenik u kojem je polje **Kontekst** postavljeno na **Kupnja** smatra se nabavnim cjenikom. Nabavni cjenici mogu se definirati tako da predstavljaju katalog nabavnih cijena za vrijeme, troškove i materijale. Nabavni cjenici nalikuju cjenicima troška i prodaje u rješenju Project Operations. Sljedeći se koncepti primjenjuju na nabavne cjenike na isti način na koji se primjenjuju na cjenike troška i prodajne cjenike:

- **Razdoblje primjene** – Nabavni cjenik ima razdoblje primjene. Razdoblje primjene prikazano je poljima datuma početka i datuma završetka na svakom cjeniku. Vrijeme između datuma početka i datuma završetka razdoblje je primjene.
- **Valuta** – Valuta u zaglavlju cjenika upotrebljava se kao valuta u kojoj su nabavne cijene izražene za rad, kategorije troškova i proizvode u katalogu.
- **Zadana jedinica vremena** – Zadana jedinica vremena izražava cijene rada za nabavu. Polje vremenske jedinice na cjeniku upotrebljava se samo za zadavanje zadane vrijednosti. Ta se vrijednost može promijeniti u pojedinačnim redcima cijena uloga.

Nabavni cjenici mogu se povezati sa zapisima o dobavljaču u skupine koje su poznate kao cjenici projekata. Ovi se cjenici upotrebljavaju za unos zadanih cijena na retke podugovora. Prema zadanim postavkama, kada je više nabavnih cjenika spojeno sa zapisom dobavljača, za podugovore koji su stvoreni za dobavljača upotrebljava se najnoviji cjenik. Samo se cjenici u kojima je polje **Kontekst** postavljeno na **Kupnja** mogu priložiti zapisima o dobavljaču.

### <a name="subcontract-specific-purchase-price-lists"></a>Nabavni cjenici specifični za podugovore

Nabavni cjenici mogu se također povezati s podugovorima u skupine koje su poznate kao cjenici projekata. Ovi se cjenici upotrebljavaju za unos zadanih cijena na retke podugovora. Prema zadanim postavkama, kada je više nabavnih cjenika priloženo podugovoru, svaki mora imati različito razdoblje primjene. Project Operations ne podržava nabavne cjenike kojima se preklapa razdoblje primjene. Samo se cjenici u kojima je polje **Kontekst** postavljeno na **Kupnja** mogu priložiti podugovorima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
