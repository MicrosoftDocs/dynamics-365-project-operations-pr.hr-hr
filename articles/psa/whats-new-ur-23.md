---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 23, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006457"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="26c31-103">Project Service Automation, izdanje ažuriranja 23, V3</span><span class="sxs-lookup"><span data-stu-id="26c31-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="26c31-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="26c31-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="26c31-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="26c31-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="26c31-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="26c31-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="26c31-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="26c31-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="26c31-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="26c31-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="26c31-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 23.</span><span class="sxs-lookup"><span data-stu-id="26c31-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="26c31-110">Broj izrade ove verzije jest V 3.10.34.30, a ona je uglavnom dostupna putem samostalnog ažuriranja u kolovozu 2020.</span><span class="sxs-lookup"><span data-stu-id="26c31-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="26c31-111">Izdanje ažuriranja 23</span><span class="sxs-lookup"><span data-stu-id="26c31-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="26c31-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="26c31-112">Bug fixes</span></span>

<span data-ttu-id="26c31-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="26c31-113">**Time and Expense**</span></span>

<span data-ttu-id="26c31-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="26c31-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="26c31-115">Obradite rubni slučaj u mogućnosti **Izbriši člana projektnog tima** kako biste omogućili značajnu iznimku.</span><span class="sxs-lookup"><span data-stu-id="26c31-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="26c31-116">Uvoz zadataka rezultira praznim zaslonom za uklanjanje.</span><span class="sxs-lookup"><span data-stu-id="26c31-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="26c31-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="26c31-117">**Resource Management**</span></span>

<span data-ttu-id="26c31-118">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="26c31-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="26c31-119">**Kartica resursa mreže za uporabu resursa** prikazuje netočne podatke kada je vremenska ljestvica dulja od pet dana.</span><span class="sxs-lookup"><span data-stu-id="26c31-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="26c31-120">Kada klijenti stvarju resurs koji se može rezervirati, dodatak povremeno ne uspijeva automatski dodati resurs u grupu sustava Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="26c31-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="26c31-121">Prikaz **Usklađivanje** pogrešno prikazuje ručne konture u prikazu **Tjedan** ili **Mjesec**.</span><span class="sxs-lookup"><span data-stu-id="26c31-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="26c31-122">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="26c31-122">**Project Management**</span></span>

<span data-ttu-id="26c31-123">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="26c31-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="26c31-124">Prekomjerni broj entiteta **Dohvati više za korisničke postavke** uzrokuju pogoršanje značajki za odobravanje projekata i ostalih operacija.</span><span class="sxs-lookup"><span data-stu-id="26c31-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="26c31-125">Pretraživanje rešetke resursa **Planiranje zadataka** ograničen je na prikaz samo do pet članova iz projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="26c31-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="26c31-126">Pretraživanje rešetke resursa **Planiranje zadataka** ne filtrira neaktivne resurse.</span><span class="sxs-lookup"><span data-stu-id="26c31-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="26c31-127">Ručni način rada ne radi prema očekivanjima u strukturnoj analizi rada na planiranju projekta.</span><span class="sxs-lookup"><span data-stu-id="26c31-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="26c31-128">Rešetka **Planiranje zadataka** prikazuje **Kategorije neaktivnih transakcija**.</span><span class="sxs-lookup"><span data-stu-id="26c31-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="26c31-129">Rešetka **Dodjela resursa** pogrešno se zaokružuje kada projekt ima više zadataka.</span><span class="sxs-lookup"><span data-stu-id="26c31-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="26c31-130">Vrijednosti zaokruživanja razlikuju se između planiranog i stvarnog troška za jedan zadatak.</span><span class="sxs-lookup"><span data-stu-id="26c31-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="26c31-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="26c31-131">**Sales**</span></span>

<span data-ttu-id="26c31-132">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="26c31-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="26c31-133">Dvostrukim klikom mogućnosti **Dohvati sve kategorije transakcija** stvara se više redaka.</span><span class="sxs-lookup"><span data-stu-id="26c31-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]