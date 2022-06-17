---
title: Razumijevanje statusa projekta
description: U ovom se članku nalaze informacije o statusu dodijeljenom projektima u sustavu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 86cb60b634b62af23f39720c0452dca82ff3ad26
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923593"
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