---
title: Predlošci projekta
description: Ova tema pruža informacije o tome kako upotrebljavati predloške projekta za brzo postavljanje projekta.
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123000"
---
# <a name="project-templates"></a><span data-ttu-id="415aa-103">Predlošci projekta</span><span class="sxs-lookup"><span data-stu-id="415aa-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="415aa-104">Predložak projekta jest unaprijed definirani okvir koji vam omogućuje da brzo i jednostavno započnete projekt.</span><span class="sxs-lookup"><span data-stu-id="415aa-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="415aa-105">Možete koristiti unaprijed definirani predložak za stvaranje novog projekta jednim klikom.</span><span class="sxs-lookup"><span data-stu-id="415aa-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="415aa-106">Što se tiče projekata, morate definirati preduvjete za predloške projekata.</span><span class="sxs-lookup"><span data-stu-id="415aa-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="415aa-107">Morate definirati kalendar projekta za svaki predložak projekta, a uloge i cjenici moraju biti unaprijed definirani u tvrtki ili ustanovi, tako da komponente predloška sadrže korisne podatke.</span><span class="sxs-lookup"><span data-stu-id="415aa-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="415aa-108">Predložak projekta sastoji se od tri komponente: rasporeda, procjena projekata i članova projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="415aa-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="415aa-109">Raspored</span><span class="sxs-lookup"><span data-stu-id="415aa-109">Schedule</span></span>

<span data-ttu-id="415aa-110">Raspored u predlošku projekta ima isti skup elemenata kao raspored u projektu.</span><span class="sxs-lookup"><span data-stu-id="415aa-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="415aa-111">Možete stvoriti hijerarhiju zadataka, povezati uloge sa zadacima, odrediti raspored atributa i postaviti ovisnosti.</span><span class="sxs-lookup"><span data-stu-id="415aa-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="415aa-112">Raspored u predlošku projekta također podržava načine zadatka za svaki zadatak.</span><span class="sxs-lookup"><span data-stu-id="415aa-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="415aa-113">Stoga podržava mehanizam zakazivanja.</span><span class="sxs-lookup"><span data-stu-id="415aa-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="415aa-114">Kalendar projekta morate povezati s projektom.</span><span class="sxs-lookup"><span data-stu-id="415aa-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="415aa-115">Prilikom stvaranja radnog rasporeda nema razlike između predloška projekta i projekta.</span><span class="sxs-lookup"><span data-stu-id="415aa-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="415aa-116">Procjene projekta</span><span class="sxs-lookup"><span data-stu-id="415aa-116">Project estimates</span></span>

<span data-ttu-id="415aa-117">Procjene projekta u predlošku projekta funkcioniraju na isti način kao procjene projekta u projektu.</span><span class="sxs-lookup"><span data-stu-id="415aa-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="415aa-118">Međutim, troškovi i prodajne cijene dohvaćaju se iz zadanih troškova i prodajnih cjenika koji su definirani u parametrima.</span><span class="sxs-lookup"><span data-stu-id="415aa-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="415aa-119">Stvaranje projekta na temelju predloška</span><span class="sxs-lookup"><span data-stu-id="415aa-119">Creating a project from a template</span></span>
 
<span data-ttu-id="415aa-120">Postoji nekoliko načina stvaranja projekta na temelju predloška projekta:</span><span class="sxs-lookup"><span data-stu-id="415aa-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="415aa-121">Kada stvorite projekt na temelju ponude, možete odabrati predložak projekta u dijaloškom okviru **Brza izrada: projekt**.</span><span class="sxs-lookup"><span data-stu-id="415aa-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dijaloški okvir Brza izrada: projekt](media/project-11.png)

- <span data-ttu-id="415aa-123">Prilikom stvaranja projekta odabirom mogućnosti **Novi projekt** stranica **Projekt** prikazat će se prije spremanja zapisa.</span><span class="sxs-lookup"><span data-stu-id="415aa-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="415aa-124">U polju **Odaberi predložak** odaberite jedan od unaprijed definiranih predložaka projekta u tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="415aa-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="415aa-125">Upotrijebite mogućnost **Stvori projekt na temelju predloška** na stranici **Entitet predloška**.</span><span class="sxs-lookup"><span data-stu-id="415aa-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="415aa-126">Kopiranje komponenata predloška u projekt</span><span class="sxs-lookup"><span data-stu-id="415aa-126">Copying components of template to project</span></span>

<span data-ttu-id="415aa-127">Kada kopirate komponente predloška projekta u projekt, može doći do nekoliko nadjačavanja, ovisno o postavkama u projektu.</span><span class="sxs-lookup"><span data-stu-id="415aa-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="415aa-128">Kopiranje rasporeda</span><span class="sxs-lookup"><span data-stu-id="415aa-128">Copying the schedule</span></span>

<span data-ttu-id="415aa-129">Kada kopirate raspored iz predloška projekta, ako projekt ima kalendar projekta različit od predloška, radno vrijeme iz kalendara projekta primijenit će se na raspored zadataka.</span><span class="sxs-lookup"><span data-stu-id="415aa-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="415aa-130">Na taj način raspored se prilagođava u skladu s kalendarom projekta.</span><span class="sxs-lookup"><span data-stu-id="415aa-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="415aa-131">Isto tako, prvi zadatak u rasporedu preuzima datum početka projekta, a raspored ostatka hijerarhije ažurira na temelju trajanja i ovisnosti navedenih u predlošku.</span><span class="sxs-lookup"><span data-stu-id="415aa-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="415aa-132">Kopiranje procjena projekta</span><span class="sxs-lookup"><span data-stu-id="415aa-132">Copying project estimates</span></span> 

<span data-ttu-id="415aa-133">Prilikom kopiranja u retke procjene projekta cjenici se ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="415aa-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="415aa-134">Za cjenik s cijenama koštanja ta se ažuriranja temelje na vlasničkoj jedinici projekta.</span><span class="sxs-lookup"><span data-stu-id="415aa-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="415aa-135">Za prodajni cjenik temelje se na klijentu.</span><span class="sxs-lookup"><span data-stu-id="415aa-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="415aa-136">Za projekte koji su povezani s entitetom prodaje cijene po jedinici i prodajne cijene određuju se na temelju ovih cjenika.</span><span class="sxs-lookup"><span data-stu-id="415aa-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="415aa-137">Kopiranje projektnog tima</span><span class="sxs-lookup"><span data-stu-id="415aa-137">Copying a project team</span></span>

<span data-ttu-id="415aa-138">Kada projektni tim kopirate iz predloška projekta u projekt, generički resursi kopiraju se zajedno s vještinama i stručnostima definiranim u predlošku.</span><span class="sxs-lookup"><span data-stu-id="415aa-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="415aa-139">Dodjele generičkih resursa također se zadržavaju kao u predlošku projekta.</span><span class="sxs-lookup"><span data-stu-id="415aa-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="415aa-140">Imenovani resursi nisu podržani u predlošcima projekta.</span><span class="sxs-lookup"><span data-stu-id="415aa-140">Named resources aren't supported in project templates.</span></span>
