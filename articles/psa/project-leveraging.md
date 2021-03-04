---
title: Procjene prodaje i projekti
description: Ova tema pruža informacije o tome kako iskoristiti prednosti rasporeda i procjena u postupku prodaje.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148364"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="48461-103">Procjene prodaje i projekti</span><span class="sxs-lookup"><span data-stu-id="48461-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="48461-104">Tijekom prodajnog postupka možete stvoriti procjenu prodaje povezivanjem projekta s prodajnom ponudom.</span><span class="sxs-lookup"><span data-stu-id="48461-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="48461-105">Na taj način moguća je deterministička procjena tijekom prodajnog postupka kako biste iskoristili prednosti mogućnosti zakazivanja i procjene projekta.</span><span class="sxs-lookup"><span data-stu-id="48461-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="48461-106">Ako se ostvari prodaja, raspored koji je korišten za svrhe procjene prodaje može se koristiti kao temelj za daljnje preciziranje plana projekta.</span><span class="sxs-lookup"><span data-stu-id="48461-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="48461-107">Povezivanje projekta s retkom ponude</span><span class="sxs-lookup"><span data-stu-id="48461-107">Linking a project to a quote line</span></span>

<span data-ttu-id="48461-108">Kada stvorite redak ponude temeljen na projektu, možete stvoriti novi projekt ili povezati postojeći projekt na stranici **Redak ponude**.</span><span class="sxs-lookup"><span data-stu-id="48461-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Obrazac retka ponude](media/project-8.png)
 
<span data-ttu-id="48461-110">Kada stvorite novi projekt na temelju pojedinosti retka ponude, možete iskoristiti prednosti predložaka projekta.</span><span class="sxs-lookup"><span data-stu-id="48461-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="48461-111">Predlošci projekata modeli su projekata koji predstavljaju standardne projektne planove i financijske procjene koje su uobičajene u tvrtki li ustanovi.</span><span class="sxs-lookup"><span data-stu-id="48461-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="48461-112">Također mogu predstavljati kopije projektnih planova i procjena iz prethodnih projekata.</span><span class="sxs-lookup"><span data-stu-id="48461-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalji retka ponude](media/project-9.png)
  
<span data-ttu-id="48461-114">Kada stvorite projekt na temelju ponude, projekt se automatski povezuje s retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="48461-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="48461-115">Komponente procjena u projektu</span><span class="sxs-lookup"><span data-stu-id="48461-115">Components of estimates in a project</span></span>

<span data-ttu-id="48461-116">Raspored omogućuje dijeljenje posla u zadatke, održavanje hijerarhije zadataka, određivanje resursa potrebnih za dovršetak zadatka i dodjelu procjene rada potrebnog za dovršetak zadatka.</span><span class="sxs-lookup"><span data-stu-id="48461-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="48461-117">Procjene rada i rasporeda možete definirati pomoću polja na kartici **Raspored** na stranici **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="48461-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="48461-118">Budući da je cjenik povezan s projektom, financijske procjene izračunavaju se pomoću cijena troškova i prodajnih cijena definiranih u cjeniku.</span><span class="sxs-lookup"><span data-stu-id="48461-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="48461-119">Uvoz procjena iz projekta u ponudu</span><span class="sxs-lookup"><span data-stu-id="48461-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="48461-120">Nakon što definirate procjene projekta, možete ih uvesti u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="48461-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="48461-121">Na stranici **Pojedinosti retka ponude** odaberite **Uvezi iz procjene** na vrpci da biste saželi procjene projekta po vrsti transakcije, ulozi ili razini zadatka.</span><span class="sxs-lookup"><span data-stu-id="48461-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
