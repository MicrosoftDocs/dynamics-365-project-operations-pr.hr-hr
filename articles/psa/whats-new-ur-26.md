---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 26, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143549"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="35b2c-103">Project Service Automation, izdanje ažuriranja 26, V3</span><span class="sxs-lookup"><span data-stu-id="35b2c-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="35b2c-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="35b2c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="35b2c-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="35b2c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="35b2c-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="35b2c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="35b2c-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="35b2c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="35b2c-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="35b2c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="35b2c-109">U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 26. izdanju ažuriranja aplikacije Project Service Automation, V3.</span><span class="sxs-lookup"><span data-stu-id="35b2c-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="35b2c-110">Ova verzija ima broj izrade V3.10.44.59 i općenito je dostupna putem samostalnog ažuriranja u prosincu 2020.</span><span class="sxs-lookup"><span data-stu-id="35b2c-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="35b2c-111">Izdanje ažuriranja 26</span><span class="sxs-lookup"><span data-stu-id="35b2c-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="35b2c-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="35b2c-112">Bug fixes</span></span>

<span data-ttu-id="35b2c-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="35b2c-113">**Time and Expense**</span></span>

<span data-ttu-id="35b2c-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="35b2c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="35b2c-115">Korisnici mogu promijeniti zadatak na unosu vremena koji je odobren/poslan.</span><span class="sxs-lookup"><span data-stu-id="35b2c-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="35b2c-116">Pogreška „Referenca objekta nije postavljena” prilikom spremanja unosa vremena.</span><span class="sxs-lookup"><span data-stu-id="35b2c-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="35b2c-117">Uvoz unosa vremena iz zadataka resursa stvara unose vremena s netočnim vrijednostima DateTime.</span><span class="sxs-lookup"><span data-stu-id="35b2c-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="35b2c-118">Kada su instalirane obje aplikacije, i Project Service Automation i Field Service, gumb **Novi** dvaput se prikazuje na naredbenoj traci za unose vremena u aplikaciji Field Service.</span><span class="sxs-lookup"><span data-stu-id="35b2c-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="35b2c-119">Ažuriranje ćelija **Omogući jedinicu** i **Grupa jedinica** sada rade na rešetki **Procjene troškova**.</span><span class="sxs-lookup"><span data-stu-id="35b2c-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="35b2c-120">Obrazac **Ažuriranje uređivanja unosa vremena** uključuje **Vremensku traku**.</span><span class="sxs-lookup"><span data-stu-id="35b2c-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="35b2c-121">Odobrenje vremena za vremenske unose koji se ne odnose na projekt blokira sustav tijekom traženja uloge odobravatelja projekta.</span><span class="sxs-lookup"><span data-stu-id="35b2c-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="35b2c-122">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="35b2c-122">**Resource Management**</span></span>

<span data-ttu-id="35b2c-123">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="35b2c-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="35b2c-124">Dodana je provjera valjanosti u programski dodatak **PostProjectCreate** za provjeru primarnog zahtjeva prije stvaranja.</span><span class="sxs-lookup"><span data-stu-id="35b2c-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="35b2c-125">Obrazac za brzo stvaranje **Član projektnog tima** izbacuje iznimku nulte vrijednosti reference ako se iz obrasca uklone polja.</span><span class="sxs-lookup"><span data-stu-id="35b2c-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="35b2c-126">Generiranje zahtjeva za 12 sati tijekom jedne godine neće uspjeti.</span><span class="sxs-lookup"><span data-stu-id="35b2c-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="35b2c-127">Poboljšana poruka o pogrešci za iznimku nulte vrijednosti reference tijekom stvaranja zahtjeva za resursom.</span><span class="sxs-lookup"><span data-stu-id="35b2c-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="35b2c-128">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="35b2c-128">**Project Management**</span></span>

<span data-ttu-id="35b2c-129">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="35b2c-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="35b2c-130">Poboljšana provjera valjanosti za rješavanje iznimke nulte vrijednosti reference generirane u programskom dodatku **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="35b2c-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="35b2c-131">Projekti koje je objavio programski dodatak radnog područja aplikacije Microsoft Project brišu neraspoređene zadatke.</span><span class="sxs-lookup"><span data-stu-id="35b2c-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="35b2c-132">Dodana je nova provjera valjanosti kada je referenca projekta zadatka nevaljana zbog iznimke nulte vrijednosti reference u programskom dodatku **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="35b2c-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="35b2c-133">Rešetka člana tima ne prikazuje različite zadatke u zapisu člana tima.</span><span class="sxs-lookup"><span data-stu-id="35b2c-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="35b2c-134">Dodane su nove provjere valjanosti i poruke o pogrešci zbog iznimke nulte vrijednosti reference u programskom dodatku **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="35b2c-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="35b2c-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="35b2c-135">**Sales**</span></span>

<span data-ttu-id="35b2c-136">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="35b2c-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="35b2c-137">Pri odabiru retka koji se temelji na projektu u ponudi ili ugovoru, gumb **Prijedlog** bi trebao biti vidljiv samo pri odabiru retka koji se temelji na proizvodu povezanog s postojećim proizvodom.</span><span class="sxs-lookup"><span data-stu-id="35b2c-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="35b2c-138">Razdvojite ovlast **Stvori_proizvod** od **Stvori_UgovoroProjektu**.</span><span class="sxs-lookup"><span data-stu-id="35b2c-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="35b2c-139">Brisanje retka fakture uzrokuje neuspješnu vrijednost reference jednaku nuli na **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="35b2c-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
