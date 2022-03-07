---
title: Članovi projektnog tima kooperanta
description: Ovaj tema objašnjava kako kooperirati članove projektnog tima u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903005"
---
# <a name="subcontracting-project-team-members"></a>Članovi projektnog tima kooperanta

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U Dynamics 365 Project Operations Microsoftu možete odabrati podugovaranje članova projektnog tima bez osoblja ili osoblja.

- Članovi projektnog tima bez osoblja imaju dodijeljen generički resurs.
- Članovi tima s osobljem imaju dodijeljen imenovani resurs.

Kada povežete člana projektnog tima s retkom kooperanta, sve dodjele zadataka koje član tima ima bit će ponovno skupe na temelju popisa nabavnih cijena pridruženih kooperantu.  Na **kartici Procjene** na **stranici Detalji o** projektu odaberite **gumb Ažuriraj cijene da biste vidjeli** ažurirane cijene i/ili troškove koji proizlaze iz odluke o podugovaranja. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima bez osoblja
**Stranica s detaljima o članu tima** ima polja crte kooperanta i kooperanta koja upravitelju projekta omogućuju da izrazi kako želi izvući potreban kapacitet iz kooperanta. Da biste podugovarali člana projektnog tima kao generički resurs, slijedite ove korake:

1.  Odaberite podugovarate na **stranici s detaljima o članu** tima.

2.  Možete odabrati samo kooperante **sa** **statusom Skica ili** Potvrđeno. **Zatvorene** ili **otkazane** podugovarače nije moguće odabrati. 

3.  **Polje retka kooperanta** postaje vidljivo nakon što odaberete kooperant.

4.  U **polju Redak kooperanta** možete odabrati samo retke kooperanta koji su za vrijeme. Ne možete odabrati retke kooperanta za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima mora odgovarati ulozi na liniji kooperanta. Time se osigurava da je vrijeme za ulogu koja se procjenjuje na projektu ista uloga koja se kupuje na retku kooperanta. 

Kada je generički član tima povezan s retkom kooperanta i kooperanta, **polje Vrsta radnika** u generičkom retku člana tima ažurirat će se na **Ugovorni** radnik, a valjanost **kooperanta bit će postavljena na** **Valjano**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima s osobljem
Kao i generički članovi tima ili članovi tima bez osoblja, kapacitet članova tima potreban za projekt također se može povezati s podizvođačem. Da biste podugovarali imenovanog člana projektnog tima, slijedite ove korake:

1.  Provjerite je li imenovani resurs postavljen kao vrsta resursa koji se može rezervirati kao ugovorni radnik. Također, provjerite odgovara li **polje Dobavljač** resursu koji se može rezervirati dobavljaču u kooperantu koji odaberete. 

2.  Podugovaranje možete odabrati samo u **statusu Skica** ili **Potvrđeno**. **Zatvorene** ili **otkazane** podugovarače nije moguće odabrati. 

3.  **Polje retka kooperanta** postaje vidljivo nakon što odaberete kooperant.

4.  U **polju Redak kooperanta** možete odabrati samo retke kooperanta koji su za vrijeme. Ne možete odabrati retke kooperanta za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima mora odgovarati ulozi na liniji kooperanta. Time se osigurava da je vrijeme za ulogu koja se procjenjuje na projektu ista uloga koja se kupuje na retku kooperanta. 

Imenovani članovi projektnog tima koji su postavljeni kao vrsta ugovornog radnika **resursa koji se može** rezervirati prikazat će se sa statusom valjanosti podugovora **koji nije valjan ako nisu povezani s** kooperantom. Kada je imenovani član projektnog tima povezan s retkom kooperanta i kooperanta, **polje Vrsta radnika** u retku člana tima ažurirat će se na **Ugovorni** radnik, a valjanost **kooperanta** bit će postavljena na **Valjano**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
