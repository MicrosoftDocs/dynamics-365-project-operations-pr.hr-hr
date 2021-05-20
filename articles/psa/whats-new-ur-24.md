---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 24, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 956dcd2a06fad1eec488ad81bec2de4bd0550e82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948906"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="3e702-103">Project Service Automation, izdanje ažuriranja 24, V3</span><span class="sxs-lookup"><span data-stu-id="3e702-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3e702-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3e702-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3e702-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="3e702-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3e702-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3e702-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3e702-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="3e702-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3e702-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3e702-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3e702-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 24.</span><span class="sxs-lookup"><span data-stu-id="3e702-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="3e702-110">Broj izrade ove verzije jest V 3.10.42.43, a ona je uglavnom dostupna putem samostalnog ažuriranja u listopadu 2020.</span><span class="sxs-lookup"><span data-stu-id="3e702-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="3e702-111">Izdanje ažuriranja 24</span><span class="sxs-lookup"><span data-stu-id="3e702-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3e702-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="3e702-112">Bug fixes</span></span>

<span data-ttu-id="3e702-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3e702-113">**Sales**</span></span>

<span data-ttu-id="3e702-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3e702-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3e702-115">Problem tijekom postavljanja zadanog cjenika proizvoda.</span><span class="sxs-lookup"><span data-stu-id="3e702-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="3e702-116">Izvršavanje dobivenih ponuda sporo je zbog ugrađenog cjenika i kopija zapisa cijena uloga.</span><span class="sxs-lookup"><span data-stu-id="3e702-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="3e702-117">**Ugovor o projektu / prodajno središte** > **Stavka retka proizvoda / količina retka narudžbe** automatski se zaokružuje na najbliži cijeli broj.</span><span class="sxs-lookup"><span data-stu-id="3e702-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="3e702-118">Tijekom čitanja cjenika podignite do povlastica sustava.</span><span class="sxs-lookup"><span data-stu-id="3e702-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="3e702-119">Kopirajte polja adrese klijenta **address1_freighttermscode** i **address1_shippingmethodcode** u ponudu / narudžbu.</span><span class="sxs-lookup"><span data-stu-id="3e702-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="3e702-120">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="3e702-120">**Time and Expense**</span></span>

<span data-ttu-id="3e702-121">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3e702-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="3e702-122">**Rešetka za unos vremena** ne podržava reakciju vremena **Samo datum**.</span><span class="sxs-lookup"><span data-stu-id="3e702-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="3e702-123">**Vremenski unos** ne osvježava se automatski.</span><span class="sxs-lookup"><span data-stu-id="3e702-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="3e702-124">Potrebno je ručno osvježavanje.</span><span class="sxs-lookup"><span data-stu-id="3e702-124">A manual refresh is required.</span></span>
- <span data-ttu-id="3e702-125">Nije moguće uvesti vremenske unose iz zadatka kada postoji prekid (0 sati) u zadacima resursa.</span><span class="sxs-lookup"><span data-stu-id="3e702-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="3e702-126">Kada stvarate vremenski unos, postavite početak na isto kao **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="3e702-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="3e702-127">Ponovno omogućite skupno uređivanje za vremenski unos.</span><span class="sxs-lookup"><span data-stu-id="3e702-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="3e702-128">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="3e702-128">**Resource Management**</span></span>

<span data-ttu-id="3e702-129">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3e702-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="3e702-130">Pokušaj ažuriranja statusa rezervacije unutar dana bez zahtjeva izbacit će iznimku null-ref.</span><span class="sxs-lookup"><span data-stu-id="3e702-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="3e702-131">Pogreška pri učitavanju mogućnosti **Prikaz usklađivanja**.</span><span class="sxs-lookup"><span data-stu-id="3e702-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="3e702-132">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="3e702-132">**Project Management**</span></span>

<span data-ttu-id="3e702-133">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3e702-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="3e702-134">U mogućnosti **Raspored projekta**, pri promjeni iz **Ručno** u **Automatski**, automatsko se spremanje ne dovršava.</span><span class="sxs-lookup"><span data-stu-id="3e702-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="3e702-135">Troškovi izdatka ne bi se trebali računati prema odstupanjima na stavci **Rešetka za praćenje projekata**.</span><span class="sxs-lookup"><span data-stu-id="3e702-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="3e702-136">Nedosljedno ponašanje stupaca **Oznaka procjena** tijekom opterećenja naspram promjene vrste **Vremenska faza**.</span><span class="sxs-lookup"><span data-stu-id="3e702-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="3e702-137">Stvarni trošak projekta možda neće odražavati ukupne iznose iz mogućnosti **Stvarni podaci**.</span><span class="sxs-lookup"><span data-stu-id="3e702-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="3e702-138">**Procijenjeni datum završetka** na kartici **Sažetak** ne podudara se sa stavkom **SAR raspored**.</span><span class="sxs-lookup"><span data-stu-id="3e702-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="3e702-139">**Ažuriranje stvarnih sati** na outdent ne radi ispravno.</span><span class="sxs-lookup"><span data-stu-id="3e702-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="3e702-140">Voditelj projekta izvan korijena **BU** ne može stvoriti projekt.</span><span class="sxs-lookup"><span data-stu-id="3e702-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="3e702-141">Promjene u zadatku ili kategoriji u stavci **Procjene troškova** nisu ostale.</span><span class="sxs-lookup"><span data-stu-id="3e702-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="3e702-142">**Kopija ugovora** kopira rasporede faktura i status pokretanja.</span><span class="sxs-lookup"><span data-stu-id="3e702-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="3e702-143">Gumb **Osvježi stvarne podatke** pogrešno izračunava sažetke zadataka.</span><span class="sxs-lookup"><span data-stu-id="3e702-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="3e702-144">Dodatak za aplikaciju Microsoft Project: Ispravite pogrešku reference nule ako neki član tima ima praznu jedinicu resursa.</span><span class="sxs-lookup"><span data-stu-id="3e702-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]