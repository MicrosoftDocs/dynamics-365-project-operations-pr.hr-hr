---
title: Mogućnosti podugovaranja za članove projektnog tima
description: Ovaj članak objašnjava opcije podugovaranja za članove projektnog tima u aplikaciji Microsoft Dynamics 365 Project Operations.
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

U aplikaciji Microsoft Dynamics 365 Project Operations možete procijeniti opcije podugovaranja dostupne za jednog ili više članova projektnog tima. Dostupne opcije podugovaranja omogućuju vam:

- Stvaranje novog podugovora i/ili stvaranje novih redaka u postojećem podugovoru za odabrane članove projektnog tima. 
- Rezerviranje za postojeći podugovor i redak podugovora. 

Možete birati između dostupnih opcija podugovaranja za generičke članove projektnog tima ili birati među članovima projektnog tima kojima je dodijeljeno osoblje s imenovanim resursom koji je ugovorni radnik. 

Nema dostupnih opcija podugovaranja za sljedeće:

- Članove projektnog tima kojima je kao osoblje dodijeljen zaposlenik. 
- Članove projektnog tima koji su već pridruženi podugovoru i retku podugovora. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima kojemu nije dodijeljeno osoblje

Da biste pregledali i odabrali među dostupnim opcijama podugovaranja za generičkog člana ili člana projektnog tima bez osoblja, slijedite ove korake:

1. Odaberite jedan ili više zapisa članova projektnog tima gdje je resurs generički resurs.
2. Osigurajte da nijedan od odabranih zapisa članova projektnog tima nije već podugovoren. 
3. Odaberite **Mogućnosti podugovaranja** na podrešetki članova projektnog tima. Otvara se dijaloški okvir **Opcije podugovaranja**: 
4. Ako ste u koraku 1 odabrali samo jedan zapis člana projektnog tima, bit će dostupne sljedeće opcije:
    - Stvorite nove retke podugovora. 
    - Rezerviranje prema postojećem podugovoru Ako ste u koraku 1 odabrali više zapisa članova projektnog tima, tada je jedina dostupna opcija stvaranje novih redaka podugovora.
5. Opcija rezerviranja za postojeći redak podugovora omogućuje vam odabir podugovora i retka podugovora za koje želite rezervirati. Prilikom odabira retka podugovora za rezerviranje kapaciteta, trebali biste osigurati da je odabrani redak podugovora za vrijeme i da uloga potrebna za člana projektnog tima odgovara ulozi koja je kupljena u retku podugovora.
6. Kada odaberete stvaranje novih redaka podugovora za članove projektnog tima, sustav će vam omogućiti da odaberete podugovor za koji želite stvoriti ove retke. Podugovor koji ste odabrali za stvaranje novih redaka trebao bi biti statusa **Skica**. S ovom opcijom za stvaranje novih redaka podugovora za odabrane članove projektnog tima, sustav će stvoriti jedan redak podugovora za vrijeme za svakog člana projektnog tima. Uloga, sati i datumi kopirat će se od člana projektnog tima u svaki stvoreni redak podugovora. 
7. Kada se generički član tima poveže s podugovorom i retkom podugovora, polje **Vrsta radnika** u retku generičkog člana tima ažurirat će se na vrijednost **Ugovorni radnik**, a vrijednost polja **Valjanost podugovora** postavit će se na **Valjano**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima kojemu je dodijeljeno osoblje

Poput generičkih članova tima ili članova tima bez osoblja, također možete vidjeti opcije podugovaranja za člana projektnog tima s osobljem sve dok je član tima s osobljem ugovorni radnik. Da biste pregledali i odabrali među dostupnim opcijama podugovaranja za člana projektnog tima s osobljem ili imenovanog člana projektnog tima, slijedite ove korake:

1. Odaberite jedan ili više zapisa članova projektnog tima gdje je resurs imenovani ugovorni radnik.
2. Osigurajte da nijedan od odabranih zapisa članova projektnog tima nije već podugovoren. 
3. Odaberite **Mogućnosti podugovaranja** na podrešetki članova projektnog tima. Otvara se dijaloški okvir **Opcije podugovaranja**: 
4. Ako ste u koraku 1 odabrali samo jedan zapis člana projektnog tima, bit će dostupne sljedeće opcije:
      - Stvorite nove retke podugovora.
      - Rezervirajte za postojeći podugovor.
  Ako ste u koraku 1 odabrali više zapisa članova projektnog tima, tada je jedina dostupna opcija stvaranje novih redaka podugovora.
5. Opcija rezerviranja za postojeći redak podugovora omogućuje vam odabir podugovora i retka podugovora za koje želite rezervirati. Prilikom odabira retka podugovora za rezerviranje kapaciteta, trebali biste osigurati sljedeće:
      - Odabrani redak podugovora je za vrijeme. 
      - Uloga koja je potrebna za člana projektnog tima odgovara ulozi koja je kupljena u retku podugovora. 
      - Dobavljač s kojim je ugovorni radnik povezan isti je kao i dobavljač na podugovoru.
6. Kada odaberete stvaranje novih redaka podugovora za članove projektnog tima, sustav će vam omogućiti da odaberete podugovor za koji želite stvoriti ove retke. Kod ove opcije trebate osigurati da je dobavljač kojemu pripada ugovorni radnik isti kao i dobavljač na podugovoru. 
7. Podugovor koji ste odabrali za stvaranje novih redaka trebao bi biti statusa **Skica**. S ovom opcijom za stvaranje novih redaka podugovora za odabrane članove projektnog tima, sustav će stvoriti jedan redak podugovora za vrijeme za svakog člana projektnog tima. Uloga, sati i datumi kopirat će se od člana projektnog tima u svaki stvoreni redak podugovora.  
8. Kada se imenovani član tima poveže s podugovorom i retkom podugovora, polje **Vrsta radnika** u retku imenovanog člana tima ažurirat će se na vrijednost **Ugovorni radnik**, a vrijednost polja **Valjanost podugovora** postavit će se na **Valjano**.

## <a name="re-costing-subcontractor-assignments"></a>Ponovno obračunavanje dodjela podizvođača

Kada se član projektnog tima (generički ili imenovani) poveže s redcima podugovora korištenjem dijaloškog okvira **Opcije podugovaranja**, sve dodjele zadataka koje ima član tima ponovno će se obračunati na temelju nabavnog cjenika priloženog podugovoru. Na kartici **Procjene** na stranici **Pojedinosti o projektu** odaberite gumb **Ažuriraj cijene** kako biste vidjeli ažurirane cijene i/ili troškove koji proizlaze iz odluke o podugovaranju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
