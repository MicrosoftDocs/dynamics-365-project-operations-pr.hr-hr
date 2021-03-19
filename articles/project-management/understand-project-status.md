---
title: Razumijevanje statusa projekta
description: U ovoj temi nalaze se informacije o statusu dodijeljenom projektima u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286464"
---
# <a name="understand-project-status"></a><span data-ttu-id="554c1-103">Razumijevanje statusa projekta</span><span class="sxs-lookup"><span data-stu-id="554c1-103">Understand project status</span></span>

<span data-ttu-id="554c1-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="554c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="554c1-105">U odjeljku **Status** na stranici **Entitet projekta** nalazi se sažetak stanja projekta na temelju troškova i rada.</span><span class="sxs-lookup"><span data-stu-id="554c1-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="554c1-106">Polja sažetka statusa</span><span class="sxs-lookup"><span data-stu-id="554c1-106">Status summary fields</span></span>

- <span data-ttu-id="554c1-107">Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta.</span><span class="sxs-lookup"><span data-stu-id="554c1-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="554c1-108">To polje upotrebljava kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="554c1-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="554c1-109">Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu.</span><span class="sxs-lookup"><span data-stu-id="554c1-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="554c1-110">Polje **Status ažuriran dana** nije moguće uređivati.</span><span class="sxs-lookup"><span data-stu-id="554c1-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="554c1-111">Vrijednost u ovom polju vremenska je oznaka koja pokazuje kada je status zadnji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="554c1-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="554c1-112">Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju rešetke praćenja.</span><span class="sxs-lookup"><span data-stu-id="554c1-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="554c1-113">Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta se polja ažuriraju na **Ispred**.</span><span class="sxs-lookup"><span data-stu-id="554c1-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="554c1-114">Kada je odstupanje rasporeda i troška za korijenski čvor negativno, ta se polja postavljaju na **Iza**.</span><span class="sxs-lookup"><span data-stu-id="554c1-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]