---
title: Praćenje rada na projektu
description: U ovoj temi nalaze se informacije o načinu praćenja rada na projektu i napretka posla.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710931"
---
# <a name="project-effort-tracking"></a>Praćenje rada na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Potreba praćenja napretka u odnosu na raspored razlikuje se ovisno o djelatnosti. Neke djelatnosti napredak prate na razini pojedinosti, dok ga druge prate na višoj razini. Ova tema pokazuje kako postaviti raspored da biste ispunili zahtjeve tvrtke ili ustanove.

## <a name="effort-tracking-view"></a>Prikaz praćenja rada

Prikaz **Praćenje rada** prati napredak zadataka u rasporedu uspoređujući stvarne radne sate utrošene na zadatak s planiranim radnim satima za zadatak. Dynamics 365 Project Operations upotrebljava sljedeće formule za izračun mjernih podataka o praćenju:

- **Postotak dovršenosti**: stvarni rad utrošen do datuma ÷ predviđen za dovršetak (EAC, Estimate at complete) 
- **Preostali rad**: Procijenjeni rad po završetku – stvarni rad izvršen do danas 
- **EAC**: preostali rad + stvarni rad do datuma 
- **Predviđeno odstupanje rada**: planirani rad – EAC

Project Operations prikazuje predviđanje odstupanja rada u zadatku. Ako je EAC veći od planiranog rada, predviđa se da će zadatak potrajati dulje nego što je prvotno planirano i da zaostaje za rasporedom. Ako je EAC manji od planiranog rada, predviđa se da će zadatak potrajati kraće nego što je prvotno planirano i da je ispred roka.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Ponovno projektiranje rada na zadacima lisnih čvorova

Upravitelji projekta često revidiraju izvorne procjene o zadatku. Ponovna predviđanja projekta proizlaze iz procjena upravitelja projekta s obzirom na trenutačno stanje projekta. Međutim, ne preporučujemo da voditelji projekata mijenjaju planirane količine rada. To je zbog toga što planirani rad na projektu predstavlja utvrđeni izvor istine za raspored projekta i procjenu troška, a svi su se dionici projekta složili s tim.

Voditelj projekta može ponoviti projektiranje rada na zadacima ažuriranjem zadanog **Preostalog rada** s novom procjenom zadatka. Ovo ažuriranje uzrokuje ponovno izračunavanje procjene po završetku zadatka (EAC, estimate at complete), postotka napretka i odstupanje projektnog rada na zadatku. EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ponovno predviđanje rada na zadacima sažetka

Rad na zadacima sažetka ili zadacima spremnika može se ponovno predvidjeti. Voditelji projekata mogu ažurirati preostali rad na zadacima sažetaka. Ažuriranje preostalog rada pokreće sljedeći skup izračuna u aplikaciji:

- Izračunava se EAC i postotak napretka na zadatku.
- Novi EAC distribuira se na podređene zadatke u istom omjeru kao izvorni EAC na zadatku.
- Izračunava se novi EAC za svaki od pojedinačnih zadataka lisnih čvorova. 
- Preostali rad i postotak napretka zahvaćenih podređenih zadataka niz lisne čvorove ponovno se izračunavaju na temelju vrijednosti EAC-a. To rezultira novim predviđanjem za odstupanje rada zadatka. 
- Ponovno se izračunavaju EAC-ovi zadataka sažetka sve do korijenskog čvora.


## <a name="project-status-summary"></a>Sažetak statusa projekta

Praćenje podataka u prikazu **Praćenje rada** i **Praćenje troškova** prikazuje napredak i potrošnju troškova u korijenskom čvoru projekta, zadacima sažetka i zadacima na razini lisnog čvora. Odjeljak **Status** na stranici **Entitet projekta** prikazuje sažetak statusa na razini projekta.

## <a name="status-summary-fields"></a>Polja sažetka statusa

Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta. Koristi kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik. Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu. Polje **Datum ažuriranja statusa** nije moguće uređivati, a vrijednost je vremenska oznaka koja označava kada je status zadnji put ažuriran.

Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju datuma praćenja. Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta polja možete postaviti na **Ispred**. Kada je odstupanje rasporeda i troška za korijenski čvor negativno, možete ih postaviti na **Iza**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
