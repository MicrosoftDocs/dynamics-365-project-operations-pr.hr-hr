---
title: Slanje zahtjeva za resurs
description: Možete poslati generirani preduvjet resursa kao zahtjev za resurs. Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279129"
---
# <a name="submit-a-resource-request"></a>Slanje zahtjeva za resurs

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Možete poslati generirani preduvjet resursa kao zahtjev za resurs. Zahtjev se zatim šalje upravitelju resursa kako bi ga ispunio.

1. U aplikaciji Dynamics 365 Project Operations, na stranici **Projekti**, odaberite karticu **Tim** kako biste pregledali popis resursa koje je moguće rezervirati. 
2. Odaberite generički resurs koji ima preduvjet resursa s popisa, a zatim kliknite **Pošalji zahtjev**.

Status zahtjeva generičkog člana tima promijenit će se u **Poslano**.

Nakon što se ispuni zahtjev, generički resurs mijenja se imenovanim resursom ako upravitelj resursa ispuni zahtjev rezerviranjem imenovanog resursa. U suprotnom, ako upravitelj resursa predlaže imenovani resurs, generički resurs ostaje u timu, a status zahtjeva mijenja se u **Potreban pregled**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]