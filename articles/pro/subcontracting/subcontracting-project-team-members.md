---
title: Podugovaranje članova projektnog tima
description: U ovom se članku objašnjava kako podugovarati članove projektnog tima u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 14abd82cbbd256770105d4272f686590737e2648
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261361"
---
# <a name="subcontracting-project-team-members"></a>Podugovaranje članova projektnog tima

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U programu Microsoft Dynamics 365 Project Operations možete odabrati podugovaranje članova projektnog tima bez osoblja ili osoblja.

- Članovima projektnog tima bez osoblja dodijeljen je generički resurs.
- Članovima tima s osobljem dodijeljen je imenovani resurs.

Kada povežete člana projektnog tima s retkom podugovaranja, svi zadaci zadacima koje član tima ima bit će povučeni na temelju popisa cijena nabave priloženog kooperantu.  Na kartici **Procjene** na **stranici Detalji o** projektu odaberite **gumb Ažuriraj cijene** da biste vidjeli ažurirane cijene i/ili troškove koji proizlaze iz odluke o podugovaranju. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima bez osoblja
Stranica **s detaljima o** članu tima ima polja retka podugovaratelja i podugovaratelja koja omogućuju voditelju projekta da izrazi kako želi izvući potreban kapacitet iz podugovaratelja. Da biste podugovarali člana projektnog tima kao generički resurs, slijedite ove korake:

1.  Odaberite kooperant na stranici Detalji o **članu** tima.

2.  Kooperante možete odabrati samo sa statusom **Skica** ili **Potvrđeno**. **Nije moguće odabrati zatvorene** ili **otkazane kooperante**. 

3.  Polje retka **kooperanta** postaje vidljivo nakon što odaberete kooperant.

4.  **U polju Redak** kooperacije možete odabrati samo retke kooperacije koji su za vrijeme. Ne možete odabrati retke kooperacije za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima mora odgovarati ulozi u retku podugovaranja. Time se osigurava da je vrijeme za ulogu koja se procjenjuje na projektu ista uloga koja se kupuje u retku podugovaranja. 

Kada je generički član tima povezan s retkom podugovaratelja i kooperacije, polje Vrsta **radnika u retku generičkog člana tima ažurirat** će se u Ugovorni radnik **,** a **Valjanost kooperanta** postavit će se na **Valjano**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima s osobljem
Poput generičkih ili neodržavanih članova tima, kapacitet članova tima s osobljem potreban za projekt također se može povezati s podugovaračem. Da biste podugovarali imenovanog člana projektnog tima, slijedite ove korake:

1.  Provjerite je li imenovani resurs postavljen kao vrsta resursa koji se može rezervirati kao ugovorni radnik. Također, provjerite **odgovara li polje Dobavljač** na resursu koji se može rezervirati dobavljaču na kooperantu koji odabirete. 

2.  Kooperante možete odabrati samo u statusu **Skica** ili **Potvrđeno**. **Nije moguće odabrati zatvorene** ili **otkazane kooperante**. 

3.  Polje retka **kooperanta** postaje vidljivo nakon što odaberete kooperant.

4.  **U polju Redak** kooperacije možete odabrati samo retke kooperacije koji su za vrijeme. Ne možete odabrati retke kooperacije za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima mora odgovarati ulozi u retku podugovaranja. Time se osigurava da je vrijeme za ulogu koja se procjenjuje na projektu ista uloga koja se kupuje u retku podugovaranja. 

Imenovani članovi projektnog tima koji su postavljeni kao ugovorni radnik vrste **resursa** koji se može rezervirati prikazat će se sa statusom valjanosti kooperanta koji **nije valjan** ako nisu povezani s podugovarateljem. Kada je imenovani član projektnog tima povezan s retkom kooperanta i podugovaranja, **polje Vrsta** radnika u retku člana tima ažurirat će se na **Ugovorni radnik**, a **Valjanost kooperanta** postavit će se na **Valjano**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
