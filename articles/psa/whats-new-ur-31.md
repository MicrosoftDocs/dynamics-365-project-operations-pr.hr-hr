---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 31, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945526"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="f849a-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 31, V3</span><span class="sxs-lookup"><span data-stu-id="f849a-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f849a-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f849a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f849a-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="f849a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f849a-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f849a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f849a-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="f849a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f849a-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f849a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f849a-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 31.</span><span class="sxs-lookup"><span data-stu-id="f849a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="f849a-110">Ova verzija ima broj međuverzije V3.10.52.77 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2021. godine.</span><span class="sxs-lookup"><span data-stu-id="f849a-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="f849a-111">Izdanje ažuriranja 31</span><span class="sxs-lookup"><span data-stu-id="f849a-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f849a-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="f849a-112">Bug fixes</span></span>

<span data-ttu-id="f849a-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="f849a-113">**Time and Expense**</span></span>

<span data-ttu-id="f849a-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="f849a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f849a-115">Naredbeni gumbi kontrole vremenskog unosa na stranici **Resursi koji se mogu rezervirati** bili su zbunjujući.</span><span class="sxs-lookup"><span data-stu-id="f849a-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="f849a-116">Iznimka nulte reference generirana je u **Project.SetTrackingFields** tijekom odobravanja vremenskog unosa.</span><span class="sxs-lookup"><span data-stu-id="f849a-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="f849a-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="f849a-117">**Resource Management**</span></span>

<span data-ttu-id="f849a-118">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="f849a-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="f849a-119">**Stvori člana tima** ne prikazuje ispravno postavke metapodataka za postavljanje rezervacije za **Stanje izvršene zadane rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="f849a-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="f849a-120">Pri nadogradnji s PSA 1.X na 3.X, postupak nadogradnje ne uspijeva na **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="f849a-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="f849a-121">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="f849a-121">**Sales**</span></span>

<span data-ttu-id="f849a-122">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="f849a-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="f849a-123">Stvarni prihod pretvara iznose u valutu projekta u rešetki za praćenje.</span><span class="sxs-lookup"><span data-stu-id="f849a-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="f849a-124">Zadana valuta nije jasna pri stvaranju redaka dnevnika, ponuda i ugovora u scenarijima kada se osnovna valuta tvrtke ili ustanove razlikuje od valute projekta.</span><span class="sxs-lookup"><span data-stu-id="f849a-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="f849a-125">Upit **Provjera valjanosti ispravka dnevnika na čekanju** ne filtrira se po projektu.</span><span class="sxs-lookup"><span data-stu-id="f849a-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="f849a-126">Preostala prodaja netočno se izračunava na projektu.</span><span class="sxs-lookup"><span data-stu-id="f849a-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="f849a-127">Ponude zasnovane na kontaktu ne uspijevaju kada se stvaraju bez cjenika.</span><span class="sxs-lookup"><span data-stu-id="f849a-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="f849a-128">Pri odabiru mogućnosti **Potvrdi fakturu** ne prikazuje se okretni gumb.</span><span class="sxs-lookup"><span data-stu-id="f849a-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="f849a-129">Pri odabiru mogućnosti **Stvori fakturu** ne prikazuje se okretni gumb.</span><span class="sxs-lookup"><span data-stu-id="f849a-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="f849a-130">Zatvaranje ponude kao izgubljene ne otkazuje rezervacije.</span><span class="sxs-lookup"><span data-stu-id="f849a-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







