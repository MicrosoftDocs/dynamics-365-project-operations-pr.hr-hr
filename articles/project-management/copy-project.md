---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073329"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

S pomoću aplikacije Dynamics 365 Project Operations možete brzo graditi nove projekte odabirom mogućnosti **Kopiraj projekt** iz obrasca **Projekti**. Kako biste kopirali projekt, otvorite projekt koji želite kopirati, a zatim odaberite **Kopiraj projekt**. Radnja će kopirati:

- Svojstava projekta
- Strukturna analiza rada
- Članovi projektnog tima
- Procjene projekta
- Procjene izdataka za projekt

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
- Predviđeni datum početka
- Datum završetka
- Rad (sati)
- Procijenjena cijena rada
- Procijenjeni troškovi

## <a name="work-breakdown-structure"></a>Strukturna analiza rada

Kada se projekt kopira, kopira se cijela strukturna analiza rada ispunjena resursima. Imenovani resursi mijenjaju se generičkim resursima. Ako imenovani resursi nemaju isto radno vrijeme kao generički resurs, raspored će se ponovno izračunati i trajanje zadatka može se promijeniti.

## <a name="project-team-members"></a>Članovi projektnog tima

Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi. Zadaci generičkih resursa također se zadržavaju onakvi kakvi su bili u izvornom projektu. Imenovani resursi pretvorit će se u generičke članove tima.

## <a name="estimates"></a>Procjene

Kada se projekt kopira, iz izvornog projekta kopiraju se i redci za procjenu resursa i troška. 

Za informacije o načinu programskog pristupanja aplikaciji Copy Project, pogledajte odjeljak [Razvoj predložaka projekata s pomoću aplikacije Copy Project](dev-copy-project.md).
