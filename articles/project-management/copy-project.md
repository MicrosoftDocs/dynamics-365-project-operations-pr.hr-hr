---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479510"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

S pomoću aplikacije Dynamics 365 Project Operations možete brzo graditi nove projekte odabirom mogućnosti **Kopiraj projekt** na obrascu **Projekti**. Kako biste kopirali projekt, otvorite projekt koji želite kopirati, a zatim odaberite **Kopiraj projekt**. Radnja će kopirati:

- Svojstva projekta (procijenjeni datum početka kopira se iz izvornog projekta)
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
