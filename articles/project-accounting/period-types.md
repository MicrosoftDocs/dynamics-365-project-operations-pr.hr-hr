---
title: Vrste razdoblja
description: U ovoj temi nalaze se informacije o načinu postavljanja vrsta razdoblja za procjenu prihoda.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013477"
---
# <a name="period-types"></a><span data-ttu-id="00188-103">Vrste razdoblja</span><span class="sxs-lookup"><span data-stu-id="00188-103">Period types</span></span>

<span data-ttu-id="00188-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="00188-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="00188-105">Vrsta razdoblja definira koliko se često procjenjuje prihod od projekta.</span><span class="sxs-lookup"><span data-stu-id="00188-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="00188-106">U ovoj temi nalaze se informacije o načinu postavljanja vrsta razdoblja za procjenu prihoda.</span><span class="sxs-lookup"><span data-stu-id="00188-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="00188-107">Stvaranje vrsta razdoblja i rad s njima</span><span class="sxs-lookup"><span data-stu-id="00188-107">Create and work with period types</span></span>
<span data-ttu-id="00188-108">Kako biste stvorili vrste razdoblja i radili s njima, poduzmite sljedeće korake:</span><span class="sxs-lookup"><span data-stu-id="00188-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="00188-109">U vašem okruženju aplikacije Dynamics 365 Finance, idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Procjene** > **Vrste razdoblja**.</span><span class="sxs-lookup"><span data-stu-id="00188-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="00188-110">Kako biste stvorili novu vrstu razdoblja, odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="00188-110">Select **New** to create new period type.</span></span> <span data-ttu-id="00188-111">Unesite naziv i opis.</span><span class="sxs-lookup"><span data-stu-id="00188-111">Enter a name and description.</span></span>
3. <span data-ttu-id="00188-112">U polje **Učestalost** unesite vrijednost:</span><span class="sxs-lookup"><span data-stu-id="00188-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="00188-113">Ako odaberete **Tjedan**, **Dvotjedno**, **Polumjesečno**, **Mjesec**, **Dan**, **Kvartal** ili **Godina**, za generiranje razdoblja upotrebljavat će se kalendar.</span><span class="sxs-lookup"><span data-stu-id="00188-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="00188-114">Ako odaberete **Računovodstveno razdoblje**, računovodstvena razdoblja iz konfiguracije Glavne knjige upotrijebit će se za generiranje razdoblja.</span><span class="sxs-lookup"><span data-stu-id="00188-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="00188-115">Ako odaberete **Neograničeno**, možete odrediti prilagođena razdoblja.</span><span class="sxs-lookup"><span data-stu-id="00188-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="00188-116">Odaberite zapis vrste razdoblja, a zatim **Generiraj razdoblja** kako biste stvorili razdoblja za vrstu razdoblja.</span><span class="sxs-lookup"><span data-stu-id="00188-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="00188-117">Na temelju učestalosti razdoblja koje ste odabrali, možda ćete moći odrediti datum početka ili broj razdoblja koja treba generirati.</span><span class="sxs-lookup"><span data-stu-id="00188-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="00188-118">Za pregled generiranih razdoblja odaberite **Razdoblja**.</span><span class="sxs-lookup"><span data-stu-id="00188-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]