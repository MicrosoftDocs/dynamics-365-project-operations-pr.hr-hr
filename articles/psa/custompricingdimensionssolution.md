---
title: Stvaranje prilagođenih rješenja za dimenzije određivanja cijena
description: U ovoj se temi objašnjava način stvaranja prilagođenog rješenja tijekom stvaranja dimenzija za prilagođeno određivanje cijena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073397"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="3d680-103">Stvaranje prilagođenih rješenja za dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="3d680-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d680-104">Sve promjene dimenzija za određivanje prilagođenih cijena tebale bi biti u zasebnom rješenju.</span><span class="sxs-lookup"><span data-stu-id="3d680-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="3d680-105">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu.</span><span class="sxs-lookup"><span data-stu-id="3d680-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="3d680-106">Nakon što izvršite sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="3d680-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="3d680-107">Odaberite **Postavke** > **Rješenja** , a zatim odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="3d680-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="3d680-108">Rješenju dodijelite naziv **\<your organization name> dimenzije za određivanje cijena** , unesite preostale potrebne podatke, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="3d680-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Izrada prilagođenog rješenja za dimenzije određivanja cijena](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="3d680-110">Dodavanje svih potrebnih entiteta i povezanih komponenti u rješenje dimenzije za određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="3d680-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="3d680-111">Morat ćete dodati sljedeće entitete programa Project Service u svoje rješenje za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="3d680-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="3d680-112">Dovršite ove korake u tom postupku kako biste izvršili neke važne promjene sheme u rješenju određivanja cijena kako bi entiteti prepoznali nove dimenzije određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="3d680-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="3d680-113">Odaberite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="3d680-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3d680-114">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="3d680-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="3d680-115">U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:</span><span class="sxs-lookup"><span data-stu-id="3d680-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="3d680-116">Stvarno</span><span class="sxs-lookup"><span data-stu-id="3d680-116">Actual</span></span>
- <span data-ttu-id="3d680-117">Resurs koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="3d680-117">Bookable Resource</span></span>
- <span data-ttu-id="3d680-118">Redak procjene</span><span class="sxs-lookup"><span data-stu-id="3d680-118">Estimate Line</span></span>
- <span data-ttu-id="3d680-119">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="3d680-119">Project Task</span></span>
- <span data-ttu-id="3d680-120">Pojedinost retka fakture</span><span class="sxs-lookup"><span data-stu-id="3d680-120">Invoice Line Detail</span></span>
- <span data-ttu-id="3d680-121">Redak u dnevniku</span><span class="sxs-lookup"><span data-stu-id="3d680-121">Journal Line</span></span>
- <span data-ttu-id="3d680-122">Pojedinost retka ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="3d680-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="3d680-123">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="3d680-123">Project Team Member</span></span>
- <span data-ttu-id="3d680-124">Pojedinost retka ponude</span><span class="sxs-lookup"><span data-stu-id="3d680-124">Quote Line Detail</span></span>
- <span data-ttu-id="3d680-125">Provizija cijene uloge</span><span class="sxs-lookup"><span data-stu-id="3d680-125">Role Price Markup</span></span>
- <span data-ttu-id="3d680-126">Cijena uloge</span><span class="sxs-lookup"><span data-stu-id="3d680-126">Role Price</span></span> 
- <span data-ttu-id="3d680-127">Unos vremena</span><span class="sxs-lookup"><span data-stu-id="3d680-127">Time Entry</span></span> 

> ![Dodaj postojeće entitete u rješenje dimenzija određivanja cijena](media/Existing-entities-to-PD-solution.png)

> ![Odaberi komponente rješenja](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="3d680-130">Obavezno uključite sve obrasce i prikaze za svaki odabrani entitet.</span><span class="sxs-lookup"><span data-stu-id="3d680-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="3d680-131">Kada se od vas zatraži da uključite sve ovisne entitete za odabrane entitete, odaberite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="3d680-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Ne, ne želim dodati sve povezane komponente.](media/Do-not-include-required.png)


