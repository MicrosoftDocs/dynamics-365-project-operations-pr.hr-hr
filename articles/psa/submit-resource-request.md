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
ms.openlocfilehash: 8976ca2360be8676350178059615c59995544a71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282234"
---
# <a name="submitting-a-resource-request"></a>Slanje zahtjeva za resurs

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Možete poslati generirani preduvjet resursa kao zahtjev za resurs. Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.

1. U programu Project Service Automation (PSA) na stranici **Projekti** kliknite karticu **Tim** da biste pregledali popis resursa koje je moguće rezervirati. 
2. Odaberite generički resurs koji ima preduvjet resursa s popisa, a zatim kliknite **Pošalji zahtjev**.

![Slanje zahtjeva za resurs](media/RM-how-to-18.png)

Status zahtjeva generičkog člana tima promijenit će se u **Poslano**.

Nakon što upravitelj resursa ispuni zahtjev, generički resurs zamijenit će se imenovanim resursom ako upravitelj resursa ispuni zahtjev rezerviranjem imenovanog resursa. U suprotnom generički resurs ostaje u timu, a status zahtjeva mijenja se u **Potreban pregled** ako je upravitelj resursa predložio imenovani resurs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]