---
title: Zašto je u stvarnim vrijednostima cijene troškova zadana cijena nula?
description: Rješavanje problema zbog kojeg je u stvarnim vrijednostima cijene troškova zadana cijena 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122109"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Zašto je u stvarnim vrijednostima cijene troškova zadana cijena nula?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova često postavljena pitanja odnose na stvarne vrijednosti u slučajevima u kojima je razred transakcije postavljen na Trošak, a vrsta transakcije je Cijena.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Rješavanje problema u vezi sa stopama troškova u stvarnim vrijednostima cijene troškova

Idite na povezanu stavku troškova i provjerite je li ispunjeno polje za stavku troškova. Ako za izvornu stavku troškova nije bilo ispunjeno polje iznosa, utvrdili ste problem.
 
Da biste riješili taj problem, ponovno izradite stavku troškova s valjanim iznosom i odobrite je.
