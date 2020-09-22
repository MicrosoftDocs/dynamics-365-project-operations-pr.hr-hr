---
title: Napredak projekta i potrošnja troškova
description: Ova tema pruža informacije o tome kako pratiti napredak projekta i potrošnju troškova.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750183"
---
# <a name="project-progress-and-cost-consumption"></a>Napredak projekta i potrošnja troškova

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Potreba praćenja napretka u odnosu na raspored razlikuje se ovisno o djelatnosti. Neke djelatnosti napredak prate na granularnoj razini, dok ga druge prate na višoj razini. Ova tema pokazuje kako postaviti raspored da biste ispunili zahtjeve tvrtke ili ustanove.

## <a name="effort-tracking-view"></a>Prikaz praćenja rada

Prikaz **Praćenje truda** prati napredak zadataka u rasporedu. Uspoređuje stvarne sate rada potrošene na zadatak i planirane sate rada za taj zadatak. PSA koristi sljedeće formule za izračun mjernih podataka o praćenju:

- Postotak napretka = stvarni rad do danas ÷ planirani rad za zadatak 
- Predviđeni dovršetak (ETC) = planirani rad – stvarni rad do danas 
- Predviđeni dovršetak (EAC) = preostali rad + stvarni rad do danas 
- Predviđeno odstupanje rada = planirani rad – EAC

PSA prikazuje predviđanje odstupanja rada u zadatku. Ako je EAC veći od planiranog rada, predviđa se da će zadatak potrajati dulje nego što je izvorno planirano. Stoga kasni za rasporedom. Ako je EAC manji od planiranog rada, predviđa se da će zadatak potrajati kraće nego što je izvorno planirano. Stoga će se dovršiti prije roka.

## <a name="re-projecting-effort"></a>Ponovno predviđanje rada

Uobičajeno je da upravitelj projekta revidira izvorne procjene u zadatku. Ponovna predviđanja projekta proizlaze iz procjena upravitelja projekta s obzirom na trenutačno stanje projekta. Međutim, upraviteljima projekta ne preporučujemo promjenu osnovnih brojeva, jer osnova projekta predstavlja utvrđeni izvor podataka za raspored projekta i procjenu troškova oko koje su se sve zainteresirane strane dogovorile.

Postoje dva načina na koje upravitelj projekta može ponovno procijeniti rad na zadacima:

- Nadjačajte zadani ETC novom procjenom stvarnog preostalog rada zadatka. 
- Nadjačajte zadani postotak napretka novom procjenom stvarnog napretka zadatka.

Svaki od tih pristupa uzrokuje ponovno izračunavanje ETC-a, EAC-a i postotka napretka zadatka te predviđena odstupanja rada na zadatku. EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Ponovno predviđanje rada na zadacima sažetka

Rad na zadacima sažetka ili zadacima spremnika može se ponovno predvidjeti. Bez obzira na to hoće li korisnik izvršiti ponovno predviđanje pomoću preostalog rada ili postotka napretka na zadacima sažetka, pokreće se sljedeći skup izračuna:

- Izračunačava se EAC, ETC i postotak napretka na zadatku.
- Novi EAC distribuira se na podređene zadatke u istom omjeru kao izvorni EAC na zadatku.
- Izračunava se novi EAC za svaki od pojedinačnih zadataka lisnih čvorova. 
- ETC i postotak napretka za zahvaćene podređene zadatke lisnih čvorova ponovno se izračunavaju na temelju vrijednosti EAC-a. To rezultira novim predviđanjem za odstupanje rada zadatka. 
- Ponovno se izračunavaju EAC-ovi zadataka sažetka sve do korijenskog čvora.

### <a name="cost-tracking-view"></a>Prikaz praćenja troškova 

Prikaz **Praćenje troškova** uspoređuje stvarni trošak koji je potrošen na zadatak s planiranim troškom zadatka. 

> [!NOTE]
> Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procjena troškova. 

PSA koristi sljedeće formule za izračun mjernih podataka o praćenju:

- Postotak potrošenog troška = stvarni trošak do danas ÷ planirani trošak za zadatak
- Trošak za dovršetak (CTC) = planirani trošak – stvarni trošak do danas
- EAC = CTC + stvarni trošak do danas
- Predviđeno odstupanje troškova = planirani trošak – EAC

Predviđanje odstupanja troškova prikazuje se u zadatku. Ako je EAC veći od planiranog troška, predviđa se da će zadatak imati veći trošak nego što je izvorno planirano. Stoga postoji tendencija premašivanja proračuna. Ako je EAC manji od planiranog troška, predviđa se da će zadatak imati manji trošak nego što je izvorno planirano. Stoga postoji tendencija neiskorištavanja proračuna.

## <a name="project-managers-re-projection-of-cost"></a>Ponovno predvđanje troškova upravitelja projekta

Kada se rad ponovno predvidi, CTC, EAC, postotak potrošenog troška i predviđeno odstupanje troška ponovno se izračunavaju u prikazu **Praćenje troškova**.

## <a name="project-status-summary"></a>Sažetak statusa projekta

Praćenje podataka u prikazu **Praćenje rada** i **Praćenje troškova** prikazuje napredak i potrošnju troškova u korijenskom čvoru projekta, zadacima sažetka i zadacima na razini lisnog čvora. Odjeljak **Status** na stranici **Entitet projekta** prikazuje sažetak statusa na razini projekta.

## <a name="status-summary-fields"></a>Polja sažetka statusa

Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta. Koristi kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik. Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu. Polje **Datum ažuriranja statusa** nije moguće uređivati, a vrijednost je vremenska oznaka koja označava kada je status zadnji put ažuriran.

Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju datuma praćenja. Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta polja možete postaviti na **Ispred**. Kada je odstupanje rasporeda i troška za korijenski čvor negativno, možete ih postaviti na **Iza**.
