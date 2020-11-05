---
title: Integracija programa Microsoft Project Client
description: Planiranje i održavanje rasporeda projekata može biti složeno, pa voditelji projekata trebaju upotrebljavati alate koji im pomažu pri upravljanju tim zadatkom. Integracija s programom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturnom analizom rada na projektu.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073449"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="bd102-104">Integracija programa Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bd102-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd102-105">Planiranje i održavanje rasporeda projekata može biti složeno, pa voditelji projekata trebaju upotrebljavati alate koji im pomažu pri upravljanju tim zadatkom.</span><span class="sxs-lookup"><span data-stu-id="bd102-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="bd102-106">Integracija s programom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturnom analizom rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="bd102-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="bd102-107">Voditelj projekta može objaviti sve promjene natrag na strukturnu analizu rada projekta aplikacije Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="bd102-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="bd102-108">Ako koristite srpanjsko ažuriranje (verzija 10.0.4), morate instalirati zakrpe KB 4054797 i 4055884.</span><span class="sxs-lookup"><span data-stu-id="bd102-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="bd102-109">Konfiguriranje dodatka programu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bd102-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="bd102-110">Kako biste omogućili integraciju s programom Microsoft Project Client, potrebno je instalirati dodatak sustava Microsoft Dynamics 365 na korisnikov klijent aplikacije Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="bd102-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="bd102-111">To se postiže otvaranjem mogućnosti **Radni prostor za upravljanje projektima**.</span><span class="sxs-lookup"><span data-stu-id="bd102-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="bd102-112">•   Kliknite **Konfiguriraj dodatak za klijenta** iz odjeljka radnog prostora **Veze** > **Postavljanje**.</span><span class="sxs-lookup"><span data-stu-id="bd102-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="bd102-113">•   Kliknite **Otvori** , a zatim, kad se od vas to zatraži, kliknite **Pokreni**.</span><span class="sxs-lookup"><span data-stu-id="bd102-113">•   Click **Open** , then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="bd102-114">Otvaranje i uređivanje postojećeg nacrta strukturne analize rada u programu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bd102-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="bd102-115">Ako projekt u aplikaciji Dynamics 365 Finance već ima stvorenu strukturnu analizu rada, ona se može otvoriti u programu Microsoft Project Client ako je strukturna analiza rada u stanju skice.</span><span class="sxs-lookup"><span data-stu-id="bd102-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="bd102-116">Za otvaranje sa stranice **Projekt** , kliknite vezu **Otvori u aplikaciji Microsoft Project** na kartici **Plan**. Ova se stranica također može otvoriti iz programa Microsoft Project Client klikom mogućnosti **Otvori** na kartici **Microsoft Dynamics 365**. S popisa odaberite **Pravna osoba** i **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="bd102-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="bd102-117">Ako upotrebljavate preglednik Internet Explorer, morat ćete kliknuti **Spremi** za ručno otvaranje s mjesta na kojem se nalazi preuzeta datoteka.</span><span class="sxs-lookup"><span data-stu-id="bd102-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="bd102-118">Ili kliknite **Spremi i otvori** kako biste datoteku otvorili u programu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bd102-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="bd102-119">Nemojte preimenovati naziv datoteke tijekom spremanja.</span><span class="sxs-lookup"><span data-stu-id="bd102-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="bd102-120">Prije bilo kakvog uređivanja datoteke s pomoću programa Microsoft Project Client, morate je provjeriti. Kliknite **Provjeri** na kartici **Microsoft Dynamics 365**. To će spriječiti druge korisnike da istodobno uređuju strukturnu analizu rada iz Financija.</span><span class="sxs-lookup"><span data-stu-id="bd102-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="bd102-121">Kako biste objavili strukturnu analizu rada nakon dovršetka uređivanja, kliknite **Prijava** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bd102-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="bd102-122">Ako je projektni tim već dodan projektu u aplikaciji Financije, popis resursa popunit će se članovima tima.</span><span class="sxs-lookup"><span data-stu-id="bd102-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="bd102-123">Ako projektni tim još nije dodan projektu, možete odabrati resurse i izgraditi tim unutar programa Microsoft Project Client tako da kliknete gumb **Resursi** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bd102-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="bd102-124">Sljedeći će se podaci sinkronizirati natrag u aplikaciju Financije kao dio postupka prijave:</span><span class="sxs-lookup"><span data-stu-id="bd102-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="bd102-125">•   Naziv zadatka</span><span class="sxs-lookup"><span data-stu-id="bd102-125">•   Task name</span></span>

<span data-ttu-id="bd102-126">•   Datum početka</span><span class="sxs-lookup"><span data-stu-id="bd102-126">•   Start date</span></span>

<span data-ttu-id="bd102-127">•   Datum završetka</span><span class="sxs-lookup"><span data-stu-id="bd102-127">•   Finish date</span></span>

<span data-ttu-id="bd102-128">•   Prethodnici</span><span class="sxs-lookup"><span data-stu-id="bd102-128">•   Predecessors</span></span>

<span data-ttu-id="bd102-129">•   Nazivi resursa</span><span class="sxs-lookup"><span data-stu-id="bd102-129">•   Resource names</span></span>

<span data-ttu-id="bd102-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="bd102-130">•   Category</span></span>

<span data-ttu-id="bd102-131">•   Kategorija resursa</span><span class="sxs-lookup"><span data-stu-id="bd102-131">•   Resource category</span></span>

<span data-ttu-id="bd102-132">•   Radno vrijeme</span><span class="sxs-lookup"><span data-stu-id="bd102-132">•   Work hours</span></span>

<span data-ttu-id="bd102-133">•   Bilješke</span><span class="sxs-lookup"><span data-stu-id="bd102-133">•   Notes</span></span>

<span data-ttu-id="bd102-134">•   Prioritet</span><span class="sxs-lookup"><span data-stu-id="bd102-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="bd102-135">Ako u datoteku programa Microsoft Project Client dodate neki drugi stupac, neće se spremiti u datoteku i neće se prikazati kad se datoteka ponovno otvori.</span><span class="sxs-lookup"><span data-stu-id="bd102-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bd102-136">Stvaranje strukturne analize rada za postojeći projekt s pomoću programa Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bd102-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bd102-137">Za stvaranje nove strukturne analize rada s pomoću programa Microsoft Project Client slijedite ove korake:</span><span class="sxs-lookup"><span data-stu-id="bd102-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="bd102-138">Otvorite program Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bd102-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bd102-139">Na kartici **Microsoft Dynamics 365** kliknite **Otvori**.</span><span class="sxs-lookup"><span data-stu-id="bd102-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="bd102-140">Odaberite mogućnost **Pravna osoba** za projekt.</span><span class="sxs-lookup"><span data-stu-id="bd102-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="bd102-141">Odaberite **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="bd102-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="bd102-142">Kliknite **Pregledaj** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bd102-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="bd102-143">Kada ste spremni za objavljivanje u Financijama, kliknite **Prijava** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="bd102-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bd102-144">Zamjena postojeće strukturne analize rada za postojeći projekt s pomoću programa Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bd102-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bd102-145">Kako biste stvorili novu strukturnu analizu rada s pomoću programa Microsoft Project Client i zamijenili postojeću strukturnu analizu rada za postojeći projekt, slijedite ove korake:</span><span class="sxs-lookup"><span data-stu-id="bd102-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="bd102-146">Otvorite program Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bd102-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bd102-147">Stvorite raspored u programu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bd102-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bd102-148">Na kartici **Microsoft Dynamics 365** kliknite **Spremi promjene** > **Zamijeni postojeći projekt**.</span><span class="sxs-lookup"><span data-stu-id="bd102-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="bd102-149">Odaberite mogućnost **Pravna osoba** za projekt.</span><span class="sxs-lookup"><span data-stu-id="bd102-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bd102-150">Odaberite **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="bd102-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="bd102-151">Kliknite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="bd102-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="bd102-152">Stvaranje novog projekta iz programa Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="bd102-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="bd102-153">Otvorite program Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bd102-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bd102-154">Stvorite raspored u programu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="bd102-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bd102-155">Na kartici **Microsoft Dynamics 365** kliknite **Spremi promjene** > **Spremi u novi projekt**.</span><span class="sxs-lookup"><span data-stu-id="bd102-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="bd102-156">Odaberite mogućnost **Pravna osoba** za projekt.</span><span class="sxs-lookup"><span data-stu-id="bd102-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bd102-157">Unesite **ID projekta** , ako je potrebno.</span><span class="sxs-lookup"><span data-stu-id="bd102-157">Enter the **Project ID** , if necessary.</span></span>

6.  <span data-ttu-id="bd102-158">Unesite **Naziv proizvoda**.</span><span class="sxs-lookup"><span data-stu-id="bd102-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="bd102-159">Odaberite mogućnost **Vrsta projekta** , **Grupa projekta** i **ID ugovora o projektu**.</span><span class="sxs-lookup"><span data-stu-id="bd102-159">Select the **Project type** , **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="bd102-160">Alternativno, klikom mogućnosti **Novo** možete stvoriti novi ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="bd102-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="bd102-161">Odaberite **Kalendar** koji će se upotrebljavati za raspodjelu resursa.</span><span class="sxs-lookup"><span data-stu-id="bd102-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="bd102-162">Kliknite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="bd102-162">Click **OK**.</span></span>
