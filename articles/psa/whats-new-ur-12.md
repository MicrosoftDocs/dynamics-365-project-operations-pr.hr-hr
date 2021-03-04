---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 12, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143819"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="b09d5-103">Project Service Automation, izdanje ažuriranja 12, V3</span><span class="sxs-lookup"><span data-stu-id="b09d5-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b09d5-104">Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="b09d5-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b09d5-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="b09d5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b09d5-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b09d5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b09d5-107">Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="b09d5-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b09d5-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b09d5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b09d5-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 12.</span><span class="sxs-lookup"><span data-stu-id="b09d5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="b09d5-110">Broj izrade ove verzije jest V3.10.2.34, a ona je uglavnom dostupna putem samostalnog ažuriranja u listopadu 2019.</span><span class="sxs-lookup"><span data-stu-id="b09d5-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="b09d5-111">Izdanje ažuriranja 12</span><span class="sxs-lookup"><span data-stu-id="b09d5-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b09d5-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="b09d5-112">Bug fixes</span></span>

- <span data-ttu-id="b09d5-113">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="b09d5-113">Time and Expense</span></span>

    - <span data-ttu-id="b09d5-114">Popravljeno: Poruka o pogrešci pri unosu vremena ažurirana je s pomoću relevantnijeg konteksta.</span><span class="sxs-lookup"><span data-stu-id="b09d5-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="b09d5-115">Popravljeno: Raspored i rešetka unosa vremena ispravno prikazuju vertikalnu traku za pomicanje kada je to potrebno.</span><span class="sxs-lookup"><span data-stu-id="b09d5-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="b09d5-116">Popravljeno: Poslani troškovi i Unos vremenai mogu se odobriti.</span><span class="sxs-lookup"><span data-stu-id="b09d5-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="b09d5-117">Popravljeno: Otkazivanje dijaloške poruke o potvrdi odobrenja ispravljeno je tako da odražava status odobrenja kada je promijenjen iz mogućnosti **Odobren** u **Poslan**.</span><span class="sxs-lookup"><span data-stu-id="b09d5-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="b09d5-118">Popravljeno: Polja **Cijena**, **Jedinica** i **Količina** sada su zaključana u zapisu troška nakon odobravanja.</span><span class="sxs-lookup"><span data-stu-id="b09d5-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="b09d5-119">Upravljanje projektom</span><span class="sxs-lookup"><span data-stu-id="b09d5-119">Project Management</span></span>

    - <span data-ttu-id="b09d5-120">Popravljeno: Uklonjena je radnja **Novo** u glavnom obrascu stavke **Član tima**.</span><span class="sxs-lookup"><span data-stu-id="b09d5-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="b09d5-121">Popravljeno: Dodijele resursa ažurirane su kako bi se evidentirale netočne pogreške u zaokruživanju, koje dovode do pomicanja datuma završetka zadatka.</span><span class="sxs-lookup"><span data-stu-id="b09d5-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="b09d5-122">Popravljeno: Korisniku će se u rešetki zadataka prikazati relevantne pogreške na strani poslužitelja.</span><span class="sxs-lookup"><span data-stu-id="b09d5-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="b09d5-123">Popravljeno: U biraču osoba za izvršenje zadataka, umjesto naziva položaja sada se prikazuje ime člana tima.</span><span class="sxs-lookup"><span data-stu-id="b09d5-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="b09d5-124">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="b09d5-124">Resource Management</span></span>

    - <span data-ttu-id="b09d5-125">Popravljeno: Pojedinosti o preduvjetima resursa za projekte stvorene iz predloška sada upotrebljavaju kalendar projekta.</span><span class="sxs-lookup"><span data-stu-id="b09d5-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="b09d5-126">Popravljeno: Vještine i kompetencije sada su zadane od glavnih podataka uloga do preduvjeta resursa stvorenih za tu ulogu.</span><span class="sxs-lookup"><span data-stu-id="b09d5-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="b09d5-127">Sales</span><span class="sxs-lookup"><span data-stu-id="b09d5-127">Sales</span></span>

    - <span data-ttu-id="b09d5-128">Popravljeno: Dvostruki ID-i objekata pronađeni na obrascu **Glavni ugovor**.</span><span class="sxs-lookup"><span data-stu-id="b09d5-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="b09d5-129">Popravljeno: Ažurirana je logika tako da kartica **Analiza ponude** bude vidljiva i prikazuje postavke metapodataka kartice.</span><span class="sxs-lookup"><span data-stu-id="b09d5-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="b09d5-130">Popravljeno: Datum obračuna na stvarnoj evidenciji sada potječe od datuma unosa vremena/troška, a ne od datuma odobrenja.</span><span class="sxs-lookup"><span data-stu-id="b09d5-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
