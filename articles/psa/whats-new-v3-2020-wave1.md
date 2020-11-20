---
title: Novosti ili promjene u aplikaciji Project Service Automation, verzija 3.x val 1 2020
description: Ova tema pruža informacije o tome što je novo i promijenjeno u aplikaciji Project Service Automation, verzija 3. val1, 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126474"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="d9606-103">Novosti ili promjene u aplikaciji Project Service Automation, verzija 3, val 1, 2020</span><span class="sxs-lookup"><span data-stu-id="d9606-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="d9606-104">Ova tema ističe ključna razmatranja nadogradnje pri prelasku na najnovije izdanje aplikacije Project Service Automation (PSA), verzije 3.x, val 1, 2020.</span><span class="sxs-lookup"><span data-stu-id="d9606-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="d9606-105">Unos vremena</span><span class="sxs-lookup"><span data-stu-id="d9606-105">Time entry</span></span>
<span data-ttu-id="d9606-106">Prošireno je iskustvo unosa vremena kako bi se pružile mogućnosti produljenja unosa vremena u više scenarija klijenta.</span><span class="sxs-lookup"><span data-stu-id="d9606-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="d9606-107">To uključuje mogućnost dodavanja vrsta unosa koji sada upravljaju određenim ponašanjem na temelju naziva sheme polja **Postavke vremenskog unosa**, prikazane kao **Vremenski izvor**.</span><span class="sxs-lookup"><span data-stu-id="d9606-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="d9606-108">Novo rješenje, pod nazivom Vrijeme, Trošak, Određivanje statusa i Odobrenja (TESA) dodano je da podrži ovu funkciju.</span><span class="sxs-lookup"><span data-stu-id="d9606-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="d9606-109">Razmatranja nadogradnje</span><span class="sxs-lookup"><span data-stu-id="d9606-109">Upgrade consideration</span></span>
<span data-ttu-id="d9606-110">Kako bi se podržala ova funkcionalnost, uloge unutar PSA ažurirane su i uključuju nove ovlasti.</span><span class="sxs-lookup"><span data-stu-id="d9606-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="d9606-111">Te ovlasti omogućuju pristup za čitanje novog entiteta, **Postavke unosa vremena**.</span><span class="sxs-lookup"><span data-stu-id="d9606-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="d9606-112">Korisnicima koji trebaju mogućnost prijavljivanja vremena treba, osim postojećih uloga, dodijeliti korisničku ulogu **Korisnik unosa vremena**.</span><span class="sxs-lookup"><span data-stu-id="d9606-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="d9606-113">Ova uloga uključuje novu funkcionalnost i osigurava nastavak rada vremenskog unosa.</span><span class="sxs-lookup"><span data-stu-id="d9606-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="d9606-114">Uz to, ako imate neki prilagođeni modul aplikacije koji uključuje sve obrasce za entitet za unos vremena, od vas će se zatražiti uklanjanje **Obrasca za brzo stvaranje unosa vremena TESA** iz modula.</span><span class="sxs-lookup"><span data-stu-id="d9606-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="d9606-115">Trenutačno proširene promjene vremenskog unosa</span><span class="sxs-lookup"><span data-stu-id="d9606-115">Currently extended time entry changes</span></span>
<span data-ttu-id="d9606-116">Kako bi se umanjio utjecaj trenutačnih korisnika vremenskog unosa, ova promjena uloge jedini je osnovni zahtjev koji je potreban za nastavak uporabe vremenskog unosa.</span><span class="sxs-lookup"><span data-stu-id="d9606-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="d9606-117">Ako ste stvorili prilagođene prikaze ili zasebna iskustva unosa vremena, morate postaviti polja **Postavljanje unosa vremena** na ispravnu vrijednost PSA.</span><span class="sxs-lookup"><span data-stu-id="d9606-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
