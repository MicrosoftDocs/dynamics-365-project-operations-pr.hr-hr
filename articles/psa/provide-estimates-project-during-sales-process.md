---
title: Pružanje procjene posla za projekt tijekom prodajnog procesa
description: Pružanje procjene posla za projekt tijekom prodajnog procesa u programu Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e9382127b2ce0b157d681fc77d67200ba9c5e59d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147959"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="fd760-103">Pružanje procjene posla za projekt tijekom prodajnog procesa (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fd760-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fd760-104">Tijekom prodajnog procesa možete izraditi procjenu prodaje na temelju redaka ponuda.</span><span class="sxs-lookup"><span data-stu-id="fd760-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="fd760-105">Mogućnosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u sustavu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] nude znanstveni i određeni način izrade procjene prodaje putem analize radnih stavki i pridruživanja relevantnih atributa koji pridonose procjeni za projekt u strukturnoj analizi rada.</span><span class="sxs-lookup"><span data-stu-id="fd760-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="fd760-106">Nakon što ste ostvarili prodaju, možete koristiti pridruženu strukturnu analizu rada u svom planu projekta i po potrebi ga podesiti za uspješni dovršetak projekta.</span><span class="sxs-lookup"><span data-stu-id="fd760-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="fd760-107">Povezivanje projekta s retkom ponude</span><span class="sxs-lookup"><span data-stu-id="fd760-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="fd760-108">Pri stvaranju retka ponude utemeljene na projektu, možete stvoriti novi projekt iz retka za ponudu.</span><span class="sxs-lookup"><span data-stu-id="fd760-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="fd760-109">Možete koristiti predloške projekta koji su ili prethodno konfigurirani standardni planovi projekta i financijske procjene uobičajene za vašu organizaciju ili kopija plana projekta i procjene iz prošlog projekta.</span><span class="sxs-lookup"><span data-stu-id="fd760-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="fd760-110">Kada stvorite projekt, odabir predloška projekta daje osnovu za fino podešavanje plana projekta, procjena te zahtjeva uloge.</span><span class="sxs-lookup"><span data-stu-id="fd760-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="fd760-111">Stvaranjem projekta iz ponude, projekt se automatski pridružuje retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fd760-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="fd760-112">Komponente procjene projekta</span><span class="sxs-lookup"><span data-stu-id="fd760-112">Project estimate components</span></span>  
 <span data-ttu-id="fd760-113">Strukturna analiza rada u projektu omogućuje način raščlambe posla na zadatke, održavanje hijerarhije zadataka i dodjelu procjene truda potrebnog za dovršetak svakog zadatka.</span><span class="sxs-lookup"><span data-stu-id="fd760-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="fd760-114">Također možete pridružiti uloge zadatku da biste naznačili procjenu vrste resursa potrebnih za dovršavanje zadatka i raspored.</span><span class="sxs-lookup"><span data-stu-id="fd760-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="fd760-115">Strukturna analiza rada će vam olakšati određivanje procjene truda i rasporeda.</span><span class="sxs-lookup"><span data-stu-id="fd760-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="fd760-116">Prema zadanim postavkama, projekt koristi zadane cjenike koje ste definirali ranije.</span><span class="sxs-lookup"><span data-stu-id="fd760-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="fd760-117">Trošak i prodajne cijene definirane u cjenicima pomažu u određivanju financijske procjene za analizu rada projekta.</span><span class="sxs-lookup"><span data-stu-id="fd760-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="fd760-118">Ako je vaš projekt povezan s ponudom, a ponuda sadrži cjenik koji je različit od zadanog, za financijsku procjenu koristi se cjenik ponude.</span><span class="sxs-lookup"><span data-stu-id="fd760-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="fd760-119">Uvoz procjene iz projekta u ponudu</span><span class="sxs-lookup"><span data-stu-id="fd760-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="fd760-120">Kada imate procjenu projekta u projektu, tu procjenu možete uvesti u redak ponude:</span><span class="sxs-lookup"><span data-stu-id="fd760-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="fd760-121">U **Detalji retka ponude** kliknite **Uvezi iz procjene**.</span><span class="sxs-lookup"><span data-stu-id="fd760-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="fd760-122">Odaberite želite li uvesti procjenu projekta sažetu prema vrsti transakcije, ulozi ili razini čvora strukturne analize rada.</span><span class="sxs-lookup"><span data-stu-id="fd760-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fd760-123">Pogledajte također</span><span class="sxs-lookup"><span data-stu-id="fd760-123">See Also</span></span>  
 [<span data-ttu-id="fd760-124">Vodič voditelja projekta</span><span class="sxs-lookup"><span data-stu-id="fd760-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
