---
title: Stvaranje projektnog tima
description: U ovoj se temi nalaze informacije o načinu izrade projektnih timova i upravljanja njima.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270849"
---
# <a name="create-a-project-team"></a><span data-ttu-id="5117f-103">Stvaranje projektnog tima</span><span class="sxs-lookup"><span data-stu-id="5117f-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5117f-104">Kako bi se upotrebljavale uloge koje su prethodno postavljene u projektu, voditelj projekta mora povezati uloge s projektom.</span><span class="sxs-lookup"><span data-stu-id="5117f-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="5117f-105">Za projekt se može dodijeliti više uloga.</span><span class="sxs-lookup"><span data-stu-id="5117f-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="5117f-106">Kako bi se spriječila zabuna, ove se uloge automatski označavaju tijekom rezervacije.</span><span class="sxs-lookup"><span data-stu-id="5117f-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="5117f-107">Na primjer, ako voditelj projekta zahtijeva tri softverska inženjera, oznake tri uloge softverskog inženjera **softverski inženjer 1**, **softverski inženjer 2** i **softverski inženjer 3** automatski se generiraju.</span><span class="sxs-lookup"><span data-stu-id="5117f-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="5117f-108">Ako su svojstva uloge prethodno postavljena za ulogu, ona se primjenjuju kao filtar tijekom pretraživanja resursa.</span><span class="sxs-lookup"><span data-stu-id="5117f-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="5117f-109">Dodatna svojstva mogu se prema potrebi dodati za daljnje sužavanje pretraživanja.</span><span class="sxs-lookup"><span data-stu-id="5117f-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="5117f-110">Postavke prikaza također se mogu prilagoditi kako bi pružile bolji prikaz dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="5117f-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="5117f-111">Postoje mogućnosti prikazivanja dostupnosti po satu, dnevno, tjedno, mjesečno, tromjesečno i godišnje.</span><span class="sxs-lookup"><span data-stu-id="5117f-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="5117f-112">Također postoji mogućnost prikaza dostupnog i preostalog kapaciteta na resursima.</span><span class="sxs-lookup"><span data-stu-id="5117f-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="5117f-113">Ova je mogućnost korisna za upravljanje vremenom kada procjenjujete dostupno vrijeme za aktivnosti ili dostupnost resursa.</span><span class="sxs-lookup"><span data-stu-id="5117f-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="5117f-114">Voditelj projekta može odabrati ulogu na stranici, a zatim, ako postoji dostupan resurs koji udovoljava zahtjevu, odabrati resurs kako bi ga rezervirao za popunjavanje uloge.</span><span class="sxs-lookup"><span data-stu-id="5117f-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="5117f-115">Imajte na umu kako resurse u fazi planiranja u ovom trenutku nije potrebno rezervirati.</span><span class="sxs-lookup"><span data-stu-id="5117f-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="5117f-116">Kada stvarate WBS uloge možete zamijeniti resursima osoblja za projekt.</span><span class="sxs-lookup"><span data-stu-id="5117f-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="5117f-117">Ako se uloge u WBS-u zamijene resursima s osobljem, postavka resursa automatski ažurira popis i raspored projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="5117f-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="5117f-118">[![Popis projektnog tima koji uključuje i uloge i stvarne resurse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="5117f-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="5117f-119">Voditelj projekta ima razne mogućnosti za rezerviranje resursa za projekt, kao što su **Preostali kapacitet**, **Puni kapacitet**, **Postotak kapaciteta** i **Navođenje sati rada**.</span><span class="sxs-lookup"><span data-stu-id="5117f-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="5117f-120">Ove mogućnosti rezervacije mogu se otkazati u bilo kojem trenutku ako se zadaci resursa promijene.</span><span class="sxs-lookup"><span data-stu-id="5117f-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="5117f-121">Podržane su dvije vrste rezervacija:</span><span class="sxs-lookup"><span data-stu-id="5117f-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="5117f-122">**Fiksna rezervacija** – Rezervacija resursa je odobrena i potvrđena za rad s određenim vremenom angažmana.</span><span class="sxs-lookup"><span data-stu-id="5117f-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="5117f-123">**Uvjetna rezervacija** – Rezervacija resursa uvjetno je potvrđena za rad s određenim vremenom angažmana.</span><span class="sxs-lookup"><span data-stu-id="5117f-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="5117f-124">U sljedećem postupku objašnjava se način stvaranja projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="5117f-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="5117f-125">Stvaranje projektnog tima</span><span class="sxs-lookup"><span data-stu-id="5117f-125">Create a project team</span></span>

1. <span data-ttu-id="5117f-126">Na stranici s popisom **Svi projekti** odaberite projekt, a zatim odaberite **Uredi**.</span><span class="sxs-lookup"><span data-stu-id="5117f-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="5117f-127">Na kartici **Projektni tim i planiranje** u polju **Planiraj datum završetka** unesite datum koji nastupa mjesec dana nakon datuma početka rasporeda.</span><span class="sxs-lookup"><span data-stu-id="5117f-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="5117f-128">Na primjer, ako je datum početka rasporeda 24. lipnja 2017. (24.6.2017.), unesite **24.07.2017.**.</span><span class="sxs-lookup"><span data-stu-id="5117f-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="5117f-129">Odaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="5117f-129">Select **Add**.</span></span>
4. <span data-ttu-id="5117f-130">U oknu **Dodaj uloge projektu** u polju **Uloga**, odaberite **Voditelj projekta višeg ranga**.</span><span class="sxs-lookup"><span data-stu-id="5117f-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="5117f-131">Odaberite **Potrebne kompetencije**.</span><span class="sxs-lookup"><span data-stu-id="5117f-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="5117f-132">Svojstva koja ste prethodno postavili za ulogu voditelja projekta višeg ranga , na stranici **Odaberi svojstva** odabiru se prema zadanim postavkama.</span><span class="sxs-lookup"><span data-stu-id="5117f-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="5117f-133">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="5117f-133">Select **OK**.</span></span>
7. <span data-ttu-id="5117f-134">Na stranici **Dodaj uloge projektu** u polje **Broj resursa** unesite **1**.</span><span class="sxs-lookup"><span data-stu-id="5117f-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="5117f-135">U polju **Resurs** pretraživanje prikazuje sve resurse koji imaju potrebne kompetencije.</span><span class="sxs-lookup"><span data-stu-id="5117f-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="5117f-136">Odaberite **Daniel Petek**, a zatim odaberite **Stvori**.</span><span class="sxs-lookup"><span data-stu-id="5117f-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="5117f-137">Na stranici **Projekt** odaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="5117f-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="5117f-138">U oknu **Dodaj uloge projektu** u polju **Uloga**, odaberite **Član tima**.</span><span class="sxs-lookup"><span data-stu-id="5117f-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="5117f-139">U polje **Broj resursa** unesite **5**.</span><span class="sxs-lookup"><span data-stu-id="5117f-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="5117f-140">Kliknite **Stvori**.</span><span class="sxs-lookup"><span data-stu-id="5117f-140">Select **Create**.</span></span>
12. <span data-ttu-id="5117f-141">Na stranici **Projekti** odaberite **Popuni resurs**.</span><span class="sxs-lookup"><span data-stu-id="5117f-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="5117f-142">Nadzirite projektne timove</span><span class="sxs-lookup"><span data-stu-id="5117f-142">Monitor project teams</span></span>
1. <span data-ttu-id="5117f-143">Na stranici **Svi projekti** odaberite vezu **Projekt ID** za projekt **2. faza nadogradnje XYZ**.</span><span class="sxs-lookup"><span data-stu-id="5117f-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="5117f-144">Na Brzoj kartici **Projektni tim i planiranje** provjerite jesu li navedeni resursi projekta točni.</span><span class="sxs-lookup"><span data-stu-id="5117f-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]