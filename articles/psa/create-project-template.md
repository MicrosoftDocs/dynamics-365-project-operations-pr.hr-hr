---
title: Izradi predložak projekta
description: Kako izraditi predložak projekta u programu Project Service
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
ms.openlocfilehash: 78d25183aad8d86593d3f2582295db59eb84cf14
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133179"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="12d21-103">Izradi predložak projekta (Project Service)</span><span class="sxs-lookup"><span data-stu-id="12d21-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="12d21-104">Predlošci projekta štede vrijeme ako se vaše poduzeće redovito prijavljuje na slične vrste projekata.</span><span class="sxs-lookup"><span data-stu-id="12d21-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="12d21-105">Nude standardni skup uloga i procijenjenih sati za vrstu projekta.</span><span class="sxs-lookup"><span data-stu-id="12d21-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="12d21-106">Upravitelji računa i projekta mogu izrađivati projekte koji se temelje na predlošku projekta ili mogu kopirati predložak i izraditi vlastiti.</span><span class="sxs-lookup"><span data-stu-id="12d21-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="12d21-107">Komponente predloška projekta</span><span class="sxs-lookup"><span data-stu-id="12d21-107">Components of project template</span></span>
 <span data-ttu-id="12d21-108">Predložak projekta sastoji se od tri komponente:</span><span class="sxs-lookup"><span data-stu-id="12d21-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="12d21-109">**Strukturna analiza rada**: strukturna analiza rada u predlošku projekta ima isti skup elemenata kao projekt.</span><span class="sxs-lookup"><span data-stu-id="12d21-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="12d21-110">Možete izraditi hijerarhiju zadataka, povezati uloge sa zadacima, odrediti atribute rasporeda, postaviti ovisnosti i prikazati sve podatake u Ganttovom dijagramu.</span><span class="sxs-lookup"><span data-stu-id="12d21-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="12d21-111">Strukturna analiza rada u predlošcima projekta podržava načine zadatka za svaki zadatak.</span><span class="sxs-lookup"><span data-stu-id="12d21-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="12d21-112">Nema razlike između predloška projekta i projekta prilikom izrade radnog rasporeda.</span><span class="sxs-lookup"><span data-stu-id="12d21-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="12d21-113">**Procjene projekta**: procjene projekta u predlošcima funkcioniraju na isti način kao i u projektima, osim što su cjenici za zadane cijene i troškove uvijek zadani cjenici troškova i prodaje definirani u parametrima sustava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="12d21-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="12d21-114">Ostale funkcije iste su kao u projektu.</span><span class="sxs-lookup"><span data-stu-id="12d21-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="12d21-115">**Formiranje tima projekta**: prilikom formiranja tima projekta za predložak projekta, nije moguće rezervirati imenovani resurs u predlošku.</span><span class="sxs-lookup"><span data-stu-id="12d21-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="12d21-116">Možete koristiti **Generiraj tim projekta** u strukturnoj analizi rada za generiranje skupa generičkih resursa.</span><span class="sxs-lookup"><span data-stu-id="12d21-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="12d21-117">Također možete navesti potrebne vještine i stručnosti za generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="12d21-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="12d21-118">Generički resurs ne možete zamijeniti s resursom koji je moguće rezervirati u predlošku projekta.</span><span class="sxs-lookup"><span data-stu-id="12d21-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="12d21-119">Izradi projekt iz predloška</span><span class="sxs-lookup"><span data-stu-id="12d21-119">Create a project from a template</span></span>  
 <span data-ttu-id="12d21-120">Projekt iz predloška možete izraditi na sljedeće načine:</span><span class="sxs-lookup"><span data-stu-id="12d21-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="12d21-121">Kada izrađujete projekt iz ponude, možete odabrati predložak projekta u obrascu za brzu izradu projekta.</span><span class="sxs-lookup"><span data-stu-id="12d21-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="12d21-122">Prilikom izrade projekta klikom na **Novi projekt**, obrazac projekta prikazuje se prije nego što spremite zapis.</span><span class="sxs-lookup"><span data-stu-id="12d21-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="12d21-123">Ovdje možete kliknuti polje **Odaberi predložak** da biste odabrali s popisa unaprijed definiranih predložaka projekta u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="12d21-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="12d21-124">Kliknite **Izradi projekt iz predloška** na stranici **Predložak projekta** da biste izradili projekt iz predloška.</span><span class="sxs-lookup"><span data-stu-id="12d21-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="12d21-125">Kopiranje komponenti predloška u projekt:</span><span class="sxs-lookup"><span data-stu-id="12d21-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="12d21-126">Kada kopirate komponente predloška u projekt, postoji nekoliko stvari o kojima biste trebali znati više.</span><span class="sxs-lookup"><span data-stu-id="12d21-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="12d21-127">**Kopiranje strukturne analize rada**: kada kopirate strukturnu analizu rada iz predloška projekta, ako projekt ima kalendar projekta različit od predloška, radno vrijeme iz kalendara projekta primijenit će se na raspored zadataka.</span><span class="sxs-lookup"><span data-stu-id="12d21-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="12d21-128">To će prilagoditi raspored kalendaru projekta.</span><span class="sxs-lookup"><span data-stu-id="12d21-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="12d21-129">Isto tako, prvi zadatak strukturne analize rada preuzima datum početka projekta, tako da se ostatak rasporeda hijerarhije zadataka ažurira na temelju trajanja i ovisnosti navedenih u strukturnoj analizi rada predloška.</span><span class="sxs-lookup"><span data-stu-id="12d21-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="12d21-130">**Kopiranje procjene projekta**: prilikom kopiranja redaka procjene projekta, cjenici se ažuriraju na temelju jedinice s vlasništvom projekta za cjenik troškova i klijenta za cjenik prodaje.</span><span class="sxs-lookup"><span data-stu-id="12d21-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="12d21-131">Jedinična cijena i prodajne cijene određuju se na temelju ovih cjenika na projektima koji su povezani s entitetom prodaje.</span><span class="sxs-lookup"><span data-stu-id="12d21-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="12d21-132">**Kopiranje tima projekta**: kada kopirate tim projekta iz predloška u projekt, generički resursi kopiraju se zajedno s vještinama i stručnostima definiranima u predlošku.</span><span class="sxs-lookup"><span data-stu-id="12d21-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="12d21-133">Dodjele generičkih resursa također se zadržavaju kao predložak projekta.</span><span class="sxs-lookup"><span data-stu-id="12d21-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="12d21-134">Također pogledajte</span><span class="sxs-lookup"><span data-stu-id="12d21-134">See Also</span></span>  
 [<span data-ttu-id="12d21-135">Vodič za voditelja projekta</span><span class="sxs-lookup"><span data-stu-id="12d21-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
