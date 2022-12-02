---
title: Prijelazi stanja na podugovoru
description: Ovaj članak objašnjava prijelaze stanja na podugovoru u aplikaciji Microsoft Dynamics 365 Project Operations dok se podugovor stvara, izvršava i zatvara.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522929"
---
# <a name="state-transitions-on-a-subcontract"></a>Prijelazi stanja na podugovoru 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Ovaj članak objašnjava prijelaze stanja na podugovoru u aplikaciji Microsoft Dynamics 365 Project Operations. Svako stanje je predstavljeno kao nacrt, potvrđeno, zatvoreno ili otkazano. Sljedeće slike predstavljaju prijelaze stanja.

![Model stanja podugovora](../media/SubconStates.png)  

Sljedeća tablica pruža opisa onoga što svako stanje predstavlja u životnom ciklusu fakture podugovora u aplikaciji Project Operations.

| Stanje | Opis | Dopušteni prijelazi |
| --- | --- | --- |
| Skica | Ovo predstavlja početno stanje podugovora. Pregovori s dobavljačem su u tijeku. Reci i cijene podložni su izmjenama. Podugovor u ovom stanju može se upotrebljavati za procjenu i dodjelu osoblja projektnim zahtjevima za resurse i materijale. Također se na nj može upućivati na vremenu, troškovima i korištenju materijala na projektu. Podugovor u ovom stanju ne može se uređivati ni brisati. | Potvrđeno |
| Potvrđeno | Ovo predstavlja fazu podugovora nakon završetka pregovora s dobavljačem o cijenama i stavkama koje se kupuju. Međutim, stvarna isporuka materijala i/ili radova od strane podugovorenih resursa još uvijek je u tijeku. Podugovor u ovom stanju može se upotrebljavati za procjenu i dodjelu osoblja projektnim zahtjevima za resurse i materijale. Također se na nj može upućivati na vremenu, troškovima i korištenju materijala na projektu. Podugovor u ovom stanju ne može se uređivati ni brisati. Gumb **Otkaži** omogućuje vam otkazivanje potvrđenog podugovora. Gumb **Ponovo otvori** omogućuje vam ponovno otvaranje podugovora kako biste ga vratili u status **Nacrt**. Upotrijebite gumb **Zatvori** za zatvaranje potvrđenog podugovora. | Zatvoren <br> Otkazano <br> Skica |
| Zatvoren | Ovo predstavlja fazu podugovora u kojoj je stvarna isporuka materijala i/ili radova od strane podugovorenih resursa dovršena. Podugovor u ovom stanju više se ne može koristiti za procjenu i dodjelu osoblja projektnim zahtjevima za resurse i materijale. Također se više ne može na nj upućivati na vremenu, troškovima i korištenju materijala na projektu. Podugovor u ovom stanju ne može se uređivati ni brisati. | Nijedno |
| Otkazano | Ovo predstavlja fazu podugovora u kojoj stvarna isporuka materijala i/ili radova od strane podugovorenih resursa više nije potrebna. Podugovor u ovom stanju ne može se koristiti za procjenu i projektne zahtjeve osoblja za resurse i materijale niti se može navoditi u vremenu, troškovima i upotrebi materijala u projektu. Podugovor u ovom stanju ne može se uređivati ni brisati. | Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
