---
title: Slanje zahtjeva za resurs
description: Možete poslati generirani preduvjet resursa kao zahtjev za resurs. Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 583524ccf33f2dc42ee6beba7e00cc5fd74819d4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598663"
---
# <a name="submit-a-resource-request"></a>Slanje zahtjeva za resurs

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Možete poslati generirani preduvjet resursa kao zahtjev za resurs. Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.

1. U aplikaciji Dynamics 365 Project Operations, na stranici **Projekti**, odaberite karticu **Tim** kako biste pregledali popis resursa koje je moguće rezervirati. 
2. Odaberite generički resurs koji ima preduvjet resursa s popisa, a zatim kliknite **Pošalji zahtjev**.

Status zahtjeva generičkog člana tima promijenit će se u **Poslano**.

Nakon što se ispuni zahtjev, generički resurs mijenja se imenovanim resursom ako upravitelj resursa ispuni zahtjev rezerviranjem imenovanog resursa. U suprotnom, ako upravitelj resursa predlaže imenovani resurs, generički resurs ostaje u timu, a status zahtjeva mijenja se u **Potreban pregled**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]