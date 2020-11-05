---
title: Zašto ne mogu izbrisati zapise iz entiteta stvarnih vrijednosti?
description: Ova tema pruža informacije o tome zašto ne možete izbrisati zapise iz entiteta stvarnih vrijednosti.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073514"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="6aaa1-103">Zašto ne mogu izbrisati zapise iz entiteta stvarnih vrijednosti?</span><span class="sxs-lookup"><span data-stu-id="6aaa1-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6aaa1-104">Project Service Automation (PSA) ne dozvoljava brisanje stvarnih vrijednosti jer služe kao izvor istine za transakcije koje imaju financijske implikacije na daljnje sustave, kao što je glavna knjiga.</span><span class="sxs-lookup"><span data-stu-id="6aaa1-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="6aaa1-105">Kad bi se stvarne vrijednosti mogle izbrisati, cjelovitost transakcija financijskog izvješćivanja bila bi upitna.</span><span class="sxs-lookup"><span data-stu-id="6aaa1-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="6aaa1-106">Da bi se uspostavila kontrola knjiženja, klijenti bi trebali koristiti dnevnike za izradu kompenzirajućih transakcija.</span><span class="sxs-lookup"><span data-stu-id="6aaa1-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

