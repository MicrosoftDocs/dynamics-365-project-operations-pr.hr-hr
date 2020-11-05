---
title: Slanje zahtjeva za resurs
description: Možete poslati generirani preduvjet resursa kao zahtjev za resurs. Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073282"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="e230a-104">Slanje zahtjeva za resurs</span><span class="sxs-lookup"><span data-stu-id="e230a-104">Submit a resource request</span></span>

<span data-ttu-id="e230a-105">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="e230a-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e230a-106">Možete poslati generirani preduvjet resursa kao zahtjev za resurs.</span><span class="sxs-lookup"><span data-stu-id="e230a-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="e230a-107">Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.</span><span class="sxs-lookup"><span data-stu-id="e230a-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="e230a-108">Na stranici **Projekti** aplikacije Dynamics 365 Project Operations, kliknite karticu **Tim** kako biste pregledali popis resursa koji se mogu rezervirati.</span><span class="sxs-lookup"><span data-stu-id="e230a-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="e230a-109">Odaberite generički resurs koji ima preduvjet resursa s popisa, a zatim kliknite **Pošalji zahtjev**.</span><span class="sxs-lookup"><span data-stu-id="e230a-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="e230a-110">Status zahtjeva generičkog člana tima promijenit će se u **Poslano**.</span><span class="sxs-lookup"><span data-stu-id="e230a-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="e230a-111">Nakon što se ispuni zahtjev, generički resurs mijenja se imenovanim resursom ako upravitelj resursa ispuni zahtjev rezerviranjem imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="e230a-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="e230a-112">U suprotnom, ako upravitelj resursa predlaže imenovani resurs, generički resurs ostaje u timu, a status zahtjeva mijenja se u **Potreban pregled**.</span><span class="sxs-lookup"><span data-stu-id="e230a-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
