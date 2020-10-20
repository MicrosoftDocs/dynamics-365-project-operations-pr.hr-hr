---
title: Stvaranje ponuda projekta iz prilika
description: U ovoj temi nalaze se informacije o stvaranju ponude projekta iz prilike.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898523"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="45270-103">Stvaranje ponuda projekta iz prilika</span><span class="sxs-lookup"><span data-stu-id="45270-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="45270-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="45270-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="45270-105">Ponude se mogu stvoriti iz prilika za projekt na sljedeće načine:</span><span class="sxs-lookup"><span data-stu-id="45270-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="45270-106">Iz kartice **Ponude** na stranici **Prilika za projekt**</span><span class="sxs-lookup"><span data-stu-id="45270-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="45270-107">Iz tijeka rada postupka prodaje prilike.</span><span class="sxs-lookup"><span data-stu-id="45270-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="45270-108">Ažuriranjem reference prilike na postojeću ponudu</span><span class="sxs-lookup"><span data-stu-id="45270-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="45270-109">Iz kartice Ponuda na stranici Prilika za projekt</span><span class="sxs-lookup"><span data-stu-id="45270-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="45270-110">Kako biste stvorili ponudu projekta iz prilike, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="45270-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="45270-111">Otvorite stranicu **Prilika za ponudu** i odaberite karticu **Ponude**.</span><span class="sxs-lookup"><span data-stu-id="45270-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="45270-112">Na podrešetki **Ponude** odaberite **+** kako biste stvorili novu ponudu projekta na temelju prilike.</span><span class="sxs-lookup"><span data-stu-id="45270-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="45270-113">Svi redci prilike i povezani cjenici za projekt, kopiraju se iz prilike u novu ponudu.</span><span class="sxs-lookup"><span data-stu-id="45270-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="45270-114">Iz tijeka rada postupka prodaje prilike.</span><span class="sxs-lookup"><span data-stu-id="45270-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="45270-115">Kako biste stvorili ponudu iz tijeka rada postupka prodaje prilike, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="45270-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="45270-116">U tijeku postupka prodaje prilike otvorite Priliku.</span><span class="sxs-lookup"><span data-stu-id="45270-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="45270-117">Odaberite fazu **Kvalificiran**.</span><span class="sxs-lookup"><span data-stu-id="45270-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="45270-118">Odaberite mogućnost **Sljedeći**, a zatim odaberite **+ Stvori** kako biste stvorili novu ponudu.</span><span class="sxs-lookup"><span data-stu-id="45270-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="45270-119">Većina podataka na kartici **Sažetak** za ovu novu ponudu zadani su iz prilike.</span><span class="sxs-lookup"><span data-stu-id="45270-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="45270-120">Unesite sve potrebne podatke koji nedostaju ili, ako je nužno, ažurirajte zadane vrijednosti na kartici **Sažetak**.</span><span class="sxs-lookup"><span data-stu-id="45270-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="45270-121">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="45270-121">Select **Save**.</span></span> <span data-ttu-id="45270-122">Nova je ponuda stvorena i povezana s prilikom.</span><span class="sxs-lookup"><span data-stu-id="45270-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="45270-123">Sada možete vidjeti podatke o ponudi na kartici **Ponude** stranice **Prilika**.</span><span class="sxs-lookup"><span data-stu-id="45270-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="45270-124">Postupak prodaje prilike prelazi u sljedeću fazu, **Predloži**.</span><span class="sxs-lookup"><span data-stu-id="45270-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="45270-125">Ažuriranjem reference prilike na postojeću ponudu</span><span class="sxs-lookup"><span data-stu-id="45270-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="45270-126">Postojeća ponuda može se povezati s prilikom.</span><span class="sxs-lookup"><span data-stu-id="45270-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="45270-127">Poduzmite sljedeće korake za ažuriranje podataka o prilici na postojećoj ponudi.</span><span class="sxs-lookup"><span data-stu-id="45270-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="45270-128">Otvorite stranicu **Ponuda** i odaberite karticu **Sažetak**.</span><span class="sxs-lookup"><span data-stu-id="45270-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="45270-129">U polju **Prilika** odaberite priliku koju želite povezati s ponudom.</span><span class="sxs-lookup"><span data-stu-id="45270-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="45270-130">Ponudu možete vidjeti u rešetki **Ponude** od Prilike.</span><span class="sxs-lookup"><span data-stu-id="45270-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="45270-131">S pomoću postupka prodaje prilike, prilika se može premjestiti u sljedeću fazu, **Predloži**.</span><span class="sxs-lookup"><span data-stu-id="45270-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="45270-132">Kada premjestite priliku u ovu fazu, možete odabrati ovu ponudu s popisa ponuda povezanih s tom prilikom.</span><span class="sxs-lookup"><span data-stu-id="45270-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="45270-133">Odabir ove ponude označava da s njom napredujete.</span><span class="sxs-lookup"><span data-stu-id="45270-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="45270-134">Sve ostale ponude povezane s prilikom i dalje će biti dostupne i aktivne dok se jedna od njih ne prihvati.</span><span class="sxs-lookup"><span data-stu-id="45270-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="45270-135">Postupak prodaje možete vratiti u prethodnu fazu **Kvalificiraj** i odabrati još jednu ponudu s kojom ćete krenuti dalje.</span><span class="sxs-lookup"><span data-stu-id="45270-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
