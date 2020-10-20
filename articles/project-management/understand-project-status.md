---
title: Razumijevanje statusa projekta
description: U ovoj temi nalaze se informacije o statusu dodijeljenom projektu u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965667"
---
# <a name="understand-project-status"></a><span data-ttu-id="21d8f-103">Razumijevanje statusa projekta</span><span class="sxs-lookup"><span data-stu-id="21d8f-103">Understand project status</span></span>

<span data-ttu-id="21d8f-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="21d8f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="21d8f-105">Odkjeljak **Status** na stranici **Entitet projekta** daje sažetak stanja projekta na temelju troškova i rada.</span><span class="sxs-lookup"><span data-stu-id="21d8f-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="21d8f-106">Polja sažetka statusa</span><span class="sxs-lookup"><span data-stu-id="21d8f-106">Status summary fields</span></span>

- <span data-ttu-id="21d8f-107">Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta.</span><span class="sxs-lookup"><span data-stu-id="21d8f-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="21d8f-108">To polje upotrebljava kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="21d8f-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="21d8f-109">Polje **Komentari** omogućuje upravitelju projekta unos određenih komentara o statusu.</span><span class="sxs-lookup"><span data-stu-id="21d8f-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="21d8f-110">Polje **Status ažuriran dana** nije moguće uređivati.</span><span class="sxs-lookup"><span data-stu-id="21d8f-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="21d8f-111">Vrijednost u ovom polju vremenska je oznaka koja pokazuje kada je status zadnji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="21d8f-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="21d8f-112">Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se iz rešetke za praćenje.</span><span class="sxs-lookup"><span data-stu-id="21d8f-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="21d8f-113">Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta polja se ažuriraju na **Ispred**.</span><span class="sxs-lookup"><span data-stu-id="21d8f-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="21d8f-114">Kada je odstupanje rasporeda i troška za korijenski čvor negativno, ta se polja postavljaju na **Iza**.</span><span class="sxs-lookup"><span data-stu-id="21d8f-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
