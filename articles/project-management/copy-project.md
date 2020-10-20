---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907967"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

S pomoću aplikacije Dynamics 365 Project Operations možete brzo graditi nove projekte uporabom radnje **Kopiraj projekt** iz postavke **Projekti**. Kako biste kopirali projekt, odaberite projekt, a zatim odaberite **Kopiraj**. Radnja će kopirati:

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