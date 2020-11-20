---
title: Napredak projekta i cijena troška
description: U ovoj temi nalaze se informacije o načinu praćenja napretka projekta i potrošnje troškova.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0793ee0c75bcbdde0fd92a16634457f73f872b5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120624"
---
# <a name="project-progress-and-cost-consumption"></a>Napredak projekta i cijena troška

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Potreba praćenja napretka u odnosu na raspored razlikuje se ovisno o djelatnosti. Neke djelatnosti napredak prate na granularnoj razini, dok ga druge prate na višoj razini. Ova tema pokazuje kako postaviti raspored da biste ispunili zahtjeve tvrtke ili ustanove.

## <a name="effort-tracking-view"></a>Prikaz praćenja rada

Prikaz **Praćenje truda** prati napredak zadataka u rasporedu. Uspoređuje sate stvarnog rada utrošenog na zadatak s planiranim satima rada na tom zadatku. Project Service Automation upotrebljava sljedeće formule za izračun mjernih podataka o praćenju:

Na početku rada na stvaranju zadatka: Planirani troškovi postavljaju se na procijenjeni trošak na završetku. Nakon što se stvarni podaci zabilježe na zadatku, slijedi izračun u prikazu praćenja za rad

- Postotak dovršenosti = stvarni rad utrošen do danas ÷ procijenjeni rad na završetku (EAC, Estimate at complete) 
- Procijenjeni rad na završetku (ETC) = procijenjeni rada na završetku (EAC) – stvarni rad utrošen do danas 
- EAC = preostali rad + stvarni rad do danas 
- Predviđeno odstupanje rada = planirani rad – EAC

Project Service Automation prikazuje predviđanje odstupanja rada u zadatku. Ako je EAC veći od planiranog rada, predviđa se da će zadatak potrajati dulje nego što je izvorno planirano. Stoga kasni za rasporedom. Ako je EAC manji od planiranog rada, predviđa se da će zadatak potrajati kraće nego što je izvorno planirano. Stoga će se dovršiti prije roka.

## <a name="reprojecting-effort"></a>Ponovno predviđanje rada

Uobičajeno je da upravitelj projekta revidira izvorne procjene u zadatku. Ponovna predviđanja projekta proizlaze iz procjena upravitelja projekta s obzirom na trenutačno stanje projekta. Međutim, upraviteljima projekta ne preporučujemo promjenu osnovnih brojeva, jer osnova projekta predstavlja utvrđeni izvor podataka za raspored projekta i procjenu troškova oko koje su se sve zainteresirane strane dogovorile.

Postoje dva načina na koja upravitelj projekta može ponovno predvidjeti rad na zadacima:

- Nadjačajte zadani ETC novom procjenom stvarnog preostalog rada zadatka. 
- Nadjačajte zadani postotak napretka novom procjenom stvarnog napretka zadatka.

Svaki od tih pristupa uzrokuje ponovno izračunavanje ETC-a, EAC-a i postotka napretka zadatka te predviđena odstupanja rada na zadatku. EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ponovno predviđanje rada na zadacima sažetka

Rad na zadacima sažetka ili zadacima spremnika može se ponovno predvidjeti. Bez obzira na to hoće li korisnik izvršiti ponovno predviđanje pomoću preostalog rada ili postotka napretka na zadacima sažetka, pokreće se sljedeći skup izračuna:

- Izračunačava se EAC, ETC i postotak napretka na zadatku.
- Novi EAC distribuira se na podređene zadatke u istom omjeru kao izvorni EAC na zadatku.
- Izračunava se novi EAC za svaki od pojedinačnih zadataka lisnih čvorova. 
- ETC i postotak napretka za zahvaćene podređene zadatke lisnih čvorova ponovno se izračunavaju na temelju vrijednosti EAC-a. To rezultira novim predviđanjem za odstupanje rada zadatka. 
- Ponovno se izračunavaju EAC-ovi zadataka sažetka sve do korijenskog čvora.

### <a name="cost-tracking-view"></a>Prikaz praćenja troškova 

Prikaz **Praćenje troškova** uspoređuje stvarni trošak koji je potrošen na zadatak s planiranim troškom. 

> [!NOTE]
> Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procjena troškova. 

Project Service Automation upotrebljava sljedeće formule za izračun mjernih podataka o praćenju:

Kada se stvara zadatak, planirani trošak jednak je procijenjenom trošku na završetku. Nakon što se stvarni podaci zabilježe na zadatku, slijedi izračun u prikazu **Praćenje** za trošak:

 - Postotak utrošenog troška = stvarni trošak utrošen do danas ÷ procijenjeni trošak na završetku zadatka
 - Trošak na završetku (CTC, Cost to complete) = procijenjeni trošak na završetku – stvarni trošak utrošen do danas
 - Procijenjeni trošak na završetku = CTC + stvarni trošak utrošen do danas
 - Predviđeno odstupanje troška = planirani trošak – procijenjeni trošak na završetku

Predviđanje odstupanja troškova prikazuje se u zadatku. Ako je procijenjeni trošak na završetku veći od planiranog troška, predviđa se da će zadatak imati veći trošak nego što je izvorno planirano. Stoga postoji tendencija premašivanja proračuna. Ako je procijenjeni trošak na završetku manji od planiranog troška, predviđa se da će zadatak imati manji trošak nego što je izvorno planirano i postoji tendencija neiskorištavanja proračuna.

## <a name="project-managers-reprojection-of-cost"></a>Ponovno predvđanje troškova od strane upravitelja projekta

Kada se rad ponovno predviđa, CTC, procijenjeni trošak na završetku, postotak utrošenog troška i predviđeno odstupanje troška ponovno se izračunavaju u prikazu **Praćenje troškova**.

## <a name="project-status-summary"></a>Sažetak statusa projekta

Praćenje podataka u prikazu **Praćenje rada** i **Praćenje troškova** prikazuje napredak i potrošnju troškova u korijenskom čvoru projekta, zadacima sažetka i zadacima na razini lisnog čvora. Odjeljak **Status** na stranici **Entitet projekta** prikazuje sažetak statusa na razini projekta.

## <a name="status-summary-fields"></a>Polja sažetka statusa

Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta. Koristi kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik. Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu. Polje **Datum ažuriranja statusa** nije moguće uređivati, a vrijednost je vremenska oznaka koja označava kada je status zadnji put ažuriran.

Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju datuma praćenja. Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta polja možete postaviti na **Ispred**. Kada je odstupanje rasporeda i troška za korijenski čvor negativno, možete ih postaviti na **Iza**.
