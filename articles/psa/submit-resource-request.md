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
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131249"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="246e4-103">Slanje zahtjeva za resurs</span><span class="sxs-lookup"><span data-stu-id="246e4-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="246e4-104">Možete poslati generirani preduvjet resursa kao zahtjev za resurs.</span><span class="sxs-lookup"><span data-stu-id="246e4-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="246e4-105">Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.</span><span class="sxs-lookup"><span data-stu-id="246e4-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="246e4-106">U programu Project Service Automation (PSA) na stranici **Projekti** kliknite karticu **Tim** da biste pregledali popis resursa koje je moguće rezervirati.</span><span class="sxs-lookup"><span data-stu-id="246e4-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="246e4-107">Odaberite generički resurs koji ima preduvjet resursa s popisa, a zatim kliknite **Pošalji zahtjev**.</span><span class="sxs-lookup"><span data-stu-id="246e4-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Slanje zahtjeva za resurs](media/RM-how-to-18.png)

<span data-ttu-id="246e4-109">Status zahtjeva generičkog člana tima promijenit će se u **Poslano**.</span><span class="sxs-lookup"><span data-stu-id="246e4-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="246e4-110">Nakon što upravitelj resursa ispuni zahtjev, generički resurs zamijenit će se imenovanim resursom ako upravitelj resursa ispuni zahtjev rezerviranjem imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="246e4-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="246e4-111">U suprotnom generički resurs ostaje u timu, a status zahtjeva mijenja se u **Potreban pregled** ako je upravitelj resursa predložio imenovani resurs.</span><span class="sxs-lookup"><span data-stu-id="246e4-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
