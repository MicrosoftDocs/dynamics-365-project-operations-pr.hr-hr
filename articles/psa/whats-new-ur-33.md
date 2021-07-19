---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 33, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334515"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="455e3-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 33, V3</span><span class="sxs-lookup"><span data-stu-id="455e3-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="455e3-104">Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="455e3-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="455e3-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="455e3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="455e3-106">Kompatibilno je sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="455e3-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="455e3-107">Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="455e3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="455e3-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="455e3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="455e3-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 33.</span><span class="sxs-lookup"><span data-stu-id="455e3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="455e3-110">Ova verzija ima broj izdanja V3.10.54.98 i općenito je dostupna putem samostalnog ažuriranja u srpnju 2021. godine.</span><span class="sxs-lookup"><span data-stu-id="455e3-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="455e3-111">Izdanje ažuriranja 33</span><span class="sxs-lookup"><span data-stu-id="455e3-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="455e3-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="455e3-112">Bug fixes</span></span>

<span data-ttu-id="455e3-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="455e3-113">**Time and Expense**</span></span>

<span data-ttu-id="455e3-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="455e3-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="455e3-115">Dva zaključana polja, **msdyn_description** i **msdyn_externaldescription**, mogu se uređivati nakon slanja.</span><span class="sxs-lookup"><span data-stu-id="455e3-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="455e3-116">Poruka o pogrešci prikazuje se ako se stvori trošak koji nije povezan s projektom.</span><span class="sxs-lookup"><span data-stu-id="455e3-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="455e3-117">Kada se stvori vremenski unos, uloga resursa prema zadanim postavkama postaje neaktivna.</span><span class="sxs-lookup"><span data-stu-id="455e3-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="455e3-118">Redci dnevnika povezani s opozvanim i izbrisanim troškom ne brišu se.</span><span class="sxs-lookup"><span data-stu-id="455e3-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="455e3-119">U stavci **Brzo stvaranje obrasca za vremenski unos** ažurirajte prikaz **Popis projektnih zadataka** za promjenu zadanog prikaza datuma u datum početka zadatka.</span><span class="sxs-lookup"><span data-stu-id="455e3-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="455e3-120">Kada stvarate vremenski unos iz kartice **Povezano** resursa koji se može rezervirati, vremenski se unos pogrešno stvara za prijavljenog korisnika umjesto za nadređeni resurs koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="455e3-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="455e3-121">Nova su polja dodana u dijaloški okvir **Skupno odobrenje MDD**.</span><span class="sxs-lookup"><span data-stu-id="455e3-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="455e3-122">**Planiranje projekta**</span><span class="sxs-lookup"><span data-stu-id="455e3-122">**Project planning**</span></span>

<span data-ttu-id="455e3-123">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="455e3-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="455e3-124">Spora izvedba stvaranja projekta kada se primjenjuju predlošci radnog vremena projekta sa složenim kalendarima.</span><span class="sxs-lookup"><span data-stu-id="455e3-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="455e3-125">Kada je datum početka veći od datuma završetka, na predlošku za kopiranje projekta prikazuje se pogreška zbog razlika u vremenskoj komponenti svakog polja.</span><span class="sxs-lookup"><span data-stu-id="455e3-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="455e3-126">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="455e3-126">**Resource management**</span></span>

<span data-ttu-id="455e3-127">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="455e3-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="455e3-128">Neispravan parametar upotrebljava se u upitu za uporabu resursa, a XML dovodi do netočnih rezultata filtra na rešetki **Uporaba resursa**.</span><span class="sxs-lookup"><span data-stu-id="455e3-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="455e3-129">Potvrda **Produži rezervacije** prikazuje netočan datum završetka za rezervacije.</span><span class="sxs-lookup"><span data-stu-id="455e3-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="455e3-130">**Prodaje**</span><span class="sxs-lookup"><span data-stu-id="455e3-130">**Sales**</span></span>

<span data-ttu-id="455e3-131">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="455e3-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="455e3-132">Prikazuje se poruka o pogrešci ako se cijena kategorije stvara s vrijednostima koje nedostaju.</span><span class="sxs-lookup"><span data-stu-id="455e3-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="455e3-133">Prikazuje se poruka o pogrešci ako se kontrolna točka u retku ugovora stvara bez retka narudžbe.</span><span class="sxs-lookup"><span data-stu-id="455e3-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
