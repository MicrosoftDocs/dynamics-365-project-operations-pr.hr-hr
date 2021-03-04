---
title: Pregled praćenja projekta
description: Ova tema pruža informacije o tome kako pratiti napredak projekta i potrošnju troškova.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127331"
---
# <a name="project-tracking-overview"></a>Pregled praćenja projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Potreba praćenja napretka u odnosu na raspored razlikuje se ovisno o djelatnosti. Neke djelatnosti napredak prate na razini pojedinosti, dok ga druge prate na višoj razini. Ova tema pokazuje kako postaviti raspored da biste ispunili zahtjeve tvrtke ili ustanove.

## <a name="effort-tracking-view"></a>Prikaz praćenja rada

Prikaz **Praćenje rada** prati napredak zadataka u rasporedu uspoređujući stvarne radne sate utrošene na zadatak s planiranim radnim satima za zadatak. Dynamics 365 Project Operations upotrebljava sljedeće formule za izračun mjernih podataka o praćenju:

- **Postotak dovršenosti**: stvarni rad utrošen do datuma ÷ predviđen za dovršetak (EAC, Estimate at complete) 
- **Predviđen za dovršetak (ETC)**: planirani rad – stvarni rad utrošen do datuma 
- **EAC**: preostali rad + stvarni rad do datuma 
- **Predviđeno odstupanje rada**: planirani rad – EAC

Project Operations prikazuje predviđanje odstupanja rada u zadatku. Ako je EAC veći od planiranog rada, predviđa se da će zadatak potrajati dulje nego što je prvotno planirano i da zaostaje za rasporedom. Ako je EAC manji od planiranog rada, predviđa se da će zadatak potrajati kraće nego što je prvotno planirano i da je ispred roka.

## <a name="reprojecting-effort"></a>Ponovno predviđanje rada

Upravitelji projekta često revidiraju izvorne procjene o zadatku. Ponovna predviđanja projekta proizlaze iz procjena upravitelja projekta s obzirom na trenutačno stanje projekta. Međutim, ne preporučujemo da voditelji projekata mijenjaju osnovne brojeve. To je zbog toga što osnova projekta predstavlja utvrđeni izvor podataka za raspored projekta i procjenu troškova oko koje su se sve zainteresirane strane dogovorile.

Postoje dva načina na koja upravitelj projekta može ponovno predvidjeti rad na zadacima:

- Nadjačajte zadani ETC novom procjenom stvarnog preostalog rada zadatka. 
- Nadjačajte zadani postotak napretka novom procjenom stvarnog napretka zadatka.

Svaki pristup uzrokuje ponovno izračunavanje ETC-a, EAC-a i postotka napretka zadatka te predviđena odstupanja rada na zadatku. EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ponovno predviđanje rada na zadacima sažetka

Rad na zadacima sažetka ili zadacima spremnika može se ponovno predvidjeti. Bez obzira na to hoće li korisnik izvršiti ponovno predviđanje pomoću preostalog rada ili postotka napretka na zadacima sažetka, pokreće se sljedeći skup izračuna:

- Izračunačava se EAC, ETC i postotak napretka na zadatku.
- Novi EAC distribuira se na podređene zadatke u istom omjeru kao izvorni EAC na zadatku.
- Izračunava se novi EAC za svaki od pojedinačnih zadataka lisnih čvorova. 
- ETC i postotak napretka za zahvaćene podređene zadatke lisnih čvorova ponovno se izračunavaju na temelju vrijednosti EAC-a. To rezultira novim predviđanjem za odstupanje rada zadatka. 
- Ponovno se izračunavaju EAC-ovi zadataka sažetka sve do korijenskog čvora.

### <a name="cost-tracking-view"></a>Prikaz praćenja troškova 

Prikaz **Praćenje troškova** uspoređuje stvarni trošak koji je potrošen na zadatak s planiranim troškom zadatka. 

> [!NOTE]
> Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procjena troškova. Project Operations upotrebljava sljedeće formule za izračun mjernih podataka o praćenju:

- **Postotak utrošenog troška**: stvarni trošak utrošen do datuma ÷ procijenjeni trošak na završetku zadatka
- **Trošak za dovršetak (CTC)**: planirani trošak – stvarni trošak do datuma
- **EAC**: preostali troškovi + stvarni troškovi potrošeni do datuma
- **Predviđeno odstupanje troškova**: planirani trošak – EAC

Predviđanje odstupanja troškova prikazuje se u zadatku. Ako je EAC veći od planiranog troška, predviđa se da će zadatak imati veći trošak nego što je izvorno planirano. Stoga postoji tendencija premašivanja proračuna. Ako je EAC manji od planiranog troška, predviđa se da će zadatak imati manji trošak nego što je izvorno planirano. Stoga postoji tendencija neiskorištavanja proračuna.

## <a name="project-managers-reprojection-of-cost"></a>Ponovno predvđanje troškova od strane upravitelja projekta

Kada se rad ponovno predvidi, CTC, EAC, postotak potrošenog troška i predviđeno odstupanje troška ponovno se izračunavaju u prikazu **Praćenje troškova**.

## <a name="project-status-summary"></a>Sažetak statusa projekta

Praćenje podataka u prikazu **Praćenje rada** i **Praćenje troškova** prikazuje napredak i potrošnju troškova u korijenskom čvoru projekta, zadacima sažetka i zadacima na razini lisnog čvora. Odjeljak **Status** na stranici **Entitet projekta** prikazuje sažetak statusa na razini projekta.

## <a name="status-summary-fields"></a>Polja sažetka statusa

Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta. Koristi kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik. Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu. Polje **Datum ažuriranja statusa** nije moguće uređivati, a vrijednost je vremenska oznaka koja označava kada je status zadnji put ažuriran.

Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju datuma praćenja. Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta polja možete postaviti na **Ispred**. Kada je odstupanje rasporeda i troška za korijenski čvor negativno, možete ih postaviti na **Iza**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]