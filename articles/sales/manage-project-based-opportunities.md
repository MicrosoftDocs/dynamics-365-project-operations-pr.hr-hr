---
title: Upravljanje projektnim prilikama
description: U ovoj temi nalaze se informacije o načinu rada s prilikama koje su povezane s projektima.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948366"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="b7e72-103">Upravljanje projektnim prilikama</span><span class="sxs-lookup"><span data-stu-id="b7e72-103">Manage project-based opportunities</span></span>

<span data-ttu-id="b7e72-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b7e72-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b7e72-105">Projektne tvrtke obično imaju svoje načine funkcioniranja pri isporuci u više zemalja i zemljopisnih područja.</span><span class="sxs-lookup"><span data-stu-id="b7e72-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="b7e72-106">Troškovi izvršenja i isporuke projekta mogu se razlikovati ovisno o tome koje zemljopisno područje ili sektor upravlja isporukom.</span><span class="sxs-lookup"><span data-stu-id="b7e72-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="b7e72-107">Zauzvrat, to može utjecati na marže posla.</span><span class="sxs-lookup"><span data-stu-id="b7e72-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="b7e72-108">Dostava projektnih usluga obično uključuje velike količine vremena koje troše ljudski resursi, značajne troškove putovanja, materijalne troškove i druge troškove.</span><span class="sxs-lookup"><span data-stu-id="b7e72-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="b7e72-109">Prilike koje se temelje na projektu u aplikaciji Dynamics 365 Project Operations dizajnirane su s proširenjima za aplikaciju Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b7e72-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="b7e72-110">Ova tema donosi pojedinosti o različitim poljima i poslovnoj logici koja je uključena u dodatnu funkcionalnost koja je potrebna projektnim tvrtkama za upravljanje projektnim mogućnostima.</span><span class="sxs-lookup"><span data-stu-id="b7e72-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="b7e72-111">Prikaz svih projektnih prilika</span><span class="sxs-lookup"><span data-stu-id="b7e72-111">View all project-based opportunities</span></span>

<span data-ttu-id="b7e72-112">Popis svih projektnih prilika može se vidjeti na stranici s popisom **Prilika**.</span><span class="sxs-lookup"><span data-stu-id="b7e72-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="b7e72-113">Idite na **Prodaja** > **Prilike**.</span><span class="sxs-lookup"><span data-stu-id="b7e72-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="b7e72-114">Upotrijebite **Preklopni gumb za prikaz** za odabir drugih filtriranih prikaza prilika.</span><span class="sxs-lookup"><span data-stu-id="b7e72-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="b7e72-115">Možete stvoriti vlastite prikaze s prilagođenim kriterijima filtra kako biste konfigurirali te prikaze i mogućnosti navigacije.</span><span class="sxs-lookup"><span data-stu-id="b7e72-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="b7e72-116">Prilike za projekt mogu se stvoriti ili izbrisati s ove stranice s popisom ili stranice s pojedinostima.</span><span class="sxs-lookup"><span data-stu-id="b7e72-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="b7e72-117">Tijek poslovnog procesa za poslove temeljene na projektima</span><span class="sxs-lookup"><span data-stu-id="b7e72-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="b7e72-118">Sljedeći tijekovi poslovnog procesa podržani su za poslove temeljene na projektima u aplikaciji Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b7e72-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="b7e72-119">Poslovni proces od potencijalnog klijenta do prilike</span><span class="sxs-lookup"><span data-stu-id="b7e72-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="b7e72-120">Proces prodaje prilike</span><span class="sxs-lookup"><span data-stu-id="b7e72-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="b7e72-121">Poslovni proces od potencijalnog klijenta do prilike</span><span class="sxs-lookup"><span data-stu-id="b7e72-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="b7e72-122">Poslovni proces od potencijalnog klijenta do prilike podržava sljedeće faze:</span><span class="sxs-lookup"><span data-stu-id="b7e72-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="b7e72-123">Faza</span><span class="sxs-lookup"><span data-stu-id="b7e72-123">Stage</span></span> | <span data-ttu-id="b7e72-124">Mapirani entitet</span><span class="sxs-lookup"><span data-stu-id="b7e72-124">Mapped entity</span></span> | <span data-ttu-id="b7e72-125">Funkcija</span><span class="sxs-lookup"><span data-stu-id="b7e72-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b7e72-126">Kvalificiraj</span><span class="sxs-lookup"><span data-stu-id="b7e72-126">Qualify</span></span> | <span data-ttu-id="b7e72-127">Potencijalni klijent</span><span class="sxs-lookup"><span data-stu-id="b7e72-127">Lead</span></span> | <span data-ttu-id="b7e72-128">Kvalificiranje potencijalnog klijenta za stvaranje računa, kontakta i prilike.</span><span class="sxs-lookup"><span data-stu-id="b7e72-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="b7e72-129">Razvij</span><span class="sxs-lookup"><span data-stu-id="b7e72-129">Develop</span></span> | <span data-ttu-id="b7e72-130">Prilika</span><span class="sxs-lookup"><span data-stu-id="b7e72-130">Opportunity</span></span> | <span data-ttu-id="b7e72-131">Pripremite priliku za dodavanje više podataka o uključenom poslu, ključnim dionicima i konkurenciji.</span><span class="sxs-lookup"><span data-stu-id="b7e72-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="b7e72-132">Predloži</span><span class="sxs-lookup"><span data-stu-id="b7e72-132">Propose</span></span> | <span data-ttu-id="b7e72-133">Prilika</span><span class="sxs-lookup"><span data-stu-id="b7e72-133">Opportunity</span></span> | <span data-ttu-id="b7e72-134">Pripremite prijedlog i nabavite odobrenje od internog tima za pregled.</span><span class="sxs-lookup"><span data-stu-id="b7e72-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="b7e72-135">Zatvaranje</span><span class="sxs-lookup"><span data-stu-id="b7e72-135">Close</span></span> | <span data-ttu-id="b7e72-136">Prilika</span><span class="sxs-lookup"><span data-stu-id="b7e72-136">Opportunity</span></span> | <span data-ttu-id="b7e72-137">Osvojite priliku kako biste okončali posao.</span><span class="sxs-lookup"><span data-stu-id="b7e72-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="b7e72-138">Proces prodaje prilike</span><span class="sxs-lookup"><span data-stu-id="b7e72-138">Opportunity sales process</span></span>
<span data-ttu-id="b7e72-139">Postupak Prodajne prilike u aplikaciji Project Operations proširenje je poslovnog tijeka postupka Prodajne prilike u aplikaciji Prodaja.</span><span class="sxs-lookup"><span data-stu-id="b7e72-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="b7e72-140">Ovaj poslovni proces dizajniran je kao gotov za podršku sljedećim fazama u projektnim prilikama.</span><span class="sxs-lookup"><span data-stu-id="b7e72-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="b7e72-141">Faza</span><span class="sxs-lookup"><span data-stu-id="b7e72-141">Stage</span></span> | <span data-ttu-id="b7e72-142">Mapirani entitet</span><span class="sxs-lookup"><span data-stu-id="b7e72-142">Mapped entity</span></span> | <span data-ttu-id="b7e72-143">Funkcija</span><span class="sxs-lookup"><span data-stu-id="b7e72-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b7e72-144">Kvalificiraj</span><span class="sxs-lookup"><span data-stu-id="b7e72-144">Qualify</span></span> | <span data-ttu-id="b7e72-145">Prilika</span><span class="sxs-lookup"><span data-stu-id="b7e72-145">Opportunity</span></span> | <span data-ttu-id="b7e72-146">Kvalificiranje potencijalnog klijenta za stvaranje računa, kontakta i prilike.</span><span class="sxs-lookup"><span data-stu-id="b7e72-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="b7e72-147">Predloži</span><span class="sxs-lookup"><span data-stu-id="b7e72-147">Propose</span></span> | <span data-ttu-id="b7e72-148">Ponuda</span><span class="sxs-lookup"><span data-stu-id="b7e72-148">Quote</span></span> | <span data-ttu-id="b7e72-149">Razradite prijedlog s pomoću ponuda projekta i nabavite odobrenje internog tima za pregled.</span><span class="sxs-lookup"><span data-stu-id="b7e72-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="b7e72-150">Ugovor</span><span class="sxs-lookup"><span data-stu-id="b7e72-150">Contract</span></span> | <span data-ttu-id="b7e72-151">Ugovor o projektu</span><span class="sxs-lookup"><span data-stu-id="b7e72-151">Project Contract</span></span> | <span data-ttu-id="b7e72-152">Ako se prihvati vaša ponuda, stvorite ugovor i počnite s izvršenjem i isporukom projekta.</span><span class="sxs-lookup"><span data-stu-id="b7e72-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="b7e72-153">Zatvaranje</span><span class="sxs-lookup"><span data-stu-id="b7e72-153">Close</span></span> | <span data-ttu-id="b7e72-154">Ugovor o projektu</span><span class="sxs-lookup"><span data-stu-id="b7e72-154">Project Contract</span></span> | <span data-ttu-id="b7e72-155">Uspješno završite posao i zatvorite ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="b7e72-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="b7e72-156">Ako je vaš projektni posao započeo s potencijalnim klijentom, poslovni proces „Od potencijalnog klijenta do prilike“ ima prednost.</span><span class="sxs-lookup"><span data-stu-id="b7e72-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="b7e72-157">Ako je vaš projektni posao započeo s Prilikom, prednost ima postupak Prodaje prilike.</span><span class="sxs-lookup"><span data-stu-id="b7e72-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="b7e72-158">Možete urediti tijek poslovnog procesa proizvoda ili stvoriti vlastite tijekove poslovnog procesa kako biste, po potrebi, pratili svoj prodajni postupak.</span><span class="sxs-lookup"><span data-stu-id="b7e72-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="b7e72-159">Dodatne informacije o tijekovima poslovnog procesa potražite u članku [Pregled tijekova poslovnog procesa](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="b7e72-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]