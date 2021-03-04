---
title: Razumijevanje statusa projekta
description: U ovoj temi nalaze se informacije o statusu dodijeljenom projektu u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127284"
---
# <a name="understand-project-status"></a>Razumijevanje statusa projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


U odjeljku **Status** na stranici **Entitet projekta** nalazi se sažetak stanja projekta na temelju troškova i rada.


## <a name="status-summary-fields"></a>Polja sažetka statusa

- Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta. To polje upotrebljava kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik. 
- Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu. 
- Polje **Status ažuriran dana** nije moguće uređivati. Vrijednost u ovom polju vremenska je oznaka koja pokazuje kada je status zadnji put ažuriran.
- Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju rešetke praćenja. Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta se polja ažuriraju na **Ispred**. Kada je odstupanje rasporeda i troška za korijenski čvor negativno, ta se polja postavljaju na **Iza**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]