---
title: Mogućnosti podugovaranja za članove projektnog tima
description: Ovaj tema objašnjava mogućnosti podugovaranja za članove projektnog tima u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903638"
---
# <a name="subcontracting-options-for-project-team-members"></a>Mogućnosti podugovaranja za članove projektnog tima

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U Dynamics 365 Project Operations Microsoftu možete procijeniti mogućnosti podugovaranja dostupne za jednog ili više članova projektnog tima. Dostupne mogućnosti podugovaranja omogućuju vam sljedeće:

- Kreirajte novi kooperant i/ili kreirajte nove retke na postojećem kooperantu za odabrane članove projektnog tima. 
- Rezervirajte prema već postojećem retku kooperanta i kooperanta. 

Možete birati između dostupnih mogućnosti podugovaranja za generičke članove projektnog tima ili odabrati članove projektnog tima koji imaju imenovani resurs koji je ugovorni radnik. 

Nema dostupnih mogućnosti podugovaranja za sljedeće:

- Članovi projektnog tima koji su zaposleni sa zaposlenikom. 
- Članovi projektnog tima koji su već pridruženi retku kooperanta i kooperanta. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima bez osoblja

Da biste pregledali i odabrali neku od dostupnih mogućnosti podugovaranja za generičkog člana projektnog tima ili člana projektnog tima bez osoblja, slijedite ove korake:

1. Odaberite jedan ili više zapisa članova projektnog tima u kojima je resurs generički resurs.
2. Provjerite nije li nijedan od odabranih zapisa članova projektnog tima već podugovaran. 
3. Odaberite **Mogućnosti podugovaranja** u podrešetki članova projektnog tima. Otvorit će **se dijaloški okvir Mogućnosti podugovaranja.** 
4. Ako ste u koraku 1 odabrali samo jedan zapis člana projektnog tima, bit će dostupne sljedeće mogućnosti:
    - Kreirajte nove retke kooperanta. 
    - Rezervirajte prema postojećem kooperantu Ako ste u koraku 1 odabrali više zapisa članova projektnog tima, jedina dostupna mogućnost je stvaranje novih redaka kooperanta.
5. Mogućnost rezerviranja u odnosu na postojeći redak kooperanta omogućuje odabir retka kooperanta i kooperanta protiv kojeg želite rezervirati. Prilikom odabira retka kooperanta za rezervaciju kapaciteta, trebali biste osigurati da odabrana linija kooperanta bude za vrijeme i da uloga potrebna članu projektnog tima odgovara ulozi kupljenoj na retku kooperanta.
6. Kada odaberete stvaranje novih redaka kooperanta za članove projektnog tima, sustav će vam omogućiti da odaberete kooperant koji želite kreirati te retke. Kooperant koji odaberete za kreiranje novih redaka trebao bi biti u **statusu** Skica. Pomoću ove mogućnosti stvaranja novih redaka kooperanta za odabrane članove projektnog tima, sustav će stvoriti jednu liniju kooperanta za vrijeme za svakog člana projektnog tima. Uloga, sati i datumi kopirat će se iz člana projektnog tima u svaki kreirani redak kooperanta. 
7. Kada je generički član tima povezan s retkom kooperanta i kooperanta, **polje Vrsta radnika** u generičkom retku člana tima ažurirat će se na **Ugovorni** radnik, a vrijednost Valjanost **kooperanta** postavit će se na **Valjano**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima s osobljem

Kao i generički članovi tima ili članovi tima bez osoblja, također možete vidjeti opcije podugovaranja za člana projektnog tima s osobljem sve dok je član tima s osobljem ugovorni radnik. Da biste pregledali i odabrali neku od dostupnih mogućnosti podugovaranja za člana projektnog tima s osobljem ili imenovanim članom projektnog tima, slijedite ove korake:

1. Odaberite jedan ili više zapisa članova projektnog tima u kojima je resurs imenovani ugovorni radnik.
2. Provjerite nije lidan od odabranih zapisa članova projektnog tima već kooperiran. 
3. Odaberite **Mogućnosti podugovaranja** u podrešetki članova projektnog tima. Otvorit će **se dijaloški okvir Mogućnosti podugovaranja.** 
4. Ako ste u koraku 1 odabrali samo jedan zapis člana projektnog tima, bit će dostupne sljedeće mogućnosti:
      - Kreirajte nove retke kooperanta.
      - Rezervirajte prema postojećem kooperantu.
  Ako ste u koraku 1 odabrali više zapisa članova projektnog tima, jedina dostupna mogućnost je stvaranje novih redaka kooperanta.
5. Mogućnost rezerviranja u odnosu na postojeći redak kooperanta omogućuje odabir retka kooperanta i kooperanta protiv kojeg želite rezervirati. Prilikom odabira retka kooperanta za rezervaciju kapaciteta provjerite sljedeće:
      - Odabrani redak kooperanta je za vrijeme. 
      - Uloga potrebna članu projektnog tima odgovara ulozi kupljenoj na liniji kooperanta. 
      - Dobavljač s kojim je ugovorni radnik povezan isti je kao i dobavljač u kooperantu.
6. Kada odaberete stvaranje novih redaka kooperanta za članove projektnog tima, sustav će vam omogućiti da odaberete kooperant koji želite kreirati te retke. Pomoću ove mogućnosti provjerite je li dobavljač kojem ugovorni radnik pripada isti kao i dobavljač u kooperantu. 
7. Kooperant koji odaberete za kreiranje novih redaka trebao bi biti u **statusu** Skica. Pomoću ove mogućnosti stvaranja novih redaka kooperanta za odabrane članove projektnog tima, sustav će stvoriti jednu liniju kooperanta za vrijeme za svakog člana projektnog tima. Uloga, sati i datumi kopirat će se iz člana projektnog tima u svaki kreirani redak kooperanta.  
8. Kada je imenovani član tima povezan s retkom kooperanta i kooperanta, polje Vrsta radnika u **retku** imenovanog člana tima ažurirat će se na **Ugovorni** radnik, a **vrijednost Valjanost kooperanta** postavit će se na **Valjano**.

## <a name="re-costing-subcontractor-assignments"></a>Dodjela kooperanta s ponovnim troškovima

Kada je član projektnog tima (generički ili imenovan) povezan s recima kooperanta pomoću **dijaloškog okvira Mogućnosti** kooperanta, sve dodjele zadataka koje član tima ima ponovno će se koštati na temelju popisa kupovnih cijena pridruženih kooperantu. Na **kartici Procjene** na **stranici Detalji o** projektu odaberite **gumb Ažuriraj cijene da biste vidjeli** ažurirane cijene i/ili troškove koji proizlaze iz odluke o podugovaranja.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
