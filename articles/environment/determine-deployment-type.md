---
title: Odredite vrstu implementacije
description: U ovoj temi nalaze se informacije koje vam pomažu pri određivanju ispravne vrste implementacije projektnih operacija za vašu tvrtku.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2da6af3240d8e561d01b1fcd8d32b657dbac1588
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479555"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="9d8f0-103">Odredite vrstu implementacije</span><span class="sxs-lookup"><span data-stu-id="9d8f0-103">Determine your deployment type</span></span>

<span data-ttu-id="9d8f0-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="9d8f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d8f0-105">Nakon kupnje licence započnite ovdje kako biste odredili najbolji model implementacije aplikacije Dynamics 365 Project Operations s pomoću [tijeka Vođene instalacije](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="9d8f0-106">Nakon što dovršite Vođeni tijek instalacije, bit ćete preusmjereni na ispravan portal za upravljanje kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="9d8f0-107">Pogledajte pojedinosti o implementaciji kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="9d8f0-108">Postojeći klijenti sustava Dynamics upotrebljavaju aplikaciju Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9d8f0-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="9d8f0-109">Project Operations uključuje mogućnosti isporučene uz uslugu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="9d8f0-110">Putanja nadogradnje objavit će se za te klijente u valu 1 izdanja za 2021.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="9d8f0-111">Postojeći klijenti aplikacije Dynamics 365 Finance upotrebljavaju Upravljanje projektima i računovodstvo</span><span class="sxs-lookup"><span data-stu-id="9d8f0-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="9d8f0-112">Postojeći klijenti aplikacije Finance koji upotrebljavaju funkciju Upravljanje projektom i računovodstvo mogu je i dalje upotrebljavati takvu kakva jest.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="9d8f0-113">Pogledajte [Project Operations za scenarije sa zalihama / radnim nalozima](#pma).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="9d8f0-114">Regija implementacije</span><span class="sxs-lookup"><span data-stu-id="9d8f0-114">Deployment regions</span></span>
<span data-ttu-id="9d8f0-115">Kako biste utvrdili koje regije podržavaju implementaciju aplikacije Project Operations, pogledajte [Geografska dostupnost izvješća sustava Dynamics 365 i Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="9d8f0-116">Odaberite **Prikaži izvješće** i proširite **Dynamics 365 > Operacijske aplikacije > Dynamics 365 Project Operations** kako biste vidjeli podržane regije.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="9d8f0-117">Vrsta implementacije</span><span class="sxs-lookup"><span data-stu-id="9d8f0-117">Deployment types</span></span>
<span data-ttu-id="9d8f0-118">Project Operations podržava više mogućnosti implementacije radi prilagodbe vašim zahtjevima.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="9d8f0-119">Bez obzira jeste li novi ili postojeći klijent sustava Dynamics 365, Project Operations može podržati vaše potrebe.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="9d8f0-120">Naš [Upitnik za raspoređivanje](https://aka.ms/provisionprojectoperations) pomoći će vam pri određivanju ispravne implementacije.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="9d8f0-121">Rezultati će vas voditi prema jednoj od sljedećih vrsta implementacije:</span><span class="sxs-lookup"><span data-stu-id="9d8f0-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="9d8f0-122">Jednostavna implementacija – od sklapanja dogovora do proforma fakture</span><span class="sxs-lookup"><span data-stu-id="9d8f0-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="9d8f0-123">Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="9d8f0-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="9d8f0-124">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="9d8f0-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="9d8f0-125">Project Operations podržava scenarije sa zalihama / proizvodnim nalozima i scenarije bez zaliha / na temelju resursa u istom okruženju putem konfiguracija na razini pravne osobe.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="9d8f0-126">Na primjer, Contoso može upotrebljavati mogućnosti skladištenja/narudžbe u svom američkom proizvodnom pogonu (pravna osoba = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="9d8f0-127">Contoso može upotrebljavati mogućnosti koje nisu skladišne / koje su zasnovane na resursima u svojem servisnom pogonu Contoso Robotics Arms u Velikoj Britaniji (pravna osoba = Contoso Robotics Ujedinjeno Kraljevstvo).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="9d8f0-128">Jednostavna implementacija – od sklapanja dogovora do predračuna</span><span class="sxs-lookup"><span data-stu-id="9d8f0-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="9d8f0-129">Jednostavna implementacija uključuje sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="9d8f0-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="9d8f0-130">Postupak prodaje za projekte koji proširuju iskustva s aplikacijom Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="9d8f0-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="9d8f0-131">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="9d8f0-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="9d8f0-132">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="9d8f0-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="9d8f0-133">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="9d8f0-133">Unified resource management</span></span>
- <span data-ttu-id="9d8f0-134">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="9d8f0-134">Time tracking</span></span>
- <span data-ttu-id="9d8f0-135">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="9d8f0-135">Basic expense</span></span>
- <span data-ttu-id="9d8f0-136">Predračun i fakturiranje prema klijentima</span><span class="sxs-lookup"><span data-stu-id="9d8f0-136">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="9d8f0-137">Koraci implementacije</span><span class="sxs-lookup"><span data-stu-id="9d8f0-137">Deployment steps</span></span>
<span data-ttu-id="9d8f0-138">Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9d8f0-139">Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](lite-preview-subscription-sign-up.md) i [Priprema novog okruženja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="9d8f0-140">Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="9d8f0-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="9d8f0-141">Project Operations za scenarije s resursom / bez zaliha uključuju sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="9d8f0-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="9d8f0-142">Postupak prodaje za projekte koji proširuju aplikaciju Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="9d8f0-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="9d8f0-143">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="9d8f0-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="9d8f0-144">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="9d8f0-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="9d8f0-145">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="9d8f0-145">Unified resource management</span></span>
- <span data-ttu-id="9d8f0-146">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="9d8f0-146">Time tracking</span></span>
- <span data-ttu-id="9d8f0-147">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="9d8f0-147">Basic expense</span></span>
- <span data-ttu-id="9d8f0-148">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="9d8f0-148">Full expense</span></span>
- <span data-ttu-id="9d8f0-149">OCR računa</span><span class="sxs-lookup"><span data-stu-id="9d8f0-149">Receipt OCR</span></span>
- <span data-ttu-id="9d8f0-150">Predračun i fakturiranje prema klijentima</span><span class="sxs-lookup"><span data-stu-id="9d8f0-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="9d8f0-151">Priznavanje prihoda za projekte</span><span class="sxs-lookup"><span data-stu-id="9d8f0-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="9d8f0-152">Koraci implementacije</span><span class="sxs-lookup"><span data-stu-id="9d8f0-152">Deployment steps</span></span>
<span data-ttu-id="9d8f0-153">Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9d8f0-154">Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](resource-sign-up-preview-subscription.md) i [Priprema novog okruženja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="9d8f0-155">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="9d8f0-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="9d8f0-156">Planiranje projekta s pomoću WBS-a</span><span class="sxs-lookup"><span data-stu-id="9d8f0-156">Project planning using WBS</span></span>
- <span data-ttu-id="9d8f0-157">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="9d8f0-157">Resource Management</span></span>
- <span data-ttu-id="9d8f0-158">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="9d8f0-158">Time Tracking</span></span>
- <span data-ttu-id="9d8f0-159">Puni izdatak</span><span class="sxs-lookup"><span data-stu-id="9d8f0-159">Full Expense</span></span>
- <span data-ttu-id="9d8f0-160">OCR računa</span><span class="sxs-lookup"><span data-stu-id="9d8f0-160">Receipt OCR</span></span>
- <span data-ttu-id="9d8f0-161">Potpuno fakturiranje</span><span class="sxs-lookup"><span data-stu-id="9d8f0-161">Full Invoicing</span></span>
- <span data-ttu-id="9d8f0-162">Priznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="9d8f0-162">Revenue Recognition</span></span>
- <span data-ttu-id="9d8f0-163">Proizvodni nalozi</span><span class="sxs-lookup"><span data-stu-id="9d8f0-163">Production Orders</span></span>
- <span data-ttu-id="9d8f0-164">Podrška za materijale</span><span class="sxs-lookup"><span data-stu-id="9d8f0-164">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="9d8f0-165">Koraci implementacije</span><span class="sxs-lookup"><span data-stu-id="9d8f0-165">Deployment steps</span></span>
<span data-ttu-id="9d8f0-166">Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9d8f0-167">Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Priprema novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-167">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
