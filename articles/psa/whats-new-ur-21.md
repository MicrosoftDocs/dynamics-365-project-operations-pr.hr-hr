---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 21, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126699"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="c55de-103">Project Service Automation, izdanje ažuriranja 21, V3</span><span class="sxs-lookup"><span data-stu-id="c55de-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="c55de-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c55de-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c55de-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="c55de-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c55de-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c55de-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c55de-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="c55de-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c55de-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c55de-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c55de-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 21.</span><span class="sxs-lookup"><span data-stu-id="c55de-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="c55de-110">Ova verzija ima broj međuverzije V 3.10.32.50 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="c55de-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="c55de-111">Izdanje ažuriranja 21</span><span class="sxs-lookup"><span data-stu-id="c55de-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c55de-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="c55de-112">Bug fixes</span></span>

<span data-ttu-id="c55de-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="c55de-113">**Time and Expense**</span></span>

<span data-ttu-id="c55de-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="c55de-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c55de-115">Tijekom hostiranja **Kontrole rešetke unosa vremena** na nadzornim pločama, rešetka ne upotrebljava cijelu širinu spremnika rešetke nadzorne ploče.</span><span class="sxs-lookup"><span data-stu-id="c55de-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="c55de-116">Za određene vremenske zone kontrola rešetke **Vremenski unos** ne prikazuje zapise.</span><span class="sxs-lookup"><span data-stu-id="c55de-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="c55de-117">Vremenski unosi koji slijede nakon 21:00 prikazuju se pogrešnog dana.</span><span class="sxs-lookup"><span data-stu-id="c55de-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="c55de-118">Korisnici ne mogu poslati troškove ako kategorija troškova **Potrebna je potvrda o troškovima** nema vrijednost.</span><span class="sxs-lookup"><span data-stu-id="c55de-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="c55de-119">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="c55de-119">**Resource Management**</span></span>

<span data-ttu-id="c55de-120">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="c55de-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="c55de-121">Neaktivne rezervacije prikazuju su u prozoru **Usklađivanje**.</span><span class="sxs-lookup"><span data-stu-id="c55de-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="c55de-122">Za ispunjenje generičkih resursa nedostajala je provjera valjanosti kako bi se osiguralo postojanje valjanog statusa rezervacije.</span><span class="sxs-lookup"><span data-stu-id="c55de-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="c55de-123">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="c55de-123">**Project Management**</span></span>

<span data-ttu-id="c55de-124">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="c55de-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="c55de-125">Rešetke obrasca **Projekta** (**Dodjela resursa**, **Zadatak**, prikaz **Usklađivanja**, **Procjene troškova**) mogu se i dalje uređivati i kad projekt nije aktivan.</span><span class="sxs-lookup"><span data-stu-id="c55de-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="c55de-126">Duplicirani klijenti ne mogu se spojiti s klijentima koji su povezani s potvrđenim projektnim ugovorima.</span><span class="sxs-lookup"><span data-stu-id="c55de-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="c55de-127">Kada se doda resurs koji nema valjani kalendar, sustav ne vraća poruku o pogrešci prilagođenu korisniku.</span><span class="sxs-lookup"><span data-stu-id="c55de-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="c55de-128">Gumb **Dodaj zadatak** na rešetki zadataka omogućen je kad je projekt povezan s **Dodatkom aplikacije Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="c55de-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="c55de-129">Napor nekontrolirano raste kada je zadatak s kategorijom dodijeljen resursu s ulogom za koju je definirana cijena koštanja.</span><span class="sxs-lookup"><span data-stu-id="c55de-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="c55de-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c55de-130">**Sales**</span></span>

<span data-ttu-id="c55de-131">Napravljena su sljedeća poboljšanja:</span><span class="sxs-lookup"><span data-stu-id="c55de-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="c55de-132">**Učestalost fakture** i **Početak naplate** preseljeni su u karticu **Raspored faktura**.</span><span class="sxs-lookup"><span data-stu-id="c55de-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="c55de-133">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="c55de-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="c55de-134">**Ukupna prodajna cijena** je nula (0) za **Kategoriju** čak i ako **Uloga** ima ukupnu prodajnu cijenu koja nije nula.</span><span class="sxs-lookup"><span data-stu-id="c55de-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="c55de-135">Klijenti ne mogu mijenjati vrijednost polja **Status fakture** u **Spremno za fakturiranje** kada neki drugi prilagođeni postupak ažurira dodatno polje.</span><span class="sxs-lookup"><span data-stu-id="c55de-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="c55de-136">Gumb **Osvježi retke fakture** može stvoriti više dupliciranih redaka ako se uzastopno odabire.</span><span class="sxs-lookup"><span data-stu-id="c55de-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="c55de-137">Gumb **Ažuriraj cijene** ne radi u podrešetki **Cijene uloga** u obrascu **Brzi pogled**.</span><span class="sxs-lookup"><span data-stu-id="c55de-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="c55de-138">Logika **Razlučivosti cjenika prodaje** nepravilno upravlja vremenskim zonama, što dovodi do pogrešnog odabira cjenika.</span><span class="sxs-lookup"><span data-stu-id="c55de-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="c55de-139">**Ukupni stvarni trošak** projekta može se isključiti djelomičnim iznosom nakon što se odobri pojedinačni unos.</span><span class="sxs-lookup"><span data-stu-id="c55de-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="c55de-140">Logika **Razlučivosti cijene** ne daje poruku o pogrešci prilagođenu korisniku ako **Dohvaćena CijenaUloge** nema vrijednosti u poljima **„Primarna jedinica”** i **„Cijena u primarnoj jedinici”**.</span><span class="sxs-lookup"><span data-stu-id="c55de-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
