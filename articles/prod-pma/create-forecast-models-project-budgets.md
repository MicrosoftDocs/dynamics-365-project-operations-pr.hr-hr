---
title: Stvaranje modela predviđanja za proračune projekata
description: U ovoj temi opisan je način stvaranja modela predviđanja za proračunske iznose koji su preostali.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073524"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="5832f-103">Stvaranje modela predviđanja za proračune projekata</span><span class="sxs-lookup"><span data-stu-id="5832f-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5832f-104">U ovoj temi opisan je način stvaranja modela predviđanja za proračunske iznose koji su preostali.</span><span class="sxs-lookup"><span data-stu-id="5832f-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="5832f-105">U projektu koji je podložan kontroli proračuna upotrebljavaju se dvije vrste proračuna: izvorni i preostali.</span><span class="sxs-lookup"><span data-stu-id="5832f-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="5832f-106">Kada stvarate proračun projekta, morate navesti modele predviđanja izvornog i preostalog proračuna koji su stvoreni na stranici **Modeli predviđanja**.</span><span class="sxs-lookup"><span data-stu-id="5832f-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="5832f-107">Proračuni projekta na temelju navedenih modela stvaraju se kada napravite proračun projekta.</span><span class="sxs-lookup"><span data-stu-id="5832f-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="5832f-108">Model predviđanja koji se upotrebljava za kontrolu proračuna ne može imati podmodel niti se može upotrebljavati kao podmodel.</span><span class="sxs-lookup"><span data-stu-id="5832f-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="5832f-109">Odaberite **Upravljanje projektima i računovodstvo** > **Postavi** > **Predviđanje**  > **Modeli predviđanja**.</span><span class="sxs-lookup"><span data-stu-id="5832f-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="5832f-110">Odaberite **Novi** za stvaranje novog modela predviđanja, a zatim unesite ID broj modela i naziv za novi model.</span><span class="sxs-lookup"><span data-stu-id="5832f-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="5832f-111">Postavite mogućnost **Zaustavljeno** na **Da** kako biste spriječili svaku promjenu u redcima predviđanja za model predviđanja.</span><span class="sxs-lookup"><span data-stu-id="5832f-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="5832f-112">Ako redci predviđanja s kojima je model povezan trebaju generirati predviđanja novčanog tijeka u glavnoj knjizi, mogućnost **Uključi u predviđanja novčanog tijeka** postavite na **Da**.</span><span class="sxs-lookup"><span data-stu-id="5832f-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="5832f-113">Kako biste datum projekta upotrijebili kao datum fakture, mogućnost **Datum predviđanja fakture** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="5832f-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="5832f-114">U polju **Vrsta proračuna** odaberite jednu od sljedećih vrsta modela:</span><span class="sxs-lookup"><span data-stu-id="5832f-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="5832f-115">**Izvorni proračun** : Upotrijebite izvorne proračunske iznose koji su dodijeljeni tijekom stvaranja i odobravanja početnog proračuna.</span><span class="sxs-lookup"><span data-stu-id="5832f-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="5832f-116">**Preostali proračun** : Upotrijebite proračunske iznose koji su preostali tijekom trajanja projekta.</span><span class="sxs-lookup"><span data-stu-id="5832f-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="5832f-117">Salda u ovom modelu predviđanja smanjuju se stvarnim transakcijama, a povećavaju ili smanjuju revizijama proračuna.</span><span class="sxs-lookup"><span data-stu-id="5832f-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="5832f-118">**Preneseni** : Upotrijebite prenesene proračunske iznose za projekt.</span><span class="sxs-lookup"><span data-stu-id="5832f-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="5832f-119">Prijenos je neobvezan postupak koji se može pokrenuti za prijenos neupotrijebljenih proračunskih iznosa s jedne poslovne godine u drugu.</span><span class="sxs-lookup"><span data-stu-id="5832f-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="5832f-120">Prema potrebi, postavite sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="5832f-120">Set the following options as required:</span></span>

   - <span data-ttu-id="5832f-121">Omogućite **Datum predviđanja fakture** kako biste datum projekta upotrijebili kao datum fakture.</span><span class="sxs-lookup"><span data-stu-id="5832f-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="5832f-122">Omogućite **Predviđanje s pomoću WIP-a** za predviđanje koje se temelji na radu u tijeku (WIP), a zatim odaberite vrstu WIP-a.</span><span class="sxs-lookup"><span data-stu-id="5832f-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="5832f-123">Možete zadržati zadanu vrijednost **Vrsta proračuna** kao **Nijedna** ili unesite novu vrstu.</span><span class="sxs-lookup"><span data-stu-id="5832f-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="5832f-124">Vrsta proračuna ne može se mijenjati nakon što promijenite zapis.</span><span class="sxs-lookup"><span data-stu-id="5832f-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="5832f-125">Ako promijenite zadanu vrstu proračuna, sve ostale mogućnosti postat će nedostupne za ažuriranja i taj model predviđanja ne možete ponovno upotrijebiti.</span><span class="sxs-lookup"><span data-stu-id="5832f-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

