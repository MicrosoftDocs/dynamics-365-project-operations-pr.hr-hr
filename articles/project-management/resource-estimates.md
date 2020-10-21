---
title: Procjene resursa
description: U ovoj temi nalaze se informacije o načinu izračuna procjena resursa u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928550"
---
# <a name="resource-estimates"></a>Procjene resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Procjene resursa potječu iz vremenski razrađenog rada koji je definiran u strukturnoj analizi rada zajedno s mjerodavnom dimenzijama cijena. Uobičajeno, izračun je **cijena/sat za svaku ulogu x sati**. Vremenski razrađeni rad za svaki resurs pohranjen je u zapisu o dodjeli resursa. Cijene su pohranjene u unaprijed definiranom cjeniku. Pretvaranje jedinice primjenjuje se na temelju mjerodavnog cjenika.

![Procjene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Zadana cijena koštanja i valuta troška

Cijene koštanja zadane su u Organizacijskoj jedinici.

## <a name="default-bill-rate-and-sales-currency"></a>Zadane cijena naplate i valute prodaje

Prodajne cijene primjenjuju se za jedan posao. Hijerarhija prodajnog cjenika prema zadanim postavkama je sljedeća:

1. Organizacija
2. Klijent
3. Ponuda/ugovor
