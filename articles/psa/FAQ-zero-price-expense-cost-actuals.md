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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="386cd-103">Zašto je u stvarnim vrijednostima cijene troškova zadana cijena nula?</span><span class="sxs-lookup"><span data-stu-id="386cd-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="386cd-104">Ova često postavljena pitanja odnose na stvarne vrijednosti u slučajevima u kojima je razred transakcije postavljen na Trošak, a vrsta transakcije je Cijena.</span><span class="sxs-lookup"><span data-stu-id="386cd-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="386cd-105">Rješavanje problema u vezi sa stopama troškova u stvarnim vrijednostima cijene troškova</span><span class="sxs-lookup"><span data-stu-id="386cd-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="386cd-106">Idite na povezanu stavku troškova i provjerite je li ispunjeno polje za stavku troškova.</span><span class="sxs-lookup"><span data-stu-id="386cd-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="386cd-107">Ako za izvornu stavku troškova nije bilo ispunjeno polje iznosa, utvrdili ste problem.</span><span class="sxs-lookup"><span data-stu-id="386cd-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="386cd-108">Da biste riješili taj problem, ponovno izradite stavku troškova s valjanim iznosom i odobrite je.</span><span class="sxs-lookup"><span data-stu-id="386cd-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
