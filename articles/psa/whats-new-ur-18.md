---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 18, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119859"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="ac446-103">Project Service Automation, izdanje ažuriranja 18, V3</span><span class="sxs-lookup"><span data-stu-id="ac446-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="ac446-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ac446-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ac446-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="ac446-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ac446-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ac446-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ac446-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="ac446-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="ac446-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ac446-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ac446-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 18.</span><span class="sxs-lookup"><span data-stu-id="ac446-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="ac446-110">Ova verzija ima broj međuverzije V3.10.8.12 i uglavnom je dostupna putem samostalnog ažuriranja u travnju 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="ac446-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="ac446-111">Izdanje ažuriranja 18</span><span class="sxs-lookup"><span data-stu-id="ac446-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ac446-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="ac446-112">Bug fixes</span></span>

<span data-ttu-id="ac446-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="ac446-113">**Time and Expense**</span></span>

- <span data-ttu-id="ac446-114">Rješeno: Mogućnosti **Podsjetnik**, **Zahtjev** i **Otkaži odobrenje** odbacuju iznimke s nejasnim porukama o pogrešci.</span><span class="sxs-lookup"><span data-stu-id="ac446-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="ac446-115">riješeno: Kada mogućnost **Otkaži odobrenje** ne uspije za trošak, relevantna se pogreška iznimke ne odbacuje.</span><span class="sxs-lookup"><span data-stu-id="ac446-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="ac446-116">Riješeno: Rešetka vremenskog unosa pogrešno obrađuje neradne dane u Australiji nakon prebacivanja ljetnog računanja vremena (DST) u listopadu.</span><span class="sxs-lookup"><span data-stu-id="ac446-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="ac446-117">Riješeno: Nepravilna zadana logika sprječava slanje troškova.</span><span class="sxs-lookup"><span data-stu-id="ac446-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="ac446-118">Riješeno: Kad odobrenje unosa ne uspije, odobrenje ostaje u stanju **U tijeku**.</span><span class="sxs-lookup"><span data-stu-id="ac446-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="ac446-119">Riješeno: SQL pogreške na skupnim odobrenjima (zastoj / vremensko ograničenje).</span><span class="sxs-lookup"><span data-stu-id="ac446-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="ac446-120">Riješeno: Značajni problemi koje su korisnici imali s performansama uzrokovani su ažuriranjem članova tima tijekom odobravanja vremenskih unosa.</span><span class="sxs-lookup"><span data-stu-id="ac446-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="ac446-121">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="ac446-121">**Project Management**</span></span>

- <span data-ttu-id="ac446-122">Riješeno: Obavijest o vremenskoj zoni premještena je s prikaza **Usklađivanje** na glavni obrazac **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ac446-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="ac446-123">Riješeno: Predložak kalendara nije se ispravno zadao kada se otvara novi obrazac projekta.</span><span class="sxs-lookup"><span data-stu-id="ac446-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="ac446-124">Riješeno: Za preglednike koji se temelje na kromu korisnici ne mogu lako odabrati prethodne zadatke za brisanje.</span><span class="sxs-lookup"><span data-stu-id="ac446-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="ac446-125">Riješeno: Stvaranje ili kopiranje mogućnosti **Projekt iz praznog predloška** dobiva nepovezane zadatke.</span><span class="sxs-lookup"><span data-stu-id="ac446-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="ac446-126">Riješeno: U specifičnim rubnim slučajevima, stvaranje novog zadatka iz rešetke zadatka pravi dvostruke zapise.</span><span class="sxs-lookup"><span data-stu-id="ac446-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="ac446-127">Riješeno: U ručnom načinu rada korisnici ne mogu ažurirati datume početka zadatka tako da budu kasniji od spremljenog trenutačnog datuma.</span><span class="sxs-lookup"><span data-stu-id="ac446-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="ac446-128">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="ac446-128">**Resource Management**</span></span>

- <span data-ttu-id="ac446-129">Riješeno: Redak međuzbroja prikaza **Usklađivanje** pogrešno izračunava odstupanje rezervacije nakon produženja rezervacije.</span><span class="sxs-lookup"><span data-stu-id="ac446-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="ac446-130">Rješeno: Prikaz mogućnosti **Usklađivanje** pogrešno prikazuje dodjele resursa kada resurs koji se može rezervirati ima kalendar koji se ne poklapa s kalendarom projekta.</span><span class="sxs-lookup"><span data-stu-id="ac446-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="ac446-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ac446-131">**Sales**</span></span>

- <span data-ttu-id="ac446-132">Riješeno: Kada se vremenski unosi ponovno odobre (**Odobri > Odustani >** odobri ponovno), stvara se dvostruki nenaplativi trenutak.</span><span class="sxs-lookup"><span data-stu-id="ac446-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
