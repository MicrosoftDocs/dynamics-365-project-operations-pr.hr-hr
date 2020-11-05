---
title: Odredite vrstu uvođenja
description: U ovoj temi nalaze se informacije koje vam pomažu pri određivanju ispravne vrste uvođenja projektnih operacija za vašu tvrtku.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073392"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="ed7bd-103">Odredite vrstu uvođenja</span><span class="sxs-lookup"><span data-stu-id="ed7bd-103">Determine your deployment type</span></span>

<span data-ttu-id="ed7bd-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="ed7bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed7bd-105">Nakon kupnje licence započnite ovdje kako biste odredili najbolji model uvođenja aplikacije Dynamics 365 Project Operations s pomoću odjeljka [Vođeni tijek instalacije](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="ed7bd-106">Nakon što dovršite Vođeni tijek instalacije, bit ćete preusmjereni na ispravan portal za upravljanje kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="ed7bd-107">Pogledajte pojedinosti o implementaciji kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="ed7bd-108">Postojeći klijenti sustava Dynamics upotrebljavaju aplikaciju Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ed7bd-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="ed7bd-109">Project Operations uključuje mogućnosti isporučene uz uslugu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="ed7bd-110">Putanja nadogradnje za te klijente objavit će se u budućnosti.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="ed7bd-111">Postojeći klijenti aplikacije Dynamics 365 Finance upotrebljavaju Upravljanje projektima i računovodstvo</span><span class="sxs-lookup"><span data-stu-id="ed7bd-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="ed7bd-112">Postojeći klijenti aplikacije Finance koji upotrebljavaju funkciju Upravljanje projektima i računovodstvo mogu je i dalje upotrebljavati takvu kakva jest.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="ed7bd-113">Pogledajte [Project Operations za scenarije sa zalihama / radnim nalozima](#pma).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="ed7bd-114">Vrsta uvođenja</span><span class="sxs-lookup"><span data-stu-id="ed7bd-114">Deployment types</span></span>
<span data-ttu-id="ed7bd-115">Project Operations podržava više mogućnosti uvođenja radi prilagodbe vašim zahtjevima.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="ed7bd-116">Bez obzira jeste li novi ili postojeći klijent sustava Dynamics 365, Project Operations može podržati vaše potrebe.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="ed7bd-117">Naš [Upitnik za raspoređivanje](https://aka.ms/provisionprojectoperations) pomoći će vam pri određivanju ispravnog uvođenja.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="ed7bd-118">Rezultati će vas voditi prema jednoj od sljedećih vrsta uvođenja:</span><span class="sxs-lookup"><span data-stu-id="ed7bd-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="ed7bd-119">Jednostavno uvođenje – od sklapanja dogovora do proforma fakture</span><span class="sxs-lookup"><span data-stu-id="ed7bd-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="ed7bd-120">Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="ed7bd-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="ed7bd-121">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="ed7bd-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="ed7bd-122">Project Operations podržava scenarije sa zalihama / proizvodnim nalozima i scenarije bez zaliha / na temelju resursa u istom okruženju putem konfiguracija na razini pravne osobe.</span><span class="sxs-lookup"><span data-stu-id="ed7bd-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="ed7bd-123">Na primjer, Contoso može upotrebljavati mogućnosti skladištenja/narudžbe u svom američkom proizvodnom pogonu (pravna osoba = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="ed7bd-124">Contoso može upotrebljavati mogućnosti koje nisu skladišne / koje su zasnovane na resursima u svojem servisnom pogonu Contoso Robotics Arms u Velikoj Britaniji (pravna osoba = Contoso Robotics Ujedinjeno Kraljevstvo).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="ed7bd-125">Jednostavno uvođenje – od sklapanja dogovora do predračuna</span><span class="sxs-lookup"><span data-stu-id="ed7bd-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="ed7bd-126">Jednostavno uvođenje uključuje sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="ed7bd-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="ed7bd-127">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="ed7bd-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ed7bd-128">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="ed7bd-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ed7bd-129">Objedinjeno upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="ed7bd-129">Unified Resource Management</span></span>
- <span data-ttu-id="ed7bd-130">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="ed7bd-130">Time Tracking</span></span>
- <span data-ttu-id="ed7bd-131">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="ed7bd-131">Basic Expense</span></span>
- <span data-ttu-id="ed7bd-132">Prijedlog fakture</span><span class="sxs-lookup"><span data-stu-id="ed7bd-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="ed7bd-133">Koraci uvođenja</span><span class="sxs-lookup"><span data-stu-id="ed7bd-133">Deployment steps</span></span>
<span data-ttu-id="ed7bd-134">Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ed7bd-135">Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](lite-preview-subscription-sign-up.md) i [Priprema novog okruženja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="ed7bd-136">Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="ed7bd-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="ed7bd-137">Project Operations za scenarije s resursom / bez zaliha uključuju sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="ed7bd-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="ed7bd-138">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="ed7bd-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ed7bd-139">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="ed7bd-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ed7bd-140">Objedinjeno upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="ed7bd-140">Unified Resource Management</span></span>
- <span data-ttu-id="ed7bd-141">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="ed7bd-141">Time Tracking</span></span>
- <span data-ttu-id="ed7bd-142">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="ed7bd-142">Basic Expense</span></span>
- <span data-ttu-id="ed7bd-143">Puni izdatak</span><span class="sxs-lookup"><span data-stu-id="ed7bd-143">Full Expense</span></span>
- <span data-ttu-id="ed7bd-144">OCR računa</span><span class="sxs-lookup"><span data-stu-id="ed7bd-144">Receipt OCR</span></span>
- <span data-ttu-id="ed7bd-145">Potpuno fakturiranje</span><span class="sxs-lookup"><span data-stu-id="ed7bd-145">Full Invoicing</span></span>
- <span data-ttu-id="ed7bd-146">Priznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="ed7bd-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="ed7bd-147">Koraci uvođenja</span><span class="sxs-lookup"><span data-stu-id="ed7bd-147">Deployment steps</span></span>
<span data-ttu-id="ed7bd-148">Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ed7bd-149">Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](resource-sign-up-preview-subscription.md) i [Priprema novog okruženja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="ed7bd-150">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="ed7bd-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="ed7bd-151">Planiranje projekta s pomoću WBS-a</span><span class="sxs-lookup"><span data-stu-id="ed7bd-151">Project planning using WBS</span></span>
- <span data-ttu-id="ed7bd-152">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="ed7bd-152">Resource Management</span></span>
- <span data-ttu-id="ed7bd-153">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="ed7bd-153">Time Tracking</span></span>
- <span data-ttu-id="ed7bd-154">Puni izdatak</span><span class="sxs-lookup"><span data-stu-id="ed7bd-154">Full Expense</span></span>
- <span data-ttu-id="ed7bd-155">OCR računa</span><span class="sxs-lookup"><span data-stu-id="ed7bd-155">Receipt OCR</span></span>
- <span data-ttu-id="ed7bd-156">Potpuno fakturiranje</span><span class="sxs-lookup"><span data-stu-id="ed7bd-156">Full Invoicing</span></span>
- <span data-ttu-id="ed7bd-157">Priznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="ed7bd-157">Revenue Recognition</span></span>
- <span data-ttu-id="ed7bd-158">Proizvodni nalozi</span><span class="sxs-lookup"><span data-stu-id="ed7bd-158">Production Orders</span></span>
- <span data-ttu-id="ed7bd-159">Podrška za materijale</span><span class="sxs-lookup"><span data-stu-id="ed7bd-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="ed7bd-160">Koraci uvođenja</span><span class="sxs-lookup"><span data-stu-id="ed7bd-160">Deployment steps</span></span>
<span data-ttu-id="ed7bd-161">Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ed7bd-162">Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Priprema novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ed7bd-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

