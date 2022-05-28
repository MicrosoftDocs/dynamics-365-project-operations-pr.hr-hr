---
title: Prijelazi stanja na fakturi dobavljača
description: Ova tema objašnjava prijelaze stanja na fakturi dobavljača u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584679"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Prijelazi stanja na fakturi dobavljača

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ova tema objašnjava prijelaze stanja na fakturi dobavljača u Microsoftu Dynamics 365 Project Operations. Koriste se sljedeća stanja: **Skica**, **U pregledu**, **Potvrđeno**, **Na čekanju** i **Otkazano**.

Sljedeće ilustracije prikazuju državne prijelaze.

![Model prijelaza države kooperanta.](../media/VI_State_Model.jpg)

Sljedeća tablica objašnjava što svaka država predstavlja u životnom ciklusu fakture dobavljača u operacijama projekta.

| Stanje | Opis | Dopušteni prijelazi |
| --- | --- | --- |
| Skica | Ovo je stanje početno stanje fakture dobavljača. Reci i cijene podložni su izmjenama. Faktura dobavljača u ovom stanju može se uređivati i brisati. | U tijeku |
| Na pregledu | Ovo stanje predstavlja stanje obrade fakture dobavljača. Najmanje jedan redak fakture dobavljača ima status **provjere U tijeku**. | Potvrđeno, na čekanju |
| Potvrđeno | Ovo stanje predstavlja fazu fakture dobavljača u kojoj je zatvaranje kreiralo stvarne troškove za svaki redak fakture dobavljača. Sve povezane stvarne troškove koje su se podudarale s recima fakture dobavljača stornirane su i zamijenjene stvarnim troškovima iz tih redaka fakture dobavljača. Fakturu dobavljača u ovom stanju nije moguće uređivati ni brisati. Pomoću gumba **Odustani** možete otkazati potvrđenu fakturu dobavljača. Akcija Odustani poništava učinak akcije Potvrda. | Otkazano |
| Na čekanju | <p>Ovo stanje predstavlja fazu fakture dobavljača u kojoj se faktura dobavljača ne može premjestiti zbog problema s fakturom ili statusom dobavljača. Fakturu dobavljača u ovom stanju nije moguće potvrditi, otkazati, urediti ili izbrisati.</p><p>Akcijom Ponovno otvaranje možete koristiti za premještanje fakture dobavljača u stanje skice **ili** **pregleda** U. Ako barem jedan redak na fakturi dobavljača ima status provjere u obliku U tijeku **ili Dovršeno**, faktura **dobavljača ponovno će se otvoriti u** stanju pregleda **U**. Ako svi reci na fakturi dobavljača imaju status provjere nije pokrenut, faktura **dobavljača ponovno će se otvoriti u stanju Skica** **.**</p> | Skica, U pregledu |
| Otkazano | Ovo stanje predstavlja fazu podugovaranja u kojoj stvarna isporuka materijala i/ili rada kooperantskim resursima više nije potrebna. Podugovaratelj u ovom stanju ne može se koristiti za procjenu i zahtjeve projekta osoblja za resurse i materijale, a također se ne može referencirati na vrijeme, troškove i upotrebu materijala na projektu. Podugovor u ovom stanju ne može se uređivati ili brisati. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
