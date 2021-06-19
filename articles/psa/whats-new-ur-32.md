---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 32, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129657"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="ec40d-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 32, V3</span><span class="sxs-lookup"><span data-stu-id="ec40d-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ec40d-104">Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ec40d-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="ec40d-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="ec40d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ec40d-106">Kompatibilno je sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ec40d-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ec40d-107">Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="ec40d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="ec40d-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ec40d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ec40d-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 32.</span><span class="sxs-lookup"><span data-stu-id="ec40d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="ec40d-110">Ova verzija ima broj međuverzije V3.10.53.108 i općenito je dostupna putem samostalnog ažuriranja u lipnju 2021. godine.</span><span class="sxs-lookup"><span data-stu-id="ec40d-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="ec40d-111">Izdanje ažuriranja 32</span><span class="sxs-lookup"><span data-stu-id="ec40d-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ec40d-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="ec40d-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="ec40d-113">Općenito</span><span class="sxs-lookup"><span data-stu-id="ec40d-113">General</span></span>

- <span data-ttu-id="ec40d-114">Kada glavna nadogradnja ne uspije, treba blokirati samo glavne ulazne točke aplikacije kako bi se osiguralo da dijeljeni entiteti i dalje budu dostupni.</span><span class="sxs-lookup"><span data-stu-id="ec40d-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="ec40d-115">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="ec40d-115">Time and Expense</span></span>

<span data-ttu-id="ec40d-116">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ec40d-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="ec40d-117">**TimeEntriesImportFromResourceAssignment** ne održava vrijeme početka i završetka isječka konture za dodjelu resursa.</span><span class="sxs-lookup"><span data-stu-id="ec40d-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="ec40d-118">Kad odaberete **Otvoreni unos** na rešetki **Vemenski unos**, možda nećete moći odabrati druge obrasce.</span><span class="sxs-lookup"><span data-stu-id="ec40d-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="ec40d-119">Dok uvozite zadatke u vremenske unose, upit kôda klijenta mogao bi generirati dugačku URL-adresu koja ne uspijeva u upitu.</span><span class="sxs-lookup"><span data-stu-id="ec40d-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="ec40d-120">U rešetki **Vremenski unos**, nakon što se vrijednost izbriše iz ćelije, fokus ne ostaje u rešetki.</span><span class="sxs-lookup"><span data-stu-id="ec40d-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="ec40d-121">Gumb **Odbaci** uklonjen je s prikaza **Obrada odobrenja** za nova odobrenja.</span><span class="sxs-lookup"><span data-stu-id="ec40d-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="ec40d-122">Na stabilnost i izvedbu skupnog odobravanja vremenskog unosa utječu zastoji i neuspješno rukovanje prilagodbama, koje su povezane s entitetom **Vremenski unos**, na odgovarajući način.</span><span class="sxs-lookup"><span data-stu-id="ec40d-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="ec40d-123">Planiranje projekta</span><span class="sxs-lookup"><span data-stu-id="ec40d-123">Project Planning</span></span>

- <span data-ttu-id="ec40d-124">Iznimka nulte reference generira se kada ažurirate projekt koji ima nultu vrijednost u polju **Ugovorna jedinica**.</span><span class="sxs-lookup"><span data-stu-id="ec40d-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="ec40d-125">**Osvježi ukupne vrijednosti projekata** pogrešno izračunava preostali trošak i preostalu prodaju na projektu.</span><span class="sxs-lookup"><span data-stu-id="ec40d-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="ec40d-126">Izračuni prekomjerne cijene utječu na učinkovitost povezanu s ažuriranjima na konturama dodjele resursa.</span><span class="sxs-lookup"><span data-stu-id="ec40d-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="ec40d-127">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="ec40d-127">Resource Management</span></span>

<span data-ttu-id="ec40d-128">Popravljen je sljedeći profil:</span><span class="sxs-lookup"><span data-stu-id="ec40d-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="ec40d-129">Kada je kalendarski kapacitet resursa koji možete rezervirati veći od 1, Project Service Automation pogrešno prepoznaje kapacitet kao 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="ec40d-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="ec40d-130">Stoga se u prikazu rasporeda prikazuje beskonačna petlja.</span><span class="sxs-lookup"><span data-stu-id="ec40d-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="ec40d-131">Prodaje</span><span class="sxs-lookup"><span data-stu-id="ec40d-131">Sales</span></span>

<span data-ttu-id="ec40d-132">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ec40d-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="ec40d-133">Kada se stvori redak dnevnika koji ima prilagođenu vrstu transakcije, prikazuje se sljedeći izuzetak nulte reference: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="ec40d-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="ec40d-134">Prije kopiranja ponude ne biste trebali dodavati uloge i kategorije koje su neaktivne u uloge koje se naplaćuju i kategorije novokopirane ponude.</span><span class="sxs-lookup"><span data-stu-id="ec40d-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="ec40d-135">Datumi dokumenta i obračuna nisu usklađeni s datumom početka koji je naveden u pojedinosti retka fakture i koji stvoren izravno na nacrtu fakture.</span><span class="sxs-lookup"><span data-stu-id="ec40d-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="ec40d-136">Iznimke nulte reference generiraju se u scenarijima koji su povezani s naktivacijom uloga i kategorija prije kopiranja ponude.</span><span class="sxs-lookup"><span data-stu-id="ec40d-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="ec40d-137">Radnja **Ažuriraj cijene** na stranici **Projekti** ne ažurira procjene troškova i materijala.</span><span class="sxs-lookup"><span data-stu-id="ec40d-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
