---
title: Načini dodjele rezervacija
description: U ovoj se temi nalaze informacije o tome kako načini dodjele rezervacija funkcioniraju u aplikaciji Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: cc539a376088627aa8d3e9678b2aec4bd5d0edc3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121479"
---
# <a name="booking-allocation-methods"></a>Načini dodjele rezervacija

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Neovisno o tome dodajete li člana tima izravno projektu na kartici **Tim** ili rezervirate resurs za projekt ili zahtjev s ploče rasporeda, postoji nekoliko različitih načina dodjele rezervacija koje možete koristiti. Ova tema objašnjava kako svaki od tih načina radi i koji način može dovesti do prevelikog broja rezervacija resursa.

## <a name="booking-allocation-methods"></a>Načini dodjele rezervacija

Možete upotrebljavati šest načina dodjele rezervacija:

- [Puni kapacitet](#full)
- [Preostali kapacitet](#remaining)
- [Postotni kapacitet](#percentage)
- [Ravnomjerna raspodjela sati](#evenly)
- [Sati umetnuti sprijeda](#front)
- [Nema](#none)

### <a name="full-capacity"></a><a name="full"></a>Puni kapacitet 
Način Puni kapacitet rezervira puni kapacitet resursa za odabrane datume od i do. Ako je, na primjer, za određeni resurs kalendar postavljen na rad od osam sati dnevno, pet dana u tjednu, postavljanje datuma početka i završetka koji pokrivaju pet radnih dana rezervira resurs na 40 sati. Rezervacija se vrši bez obzira na preostali kapacitet resursa. Ako je resurs već rezerviran tijekom tog razdoblja na drugim projektima, 40 sati se rezerviraju kao dodatni sati, što može dovesti do prevelikog broja rezervacija.

### <a name="remaining-capacity"></a><a name="remaining"></a>Preostali kapacitet
Način Preostali kapacitet dostupan je samo kada rezervirate izravno na projekt koristeći ploču s rasporedom. Ova metoda rezervira dostupni kapacitet resursa u navedenom datumskom rasponu. Na primjer, ako resurs ima kapacitet 40 sati tjedno i već je rezerviran 10 sati, rezervacija za isti tjedan dovodi do rezerviranja preostalih 30 sati kapaciteta za taj tjedan.

### <a name="percentage-capacity"></a><a name="percentage"></a>Postotni kapacitet
Način Postotni kapacitet rezervira resurs za postotak kapaciteta za odabrane datume od i do. Ako je, na primjer, kalendar resursa postavljen na rad od osam sati dnevno, pet dana u tjednu, postavljanje datuma početka i završetka koji pokrivaju pet radnih dana pri kapacitetu od 50% rezervira resurs na 20 sati. Pojedinačne dnevne rezervacije se ravnomjerno raspoređuju tijekom određenog razdoblja, četiri sata dnevno u ovom primjeru. Rezervacija se vrši bez obzira na preostali kapacitet resursa. Ako je resurs već rezerviran tijekom tog razdoblja na drugim projektima, 20 sati se rezerviraju kao dodatni sati, što može dovesti do prevelikog broja rezervacija.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Ravnomjerno raspodijeljeni sati
Način Ravnomjerna raspodjela po satima rezervira resurs na određeni broj sati, ravnomjerno ih raspoređujući svakog dana za vrijeme određenih od i do datuma. Ako, na primjer, rezervirate resurs na 20 sati tijekom razdoblja od pet dana, ovaj način raspodjeljuje 20 sati ravnomjerno na četiri sata dnevno. Rezervacija se vrši bez obzira na preostali kapacitet resursa. Ako je resurs već rezerviran tijekom tog razdoblja na drugim projektima, 20 sati se rezerviraju kao dodatni sati, što može dovesti do prevelikog broja rezervacija.

### <a name="front-load-hours"></a><a name="front"></a>Sati umetnuti sprijeda
Način Punjenje sprijeda po satima rezervira resurs na određeni broj sati, umečući sprijeda sate svakog dana za vrijeme određenih od i do datuma. Umetanje sprijeda troši dostupni kapacitet resursa po pravilu "prvo-troši-što-je-prvo-na-redu". Ako je, na primjer, radni raspored resursa osam sati dnevno pet dana u tjednu, i trenutačno nema rezervacija, rezerviranje tog resursa na 20 sati tijekom razdoblja od 5 radnih dana rezultirat će sljedećim uzorkom dnevne rezervacije: 

|                           |    Dan 1    |    Dan 2    |    Dan 3    |    Dan 4    |    Dan 5    |    Ukupno    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Postojeće   rezervacije**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nova   rezervacija**          |    8        |    8        |    4        |    0        |    0        |    20       |

Metoda umetanja sprijeda uzima u obzir postojeće rezervacije i dostupni kapacitet. Ako, na primjer, određeni resurs već ima rezerviranih 20 sati u određenom radnom tjednu, nove rezervacije troše preostali kapacitet na sljedeći način:

|                     | Dan 1 | Dan 2 | Dan 3 | Dan 4 | Dan 5 | Ukupno |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Postojeće   rezervacije** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Nova   rezervacija**       | 0     | 0     | 4     | 8     | 8     | 20    |

Budući da se preostali kapacitet uzima u obzir, možete dobiti poruku o pogrešci ako resurs nema preostalog kapaciteta koji se može potrošiti rezervacijom. S ovom metodom ne možete prebukirati.

### <a name="none"></a><a name="none"></a>Nema
Način Nijedna je dostupan samo kada rezervirate putem kartice **Tim** unutar projekta. Ova metoda dodaje resurs kao člana tima projekta, ali ne stvara nikakve rezervacije koje troše kapacitet resursa. Ova metoda se koristi kada se, nakon stvaranja projekta, doda član tima koji je zadani upravitelj projekta. Korisnik koji je upravitelj projekta i koji je stvorio projekat automatski se dodaje projektu da bi zapis entiteta projekta imao vlasnika i da bi postojao jedan odobravatelj u projektu. Budući da taj korisnik nema nikakve rezervacije, ako želite rezervirati resurs, možete ga izbrisati i zatim ponovno dodati koristeći drugi način dodjele ili dodati resurs zadacima i zatim koristiti **Produži rezervacije** na kartici **Usklađivanje** da biste izradili rezervacije za zadatke.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Metode dodjeljivanja koje dovode do prebukiranja
Da sumiramo, sljedeće metode dodjeljivanja dovode do prebukiranja ako je resurs već dodijeljen drugim projektima (ili drugim radnim nalozima ili entitetima koje je moguće zakazati):

- Puni kapacitet
- Postotni kapacitet
- Ravnomjerno raspodijeli sate

Kada koristite bilo koju od ove tri metode dodjeljivanja, nećete biti obaviješteni da je resurs prebukiran. Da biste riješili problem prevelikog broja rezervacija, morat ćete koristiti ploču s rasporedom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]