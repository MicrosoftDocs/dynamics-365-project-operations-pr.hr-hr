---
title: Slanje zahtjeva za resurs
description: Ovaj tema pruža informacije o slanju zahtjeva za resurs projekta.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149714"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="adbe5-103">Slanje zahtjeva za resurs</span><span class="sxs-lookup"><span data-stu-id="adbe5-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="adbe5-104">Možete poslati generirani preduvjet resursa kao zahtjev za resurs.</span><span class="sxs-lookup"><span data-stu-id="adbe5-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="adbe5-105">Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.</span><span class="sxs-lookup"><span data-stu-id="adbe5-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="adbe5-106">U programu Project Service Automation (PSA) na stranici **Projekti** kliknite karticu **Tim** da biste pregledali popis resursa koje je moguće rezervirati.</span><span class="sxs-lookup"><span data-stu-id="adbe5-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="adbe5-107">Odaberite generički resurs koji ima preduvjet resursa s popisa, a zatim kliknite **Pošalji zahtjev**.</span><span class="sxs-lookup"><span data-stu-id="adbe5-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Slanje zahtjeva za resurs](media/RM-how-to-18.png)

<span data-ttu-id="adbe5-109">Status zahtjeva generičkog člana tima promijenit će se u **Poslano**.</span><span class="sxs-lookup"><span data-stu-id="adbe5-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="adbe5-110">Nakon što upravitelj resursa ispuni zahtjev, generički resurs zamijenit će se imenovanim resursom ako upravitelj resursa ispuni zahtjev rezerviranjem imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="adbe5-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="adbe5-111">U suprotnom generički resurs ostaje u timu, a status zahtjeva mijenja se u **Potreban pregled** ako je upravitelj resursa predložio imenovani resurs.</span><span class="sxs-lookup"><span data-stu-id="adbe5-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
