---
title: Novosti ili promjene u aplikaciji Project Service Automation, verzija 3.x val 1 2020
description: Ova tema pruža informacije o tome što je novo i promijenjeno u aplikaciji Project Service Automation, verzija 3. val1, 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750120"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="75642-103">Novosti ili promjene u aplikaciji Project Service Automation, verzija 3, val 1, 2020</span><span class="sxs-lookup"><span data-stu-id="75642-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="75642-104">Ova tema ističe ključna razmatranja nadogradnje pri prelasku na najnovije izdanje aplikacije Project Service Automation (PSA), verzije 3.x, val 1, 2020.</span><span class="sxs-lookup"><span data-stu-id="75642-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="75642-105">Unos vremena</span><span class="sxs-lookup"><span data-stu-id="75642-105">Time entry</span></span>
<span data-ttu-id="75642-106">Prošireno je iskustvo unosa vremena kako bi se pružile mogućnosti produljenja unosa vremena u više scenarija klijenta.</span><span class="sxs-lookup"><span data-stu-id="75642-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="75642-107">To uključuje mogućnost dodavanja vrsta unosa koji sada upravljaju određenim ponašanjem na temelju naziva sheme polja **Postavke unosa vremena**, prikazane kao **Vremenski izvor**.</span><span class="sxs-lookup"><span data-stu-id="75642-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="75642-108">Razmatranja nadogradnje</span><span class="sxs-lookup"><span data-stu-id="75642-108">Upgrade consideration</span></span>
<span data-ttu-id="75642-109">Kako bi se podržala ova funkcionalnost, uloge unutar PSA ažurirane su i uključuju nove ovlasti.</span><span class="sxs-lookup"><span data-stu-id="75642-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="75642-110">Te ovlasti omogućuju pristup za čitanje novog entiteta, **Postavke unosa vremena**.</span><span class="sxs-lookup"><span data-stu-id="75642-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="75642-111">Korisnicima koji trebaju mogućnost prijavljivanja vremena treba, osim postojećih uloga, dodijeliti korisničku ulogu **Korisnik unosa vremena**.</span><span class="sxs-lookup"><span data-stu-id="75642-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="75642-112">Ova uloga uključuje novu funkcionalnost i osigurava nastavak rada unosa vremena.</span><span class="sxs-lookup"><span data-stu-id="75642-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="75642-113">Trenutačno proširene promjene unosa vremena</span><span class="sxs-lookup"><span data-stu-id="75642-113">Currently extended time entry changes</span></span>
<span data-ttu-id="75642-114">Kako bi se umanjio utjecaj trenutačnih korisnika unosa vremena, ova promjena uloge jedini je osnovni zahtjev koji je potreban za nastavak uporabe unosa vremena.</span><span class="sxs-lookup"><span data-stu-id="75642-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="75642-115">Ako ste stvorili prilagođene prikaze ili zasebna iskustva unosa vremena, morate postaviti polja **Postavljanje unosa vremena** na ispravnu vrijednost PSA.</span><span class="sxs-lookup"><span data-stu-id="75642-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
