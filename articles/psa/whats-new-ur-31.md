---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 31, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 31, V3.
author: ruhercul
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999122"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="b5d45-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 31, V3</span><span class="sxs-lookup"><span data-stu-id="b5d45-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b5d45-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b5d45-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b5d45-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="b5d45-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b5d45-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b5d45-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b5d45-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="b5d45-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b5d45-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b5d45-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b5d45-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 31.</span><span class="sxs-lookup"><span data-stu-id="b5d45-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="b5d45-110">Ova verzija ima broj međuverzije V3.10.52.77 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2021. godine.</span><span class="sxs-lookup"><span data-stu-id="b5d45-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="b5d45-111">Izdanje ažuriranja 31</span><span class="sxs-lookup"><span data-stu-id="b5d45-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b5d45-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="b5d45-112">Bug fixes</span></span>

<span data-ttu-id="b5d45-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="b5d45-113">**Time and Expense**</span></span>

<span data-ttu-id="b5d45-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="b5d45-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b5d45-115">Naredbeni gumbi kontrole vremenskog unosa na stranici **Resursi koji se mogu rezervirati** bili su zbunjujući.</span><span class="sxs-lookup"><span data-stu-id="b5d45-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="b5d45-116">Iznimka nulte reference generirana je u **Project.SetTrackingFields** tijekom odobravanja vremenskog unosa.</span><span class="sxs-lookup"><span data-stu-id="b5d45-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="b5d45-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="b5d45-117">**Resource Management**</span></span>

<span data-ttu-id="b5d45-118">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="b5d45-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b5d45-119">**Stvori člana tima** ne prikazuje ispravno postavke metapodataka za postavljanje rezervacije za **Stanje izvršene zadane rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="b5d45-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="b5d45-120">Pri nadogradnji s PSA 1.X na 3.X, postupak nadogradnje ne uspijeva na **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="b5d45-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="b5d45-121">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="b5d45-121">**Sales**</span></span>

<span data-ttu-id="b5d45-122">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="b5d45-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="b5d45-123">Stvarni prihod pretvara iznose u valutu projekta u rešetki za praćenje.</span><span class="sxs-lookup"><span data-stu-id="b5d45-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="b5d45-124">Zadana valuta nije jasna pri stvaranju redaka dnevnika, ponuda i ugovora u scenarijima kada se osnovna valuta tvrtke ili ustanove razlikuje od valute projekta.</span><span class="sxs-lookup"><span data-stu-id="b5d45-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="b5d45-125">Upit **Provjera valjanosti ispravka dnevnika na čekanju** ne filtrira se po projektu.</span><span class="sxs-lookup"><span data-stu-id="b5d45-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="b5d45-126">Preostala prodaja netočno se izračunava na projektu.</span><span class="sxs-lookup"><span data-stu-id="b5d45-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="b5d45-127">Ponude zasnovane na kontaktu ne uspijevaju kada se stvaraju bez cjenika.</span><span class="sxs-lookup"><span data-stu-id="b5d45-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="b5d45-128">Pri odabiru mogućnosti **Potvrdi fakturu** ne prikazuje se okretni gumb.</span><span class="sxs-lookup"><span data-stu-id="b5d45-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="b5d45-129">Pri odabiru mogućnosti **Stvori fakturu** ne prikazuje se okretni gumb.</span><span class="sxs-lookup"><span data-stu-id="b5d45-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="b5d45-130">Zatvaranje ponude kao izgubljene ne otkazuje rezervacije.</span><span class="sxs-lookup"><span data-stu-id="b5d45-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







