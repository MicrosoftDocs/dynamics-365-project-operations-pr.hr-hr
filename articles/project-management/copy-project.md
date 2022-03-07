---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007182"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

S pomoću aplikacije Dynamics 365 Project Operations možete brzo graditi nove projekte odabirom mogućnosti **Kopiraj projekt** na obrascu **Projekti**. Kako biste kopirali projekt, otvorite projekt koji želite kopirati, a zatim odaberite **Kopiraj projekt**. Radnja će kopirati sljedeće:

- Svojstava projekta 
- Strukturna analiza rada
- Članovi projektnog tima
- Procjene projekta
- Procjene izdataka za projekt
- Procjene materijala za projekt

## <a name="project-properties"></a>Svojstava projekta

Kada se projekt kopira, kopiraju se vrijednosti u sljedećim poljima:

- Ime
- Opis
- Klijent
- Predložak kalendara
- Valuta
- Ugovorena jedinica
- Voditelj projekta
- Stanje
- Sveukupno stanje projekta
- Komentari
- Procjene
- Procijenjeni datum početka: Ovo je datum kada je projekt stvoren iz kopije.
- Procijenjeni datum završetka: Ovaj se datum prilagođava na temelju datuma početka novog projekta izrađenog iz kopije.
- Rad (sati)
- Procijenjena cijena rada
- Procijenjena cijena troška
- Procijenjena cijena materijala

> [!NOTE]
> Projekt kopiranja dugotrajan je postupak. Kopiraju se i projektni zapisi, njihovi relevantni atributi i mnogi povezani entiteti. Zbog dugotrajnosti postupka, nakon započinjanja kopiranja, ciljna stranica projekta zaključava se kako se ne bi mogla uređivati dok se postupak kopiranja ne dovrši.

## <a name="work-breakdown-structure"></a>Strukturna analiza rada

Kada se projekt kopira, kopira se cijela strukturna analiza rada ispunjena resursima. Imenovani resursi mijenjaju se generičkim resursima. Ako imenovani resursi nemaju isto radno vrijeme kao generički resurs, raspored će se ponovno izračunati i trajanje zadatka može se promijeniti.

## <a name="project-team-members"></a>Članovi projektnog tima

Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi. Zadaci generičkih resursa također se zadržavaju onakvi kakvi su bili u izvornom projektu. Imenovani resursi pretvorit će se u generičke članove tima.

## <a name="estimates"></a>Procjene

Kada se projekt kopira, redci procjene resursa, troškova i materijala kopiraju se iz izvornog projekta. 

Za informacije o načinu programskog pristupanja aplikaciji Copy Project, pogledajte odjeljak [Razvoj predložaka projekata s pomoću aplikacije Copy Project](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
