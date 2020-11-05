---
title: Nadogradnja početne stranice
description: Ova tema pokazuje gdje pronaći važne informacije o novim i promijenjenim značajkama u sustavu Dynamics 365 Project Service Automation i procesu nadogradnje na najnoviju verziju.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073469"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="e5b99-103">Nadogradnja početne stranice</span><span class="sxs-lookup"><span data-stu-id="e5b99-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="e5b99-104">Nadogradnja aplikacije PSA s verzije 2.x ili 1.x na verziju 3.x</span><span class="sxs-lookup"><span data-stu-id="e5b99-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="e5b99-105">Nove instance</span><span class="sxs-lookup"><span data-stu-id="e5b99-105">New instances</span></span>

<span data-ttu-id="e5b99-106">Od 17. svibnja 2019. godine kada je aplikacija Project Service Automation odabrana tijekom pripreme nove instance, prema zadanim je postavkama instalirana verzija 3.x.</span><span class="sxs-lookup"><span data-stu-id="e5b99-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="e5b99-107">Postojeće instance</span><span class="sxs-lookup"><span data-stu-id="e5b99-107">Existing instances</span></span>

<span data-ttu-id="e5b99-108">Klijenti koji su imali instancu PSA verzije 2.x i trebali su se nadograditi na verziju 3.x, što je verzija PSA koja je temeljena na objedinjenom klijentskom sučelju (UCI), ranije su se morali obratiti podršci i pružiti pojedinosti o svojoj instanci, tako da podrška može omogućiti instancu za nadogradnju na verziju 3.x.</span><span class="sxs-lookup"><span data-stu-id="e5b99-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="e5b99-109">Od 1. ožujka 2020. klijenti koji imaju instancu PSA verzije 2.x i trebaju je nadograditi na verziju 3.x, moći će nadograditi svoje instance izravno s portala administratora bez potrebe za obraćanjem Microsoftovoj službi za podršku.</span><span class="sxs-lookup"><span data-stu-id="e5b99-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="e5b99-110">Verzija 3.x aplikacije PSA uključuje značajne promjene.</span><span class="sxs-lookup"><span data-stu-id="e5b99-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="e5b99-111">Izgrađena je na okviru objedinjenog sučelja kako bi pomogla u pružanju poboljšanog korisničkog doživljaja.</span><span class="sxs-lookup"><span data-stu-id="e5b99-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="e5b99-112">Redizajnirana aplikacija donosi dosljedno, objedinjeno korisničko sučelje (UI), a slijedi načela responzivnog dizajna za optimalan prikaz na bilo kojoj veličini zaslona ili bilo kojem uređaju.</span><span class="sxs-lookup"><span data-stu-id="e5b99-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="e5b99-113">Aplikacija donosi i druge promjene.</span><span class="sxs-lookup"><span data-stu-id="e5b99-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="e5b99-114">Neka od područja koja su promijenjena uključuju određivanje cijena, rezervacije i dodjeljivanje resursa, vremena, troškova i odobrenja.</span><span class="sxs-lookup"><span data-stu-id="e5b99-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="e5b99-115">Prije početka postupka nadogradnje preporučujemo da dovršite sljedeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="e5b99-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="e5b99-116">Provjerite jesu li sustav Dynamics 365 Field Service i aplikacija Project Service Automation instalirani na identificiranoj nstanci.</span><span class="sxs-lookup"><span data-stu-id="e5b99-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="e5b99-117">Ako su instalirana oba rješenja, trebali biste planirati nadogradnju prije nego što nastavite uobičajeno korištenje instance.</span><span class="sxs-lookup"><span data-stu-id="e5b99-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="e5b99-118">Pažljivo pregledajte sljedeće teme.</span><span class="sxs-lookup"><span data-stu-id="e5b99-118">Carefully review the following topics.</span></span> <span data-ttu-id="e5b99-119">Svijest i razumijevanje promjena između verzija pomoći će vam s postupkom nadogradnje.</span><span class="sxs-lookup"><span data-stu-id="e5b99-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="e5b99-120">Te teme pružaju informacije o glavnim promjenama u aplikaciji PSA, zajedno s razmatranjima i preporukama za planiranje nadogradnje na verziju 3.x.</span><span class="sxs-lookup"><span data-stu-id="e5b99-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="e5b99-121">Što je novo ili promijenjeno u aplikaciji Project Service Automation, verzija 3</span><span class="sxs-lookup"><span data-stu-id="e5b99-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="e5b99-122">Razmatranja nadogradnje – Project Service Automation, verzija 2.x ili 1.x na verziju 3</span><span class="sxs-lookup"><span data-stu-id="e5b99-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="e5b99-123">Nadogradite instancu za testiranje da biste procijenili promjene u implementaciji prije nadogradnje proizvodne instance.</span><span class="sxs-lookup"><span data-stu-id="e5b99-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="e5b99-124">Nakon što pregledate teme koje su ranije spomenute i spremni ste za nadogradnju aplikacije PSA, verzija 3.x ili verzija temeljena na UCI-ju, pošaljite zahtjev Microsoftovoj podršci da biste nadogradnju učinili dostupnom iz centra za administratore.</span><span class="sxs-lookup"><span data-stu-id="e5b99-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="e5b99-125">U zahtjevu navedite pojedinosti o svojoj instanci.</span><span class="sxs-lookup"><span data-stu-id="e5b99-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="e5b99-126">Starije verzije aplikacije PSA (verzija 2.x aplikacije PSA) u novostvorenoj instanci</span><span class="sxs-lookup"><span data-stu-id="e5b99-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="e5b99-127">Od 17. svibnja 2019. godine sve će nove instance imati UCI kao zadani klijent.</span><span class="sxs-lookup"><span data-stu-id="e5b99-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="e5b99-128">Verzija 3.x aplikacije PSA i Field Service verzija 8.x za usklađivanje će s ovom promjenom biti dodijeljene prema zadanim postavkama jer su te verzije dizajnirane za rad s klijentskim UCI-jom.</span><span class="sxs-lookup"><span data-stu-id="e5b99-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="e5b99-129">Od 1. ožujka 2020. klijenti sustava Dynamics PSA više neće moći stvarati nova okruženja sa starijim verzijama PSA, na primjer PSA verzije 2.x ili starije.</span><span class="sxs-lookup"><span data-stu-id="e5b99-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="e5b99-130">Svako novo okruženje dobit će samo PSA verzije 3.x.</span><span class="sxs-lookup"><span data-stu-id="e5b99-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="e5b99-131">Za najbolji doživljaj prilikom korištenja starijih verzija aplikacija Field service i PSA, idite na **Postavke sustava** , a za polje **Koristi samo novo objedinjeno sučelje (preporučeno)** , odaberite **Ne** jer ove verzije nisu dizajnirane da se ispravno učitavaju u UCI-ju.</span><span class="sxs-lookup"><span data-stu-id="e5b99-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="e5b99-132">Nakon što ste isključili UCI, možete otvoriti i pokrenuti ove verzije aplikacija Field Service i PSA pomoću starog web-klijenta.</span><span class="sxs-lookup"><span data-stu-id="e5b99-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
