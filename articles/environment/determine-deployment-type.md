---
title: Odredite vrstu implementacije
description: U ovoj temi nalaze se informacije koje vam pomažu pri određivanju ispravne vrste implementacije projektnih operacija za vašu tvrtku.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997097"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="9a851-103">Odredite vrstu implementacije</span><span class="sxs-lookup"><span data-stu-id="9a851-103">Determine your deployment type</span></span>

<span data-ttu-id="9a851-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="9a851-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a851-105">Nakon kupnje licence započnite ovdje kako biste odredili najbolji model implementacije aplikacije Dynamics 365 Project Operations s pomoću [tijeka Vođene instalacije](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9a851-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="9a851-106">Nakon što dovršite Vođeni tijek instalacije, bit ćete preusmjereni na ispravan portal za upravljanje kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="9a851-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="9a851-107">Pogledajte pojedinosti o implementaciji kako biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="9a851-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="9a851-108">Postojeći klijenti sustava Dynamics upotrebljavaju aplikaciju Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9a851-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="9a851-109">Project Operations uključuje mogućnosti isporučene uz uslugu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9a851-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="9a851-110">Putanja nadogradnje objavit će se za te klijente u valu 1 izdanja za 2021.</span><span class="sxs-lookup"><span data-stu-id="9a851-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="9a851-111">Postojeći klijenti aplikacije Dynamics 365 Finance upotrebljavaju Upravljanje projektima i računovodstvo</span><span class="sxs-lookup"><span data-stu-id="9a851-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="9a851-112">Postojeći klijenti aplikacije Finance koji upotrebljavaju funkciju Upravljanje projektom i računovodstvo mogu je i dalje upotrebljavati takvu kakva jest.</span><span class="sxs-lookup"><span data-stu-id="9a851-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="9a851-113">Pogledajte [Project Operations za scenarije sa zalihama / radnim nalozima](#pma).</span><span class="sxs-lookup"><span data-stu-id="9a851-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="9a851-114">Regija implementacije</span><span class="sxs-lookup"><span data-stu-id="9a851-114">Deployment regions</span></span>
<span data-ttu-id="9a851-115">Kako biste utvrdili koje regije podržavaju implementaciju aplikacije Project Operations, pogledajte [Geografska dostupnost izvješća sustava Dynamics 365 i Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="9a851-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="9a851-116">Odaberite **Prikaži izvješće** i proširite **Dynamics 365 > Operacijske aplikacije > Dynamics 365 Project Operations** kako biste vidjeli podržane regije.</span><span class="sxs-lookup"><span data-stu-id="9a851-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="9a851-117">Vrsta implementacije</span><span class="sxs-lookup"><span data-stu-id="9a851-117">Deployment types</span></span>
<span data-ttu-id="9a851-118">Project Operations podržava više mogućnosti implementacije radi prilagodbe vašim zahtjevima.</span><span class="sxs-lookup"><span data-stu-id="9a851-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="9a851-119">Bez obzira jeste li novi ili postojeći klijent sustava Dynamics 365, Project Operations može podržati vaše potrebe.</span><span class="sxs-lookup"><span data-stu-id="9a851-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="9a851-120">Naš [Upitnik za raspoređivanje](https://aka.ms/provisionprojectoperations) pomoći će vam pri određivanju ispravne implementacije.</span><span class="sxs-lookup"><span data-stu-id="9a851-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="9a851-121">Rezultati će vas voditi prema jednoj od sljedećih vrsta implementacije:</span><span class="sxs-lookup"><span data-stu-id="9a851-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="9a851-122">Jednostavna implementacija – od sklapanja dogovora do proforma fakture</span><span class="sxs-lookup"><span data-stu-id="9a851-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="9a851-123">Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="9a851-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="9a851-124">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="9a851-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="9a851-125">Project Operations podržava scenarije sa zalihama / proizvodnim nalozima i scenarije bez zaliha / na temelju resursa u istom okruženju putem konfiguracija na razini pravne osobe.</span><span class="sxs-lookup"><span data-stu-id="9a851-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="9a851-126">Na primjer, Contoso može upotrebljavati mogućnosti narudžbe iz skladišta/proizvodnje u svom američkom proizvodnom pogonu (pravna osoba = Contoso proizvodnja Sjedinjene Države).</span><span class="sxs-lookup"><span data-stu-id="9a851-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="9a851-127">Contoso može upotrebljavati mogućnosti bez zaliha / na temelju resursa u svojem servisnom objektu Contoso Robotics Arms u Velikoj Britaniji (pravna osoba = Contoso Robotics Ujedinjeno Kraljevstvo).</span><span class="sxs-lookup"><span data-stu-id="9a851-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="9a851-128">Osnovna implementacija – od sklapanja posla do predračuna</span><span class="sxs-lookup"><span data-stu-id="9a851-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="9a851-129">Jednostavna implementacija uključuje sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="9a851-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="9a851-130">Postupak prodaje za projekte koji proširuju iskustva s aplikacijom Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="9a851-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="9a851-131">Planiranje projekta s pomoću aplikacije Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="9a851-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="9a851-132">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="9a851-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="9a851-133">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="9a851-133">Unified resource management</span></span>
- <span data-ttu-id="9a851-134">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="9a851-134">Time tracking</span></span>
- <span data-ttu-id="9a851-135">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="9a851-135">Basic expense</span></span>
- <span data-ttu-id="9a851-136">Predračun za pregled i uređivanje od strane voditelja projekta</span><span class="sxs-lookup"><span data-stu-id="9a851-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="9a851-137">Koraci implementacije</span><span class="sxs-lookup"><span data-stu-id="9a851-137">Deployment steps</span></span>
<span data-ttu-id="9a851-138">Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9a851-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9a851-139">Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](lite-preview-subscription-sign-up.md) i [Priprema novog okruženja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="9a851-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="9a851-140">Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="9a851-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="9a851-141">Project Operations za scenarije s resursom / bez zaliha uključuju sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="9a851-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="9a851-142">Postupak prodaje za projekte koji proširuju aplikaciju Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="9a851-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="9a851-143">Planiranje projekta s pomoću aplikacije Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="9a851-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="9a851-144">Višedimenzionalno određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="9a851-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="9a851-145">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="9a851-145">Unified resource management</span></span>
- <span data-ttu-id="9a851-146">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="9a851-146">Time tracking</span></span>
- <span data-ttu-id="9a851-147">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="9a851-147">Basic expense</span></span>
- <span data-ttu-id="9a851-148">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="9a851-148">Full expense</span></span>
- <span data-ttu-id="9a851-149">OCR računa</span><span class="sxs-lookup"><span data-stu-id="9a851-149">Receipt OCR</span></span>
- <span data-ttu-id="9a851-150">Predračun i fakturiranje prema klijentima</span><span class="sxs-lookup"><span data-stu-id="9a851-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="9a851-151">Priznavanje prihoda za projekte</span><span class="sxs-lookup"><span data-stu-id="9a851-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="9a851-152">Koraci implementacije</span><span class="sxs-lookup"><span data-stu-id="9a851-152">Deployment steps</span></span>
<span data-ttu-id="9a851-153">Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9a851-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9a851-154">Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](resource-sign-up-preview-subscription.md) i [Priprema novog okruženja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9a851-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="9a851-155">Project Operations za scenarije temeljene na zalihama / radnim nalozima</span><span class="sxs-lookup"><span data-stu-id="9a851-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="9a851-156">Planiranje projekta s pomoću WBS-a</span><span class="sxs-lookup"><span data-stu-id="9a851-156">Project planning using WBS</span></span>
- <span data-ttu-id="9a851-157">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="9a851-157">Resource management</span></span>
- <span data-ttu-id="9a851-158">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="9a851-158">Time tracking</span></span>
- <span data-ttu-id="9a851-159">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="9a851-159">Full expense</span></span>
- <span data-ttu-id="9a851-160">OCR računa</span><span class="sxs-lookup"><span data-stu-id="9a851-160">Receipt OCR</span></span>
- <span data-ttu-id="9a851-161">Potpuno fakturiranje</span><span class="sxs-lookup"><span data-stu-id="9a851-161">Full invoicing</span></span>
- <span data-ttu-id="9a851-162">Priznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="9a851-162">Revenue recognition</span></span>
- <span data-ttu-id="9a851-163">Proizvodni nalozi</span><span class="sxs-lookup"><span data-stu-id="9a851-163">Production orders</span></span>
- <span data-ttu-id="9a851-164">Podrška materijalima na zalihi s inventarom</span><span class="sxs-lookup"><span data-stu-id="9a851-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="9a851-165">Koraci implementacije</span><span class="sxs-lookup"><span data-stu-id="9a851-165">Deployment steps</span></span>
<span data-ttu-id="9a851-166">Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="9a851-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9a851-167">Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) i [Priprema novog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="9a851-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]