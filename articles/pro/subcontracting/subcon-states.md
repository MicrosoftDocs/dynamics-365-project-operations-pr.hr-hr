---
title: Prijelazi stanja na podugovoru
description: U ovom se članku objašnjavaju prijelazi stanja na podugovaranju u Microsoftu Dynamics 365 Project Operations dok se kooperant stvara, izvršava i zatvara.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919729"
---
# <a name="state-transitions-on-a-subcontract"></a>Prijelazi stanja na podugovoru 

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U ovom se članku objašnjavaju prijelazi stanja na podugovaranju u Microsoftu Dynamics 365 Project Operations. Svaka je država predstavljena kao skica, potvrđena, zatvorena ili otkazana. Sljedeća slika predstavlja državne prijelaze.

![Model stanja podugovaranja](../media/SubconStates.png)  

Sljedeća tablica daje opis onoga što svaka država predstavlja u životnom ciklusu podugovaratelja u projektnim operacijama.

| Stanje | Opis | Dopušteni prijelazi |
| --- | --- | --- |
| Skica | To predstavlja početno stanje podugovaranja. Pregovori s dobavljačem su u tijeku. Reci i cijene podložni su izmjenama. Podugovaratelj u ovoj državi može se koristiti za procjenu i zahtjeve projekata osoblja za resurse i materijale. Također se može referencirati na vrijeme, trošak i korištenje materijala na projektu. Kooperant u ovom stanju može se uređivati i brisati. | Potvrđeno |
| Potvrđeno | To predstavlja fazu podugovaranja nakon što se završe pregovori s dobavljačem o cijenama i artiklima za retke koji se kupuju. Međutim, stvarna isporuka materijala i/ili rada od strane kooperantskih resursa još uvijek je u tijeku. Podugovaratelj u ovoj državi može se koristiti za procjenu i zahtjeve projekata osoblja za resurse i materijale. Također se može referencirati na vrijeme, trošak i korištenje materijala na projektu. Podugovor u ovom stanju ne može se uređivati ili brisati. Gumb **Odustani** omogućuje vam otkazivanje potvrđenog podugovaratelja. Gumb **Ponovno otvori** omogućuje vam ponovno otvaranje podugovaranja kako biste ga vratili u **status skice**. Pomoću gumba **Zatvori** zatvorite potvrđeni kooperant. | Zatvoren <br> Otkazano <br> Skica |
| Zatvoren | To predstavlja fazu podugovaranja kada se dovrši stvarna isporuka materijala i/ili rad kooperantskim resursima. Podugovaratelj u ovom stanju više se ne može koristiti za procjenu i zahtjeve projekata osoblja za resurse i materijale. Također, više se ne može referencirati na vrijeme, trošak i korištenje materijala na projektu. Podugovor u ovom stanju ne može se uređivati ili brisati. | Nijedno |
| Otkazano | To predstavlja fazu podugovaranja kada stvarna isporuka materijala i/ili rad podugovarajućih resursa više nije potrebna. Podugovaratelj u ovom stanju ne može se koristiti za procjenu i zahtjeve projekta osoblja za resurse i materijale niti se može navesti na vrijeme, trošak i upotrebu materijala na projektu. Podugovor u ovom stanju ne može se uređivati ili brisati. | Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
