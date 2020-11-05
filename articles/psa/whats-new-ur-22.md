---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 22, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073336"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="63be0-103">Project Service Automation, izdanje ažuriranja 22, V3</span><span class="sxs-lookup"><span data-stu-id="63be0-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="63be0-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="63be0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="63be0-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="63be0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="63be0-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="63be0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="63be0-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="63be0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="63be0-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="63be0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="63be0-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 22.</span><span class="sxs-lookup"><span data-stu-id="63be0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="63be0-110">Ova verzija ima broj međuverzije V 3.10.33.48 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="63be0-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="63be0-111">Izdanje ažuriranja 22</span><span class="sxs-lookup"><span data-stu-id="63be0-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="63be0-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="63be0-112">Bug fixes</span></span>



<span data-ttu-id="63be0-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="63be0-113">**Time and Expense**</span></span>

<span data-ttu-id="63be0-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="63be0-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="63be0-115">**Vremenski unosi** ne dodaju se automatski u raspored vremenskih unosa nakon uvoza.</span><span class="sxs-lookup"><span data-stu-id="63be0-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="63be0-116">Alat za odabir datuma rešetke **Vremenski unos** ne prepoznaje regionalne postavke korisnika.</span><span class="sxs-lookup"><span data-stu-id="63be0-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="63be0-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="63be0-117">**Resource Management**</span></span>

<span data-ttu-id="63be0-118">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="63be0-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="63be0-119">U ručnom načinu rada, promjene obrisa **Dodjela resursa** ne prepoznaju se pri generiranju mogućosti **Preduvjeti za resurse**.</span><span class="sxs-lookup"><span data-stu-id="63be0-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="63be0-120">**Zahtjevi za resursima** ne podržavaju statuse prilagođenih zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="63be0-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="63be0-121">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="63be0-121">**Project Management**</span></span>

<span data-ttu-id="63be0-122">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="63be0-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="63be0-123">S pomoću dvostrukog klika na EstimateGridControl neće se pravilno raščlaniti brojevi holandskog formata.</span><span class="sxs-lookup"><span data-stu-id="63be0-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="63be0-124">Zadani sati ne ažuriraju se ispravno kad se zadaci mijenjaju s pomoću dodatka za klijent radne površine aplikacije Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="63be0-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="63be0-125">Rešetke za praćenje i procjene projekta prikazuju pogrešan kôd valute prodaje kada je ugovorena valuta različita od valute kupca, a tvrtka ili ustanova konfigurirana je za prikaz kodova valuta umjesto simbola valuta.</span><span class="sxs-lookup"><span data-stu-id="63be0-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="63be0-126">Datum završetka člana Tima dodati će jedan dan ako je raspored sati rada 24 sata dnevno.</span><span class="sxs-lookup"><span data-stu-id="63be0-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="63be0-127">U Projektnom rasporedu, dodavanje Transakcijske kategorije zadatku ne aktivira automatsko spremanje.</span><span class="sxs-lookup"><span data-stu-id="63be0-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="63be0-128">Sljedeća greška prikazuje se tijekom dodavanja člana tima u predložak projekta: „Preduvjeti za resurse ne mogu se povezati s predlošcima projekta”.</span><span class="sxs-lookup"><span data-stu-id="63be0-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="63be0-129">Skripta pravila vrpce „msdyn.Approval.CanApproveOrReject” prikazuje pogrešku vremenskog ograničenja.</span><span class="sxs-lookup"><span data-stu-id="63be0-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="63be0-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="63be0-130">**Sales**</span></span>

<span data-ttu-id="63be0-131">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="63be0-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="63be0-132">Poruka o pogrešci provjere ne prikazuje se kada je u pretraživanju cjenika na obrascu „Nova ponuda cjenika projekta” odabran cjenik.</span><span class="sxs-lookup"><span data-stu-id="63be0-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="63be0-133">Zatvaranje prihvaćene ponude ne prelazi na stvoreni ugovor ako je BPF u prilogu ponude u završnoj fazi.</span><span class="sxs-lookup"><span data-stu-id="63be0-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="63be0-134">Storniranje **Nenaplaćene prodaje** povezano je s izvornim troškom kad se opozove unos vremena.</span><span class="sxs-lookup"><span data-stu-id="63be0-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="63be0-135">Nakon odabira gumba **Potvrdi** , status fakture se ne mijenja u **Potvrđen** sve dok se faktura ne osvježi.</span><span class="sxs-lookup"><span data-stu-id="63be0-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
