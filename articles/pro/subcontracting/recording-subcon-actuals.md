---
title: Evidentiranje vremena, troškova i uporabe materijala za podugovorne komponente
description: Ovaj članak objašnjava kako Microsoft Dynamics 365 Project Operations prati vrijeme, troškove i potrošnju materijala zabilježene na projektima iz podugovorenih komponenti.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522504"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Evidentiranje vremena, troškova i uporabe materijala na projektima za podugovorne komponente

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Ovaj članak objašnjava kako Microsoft Dynamics 365 Project Operations prati vrijeme, troškove i potrošnju materijala zabilježene na projektima iz podugovorenih komponenti.

## <a name="costing-for-subcontractor-time-on-projects"></a>Troškovi vremena podizvođača na projektima
U Project Operations ugovorni radnici mogu bilježiti vrijeme na projektima na sličan način kao i zaposlenici. Tijekom unošenja vremena na projektima i/ili zadacima projekata, radnik po ugovoru može odabrati određeni podugovor i redak podugovora.

Kada se vrijeme koje su dostavili ugovorni radnici odobri, trošak projekta se bilježi korištenjem stope jediničnog troška koja je postavljena za taj resurs ugovornog radnika u odjeljku **Cijene uloga** nabavnog cjenika podugovora.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Cijene za podugovorne troškove na projektima
Prilikom unosa troškova nastalih na projektima, na unosu troška možete odabrati podugovor i redak podugovora. 

Kada se taj unos troška dostavi i odobri, cijena troška bilježi se na projektu na temelju jedinične cijene koja je postavljena za tu kategoriju transakcije u odjeljku **Cijene kategorija** nabavnog cjenika podugovora.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Cijene za podugovorne materijale na projektima
Prilikom unosa korištenja materijala na projektima, u zapisniku korištenja materijala možete odabrati podugovor i redak podugovora. Kada se zapisnik korištenja materijala dostavi i odobri, cijena materijala bilježi se na projektu na temelju jedinične cijene koja je postavljena za taj proizvod u odjeljku **Stavke cjenika** nabavnog cjenika podugovora.

Korištenje materijala također se može zabilježiti za dopisane proizvode na projektima. Ova vrsta korištenja materijala također se može povezati s podugovorom i retkom podugovora. Kada bilježite korištenje materijala za dopisane proizvode, trebate unijeti jediničnu cijenu dopisanog proizvoda. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
