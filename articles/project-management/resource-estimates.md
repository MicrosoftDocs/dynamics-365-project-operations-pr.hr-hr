---
title: Procjene resursa
description: U ovoj temi nalaze se informacije o načinu izračuna procjena resursa u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127342"
---
# <a name="resource-estimates"></a>Procjene resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Procjene resursa potječu iz vremenski razrađenog rada koji je definiran u strukturnoj analizi rada zajedno s mjerodavnom dimenzijama cijena. Uobičajeno, izračun je **cijena/sat za svaku ulogu x sati**. Vremenski razrađeni rad za svaki resurs pohranjen je u zapisu o dodjeli resursa. Cijene su pohranjene u unaprijed definiranom cjeniku. Pretvaranje jedinice primjenjuje se na temelju mjerodavnog cjenika.

![Procjene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Zadana cijena koštanja i valuta troška

Cijene koštanja zadane su u Organizacijskoj jedinici.

## <a name="default-bill-rate-and-sales-currency"></a>Zadane cijena naplate i valute prodaje

Prodajne cijene primjenjuju se za jedan posao. Hijerarhija prodajnog cjenika prema zadanim postavkama je sljedeća:

1. Organizacija
2. Klijent
3. Ponuda/ugovor


[!INCLUDE[footer-include](../includes/footer-banner.md)]