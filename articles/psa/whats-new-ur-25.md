---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 25, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948862"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="e632d-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 25, V3</span><span class="sxs-lookup"><span data-stu-id="e632d-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e632d-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e632d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e632d-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="e632d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e632d-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e632d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e632d-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="e632d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e632d-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e632d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e632d-109">U ovoj temi navode se značajke i popravci koji su novi ili promijenjeni za aplikaciju Project Service Automation V3, izdanje ažuriranja 25. Ova verzija ima broj međuverzije V 3.10.43.76 i općenito je dostupna putem samoažuriranja u listopadu 2020.</span><span class="sxs-lookup"><span data-stu-id="e632d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="e632d-110">Izdanje ažuriranja 25</span><span class="sxs-lookup"><span data-stu-id="e632d-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e632d-111">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="e632d-111">Bug fixes</span></span>

<span data-ttu-id="e632d-112">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="e632d-112">**Time and Expense**</span></span>

<span data-ttu-id="e632d-113">Popravljen je sljedeći profil:</span><span class="sxs-lookup"><span data-stu-id="e632d-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="e632d-114">Grafikon unosa vremena koji prikazuje dodatne podatke na temelju prevelikog intervala koji se dohvaća.</span><span class="sxs-lookup"><span data-stu-id="e632d-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="e632d-115">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="e632d-115">**Resource Management**</span></span>

<span data-ttu-id="e632d-116">Popravljen je sljedeći profil:</span><span class="sxs-lookup"><span data-stu-id="e632d-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="e632d-117">Dodan je kod za alat Package deployer kako bi se preskočio uvoz zakrpe za aplikaciju Universal Resource Scheduling ako već postoji zakrpa više verzije.</span><span class="sxs-lookup"><span data-stu-id="e632d-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="e632d-118">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="e632d-118">**Project Management**</span></span>

<span data-ttu-id="e632d-119">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="e632d-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="e632d-120">Ispravljena neusklađenost zaokruživanja i tečajne razlike koja je rezultirala netočnim planiranim troškovima u rešetki za praćenje projekta.</span><span class="sxs-lookup"><span data-stu-id="e632d-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="e632d-121">Podrška mogućnosti prikaza dvije ili više rešetki za reakciju na obrascu **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e632d-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="e632d-122">Pod uvjetom da se provjera valjanosti odnosi na mogućnost dodijele zadatka nakon datuma završetka kalendara, što rezultira neuspjelom dodjelom resursa.</span><span class="sxs-lookup"><span data-stu-id="e632d-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="e632d-123">Poboljšano rukovanje pogreškama za rješavanje iznimke reference vrijednosti jednake nuli generirane iz sljedećeg:</span><span class="sxs-lookup"><span data-stu-id="e632d-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="e632d-124">Programski dodatak **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="e632d-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="e632d-125">**PreValidateProjectTaskCreate** kada se projektni zadatak stvori bez povezanog projekta</span><span class="sxs-lookup"><span data-stu-id="e632d-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="e632d-126">Programski dodatak **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="e632d-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="e632d-127">Programski dodatak **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="e632d-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="e632d-128">Programski dodatak **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="e632d-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="e632d-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e632d-129">**Sales**</span></span>

<span data-ttu-id="e632d-130">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="e632d-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="e632d-131">Poboljšano rukovanje pogreškama za rješavanje iznimki reference koja ima vrijednost jednaku nuli generiranih iz **Kopiraj projekt: Upravljanje procjenama pomoćnih resursa**.</span><span class="sxs-lookup"><span data-stu-id="e632d-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="e632d-132">**Nije spremno za fakturiranje** na **Zaostatak naplate vremena i materijala** ne čisti status naplate.</span><span class="sxs-lookup"><span data-stu-id="e632d-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="e632d-133">Ispravljeno pogrešno označavanje gumba **Cijene** na karticama **Cijena uloge** i **Predmeti iz kataloga**.</span><span class="sxs-lookup"><span data-stu-id="e632d-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]