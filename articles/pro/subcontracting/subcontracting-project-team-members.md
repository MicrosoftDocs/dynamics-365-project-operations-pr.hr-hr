---
title: Članovi projektnog tima kooperanta
description: Ovaj tema objašnjava kako kooperirati članove projektnog tima u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: b98fc356d7de77fa7f05667acaa5569a7053e4d1
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903632"
---
# <a name="subcontracting-project-team-members"></a>Članovi projektnog tima kooperanta

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U Dynamics 365 Project Operations Microsoftu možete odabrati podugovaranje članova projektnog tima bez osoblja ili osoblja.

- Članovi projektnog tima bez osoblja imaju dodijeljen generički resurs.
- Članovi tima s osobljem imaju dodijeljen imenovani resurs.

Kada člana projektnog tima povežete s retkom kooperanta, sve dodjele zadataka koje član tima ima ponovno će se izvršiti na temelju popisa kupovnih cijena pridruženih kooperantu.  Na **kartici Procjene** na **stranici Detalji o** projektu odaberite **gumb Ažuriraj cijene da biste vidjeli** ažurirane cijene i/ili troškove koji proizlaze iz odluke o podugovaranja. 

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
