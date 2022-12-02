---
title: Podugovaranje članova projektnog tima
description: Ovaj članak objašnjava kako podugovarati članove projektnog tima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522786"
---
# <a name="subcontracting-project-team-members"></a>Podugovaranje članova projektnog tima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U aplikaciji Microsoft Dynamics 365 Project Operations možete odlučiti podugovarati članove projektnog tima koji imaju ili nemaju osoblje.

- Članovi projektnog tima koji nemaju osoblje imaju dodijeljen generički resurs.
- Članovi tima koji imaju osoblje imaju dodijeljen imenovani resurs.

Kada člana projektnog tima povežete s retkom podugovora, sve dodjele zadataka koje ima član tima ponovno će se obračunati na temelju nabavnog cjenika priloženog podugovoru.  Na kartici **Procjene** na stranici **Pojedinosti o projektu** odaberite gumb **Ažuriraj cijene** kako biste vidjeli ažurirane cijene i/ili troškove koji proizlaze iz odluke o podugovaranju. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima kojemu nije dodijeljeno osoblje
Stranica **Podaci o članu tima** ima polja za podugovor i redak podugovora koja omogućuju voditelju projekta da izrazi kako bi želio izvući potreban kapacitet iz podugovora. Za podugovaranje člana projektnog tima kao generičkog resursa slijedite ove korake:

1.  Odaberite podugovor na stranici **Pojedinosti o članu tima**.

2.  Možete odabrati samo podugovore koji imaju status **Skica** ili **Potvrđeno**. **Zatvoreni** ili **Otkazani** podugovori ne mogu se odabrati. 

3.  Polje **Redak podugovora** postaje vidljivo nakon odabira podugovora.

4.  U polju **Redak podugovora** možete odabrati samo retke podugovora koji su za vrijeme. Ne možete odabrati retke podugovora za trošak ili materijal.

5.  Uloga za zapis člana projektnog tima mora odgovarati ulozi na retku podugovora. Time se osigurava da je vrijeme za ulogu koja se procjenjuje na projektu isto kao i za ulogu koja je kupljena u retku podugovora. 

Kada se generički član tima poveže s podugovorom i retkom podugovora, polje **Vrsta radnika** u retku generičkog člana tima ažurirat će se na vrijednost **Ugovorni radnik**, a polje **Valjanost podugovora** postavit će se na **Valjano**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima kojemu je dodijeljeno osoblje
Poput generičkih članova tima ili članova tima koji imaju osoblje, kapaciteti članova tima koji nemaju osoblje potrebnih za projekt mogu se također povezati s podugovorom. Za podugovaranje imenovanog člana projektnog tima slijedite ove korake:

1.  Provjerite je li imenovani resurs postavljen kao tip resursa koji se može rezervirati Ugovorni radnik. Također, provjerite je odgovara li polje **Dobavljač** na resursu koji se može rezervirati dobavljaču na podugovoru koji odabirete. 

2.  Možete odabrati samo podugovore koji imaju status **Skica** ili **Potvrđeno**. **Zatvoreni** ili **Otkazani** podugovori ne mogu se odabrati. 

3.  Polje **Redak podugovora** postaje vidljivo nakon odabira podugovora.

4.  U polju **Redak podugovora** možete odabrati samo retke podugovora koji su za vrijeme. Ne možete odabrati retke podugovora za trošak ili materijal.

5.  Uloga za zapis člana projektnog tima mora odgovarati ulozi na retku podugovora. Time se osigurava da je vrijeme za ulogu koja se procjenjuje na projektu isto kao i za ulogu koja je kupljena u retku podugovora. 

Imenovani članovi projektnog tima koji su postavljeni kao ugovorni radnici tipa **Resurs koji se može rezervirati** prikazat će se sa statusom valjanosti podugovora **Nevaljano** ako nisu povezani s podugovorom. Kada se imenovani član projektnog tima poveže s podugovorom i retkom podugovora, polje **Vrsta radnika** u retku člana tima ažurirat će se na vrijednost **Ugovorni radnik**, a polje **Valjanost podugovora** postavit će se na **Valjano**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
