---
title: Postavljanje resursa projekta
description: U ovoj temi nalaze se informacije o načinu postavljanja ili zahtijevanja resursa za projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073560"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="60663-103">Postavljanje resursa projekta</span><span class="sxs-lookup"><span data-stu-id="60663-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60663-104">Morate postaviti kalendar i povezati ga sa zaposlenikom ili radnikom.</span><span class="sxs-lookup"><span data-stu-id="60663-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="60663-105">Kalendar se upotrebljava za planiranje projekta i radnog vremena resursa rezerviranih za projekt.</span><span class="sxs-lookup"><span data-stu-id="60663-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="60663-106">Tijekom postavljanja kalendara, voditelji projekata mogu izvršiti ujednačavanje resursa kao dio optimizacije resursa.</span><span class="sxs-lookup"><span data-stu-id="60663-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="60663-107">Na temelju kalendarskog rasporeda na resurse se mogu staviti ograničenja.</span><span class="sxs-lookup"><span data-stu-id="60663-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="60663-108">Kalendar možete postaviti na stranicu **Kalendari**.</span><span class="sxs-lookup"><span data-stu-id="60663-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="60663-109">Kada radnika postavite kao resurs projekta, možete birati između radnika koji rade u tvrtki za koju postavljate resurse.</span><span class="sxs-lookup"><span data-stu-id="60663-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="60663-110">Možete odabrati i radnike iz drugih tvrtki unutar svoje tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="60663-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="60663-111">Ti su radnici poznati kao resursi unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="60663-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="60663-112">U slijedećim se postupcima objašnjava način za postavljanje radnika kao resursa projekta u vašoj tvrtki i način za postavljanje resursa unutar tvrtke za projekt.</span><span class="sxs-lookup"><span data-stu-id="60663-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="60663-113">Postavljanje radnika kao resursa projekta</span><span class="sxs-lookup"><span data-stu-id="60663-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="60663-114">Na stranici **Radnici** , na popisu **Radnici** , odaberite radnika kojeg dodajete kao resurs projekta i otvorite zapis za radnika.</span><span class="sxs-lookup"><span data-stu-id="60663-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="60663-115">U oknu radnji odaberite **Projekt** &gt; **Postavljanje** &gt; **Postavljanje projekta**.</span><span class="sxs-lookup"><span data-stu-id="60663-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="60663-116">Odaberite kalendar, a zatim zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="60663-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="60663-117">Također možete odrediti zadane projekte za resurs kao vrstu prethodne dodjele.</span><span class="sxs-lookup"><span data-stu-id="60663-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="60663-118">Prethodne dodjele mogu se upotrebljavati kada voditelj resursa ili voditelj projekata unaprijed zna na kojim će projektima resurs raditi.</span><span class="sxs-lookup"><span data-stu-id="60663-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="60663-119">Prethodne dodjele također se mogu temeljiti na zahtjevu sponzora projekta ili klijenta.</span><span class="sxs-lookup"><span data-stu-id="60663-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="60663-120">Kako biste unaprijed dodijelili projekt, odaberite odgovarajući projekt na stranici **Dodijeli projekte** , na kartici **Projekti** s popisa **Preostali projekti**.</span><span class="sxs-lookup"><span data-stu-id="60663-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="60663-121">Postavljanje resursa unutar tvrtke</span><span class="sxs-lookup"><span data-stu-id="60663-121">Set up an intercompany resource</span></span>

<span data-ttu-id="60663-122">Kada radnika postavite kao resurs unutar tvrtke, morate dovršiti postavljanje i u tvrtki davateljici posudbe i u tvrtki primateljici posudbe.</span><span class="sxs-lookup"><span data-stu-id="60663-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="60663-123">U tvrtki davateljici posudbe</span><span class="sxs-lookup"><span data-stu-id="60663-123">In the lending company</span></span>

1. <span data-ttu-id="60663-124">U Financijama provjerite je li odabrana tvrtka davateljica posudbe, a zatim dovršite postupak iz prethodnog odjeljka „Postavljanje radnika kao resursa projekta”.</span><span class="sxs-lookup"><span data-stu-id="60663-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="60663-125">Na stranici **Računovodstvo unutar tvrtke** odaberite mogućnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="60663-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="60663-126">U polju **ID pravne osobe** , odaberite tvrtku davateljicu posudbe.</span><span class="sxs-lookup"><span data-stu-id="60663-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="60663-127">Prema potrebi popunite preostala polja, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="60663-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="60663-128">Na stranici **Cijena prijenosa** odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="60663-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="60663-129">U polju **Pravna osoba koja prima posudbu** odaberite odgovarajuću tvrtku.</span><span class="sxs-lookup"><span data-stu-id="60663-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="60663-130">Kako biste posudili tvrtki primateljici posudbe samo one resurse koje ste stvorili na početku ovog odjeljka u polju **Resurs** , odaberite naziv resursa koji ste stvorili.</span><span class="sxs-lookup"><span data-stu-id="60663-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="60663-131">Kako biste tvrtki primateljici posudbe omogućili sve resurse tvrtke davateljice posudbe, polje **Resurs** ostavite prazno.</span><span class="sxs-lookup"><span data-stu-id="60663-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="60663-132">Na stranici **Parametri upravljanja projektom i računovodstveni parametri** , na kartici **Unutar tvrtke** , postavite mogućnost **Omogući raspoređivanje resursa i evidencija radnog vremena unutar tvrtke** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="60663-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="60663-133">U tvrtki primateljici posudbe</span><span class="sxs-lookup"><span data-stu-id="60663-133">In the borrowing company</span></span>

- <span data-ttu-id="60663-134">U filtar za pretraživanje na stranici **Popis resursa** unesite naziv resursa koji ste stvorili za tvrtku primateljicu posudbe kako biste provjerili je li ime uključeno u popis resursa za tvrtku primateljicu posudbe.</span><span class="sxs-lookup"><span data-stu-id="60663-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="60663-135">Zahtjevi za resurse za projekt</span><span class="sxs-lookup"><span data-stu-id="60663-135">Request project resources</span></span>
<span data-ttu-id="60663-136">Funkcionalnost za planiranje resursa projekata omogućuju voditeljima resursa samo da raspoređuju resurse osoblja na angažmanima ili projektima.</span><span class="sxs-lookup"><span data-stu-id="60663-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="60663-137">Kako biste omogućili ovu funkciju, dovršite sljedeće zadatke ili provjerite jesu li dovršeni:</span><span class="sxs-lookup"><span data-stu-id="60663-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="60663-138">Postavite nizove brojeva.</span><span class="sxs-lookup"><span data-stu-id="60663-138">Set up number sequences.</span></span>
- <span data-ttu-id="60663-139">Postavite tijekove upravljanja projektima i računovodstva.</span><span class="sxs-lookup"><span data-stu-id="60663-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="60663-140">Omogućite tijekove zahtjeva za resursima.</span><span class="sxs-lookup"><span data-stu-id="60663-140">Enable resource request workflows.</span></span>

<span data-ttu-id="60663-141">Nakon dovršenja prethodnih zadataka, prema potrebi možete izvršiti sljedeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="60663-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="60663-142">Izraditi zahtjev za resursom iz uvjetnog resursa osoblja.</span><span class="sxs-lookup"><span data-stu-id="60663-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="60663-143">Nadzirati zahtjeve za resursom.</span><span class="sxs-lookup"><span data-stu-id="60663-143">Monitor resource requests.</span></span>
- <span data-ttu-id="60663-144">Ispuniti zahtjev za resurse.</span><span class="sxs-lookup"><span data-stu-id="60663-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="60663-145">Zatražiti resurs osoblja iz WBS-a.</span><span class="sxs-lookup"><span data-stu-id="60663-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="60663-146">Rezervirajte resurse za projekt bez zahtjeva za resursom osoblja.</span><span class="sxs-lookup"><span data-stu-id="60663-146">Book resources to a project without having a request for a staffed resource.</span></span>
