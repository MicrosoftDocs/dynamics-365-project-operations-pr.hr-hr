---
title: Stvaranje novog projekta
description: U ovoj temi nalaze se informacije o načinu stvaranja novog projekta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270714"
---
# <a name="create-a-new-project"></a><span data-ttu-id="f1b44-103">Stvaranje novog projekta</span><span class="sxs-lookup"><span data-stu-id="f1b44-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1b44-104">Poduzmite sljedeće korake za stvaranje novog projekta.</span><span class="sxs-lookup"><span data-stu-id="f1b44-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="f1b44-105">Na stranici **Upravljanje projektom** odaberite **Novi projekt** i unesite sljedeće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="f1b44-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="f1b44-106">**Vrsta projekta:** Vrijeme i materijal</span><span class="sxs-lookup"><span data-stu-id="f1b44-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="f1b44-107">**Naziv projekta:** XYZ nadogradnja 2. faze</span><span class="sxs-lookup"><span data-stu-id="f1b44-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="f1b44-108">**Grupa projekata:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="f1b44-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="f1b44-109">**ID ugovora projekta:** 00000002</span><span class="sxs-lookup"><span data-stu-id="f1b44-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="f1b44-110">Odaberite **Stvori projekt**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="f1b44-111">Dodjela resursa projektu</span><span class="sxs-lookup"><span data-stu-id="f1b44-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="f1b44-112">Na stranici **Radnici**, na popisu **Radnici**, odaberite zapis za radnika za kojeg ste prethodno postavili kompetencije i otvorite zapis za radnika.</span><span class="sxs-lookup"><span data-stu-id="f1b44-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="f1b44-113">U Oknu radnji na kartici **Projekt** u grupi **Postavljanje**, kliknite mogućnost **Dodjeli projekte**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="f1b44-114">Na stranici **Projektni zadaci za provjeru valjanosti resursa**, na kartici **Projekti** u polju **Dodajte projekt odabranim projektima**, filtrirajte na projekt **XYZ nadogradnja 2. faze**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="f1b44-115">U oknu **Preostali projekti** odaberite projekt, a zatim odaberite gumb sa strelicom kako biste ga dodali u okno **Odabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="f1b44-116">Prema potrebi možete dodijeliti i kategorije za resurs.</span><span class="sxs-lookup"><span data-stu-id="f1b44-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="f1b44-117">Ta je vrsta kategorije ili **Trošak** ili **Prihod**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="f1b44-118">Vrstu kategorije određuje vaša tvrtka ili ustanova.</span><span class="sxs-lookup"><span data-stu-id="f1b44-118">The category type is determined by your organization.</span></span> <span data-ttu-id="f1b44-119">Ako za resurs nisu dodijeljene kategorije, Financije pretražuju zadanu kategoriju cijena radnih sati za trošak i prihod.</span><span class="sxs-lookup"><span data-stu-id="f1b44-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="f1b44-120">Postavljanje svojstava resursa i uloga za projekt</span><span class="sxs-lookup"><span data-stu-id="f1b44-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="f1b44-121">Voditelj projekta može upotrijebiti funkcionalnost projektnih resursa za stvaranje uloga potrebnih za projekt.</span><span class="sxs-lookup"><span data-stu-id="f1b44-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="f1b44-122">Uloge se mogu upotrebljavati ako su potvrđeni resursi i dalje nepoznati u vrijeme rezerviranja resursa.</span><span class="sxs-lookup"><span data-stu-id="f1b44-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="f1b44-123">Uloge se mogu privremeno rezervirati kao planirani resursi, tako da možete nastaviti faze planiranja projekta.</span><span class="sxs-lookup"><span data-stu-id="f1b44-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="f1b44-124">[![Primjer uloge](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="f1b44-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="f1b44-125">**Scenarij:** Contoso je angažiran da dovrši projekt Vrijeme i materijal koji ima odobren ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="f1b44-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="f1b44-126">Voditelj projekta nižeg ranga još uvijek dovršava djelokrug projekta.</span><span class="sxs-lookup"><span data-stu-id="f1b44-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="f1b44-127">Voditelj resursa trenutačno identificira određene resurse koji će se rezervirati za rad na novom projektu.</span><span class="sxs-lookup"><span data-stu-id="f1b44-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="f1b44-128">Zbog kritične naravi projekta, sponzor projekta zatražio je ulogu voditelja projekta višeg ranga kao jednu od uloga.</span><span class="sxs-lookup"><span data-stu-id="f1b44-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="f1b44-129">Voditelj resursa mora nabaviti novi resurs i definirati ulogu u sustavu u slučaju da voditelj projekta nižeg ranga tijekom planiranja projekta zatraži podatke o resursima.</span><span class="sxs-lookup"><span data-stu-id="f1b44-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="f1b44-130">U sljedećim koracima pokazan je način na koji upravitelj resursa može postaviti ulogu voditelja projekta višeg ranga i s njom povezati svojstva resursa.</span><span class="sxs-lookup"><span data-stu-id="f1b44-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="f1b44-131">Kasnije se uloga može upotrijebiti za traženje dostupnih resursa koji se podudaraju s potrebnim kompetencijama resursa.</span><span class="sxs-lookup"><span data-stu-id="f1b44-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="f1b44-132">Na stranici **Postavljanje uloga** odaberite **Novo** i unesite sljedeće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="f1b44-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="f1b44-133">**ID uloge:** Voditelj projekta višeg ranga</span><span class="sxs-lookup"><span data-stu-id="f1b44-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="f1b44-134">**ID uloge:** Voditelj projekta višeg ranga</span><span class="sxs-lookup"><span data-stu-id="f1b44-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="f1b44-135">Kliknite **Stvori**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-135">Select **Create**.</span></span>
3. <span data-ttu-id="f1b44-136">Odaberite ulogu **Voditelj projekta višeg ranga**, a zatim odaberite **Konfiguriraj svojstva**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="f1b44-137">U polju **Vrste svojstava** odaberite **Vještina**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="f1b44-138">U polju **Dostupna svojstva** unesite vještinu koja se traži.</span><span class="sxs-lookup"><span data-stu-id="f1b44-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="f1b44-139">U polju **Vrsta svojstva** odaberite **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="f1b44-140">U polju **Dostupna svojstva** unesite vrstu certifikata koja se traži.</span><span class="sxs-lookup"><span data-stu-id="f1b44-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="f1b44-141">Dodjela projektu odgovarajućih resursa</span><span class="sxs-lookup"><span data-stu-id="f1b44-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="f1b44-142">Na stranici **Svi projekti** odaberite projekt **XYZ nadogradnja 2. faze**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="f1b44-143">Na kartici **Projektni tim i planiranje** odaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="f1b44-144">U polju **Uloga** odaberite **Član tima**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="f1b44-145">Odaberite **Rezerviraj iz kalendara**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="f1b44-146">Na stranici **Dostupnost resursa** odaberite **Prikaz postavki**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="f1b44-147">Na stranici **Prilagodi postavke prikaza** unesite sljedeće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="f1b44-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="f1b44-148">**Oblik prikaza raspona datuma:** Dan</span><span class="sxs-lookup"><span data-stu-id="f1b44-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="f1b44-149">**Prikaži dostupne opise:** Da</span><span class="sxs-lookup"><span data-stu-id="f1b44-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="f1b44-150">**Prikaži preostali kapacitet:** Da</span><span class="sxs-lookup"><span data-stu-id="f1b44-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="f1b44-151">S popisa resursa odaberite resurs.</span><span class="sxs-lookup"><span data-stu-id="f1b44-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="f1b44-152">Odaberite **Fiksna rezervacija** i **Puni kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="f1b44-153">Dodjela resursa zadanoj ulozi</span><span class="sxs-lookup"><span data-stu-id="f1b44-153">Assign a resource to a default role</span></span>

<span data-ttu-id="f1b44-154">Kako bi se pomoglo upraviteljima projekata ili resursa, mogu vršiti pretraživanje kroz razine naniže na resursima koji se mogu rezervirati za projekt.</span><span class="sxs-lookup"><span data-stu-id="f1b44-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="f1b44-155">Zadanu ulogu možete povezati s postojećim ili novostečenim resursom.</span><span class="sxs-lookup"><span data-stu-id="f1b44-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="f1b44-156">Primjerice, kad je Daniel zaposlen, imao je iskustva i vještine da ispuni ulogu poslovnog analitičara.</span><span class="sxs-lookup"><span data-stu-id="f1b44-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="f1b44-157">Voditelj resursa dodijelio je ovu ulogu Danielu kao zadanu ulogu.</span><span class="sxs-lookup"><span data-stu-id="f1b44-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="f1b44-158">Stoga je voditelj resursa dodao Daniela u skup poslovnih analitičara koji su dostupni za rad na projektima.</span><span class="sxs-lookup"><span data-stu-id="f1b44-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="f1b44-159">Tijekom rezervacije resursa, voditelji projekata mogu filtrirati uloge resursa koje su dostupne za rad na projektima.</span><span class="sxs-lookup"><span data-stu-id="f1b44-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="f1b44-160">Te podatke mogu upotrebljavati kao jedan kriterij kada provode višekriterijsku analizu odluka tijekom realizacije resursa.</span><span class="sxs-lookup"><span data-stu-id="f1b44-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="f1b44-161">U filtar mogu dodati i druga svojstva resursa za traženje resursa koji imaju određene vještine, obrazovanje i iskustvo za dani projekt.</span><span class="sxs-lookup"><span data-stu-id="f1b44-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="f1b44-162">**Scenarij:** Odobreni je projekt započeo, a uloga voditelja projekta višeg ranga rezervirana je tijekom faze planiranja projekta kao planirani resurs.</span><span class="sxs-lookup"><span data-stu-id="f1b44-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="f1b44-163">Upravitelj resursa sada je nabavio resurs za ispunjavanje uloge voditelja projekta višeg ranga.</span><span class="sxs-lookup"><span data-stu-id="f1b44-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="f1b44-164">Na stranici **Popis resursa** odaberite **Daniel Petek**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="f1b44-165">Na stranici **Uloga za resurs** odaberite **Novo** i unesite sljedeće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="f1b44-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="f1b44-166">**Na snazi:** Unesite trenutačni datum.</span><span class="sxs-lookup"><span data-stu-id="f1b44-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="f1b44-167">**Istek:** Unesite **Nikada**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="f1b44-168">**Uloga:** Unesite **Voditelj projekta višeg ranga**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="f1b44-169">Odaberite **Spremi** i zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="f1b44-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="f1b44-170">Na kartici **Kompetencije** dodajte vještinu **ProjectMgmt** i certifikat **PMP**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]