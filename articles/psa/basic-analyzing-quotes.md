---
title: Analiza ponuda projekta
description: Ova tema pruža informacije o analizi ponuda projekta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073504"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="7d45a-103">Analiza ponuda projekta</span><span class="sxs-lookup"><span data-stu-id="7d45a-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7d45a-104">Dynamics 365 Project Service Automation analizira ponude projekta za procjenu profitabilnosti.</span><span class="sxs-lookup"><span data-stu-id="7d45a-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="7d45a-105">Također analizira koliko je dobro ponuda usklađena s očekivanjima klijenta o datumu isporuke ili datumu završetka i o proračunu.</span><span class="sxs-lookup"><span data-stu-id="7d45a-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="7d45a-106">Analiza profitabilnosti</span><span class="sxs-lookup"><span data-stu-id="7d45a-106">Profitability analysis</span></span>

<span data-ttu-id="7d45a-107">Project Service Automation analizira profitabilnost s pomoću bruto marže i prilagođene bruto marže.</span><span class="sxs-lookup"><span data-stu-id="7d45a-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="7d45a-108">Bruto marže izračunavaju se s pomoću sljedeće formule:</span><span class="sxs-lookup"><span data-stu-id="7d45a-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="7d45a-109">Prilagođena bruto marža izračunava se s pomoću sljedeće formule:</span><span class="sxs-lookup"><span data-stu-id="7d45a-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="7d45a-110">Ako vrijednosti za bruto maržu i prilagođenu bruto maržu znatno odstupaju, velik dio rada u ponudi klasificira se kao nenaplativ.</span><span class="sxs-lookup"><span data-stu-id="7d45a-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="7d45a-111">Analiza očekivanja klijenta</span><span class="sxs-lookup"><span data-stu-id="7d45a-111">Analysis of customer expectations</span></span>

<span data-ttu-id="7d45a-112">Možete analizirati ponude i generirati grafikone za očekivanja klijenta o rasporedu i proračunu ako unesete vrijednosti za sljedeća polja:</span><span class="sxs-lookup"><span data-stu-id="7d45a-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="7d45a-113">Polje **Traženi datum isporuke** u zaglavlju ponude.</span><span class="sxs-lookup"><span data-stu-id="7d45a-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="7d45a-114">Polje **Proračun klijenta** za svaki redak ponude (za retke koji se temelje na projektu i retke koji se temelje na proizvodu).</span><span class="sxs-lookup"><span data-stu-id="7d45a-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="7d45a-115">Analiza očekivanja klijenta o rasporedu provodi se uspoređivanjem najnovijeg datuma završetka detalja retka ponude s traženim datumom isporuke u svim recima ponude u ponudi.</span><span class="sxs-lookup"><span data-stu-id="7d45a-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="7d45a-116">Analiza očekivanja klijenta o proračunu provodi se uspoređivanjem zbroja ukupnog proračuna klijenta s navedenim iznosom u svim recima ponude.</span><span class="sxs-lookup"><span data-stu-id="7d45a-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
