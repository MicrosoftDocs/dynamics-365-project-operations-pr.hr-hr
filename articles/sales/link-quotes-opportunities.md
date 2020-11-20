---
title: Stvaranje ponuda projekta iz prilika
description: U ovoj temi nalaze se informacije o stvaranju ponude projekta iz prilike.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d2cc35e3205332d2941bf17fb8c7d8c9d9f310c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118104"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="b65c1-103">Stvaranje ponuda projekta iz prilika</span><span class="sxs-lookup"><span data-stu-id="b65c1-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="b65c1-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b65c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b65c1-105">Ponude se mogu stvoriti iz prilika za projekt na sljedeće načine:</span><span class="sxs-lookup"><span data-stu-id="b65c1-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="b65c1-106">Iz kartice **Ponude** na stranici **Prilika za projekt**</span><span class="sxs-lookup"><span data-stu-id="b65c1-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="b65c1-107">Iz tijeka rada postupka prodaje prilike.</span><span class="sxs-lookup"><span data-stu-id="b65c1-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="b65c1-108">Ažuriranjem reference prilike na postojeću ponudu</span><span class="sxs-lookup"><span data-stu-id="b65c1-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="b65c1-109">Iz kartice Ponuda na stranici Prilika za projekt</span><span class="sxs-lookup"><span data-stu-id="b65c1-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="b65c1-110">Kako biste stvorili ponudu projekta iz prilike, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="b65c1-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="b65c1-111">Otvorite stranicu **Prilika za ponudu** i odaberite karticu **Ponude**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="b65c1-112">U podrešetki **Ponude** odaberite **+** kako biste stvorili novu ponudu projekta koja se temelji na prilici.</span><span class="sxs-lookup"><span data-stu-id="b65c1-112">On the **Quotes** subgrid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="b65c1-113">Svi redci prilike i povezani cjenici za projekt, kopiraju se iz prilike u novu ponudu.</span><span class="sxs-lookup"><span data-stu-id="b65c1-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="b65c1-114">Iz tijeka rada postupka prodaje prilike.</span><span class="sxs-lookup"><span data-stu-id="b65c1-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="b65c1-115">Kako biste stvorili ponudu iz tijeka rada postupka prodaje prilike, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="b65c1-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="b65c1-116">U tijeku postupka prodaje prilike otvorite Priliku.</span><span class="sxs-lookup"><span data-stu-id="b65c1-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="b65c1-117">Odaberite fazu **Kvalificiran**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="b65c1-118">Odaberite mogućnost **Sljedeći**, a zatim odaberite **+ Stvori** kako biste stvorili novu ponudu.</span><span class="sxs-lookup"><span data-stu-id="b65c1-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="b65c1-119">Većina podataka na kartici **Sažetak** za ovu novu ponudu zadani su iz prilike.</span><span class="sxs-lookup"><span data-stu-id="b65c1-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="b65c1-120">Unesite sve potrebne podatke koji nedostaju ili, ako je nužno, ažurirajte zadane vrijednosti na kartici **Sažetak**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="b65c1-121">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-121">Select **Save**.</span></span> <span data-ttu-id="b65c1-122">Nova je ponuda stvorena i povezana s prilikom.</span><span class="sxs-lookup"><span data-stu-id="b65c1-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="b65c1-123">Sada možete vidjeti podatke o ponudi na kartici **Ponude** stranice **Prilika**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="b65c1-124">Postupak prodaje prilike prelazi u sljedeću fazu, **Predloži**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="b65c1-125">Ažuriranjem reference prilike na postojeću ponudu</span><span class="sxs-lookup"><span data-stu-id="b65c1-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="b65c1-126">Postojeća ponuda može se povezati s prilikom.</span><span class="sxs-lookup"><span data-stu-id="b65c1-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="b65c1-127">Poduzmite sljedeće korake za ažuriranje podataka o prilici na postojećoj ponudi.</span><span class="sxs-lookup"><span data-stu-id="b65c1-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="b65c1-128">Otvorite stranicu **Ponuda** i odaberite karticu **Sažetak**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="b65c1-129">U polju **Prilika** odaberite priliku koju želite povezati s ponudom.</span><span class="sxs-lookup"><span data-stu-id="b65c1-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="b65c1-130">Ponudu možete vidjeti u rešetki **Ponude** od Prilike.</span><span class="sxs-lookup"><span data-stu-id="b65c1-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="b65c1-131">S pomoću postupka prodaje prilike, prilika se može premjestiti u sljedeću fazu, **Predloži**.</span><span class="sxs-lookup"><span data-stu-id="b65c1-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="b65c1-132">Kada premjestite priliku u ovu fazu, možete odabrati ovu ponudu s popisa ponuda povezanih s tom prilikom.</span><span class="sxs-lookup"><span data-stu-id="b65c1-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="b65c1-133">Odabir ove ponude označava da s njom napredujete.</span><span class="sxs-lookup"><span data-stu-id="b65c1-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="b65c1-134">Sve ostale ponude povezane s prilikom i dalje će biti dostupne i aktivne dok se jedna od njih ne prihvati.</span><span class="sxs-lookup"><span data-stu-id="b65c1-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="b65c1-135">Postupak prodaje možete vratiti u prethodnu fazu **Kvalificiraj** i odabrati još jednu ponudu s kojom ćete krenuti dalje.</span><span class="sxs-lookup"><span data-stu-id="b65c1-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
