---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 29, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664634"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="12739-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 29, V3</span><span class="sxs-lookup"><span data-stu-id="12739-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="12739-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="12739-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="12739-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="12739-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="12739-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="12739-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="12739-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="12739-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="12739-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="12739-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="12739-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 29.</span><span class="sxs-lookup"><span data-stu-id="12739-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="12739-110">Ova verzija ima broj izrade V3.10.47.7 i općenito je dostupna putem samostalnog ažuriranja u veljači 2021.</span><span class="sxs-lookup"><span data-stu-id="12739-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="12739-111">Izdanje ažuriranja 29</span><span class="sxs-lookup"><span data-stu-id="12739-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="12739-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="12739-112">Bug fixes</span></span>

<span data-ttu-id="12739-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="12739-113">**Time and Expense**</span></span>

<span data-ttu-id="12739-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="12739-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="12739-115">Korisnici ne mogu vidjeti radno vrijeme zabilježeno neradnim danima u rešetki vremenskog unosa.</span><span class="sxs-lookup"><span data-stu-id="12739-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="12739-116">Odobreni unosi troškova mogu se uređivati na rešetki.</span><span class="sxs-lookup"><span data-stu-id="12739-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="12739-117">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="12739-117">**Project Management**</span></span>

<span data-ttu-id="12739-118">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="12739-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="12739-119">Nedostaje logika provjere valjanosti kako bi se osiguralo da sati rada resursa na zadatku ne mogu biti negativni.</span><span class="sxs-lookup"><span data-stu-id="12739-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="12739-120">Prilagođena radnja, **AssignResourcesForTask** ažurira sva polja, a ne samo promijenjena.</span><span class="sxs-lookup"><span data-stu-id="12739-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="12739-121">Pri kopiranju projekta u okruženje s dodacima ili tijekovima rada koji su registrirani na događaju **CreateProject**, atribut **msdyn_bulkgenerationstatus** ne ažurira se ako **CopyWBSToProject** ne uspije.</span><span class="sxs-lookup"><span data-stu-id="12739-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="12739-122">Kada proširite kalendar projekta, radni dani se ne sortiraju uzlazno, što uzrokuje neuspjeh ažuriranja nekih projektnih zadataka.</span><span class="sxs-lookup"><span data-stu-id="12739-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="12739-123">Promjena Voditelja projekta na postojećem projektu pokreće zadanu logiku organizacijske jedinice.</span><span class="sxs-lookup"><span data-stu-id="12739-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="12739-124">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="12739-124">**Sales**</span></span>

<span data-ttu-id="12739-125">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="12739-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="12739-126">Kartica **Izvršenje ugovora** na stranici **Ugovor** nečujno ne uspijeva tijekom inicijalizacije ako ne postoje redci ugovora.</span><span class="sxs-lookup"><span data-stu-id="12739-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
