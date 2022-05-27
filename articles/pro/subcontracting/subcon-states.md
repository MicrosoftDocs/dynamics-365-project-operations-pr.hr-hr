---
title: Prijelazi stanja na podugovoru
description: Ova tema objašnjava prijelaze stanja na podugovaranju u Microsoftu Dynamics 365 Project Operations dok se kooperant stvara, izvršava i zatvara.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c9533d046398c708c55467e6b1a25acf6abade3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579159"
---
# <a name="state-transitions-on-a-subcontract"></a>Prijelazi stanja na podugovoru 

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ova tema objašnjava prijelaze stanja na podugovaratelju u Microsoftu Dynamics 365 Project Operations. Svaka je država predstavljena kao skica, potvrđena, zatvorena ili otkazana. Sljedeća slika predstavlja državne prijelaze.

![Model stanja podugovaranja](../media/SubconStates.png)  

Sljedeća tablica daje opis onoga što svaka država predstavlja u životnom ciklusu podugovaratelja u projektnim operacijama.

| Stanje | Opis | Dopušteni prijelazi |
| --- | --- | --- |
| Skica | To predstavlja početno stanje podugovaranja. Pregovori s dobavljačem su u tijeku. Reci i cijene podložni su izmjenama. Podugovaratelj u ovoj državi može se koristiti za procjenu i zahtjeve projekata osoblja za resurse i materijale. Također se može referencirati na vrijeme, trošak i korištenje materijala na projektu. Kooperant u ovom stanju može se uređivati i brisati. | Potvrđeno |
| Potvrđeno | To predstavlja fazu podugovaranja nakon što se završe pregovori s dobavljačem o cijenama i artiklima za retke koji se kupuju. Međutim, stvarna isporuka materijala i/ili rada od strane kooperantskih resursa još uvijek je u tijeku. Podugovaratelj u ovoj državi može se koristiti za procjenu i zahtjeve projekata osoblja za resurse i materijale. Također se može referencirati na vrijeme, trošak i korištenje materijala na projektu. Podugovor u ovom stanju ne može se uređivati ili brisati. Gumb **Odustani** omogućuje vam otkazivanje potvrđenog podugovaratelja. Gumb **Ponovno otvori** omogućuje vam ponovno otvaranje podugovaranja kako biste ga vratili u **status skice**. Pomoću gumba **Zatvori** zatvorite potvrđeni kooperant. | Zatvoren <br> Otkazano <br> Skica |
| Zatvoren | To predstavlja fazu podugovaranja kada se dovrši stvarna isporuka materijala i/ili rad kooperantskim resursima. Podugovaratelj u ovom stanju više se ne može koristiti za procjenu i zahtjeve projekata osoblja za resurse i materijale. Također, više se ne može referencirati na vrijeme, trošak i korištenje materijala na projektu. Podugovor u ovom stanju ne može se uređivati ili brisati. | Nijedno |
| Otkazano | To predstavlja fazu podugovaranja kada stvarna isporuka materijala i/ili rad podugovarajućih resursa više nije potrebna. Podugovaratelj u ovom stanju ne može se koristiti za procjenu i zahtjeve projekta osoblja za resurse i materijale niti se može navesti na vrijeme, trošak i upotrebu materijala na projektu. Podugovor u ovom stanju ne može se uređivati ili brisati. | Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
