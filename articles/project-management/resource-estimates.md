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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286509"
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