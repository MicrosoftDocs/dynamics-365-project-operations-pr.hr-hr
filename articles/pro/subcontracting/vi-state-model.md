---
title: Prijelazi stanja na fakturi dobavljača
description: Ovaj članak objašnjava prijelaze stanja na fakturi dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261007"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Prijelazi stanja na fakturi dobavljača

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj članak objašnjava prijelaze stanja na fakturi dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations. Koriste se sljedeća stanja: **Nacrt**, **U pregledu**, **Potvrđeno**, **Na čekanju** i **Otkazano**.

Sljedeće ilustracije prikazuju prijelaze stanja.

![Model prijelaza stanja podugovora.](../media/VI_State_Model.jpg)

Sljedeća tablica objašnjava što svako stanje predstavlja u životnom ciklusu fakture dobavljača u aplikaciji Project Operations.

| Stanje | Opis | Dopušteni prijelazi |
| --- | --- | --- |
| Skica | Ovo stanje je početno stanje fakture dobavljača. Reci i cijene podložni su izmjenama. Faktura dobavljača u ovom stanju može se uređivati i brisati. | U obradi |
| Na pregledu | Ovo stanje predstavlja stanje obrade fakture dobavljača. Barem jedan redak fakture dobavljača ima status provjere **U tijeku**. | Potvrđeno, Na čekanju |
| Potvrđeno | Ovo stanje predstavlja fazu fakture dobavljača u kojoj je aplikacija stvorila stvarne troškove za svaki redak fakture dobavljača. Svi povezani stvarni troškovi koji su bili usklađeni s recima fakture dobavljača poništeni su i zamijenjeni stvarnim troškovima iz tih redaka fakture dobavljača. Faktura dobavljača u ovom stanju ne može se uređivati ni brisati. Možete koristiti gumb **Otkaži** da biste otkazali potvrđenu fakturu dobavljača. Radnja Otkažu poništava učinak radnje Potvrdi. | Otkazano |
| Na čekanju | <p>Ovo stanje predstavlja fazu fakture dobavljača u kojoj se faktura dobavljača ne može premjestiti zbog problema s fakturom ili statusom dobavljača. Faktura dobavljača u ovom stanju ne može se, potvrditi, otkazati, uređivati ni brisati.</p><p>Možete koristiti radnju Otvori ponovno za premještanje fakture dobavljača u stanje **Nacrt** ili **Na pregledu**. Ako barem jedan redak na fakturi dobavljača ima status provjere **U tijeku** ili **Završeno**, faktura dobavljača ponovno će se otvoriti u stanju **Na pregledu**. Ako svi reci na fakturi dobavljača imaju status provjere **Nije započeto**, faktura dobavljača ponovno će se otvoriti u stanju **Nacrt**.</p> | Nacrt, Na pregledu |
| Otkazano | Ovo stanje predstavlja fazu podugovora u kojoj više nije potrebna stvarna isporuka materijala i/ili radova od strane podugovorenih resursa. Podugovor u ovom stanju ne može se koristiti za procjenu i projektne zahtjeve osoblja za resurse i materijale te se ne može navoditi u vremenu, troškovima i upotrebi materijala u projektu. Podugovor u ovom stanju ne može se uređivati ni brisati. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
