---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 30, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852837"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="15739-103">Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 30, V3</span><span class="sxs-lookup"><span data-stu-id="15739-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="15739-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="15739-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="15739-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="15739-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="15739-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="15739-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="15739-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="15739-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="15739-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="15739-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="15739-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 30.</span><span class="sxs-lookup"><span data-stu-id="15739-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="15739-110">Ova verzija ima broj međuverzije V3.10.51.61 i uglavnom je dostupna putem samostalnog ažuriranja u travnju 2021. godine.</span><span class="sxs-lookup"><span data-stu-id="15739-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="15739-111">Izdanje ažuriranja 30</span><span class="sxs-lookup"><span data-stu-id="15739-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="15739-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="15739-112">Bug fixes</span></span>

<span data-ttu-id="15739-113">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="15739-113">**Time and Expense**</span></span>

<span data-ttu-id="15739-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="15739-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="15739-115">Do pogreške dolazi kada stvorite i spremite vremenski unos na stranici **Brzo stvaranje** ako je uklonjeno polje **Uloga**.</span><span class="sxs-lookup"><span data-stu-id="15739-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="15739-116">Filtar Unos vremena primjenjuje pogrešni operator filtra.</span><span class="sxs-lookup"><span data-stu-id="15739-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="15739-117">Kopirane vremenske tablice ne prikazuju se automatski kada odaberete **Kopiraj tjedan** na kontroli vremenskog unosa.</span><span class="sxs-lookup"><span data-stu-id="15739-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="15739-118">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="15739-118">**Resource Management**</span></span>

<span data-ttu-id="15739-119">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="15739-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="15739-120">Kada produžujete rezervaciju, stanje rezervacije dodijeljeno fiksnoj rezervaciji nije ispravno.</span><span class="sxs-lookup"><span data-stu-id="15739-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="15739-121">Produljenjem rezervacije poštuje se stanje rezervacije definirano kao **Izvršeno** u metapodacima postavki rezervacije.</span><span class="sxs-lookup"><span data-stu-id="15739-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="15739-122">Kada nije navedeno valjano stanje rezervacije, poruka o pogrešci nije pravilno lokalizirana.</span><span class="sxs-lookup"><span data-stu-id="15739-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="15739-123">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="15739-123">**Project Management**</span></span>

<span data-ttu-id="15739-124">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="15739-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="15739-125">Projekti se ne mogu stvarati u jednoj valuti, a da obuhvaćaju povezane zadatke u drugoj valuti.</span><span class="sxs-lookup"><span data-stu-id="15739-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="15739-126">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="15739-126">**Sales**</span></span>

<span data-ttu-id="15739-127">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="15739-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="15739-128">Kada se cjenik kopira, cijene se ne ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="15739-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="15739-129">Zatvaranje ponude kao prihvaćene ne uspijeva kada pojedinost troška ima vrijednost za original.</span><span class="sxs-lookup"><span data-stu-id="15739-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="15739-130">U entitetu **Zadatak projekta**, **Procijenjeni trošak** preimenovan je u **Planirani trošak (osnovni)**.</span><span class="sxs-lookup"><span data-stu-id="15739-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="15739-131">Izuzetak nulte reference generira se kad se fakture stvore ili izbrišu.</span><span class="sxs-lookup"><span data-stu-id="15739-131">A null reference exception is generated when invoices are created or deleted.</span></span>
