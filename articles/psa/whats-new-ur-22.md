---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 22, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 389897c2604974a0bf7f221758dd03e1748ffeb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280569"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="77d5c-103">Project Service Automation, izdanje ažuriranja 22, V3</span><span class="sxs-lookup"><span data-stu-id="77d5c-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="77d5c-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="77d5c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="77d5c-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="77d5c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="77d5c-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="77d5c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="77d5c-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="77d5c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="77d5c-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="77d5c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="77d5c-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 22.</span><span class="sxs-lookup"><span data-stu-id="77d5c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="77d5c-110">Ova verzija ima broj međuverzije V 3.10.33.48 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="77d5c-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="77d5c-111">Izdanje ažuriranja 22</span><span class="sxs-lookup"><span data-stu-id="77d5c-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="77d5c-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="77d5c-112">Bug fixes</span></span>



<span data-ttu-id="77d5c-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="77d5c-113">**Time and Expense**</span></span>

<span data-ttu-id="77d5c-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="77d5c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="77d5c-115">**Vremenski unosi** ne dodaju se automatski u raspored vremenskih unosa nakon uvoza.</span><span class="sxs-lookup"><span data-stu-id="77d5c-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="77d5c-116">Alat za odabir datuma rešetke **Vremenski unos** ne prepoznaje regionalne postavke korisnika.</span><span class="sxs-lookup"><span data-stu-id="77d5c-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="77d5c-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="77d5c-117">**Resource Management**</span></span>

<span data-ttu-id="77d5c-118">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="77d5c-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="77d5c-119">U ručnom načinu rada, promjene obrisa **Dodjela resursa** ne prepoznaju se pri generiranju mogućosti **Preduvjeti za resurse**.</span><span class="sxs-lookup"><span data-stu-id="77d5c-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="77d5c-120">**Zahtjevi za resursima** ne podržavaju statuse prilagođenih zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="77d5c-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="77d5c-121">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="77d5c-121">**Project Management**</span></span>

<span data-ttu-id="77d5c-122">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="77d5c-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="77d5c-123">S pomoću dvostrukog klika na EstimateGridControl neće se pravilno raščlaniti brojevi holandskog formata.</span><span class="sxs-lookup"><span data-stu-id="77d5c-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="77d5c-124">Zadani sati ne ažuriraju se ispravno kad se zadaci mijenjaju s pomoću dodatka za klijent radne površine aplikacije Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="77d5c-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="77d5c-125">Rešetke za praćenje i procjene projekta prikazuju pogrešan kôd valute prodaje kada je ugovorena valuta različita od valute klijenta, a tvrtka ili ustanova konfigurirana je za prikaz kodova valuta umjesto simbola valuta.</span><span class="sxs-lookup"><span data-stu-id="77d5c-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="77d5c-126">Datum završetka člana Tima dodati će jedan dan ako je raspored sati rada 24 sata dnevno.</span><span class="sxs-lookup"><span data-stu-id="77d5c-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="77d5c-127">U Projektnom rasporedu, dodavanje Transakcijske kategorije zadatku ne aktivira automatsko spremanje.</span><span class="sxs-lookup"><span data-stu-id="77d5c-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="77d5c-128">Sljedeća greška prikazuje se tijekom dodavanja člana tima u predložak projekta: „Preduvjeti za resurse ne mogu se povezati s predlošcima projekta”.</span><span class="sxs-lookup"><span data-stu-id="77d5c-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="77d5c-129">Skripta pravila vrpce „msdyn.Approval.CanApproveOrReject” prikazuje pogrešku vremenskog ograničenja.</span><span class="sxs-lookup"><span data-stu-id="77d5c-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="77d5c-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="77d5c-130">**Sales**</span></span>

<span data-ttu-id="77d5c-131">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="77d5c-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="77d5c-132">Poruka o pogrešci provjere ne prikazuje se kada je u pretraživanju cjenika na obrascu „Nova ponuda cjenika projekta” odabran cjenik.</span><span class="sxs-lookup"><span data-stu-id="77d5c-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="77d5c-133">Zatvaranje prihvaćene ponude ne prelazi na stvoreni ugovor ako je BPF u prilogu ponude u završnoj fazi.</span><span class="sxs-lookup"><span data-stu-id="77d5c-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="77d5c-134">Storniranje **Nenaplaćene prodaje** povezano je s izvornim troškom kad se opozove unos vremena.</span><span class="sxs-lookup"><span data-stu-id="77d5c-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="77d5c-135">Nakon odabira gumba **Potvrdi**, status fakture se ne mijenja u **Potvrđen** sve dok se faktura ne osvježi.</span><span class="sxs-lookup"><span data-stu-id="77d5c-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]