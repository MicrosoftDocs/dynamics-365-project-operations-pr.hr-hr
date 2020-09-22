---
title: Zašto je u stvarnim vrijednostima cijene troškova zadana cijena nula?
description: Rješavanje problema zbog kojeg je u stvarnim vrijednostima cijene troškova zadana cijena 0.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750117"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Zašto je u stvarnim vrijednostima cijene troškova zadana cijena nula?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova često postavljena pitanja odnose na stvarne vrijednosti u slučajevima u kojima je razred transakcije postavljen na Trošak, a vrsta transakcije je Cijena.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Rješavanje problema u vezi sa stopama troškova u stvarnim vrijednostima cijene troškova

Idite na povezanu stavku troškova i provjerite je li ispunjeno polje za stavku troškova. Ako za izvornu stavku troškova nije bilo ispunjeno polje iznosa, utvrdili ste problem.
 
Da biste riješili taj problem, ponovno izradite stavku troškova s valjanim iznosom i odobrite je.
