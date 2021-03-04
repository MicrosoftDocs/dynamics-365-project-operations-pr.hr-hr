---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 28, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150614"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="51031-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 28, V3</span><span class="sxs-lookup"><span data-stu-id="51031-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="51031-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="51031-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="51031-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="51031-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="51031-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="51031-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="51031-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="51031-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="51031-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="51031-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="51031-109">U ovoj temi navode se značajke i popravci koji su novi ili promijenjeni za aplikaciju Project Service Automation V3, izdanje ažuriranja 28. Ova verzija ima broj međuverzije V 3.10.46.32 i općenito je dostupna putem samoažuriranja u siječnju 2021.</span><span class="sxs-lookup"><span data-stu-id="51031-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="51031-110">Izdanje ažuriranja 28</span><span class="sxs-lookup"><span data-stu-id="51031-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="51031-111">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="51031-111">Bug fixes</span></span>

<span data-ttu-id="51031-112">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="51031-112">**Time and Expense**</span></span>

<span data-ttu-id="51031-113">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="51031-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="51031-114">Korisnici mogu upotrijebiti **Skupno uređivanje** za ažuriranje vremenskih zapisa koji su odobreni i poslani.</span><span class="sxs-lookup"><span data-stu-id="51031-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="51031-115">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="51031-115">**Project Management**</span></span>

<span data-ttu-id="51031-116">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="51031-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="51031-117">U slučajevima kada se GUID zadatka tumači kao broj, zadaci se ne mogu otvoriti za uređivanje s pomoću mogućnosti **Uredi zadatak** s vrpce na stranici **Strukturna analiza rada**.</span><span class="sxs-lookup"><span data-stu-id="51031-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="51031-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="51031-118">**Sales**</span></span>

<span data-ttu-id="51031-119">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="51031-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="51031-120">Iznimka nulte reference generira se kada se pozove dodatak **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="51031-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="51031-121">Mogućnost **Označi spremnim za fakturiranje** na rešetki kontrolne točke samo djelomično ažurira atribute, osim atributa **Status fakture**, koji se ažurira.</span><span class="sxs-lookup"><span data-stu-id="51031-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

