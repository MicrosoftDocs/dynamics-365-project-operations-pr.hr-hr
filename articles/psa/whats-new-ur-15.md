---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 15, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 15, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949310"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="3aec8-103">Project Service Automation, izdanje ažuriranja 15, V3</span><span class="sxs-lookup"><span data-stu-id="3aec8-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3aec8-104">Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="3aec8-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3aec8-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="3aec8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3aec8-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3aec8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3aec8-107">Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="3aec8-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3aec8-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3aec8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3aec8-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 15.</span><span class="sxs-lookup"><span data-stu-id="3aec8-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="3aec8-110">Broj izrade ove verzije jest V3.10.5.28, a ona je uglavnom dostupna putem samostalnog ažuriranja u siječnju 2020.</span><span class="sxs-lookup"><span data-stu-id="3aec8-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="3aec8-111">Izdanje ažuriranja 15</span><span class="sxs-lookup"><span data-stu-id="3aec8-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="3aec8-112">Poboljšanja</span><span class="sxs-lookup"><span data-stu-id="3aec8-112">Enhancements</span></span>

- <span data-ttu-id="3aec8-113">Upravljanje projektom</span><span class="sxs-lookup"><span data-stu-id="3aec8-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3aec8-114">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="3aec8-114">Bug fixes</span></span>

- <span data-ttu-id="3aec8-115">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="3aec8-115">Time and Expense</span></span>

  - <span data-ttu-id="3aec8-116">Popravljeno: Dodavanje upravljanja pogreškama u tijeku u prikazu usklađivanja.</span><span class="sxs-lookup"><span data-stu-id="3aec8-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="3aec8-117">Popravljeno: Središte resursa projekta: Preimenujte stavku **Količina** kako biste smanjili nejasnoće.</span><span class="sxs-lookup"><span data-stu-id="3aec8-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="3aec8-118">Popravljeno: Prilagodite prikaz **Kopiraj stupce unosa vremena** kako bi obuhvaćao vrstu.</span><span class="sxs-lookup"><span data-stu-id="3aec8-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="3aec8-119">Popravljeno: Uređivanje trajanja unosa vremena u prikazu rešetke s pomoću decimalnih brojeva stvara nepoznatu pogrešku za neke brojeve.</span><span class="sxs-lookup"><span data-stu-id="3aec8-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="3aec8-120">Upravljanje projektom</span><span class="sxs-lookup"><span data-stu-id="3aec8-120">Project Management</span></span>

  - <span data-ttu-id="3aec8-121">Popravljeno: Padajući izbornik mogućnosti **Upotrijebi u prikazu praćenja** sada se proširuje na temelju širine mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="3aec8-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="3aec8-122">Popravljeno: Kada upravljate projektima u vremenskoj zoni +13, proračuni zadataka mogu prikazati netočne rezultate.</span><span class="sxs-lookup"><span data-stu-id="3aec8-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="3aec8-123">Popravljeno: Mogućnost **Vrijeme završetka za člana tima** ispravljeno je u slučaju uporabe 24-satnog kalendara.</span><span class="sxs-lookup"><span data-stu-id="3aec8-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="3aec8-124">Popravljeno: Ponovno je aktivirana mogućnost **BPF** u glavnom obrascu **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="3aec8-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="3aec8-125">Popravljeno: Izračuni dodjela više ne zanemaruju jedan dan.</span><span class="sxs-lookup"><span data-stu-id="3aec8-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="3aec8-126">Popravljeno: Novi natpis obavijesti dodan je obrascu projekta kada se vremenska zona korisnika i projekta razlikuje.</span><span class="sxs-lookup"><span data-stu-id="3aec8-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="3aec8-127">Sales</span><span class="sxs-lookup"><span data-stu-id="3aec8-127">Sales</span></span>

  - <span data-ttu-id="3aec8-128">Popravljeno: Pretraživanje kategorije procjene troškova može se upotrebljavati za filtriranje duplikata.</span><span class="sxs-lookup"><span data-stu-id="3aec8-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="3aec8-129">Popravljeno: Kod u stavci **PluginDomain.ExecuteInTryCatchBlock(..)** više ne skriva izvorište iznimke.</span><span class="sxs-lookup"><span data-stu-id="3aec8-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="3aec8-130">Popravljeno: Više se ne prikazuje poruka o pogrešci u stavci **Pretraživanje projekta** u obrascu **Redak ponude** kada ima više od 1000 projekata.</span><span class="sxs-lookup"><span data-stu-id="3aec8-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="3aec8-131">Popravljeno: Rešetka za procjenu rada i troškova **Procjene** sada prikazuje točan simbol valute.</span><span class="sxs-lookup"><span data-stu-id="3aec8-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="3aec8-132">Popravljeno: Nakon što tvrtka ili ustanova ažurira PSA s izdanja ažuriranja 14 u izdanje ažuriranja 15, kartica **Raspored** više se ne prikazuje prazna u obrascu **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="3aec8-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]