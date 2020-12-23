---
title: Stvaranje rješenja za prilagođene veličine za određivanje cijena
description: U ovoj temi nalaze se informacije o načinu stvaranja rješenja prilagođenih veličina za određivanje cijena.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513967"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="33209-103">Stvaranje rješenja za prilagođene veličine za određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="33209-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="33209-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="33209-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="33209-105">Sve promjene dimenzija za određivanje prilagođenih cijena tebale bi biti u zasebnom rješenju.</span><span class="sxs-lookup"><span data-stu-id="33209-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="33209-106">Ova značajna najbolja praksa omogućuje fleksibilnost za ažuriranje ili uklanjanje promjena po potrebi, pomaže u ponovnoj uporabi vašeg rada i olakšava prijenos tih promjena na drugu instancu.</span><span class="sxs-lookup"><span data-stu-id="33209-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="33209-107">Nakon što napravite potrebne promjene, izvezite ovo rješenje kao **Upravljano** rješenje i zatim ga uvezite u druge instance radi ponovne uporabe.</span><span class="sxs-lookup"><span data-stu-id="33209-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="33209-108">Stvaranje rješenja za prilagođene veličine za određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="33209-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="33209-109">Odaberite **Postavke** > **Rješenja**, a zatim odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="33209-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="33209-110">Imenujte rješenje, *<your organization name> veličine za određivanje cijene*.</span><span class="sxs-lookup"><span data-stu-id="33209-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="33209-111">Unesite preostale potrebne informacije, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="33209-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Stvaranje rješenja za prilagođene veličine za određivanje cijena](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="33209-113">Dodavanje svih potrebnih entiteta i povezanih komponenti u rješenje dimenzije za određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="33209-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="33209-114">Dodajte sljedeće entitete aplikacije Project Service u svoje rješenje za određivanje cijene kako biste napravili bitne promjene sheme u rješenju za određivanje cijene.</span><span class="sxs-lookup"><span data-stu-id="33209-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="33209-115">Nakon što dovršite ovaj postupak, entiteti će prepoznati nove veličine za određivanje cijene.</span><span class="sxs-lookup"><span data-stu-id="33209-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="33209-116">Odaberite **Postavke** > **Rješenja** i zatim dvaput kliknite **<*naziv svoje tvrtke ili ustanove*> veličine za određivanje cijene**.</span><span class="sxs-lookup"><span data-stu-id="33209-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="33209-117">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="33209-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="33209-118">U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:</span><span class="sxs-lookup"><span data-stu-id="33209-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="33209-119">**Stvarno**</span><span class="sxs-lookup"><span data-stu-id="33209-119">**Actual**</span></span>
   - <span data-ttu-id="33209-120">**Resurs koji je moguće rezervirati**</span><span class="sxs-lookup"><span data-stu-id="33209-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="33209-121">**Redak procjene**</span><span class="sxs-lookup"><span data-stu-id="33209-121">**Estimate Line**</span></span>
   - <span data-ttu-id="33209-122">**Projektni zadatak**</span><span class="sxs-lookup"><span data-stu-id="33209-122">**Project Task**</span></span>
   - <span data-ttu-id="33209-123">**Pojedinost retka fakture**</span><span class="sxs-lookup"><span data-stu-id="33209-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="33209-124">**Redak u dnevniku**</span><span class="sxs-lookup"><span data-stu-id="33209-124">**Journal Line**</span></span>
   - <span data-ttu-id="33209-125">**Pojedinost retka ugovora projekta**</span><span class="sxs-lookup"><span data-stu-id="33209-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="33209-126">**Član projektnog tima**</span><span class="sxs-lookup"><span data-stu-id="33209-126">**Project Team Member**</span></span>
   - <span data-ttu-id="33209-127">**Pojedinost retka ponude**</span><span class="sxs-lookup"><span data-stu-id="33209-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="33209-128">**Provizija cijene uloge**</span><span class="sxs-lookup"><span data-stu-id="33209-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="33209-129">**Cijena uloge**</span><span class="sxs-lookup"><span data-stu-id="33209-129">**Role Price**</span></span>
   - <span data-ttu-id="33209-130">**Unos vremena**</span><span class="sxs-lookup"><span data-stu-id="33209-130">**Time Entry**</span></span>
 
   ![Dodavanje postojećih entiteta s rješenjem prilagođene veličine za određivanje cijene](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="33209-132">Pregledajte komponente koje se dodaju i konačni popis sredstava entiteta za svaki entitet.</span><span class="sxs-lookup"><span data-stu-id="33209-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="33209-133">Uključite sve obrasce i prikaze za svaki odabrani entitet.</span><span class="sxs-lookup"><span data-stu-id="33209-133">Include all forms and views for each of the selected entities.</span></span>

  ![Dodani entiteti](./media/solution-component-selection.png)


5.  <span data-ttu-id="33209-135">Kada se od vas zatraži da uključite bilo koji ovisni entitet za odabrane entitete, odaberite **Nemoj uključivati potrebne komponente.**</span><span class="sxs-lookup"><span data-stu-id="33209-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Uključivanje ovisnih entiteta](./media/Do-not-include-required.png)
