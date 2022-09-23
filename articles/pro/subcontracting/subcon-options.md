---
title: Mogućnosti podugovaranja za članove projektnog tima
description: U ovom se članku objašnjavaju mogućnosti podugovaranja za članove projektnog tima u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522269"
---
# <a name="subcontracting-options-for-project-team-members"></a>Mogućnosti podugovaranja za članove projektnog tima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U programu Microsoft Dynamics 365 Project Operations možete procijeniti mogućnosti podugovaranja dostupne jednom ili više članova projektnog tima. Dostupne mogućnosti podugovaranja omogućuju vam sljedeće:

- Stvorite novi kooperant i/ili stvorite nove retke na postojećem podugovaranju za odabrane članove projektnog tima. 
- Rezervirajte na već postojećoj liniji podugovaranja i podugovaranja. 

Možete birati između dostupnih mogućnosti podugovaranja za generičke članove projektnog tima ili birati između članova projektnog tima koji imaju osoblje s imenovanim resursom koji je ugovorni radnik. 

Nema dostupnih mogućnosti podugovaranja za sljedeće:

- Članovi projektnog tima koji su radili sa zaposlenikom. 
- Članovi projektnog tima koji su već povezani s linijom podugovaranja i podugovaranja. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima bez osoblja

Da biste pregledali i odabrali jednu od dostupnih mogućnosti podugovaranja za generičkog člana projektnog tima ili člana projektnog tima bez osoblja, slijedite ove korake:

1. Odaberite jedan ili više zapisa članova projektnog tima u kojima je resurs generički resurs.
2. Provjerite nije li nijedan od odabranih zapisa članova projektnog tima već kooperant. 
3. Odaberite **Mogućnosti** podugovaranja u podrešetki članova projektnog tima. Otvorit će se **dijaloški okvir Mogućnosti** podugovaranja. 
4. Ako ste u prvom koraku odabrali samo jedan zapis člana projektnog tima, bit će dostupne sljedeće mogućnosti:
    - Stvorite nove retke kooperacije. 
    - Rezervirajte na postojećem podugovaranju Ako ste u prvom koraku odabrali više zapisa članova projektnog tima, jedina dostupna mogućnost je stvaranje novih redaka kooperacije.
5. Mogućnost rezerviranja u odnosu na postojeći redak podugovaranja omogućuje vam odabir retka podugovaratelja i podugovaranja prema kojem želite rezervirati. Prilikom odabira retka podugovaranja radi rezervacije kapaciteta, trebali biste osigurati da je odabrani redak kooperanta za vrijeme i da uloga potrebna članu projektnog tima odgovara ulozi kupljenoj u retku podugovaranja.
6. Kada odaberete stvaranje novih redaka kooperacije za članove projektnog tima, sustav će vam omogućiti da odaberete kooperant koji želite stvoriti te retke. Kooperant koji odaberete za stvaranje novih redaka u sustavu trebao bi biti u **statusu Skica**. S ovom mogućnošću stvaranja novih linija podugovaranja za odabrane članove projektnog tima, sustav će stvoriti jednu liniju kooperanta za vrijeme za svakog člana projektnog tima. Uloga, sati i datumi kopirat će se iz člana projektnog tima u svaki redak kooperanta koji se kreira. 
7. Kada je generički član tima povezan s retkom kooperanta i kooperanta, polje Vrsta **radnika u retku generičkog člana tima ažurirat** će se u Ugovorni radnik **,** a **vrijednost Valjanost kooperanta** postavit će se na **Valjano**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima s osobljem

Poput generičkih ili nepokolebljivih članova tima, također možete vidjeti opcije podugovaranja za člana projektnog tima s osobljem sve dok je član tima s osobljem ugovorni radnik. Da biste pregledali i odabrali jednu od dostupnih mogućnosti podugovaranja za zaposlenika ili imenovanog člana projektnog tima, slijedite ove korake:

1. Odaberite jedan ili više zapisa članova projektnog tima u kojima je resurs imenovani ugovorni radnik.
2. Provjerite nije li nijedan od odabranih zapisa članova projektnog tima već podizvođač. 
3. Odaberite **Mogućnosti** podugovaranja u podrešetki članova projektnog tima. Otvorit će se **dijaloški okvir Mogućnosti** podugovaranja. 
4. Ako ste u prvom koraku odabrali samo jedan zapis člana projektnog tima, bit će dostupne sljedeće mogućnosti:
      - Stvorite nove retke kooperacije.
      - Rezervirajte protiv postojećeg podugovaratelja.
  Ako ste odabrali više zapisa članova projektnog tima u prvom koraku, jedina dostupna mogućnost je stvaranje novih redaka kooperanta.
5. Mogućnost rezerviranja u odnosu na postojeći redak podugovaranja omogućuje vam odabir retka podugovaratelja i podugovaranja prema kojem želite rezervirati. Prilikom odabira retka podugovaranja radi rezervacije kapaciteta, trebali biste osigurati sljedeće:
      - Odabrani redak kooperanta je za vrijeme. 
      - Uloga potrebna članu projektnog tima odgovara ulozi kupljenoj u retku podugovaranja. 
      - Dobavljač s kojim je povezan ugovorni radnik isti je kao i dobavljač na kooperantu.
6. Kada odaberete stvaranje novih redaka kooperacije za članove projektnog tima, sustav će vam omogućiti da odaberete kooperant koji želite stvoriti te retke. Pomoću ove mogućnosti trebali biste osigurati da je dobavljač kojem pripada ugovorni radnik isti kao i dobavljač na podugovaranju. 
7. Kooperant koji odaberete za stvaranje novih redaka u sustavu trebao bi biti u **statusu Skica**. S ovom mogućnošću stvaranja novih linija podugovaranja za odabrane članove projektnog tima, sustav će stvoriti jednu liniju kooperanta za vrijeme za svakog člana projektnog tima. Uloga, sati i datumi kopirat će se iz člana projektnog tima u svaki redak kooperanta koji se kreira.  
8. Kada je imenovani član tima povezan s retkom podugovaratelja i podugovaratelja, polje Vrsta **radnika u retku imenovanog člana tima ažurirat** će se u Ugovorni radnik **,** a **vrijednost Valjanost kooperanta** postavit će se na **Valjano**.

## <a name="re-costing-subcontractor-assignments"></a>Re-costing dodjele kooperanata

Kada je član projektnog tima (generički ili imenovan) povezan s recima podugovaranja pomoću dijaloškog **okvira Mogućnosti** podugovaranja, sve dodjele zadataka koje član tima ima ponovno će se koštati na temelju popisa cijena nabave priloženog kooperantu. Na kartici **Procjene** na **stranici Detalji o** projektu odaberite **gumb Ažuriraj cijene** da biste vidjeli ažurirane cijene i/ili troškove koji proizlaze iz odluke o podugovaranju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
