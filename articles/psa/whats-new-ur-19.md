---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 19, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126824"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="d2b47-103">Project Service Automation, izdanje ažuriranja 19, V3</span><span class="sxs-lookup"><span data-stu-id="d2b47-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="d2b47-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d2b47-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d2b47-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="d2b47-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d2b47-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d2b47-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d2b47-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="d2b47-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d2b47-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d2b47-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d2b47-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 19.</span><span class="sxs-lookup"><span data-stu-id="d2b47-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="d2b47-110">Ova verzija ima broj međuverzije V3.10.30.41 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="d2b47-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="d2b47-111">Izdanje ažuriranja 19</span><span class="sxs-lookup"><span data-stu-id="d2b47-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d2b47-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="d2b47-112">Bug fixes</span></span>

<span data-ttu-id="d2b47-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="d2b47-113">**Time and Expense**</span></span>

<span data-ttu-id="d2b47-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="d2b47-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="d2b47-115">Pogreške proizašle iz uvoza unosa vremena nisu se ispravno prikazale.</span><span class="sxs-lookup"><span data-stu-id="d2b47-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="d2b47-116">Rešetka za unos vremena ne podržava ponašanje polja **Samo datum**.</span><span class="sxs-lookup"><span data-stu-id="d2b47-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="d2b47-117">Resursi projekta ne mogu stvoriti trošak s pomoću projekta.</span><span class="sxs-lookup"><span data-stu-id="d2b47-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="d2b47-118">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="d2b47-118">**Project Management**</span></span>

<span data-ttu-id="d2b47-119">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="d2b47-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="d2b47-120">Zadatak podređenog uzrokuje pogrešnu procjenu napora tijekom dovršavanja (EAC) izračuna.</span><span class="sxs-lookup"><span data-stu-id="d2b47-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="d2b47-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d2b47-121">**Sales**</span></span>

<span data-ttu-id="d2b47-122">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="d2b47-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="d2b47-123">Radnja **Ponovni izračun** ne funkcionira s pojedinostima retka ugovora o troškovima ili retka ponude.</span><span class="sxs-lookup"><span data-stu-id="d2b47-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="d2b47-124">**Ažuriraj cijene** nedostaje za procjenu troškova.</span><span class="sxs-lookup"><span data-stu-id="d2b47-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="d2b47-125">Klijenti ne mogu odabrati razloge statusa prilagođenog ugovora na stranici **Ugovor o projektu**.</span><span class="sxs-lookup"><span data-stu-id="d2b47-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="d2b47-126">Klijenti imaju smanjene performanse pri izradi prilagođenog cjenika iz ponude.</span><span class="sxs-lookup"><span data-stu-id="d2b47-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="d2b47-127">Klijenti doživljavaju nedosljednost zadanih postavki **jedinice** na stranicama **Pojedinosti retka ponude** i **Pojedinosti retka ugovora**.</span><span class="sxs-lookup"><span data-stu-id="d2b47-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="d2b47-128">Dodavanje stavki iz kategorije nenaplativih transakcija u naplativi redak ugovora neće poštovati vrstu naplate kategorije transakcije **Nenaplativo**.</span><span class="sxs-lookup"><span data-stu-id="d2b47-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="d2b47-129">Klijenti ne mogu upotrijebiti novododane uloge i kategoriju na prethodno stvorenim ugovorima.</span><span class="sxs-lookup"><span data-stu-id="d2b47-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="d2b47-130">Klijenti imaju smanjenu učinkovitost značajke Nepotrebno preuzimanje u PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="d2b47-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="d2b47-131">Uloge postavljene na popis **Kategorije resursa** kao nenaplative treba dodati na karticu **Naplative uloge** kao **Nenaplative** na retku ugovora za projekt.</span><span class="sxs-lookup"><span data-stu-id="d2b47-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="d2b47-132">Klijenti mogu imati smanjene performanse pri stvaranju projekta jer **GetBookableResourceIdFromUser** dohvaća sve stupce resursa koji se mogu rezervirati, a ne samo primarnog ID-a.</span><span class="sxs-lookup"><span data-stu-id="d2b47-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="d2b47-133">Entitetu **Vrsta transakcije** nedostaje dodatak za ažuriranje prethodne provjere valjanosti kako bi se spriječilo korisnike da uđu u **Jedinice** i **Grupe jedinica** koji nisu valjani za vrste transakcija.</span><span class="sxs-lookup"><span data-stu-id="d2b47-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="d2b47-134">Korak **Ukloni** ne funkcionira za uvoz unosa vremena.</span><span class="sxs-lookup"><span data-stu-id="d2b47-134">The **Remove** step does not work for time entry import.</span></span>
