---
title: Pregled načina upravljanja resursima
description: U ovoj temi nalaze se informacije o funkcionalnosti Upravljanja resursima u sustavu Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930082"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="27d16-103">Pregled načina upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="27d16-103">Resource management modes overview</span></span>

<span data-ttu-id="27d16-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="27d16-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="27d16-105">Dynamics 365 Project Operations podržava dva načina kako biste izvršili cjelokupni tijek rezervacije.</span><span class="sxs-lookup"><span data-stu-id="27d16-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="27d16-106">Način upravljanja definiran je kao parametar projekta i može se izmijeniti ako vaše poslovanje treba promjenu.</span><span class="sxs-lookup"><span data-stu-id="27d16-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="27d16-107">Središnji način rada</span><span class="sxs-lookup"><span data-stu-id="27d16-107">Central mode</span></span>
<span data-ttu-id="27d16-108">Za tvrtke ili ustanove koje centraliziraju dodjelu resursa projektima, središnji način omogućuje način da menadžeri projekata mogu definirati preduvjete resursa na razini projekta.</span><span class="sxs-lookup"><span data-stu-id="27d16-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="27d16-109">Ispunjavanje preduvjeta resursa delegira se upravitelju resursa.</span><span class="sxs-lookup"><span data-stu-id="27d16-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="27d16-110">Upravitelji projekata mogu prihvatiti ili odbaciti resurse koje predloži upravitelj resursa.</span><span class="sxs-lookup"><span data-stu-id="27d16-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Središnji način](./media/resource-management-central.png)

<span data-ttu-id="27d16-112">Kako biste upravljali resursima s pomoću Središnjeg načina, pogledajte sljedeće:</span><span class="sxs-lookup"><span data-stu-id="27d16-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="27d16-113">Dodjeljivanje zadatku generičkih resursa koji se mogu rezervirati i generiranje preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="27d16-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="27d16-114">Rezerviranje imenovanih resursa iz preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="27d16-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="27d16-115">Slanje zahtjeva za resurs</span><span class="sxs-lookup"><span data-stu-id="27d16-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="27d16-116">Ispunjavanje zahtjeva za resurse</span><span class="sxs-lookup"><span data-stu-id="27d16-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="27d16-117">Prihvaćanje ili odbacivanje predloženog resursa za projekt iz zahtjeva za resurs</span><span class="sxs-lookup"><span data-stu-id="27d16-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="27d16-118">Hibridni način</span><span class="sxs-lookup"><span data-stu-id="27d16-118">Hybrid mode</span></span>
<span data-ttu-id="27d16-119">Za tvrtke ili ustanove kojima je potrebna fleksibilnost u raspodjeli resursa, hibridni način pruža upraviteljima projekata i upraviteljima resursa mogućnost rezerviranja resursa.</span><span class="sxs-lookup"><span data-stu-id="27d16-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hibridni način](./media/resource-management-hybrid.png)

<span data-ttu-id="27d16-121">Uz podržani postupak Središnjeg načina, pogledajte sljedeće teme za upravljanje svim ostalim podržanim tijekovima rezervacije u hibridnom načinu:</span><span class="sxs-lookup"><span data-stu-id="27d16-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="27d16-122">Rezervirajte resurs izravno projektu:</span><span class="sxs-lookup"><span data-stu-id="27d16-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="27d16-123">Rezerviraj imenovane resurse koji se mogu rezervirati za projektni tim i dodijeli zadatke</span><span class="sxs-lookup"><span data-stu-id="27d16-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="27d16-124">Rezervirajte resurs iz preduvjeta resursa:</span><span class="sxs-lookup"><span data-stu-id="27d16-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="27d16-125">Dodjeljivanje zadatku generičkih resursa koji se mogu rezervirati i generiranje preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="27d16-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="27d16-126">Rezerviranje imenovanih resursa iz preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="27d16-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
