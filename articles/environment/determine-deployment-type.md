---
title: Vrsta uvođenja
description: U ovoj temi nalaze se informacije koje vam pomažu pri određivanju ispravne vrste uvođenja projektnih operacija za vašu tvrtku.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948788"
---
# <a name="deployment-types"></a><span data-ttu-id="0c049-103">Vrsta uvođenja</span><span class="sxs-lookup"><span data-stu-id="0c049-103">Deployment types</span></span>

<span data-ttu-id="0c049-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="0c049-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c049-105">Nakon kupnje licence započnite ovdje kako biste odredili najbolji model uvođenja aplikacije Dynamics 365 Project Operations s pomoću odjeljka [Vođeni tijek instalacije](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="0c049-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="0c049-106">Nakon što dovršite Vođeni tijek instalacije, bit ćete preusmjereni na ispravan portal za upravljanje kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="0c049-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="0c049-107">U nastavku pogledajte pojedinosti o uvođenju kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="0c049-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="0c049-108">Postojeći klijenti sustava Dynamics upotrebljavaju aplikaciju Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0c049-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="0c049-109">Project Operations uključuje mogućnosti isporučene uz uslugu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0c049-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="0c049-110">Putanja nadogradnje za te klijente objavit će se u budućnosti.</span><span class="sxs-lookup"><span data-stu-id="0c049-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="0c049-111">Postojeći klijenti aplikacije Dynamics 365 Finance upotrebljavaju Upravljanje projektima i računovodstvo</span><span class="sxs-lookup"><span data-stu-id="0c049-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="0c049-112">Postojeći klijenti aplikacije Finance koji upotrebljavaju funkciju Upravljanje projektima i računovodstvo mogu je i dalje upotrebljavati takvu kakva jest.</span><span class="sxs-lookup"><span data-stu-id="0c049-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="0c049-113">Pogledajte [Project Operations za scenarije sa zalihama / radnim nalozima](#pma).</span><span class="sxs-lookup"><span data-stu-id="0c049-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="0c049-114">Project Operations podržava više mogućnosti uvođenja radi prilagodbe vašim zahtjevima.</span><span class="sxs-lookup"><span data-stu-id="0c049-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="0c049-115">Bez obzira jeste li novi ili postojeći klijent sustava Dynamics 365, Project Operations može podržati vaše potrebe.</span><span class="sxs-lookup"><span data-stu-id="0c049-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="0c049-116">Naš [Upitnik za raspoređivanje](https://aka.ms/provisionprojectoperations) pomoći će vam pri određivanju ispravnog uvođenja.</span><span class="sxs-lookup"><span data-stu-id="0c049-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="0c049-117">Rezultati će vas voditi prema jednoj od sljedećih vrsta uvođenja:</span><span class="sxs-lookup"><span data-stu-id="0c049-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="0c049-118">Jednostavno uvođenje – od sklapanja dogovora do proforma fakture</span><span class="sxs-lookup"><span data-stu-id="0c049-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="0c049-119">Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="0c049-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="0c049-120">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="0c049-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="0c049-121">Project Operations podržava scenarije sa zalihama / proizvodnim nalozima i scenarije bez zaliha / na temelju resursa u istom okruženju putem konfiguracija na razini pravne osobe.</span><span class="sxs-lookup"><span data-stu-id="0c049-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="0c049-122">Na primjer, Contoso može iskoristiti mogućnosti sa zalihama / proizvodni nalog u svom proizvodnom pogonu u SAD-u (pravna osoba = Contoso Manufacturing United States) i mogućnosti bez zaliha / na temelju resursa u svom servisnom pogonu Contoso Robotics Arms u Velikoj Britaniji (pravna osoba = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="0c049-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="0c049-123"><a name="lite"><a/>Jednostavno uvođenje – od sklapanja dogovora do predračuna</span><span class="sxs-lookup"><span data-stu-id="0c049-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="0c049-124">Jednostavno uvođenje uključuje sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="0c049-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="0c049-125">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="0c049-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="0c049-126">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="0c049-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="0c049-127">Objedinjeno upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="0c049-127">Unified Resource Management</span></span>
- <span data-ttu-id="0c049-128">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="0c049-128">Time Tracking</span></span>
- <span data-ttu-id="0c049-129">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="0c049-129">Basic Expense</span></span>
- <span data-ttu-id="0c049-130">Prijedlog fakture</span><span class="sxs-lookup"><span data-stu-id="0c049-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="0c049-131">Koraci uvođenja:</span><span class="sxs-lookup"><span data-stu-id="0c049-131">Deployment steps:</span></span>
<span data-ttu-id="0c049-132">Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="0c049-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0c049-133">Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](lite-preview-subscription-sign-up.md) i [Priprema novog okruženja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="0c049-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="0c049-134"><a name="integrated"><a/>Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="0c049-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="0c049-135">Project Operations za scenarije s resursom / bez zaliha uključuju sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="0c049-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="0c049-136">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="0c049-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="0c049-137">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="0c049-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="0c049-138">Objedinjeno upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="0c049-138">Unified Resource Management</span></span>
- <span data-ttu-id="0c049-139">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="0c049-139">Time Tracking</span></span>
- <span data-ttu-id="0c049-140">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="0c049-140">Basic Expense</span></span>
- <span data-ttu-id="0c049-141">Puni izdatak</span><span class="sxs-lookup"><span data-stu-id="0c049-141">Full Expense</span></span>
- <span data-ttu-id="0c049-142">OCR računa</span><span class="sxs-lookup"><span data-stu-id="0c049-142">Receipt OCR</span></span>
- <span data-ttu-id="0c049-143">Potpuno fakturiranje</span><span class="sxs-lookup"><span data-stu-id="0c049-143">Full Invoicing</span></span>
- <span data-ttu-id="0c049-144">Priznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="0c049-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="0c049-145">Koraci uvođenja:</span><span class="sxs-lookup"><span data-stu-id="0c049-145">Deployment steps:</span></span>
<span data-ttu-id="0c049-146">Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="0c049-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0c049-147">Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](resource-sign-up-preview-subscription.md) i [Priprema novog okruženja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0c049-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="0c049-148">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="0c049-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="0c049-149">Planiranje projekta s pomoću WBS-a</span><span class="sxs-lookup"><span data-stu-id="0c049-149">Project planning using WBS</span></span>
- <span data-ttu-id="0c049-150">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="0c049-150">Resource Management</span></span>
- <span data-ttu-id="0c049-151">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="0c049-151">Time Tracking</span></span>
- <span data-ttu-id="0c049-152">Puni izdatak</span><span class="sxs-lookup"><span data-stu-id="0c049-152">Full Expense</span></span>
- <span data-ttu-id="0c049-153">OCR računa</span><span class="sxs-lookup"><span data-stu-id="0c049-153">Receipt OCR</span></span>
- <span data-ttu-id="0c049-154">Potpuno fakturiranje</span><span class="sxs-lookup"><span data-stu-id="0c049-154">Full Invoicing</span></span>
- <span data-ttu-id="0c049-155">Priznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="0c049-155">Revenue Recognition</span></span>
- <span data-ttu-id="0c049-156">Proizvodni nalozi</span><span class="sxs-lookup"><span data-stu-id="0c049-156">Production Orders</span></span>
- <span data-ttu-id="0c049-157">Podrška za materijale</span><span class="sxs-lookup"><span data-stu-id="0c049-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="0c049-158">Koraci uvođenja:</span><span class="sxs-lookup"><span data-stu-id="0c049-158">Deployment steps:</span></span>
<span data-ttu-id="0c049-159">Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="0c049-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="0c049-160">Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Priprema novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="0c049-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



