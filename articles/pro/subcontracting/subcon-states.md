---
title: Prijelazi stanja na kooperantu
description: Ovaj tema objašnjava prijelaze stanja na podugovaranja u Dynamics 365 Project Operations Microsoftu dok se kooperant stvara, izvršava i zatvara.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903635"
---
# <a name="state-transitions-on-a-subcontract"></a>Prijelazi stanja na kooperantu 

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj tema objašnjava prijelaze stanja na podugovaranja u Microsoftu Dynamics 365 Project Operations. Svaka država predstavljena je kao skica, potvrđena, zatvorena ili otkazana. Sljedeća slika predstavlja prijelaze stanja.

![Model stanja kooperanta](../media/SubconStates.png)  

Sljedeća tablica sadrži opis onoga što svako stanje predstavlja u životnom ciklusu kooperanta u projektnim operacijama.

| Stanje | Opis | Dopušteni prijelazi |
| --- | --- | --- |
| Skica | Ovo predstavlja početno stanje kooperanta. Pregovori s dobavljačem su u tijeku. Linije i cijene podložne su izmjenama. Podugovor u ovom stanju može se koristiti za procjenu i zahtjeve projekta osoblja za resurse i materijale. Također se može referencirati na vrijeme, trošak i upotrebu materijala na projektu. Kooperant u ovom stanju može se uređivati i brisati. | Potvrđeno |
| Potvrđeno | Ovo predstavlja fazu kooperanta nakon završetka pregovora s dobavljačem o cijenama i artiklima u retku koji se nabavljaju. Međutim, stvarna isporuka materijala i/ili rada po kooperantskim resursima još uvijek je u tijeku. Podugovor u ovom stanju može se koristiti za procjenu i zahtjeve projekta osoblja za resurse i materijale. Također se može referencirati na vrijeme, trošak i upotrebu materijala na projektu. Kooperant u ovom stanju ne može se uređivati ni brisati. **Gumb Odustani** omogućuje otkazivanje potvrđenog kooperanta. Gumb **Ponovno otvaranje omogućuje ponovno otvaranje** kooperanta da biste ga vratili u **status** Skica. Pomoću **gumba Zatvori** zatvorite potvrđeni kooperant. | Zatvoren <br> Otkazano <br> Skica |
| Zatvoren | To predstavlja fazu podugovaranja kada se dovrši stvarna isporuka materijala i/ili rad po kooperantskim resursima. Podugovaranje u ovom stanju više se ne može koristiti za procjenu i zahtjeve projekta osoblja za resurse i materijale. Također, više se ne može referencirati na vrijeme, trošak i upotrebu materijala na projektu. Kooperant u ovom stanju ne može se uređivati ni brisati. | Nijedno |
| Otkazano | To predstavlja fazu podugovaranja kada stvarna isporuka materijala i/ili rad po kooperantskim resursima više nije potreban. Podugovor u ovom stanju ne može se koristiti za procjenu i zahtjeve projekta osoblja za resurse i materijale niti se može na njega upućivati na vrijeme, trošak i upotrebu materijala na projektu. Kooperant u ovom stanju ne može se uređivati ni brisati. | Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
