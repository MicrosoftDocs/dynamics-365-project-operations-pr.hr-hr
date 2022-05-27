---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574421"
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
- Kontrolni popisi projekata
- Grupe projekata

## <a name="project-properties"></a>Svojstava projekta

Kada se projekt kopira, kopiraju se vrijednosti u sljedećim poljima.

| Polje | Projektne operacije Ne-opskrbljeni materijali | Projektne operacije Lite | Projekt za web |
|-------|------------------------------------------|-------------------------|---------------------|
| Ime/naziv | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Opis | :heavy_check_mark: | :heavy_check_mark: | |
| klijente | :heavy_check_mark: | :heavy_check_mark: | |
| Predložak kalendara | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuta | :heavy_check_mark: | :heavy_check_mark: | |
| Ugovorna jedinica | :heavy_check_mark: | :heavy_check_mark: | |
| Tvrtka vlasnik | :heavy_check_mark: | | |
| Voditelj projekta | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Stanje | :heavy_check_mark: | :heavy_check_mark: | |
| Sveukupno stanje projekta | :heavy_check_mark: | :heavy_check_mark: | |
| Komentari | :heavy_check_mark: | :heavy_check_mark: | |
| Procjene | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Predviđeni datum početka</p><p><strong>Napomena:</strong> Ovo polje određuje datum stvaranja projekta iz kopije. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Procijenjeni datum završetka</p><p><strong>Napomena:</strong> Datum u ovom polju prilagođava se na temelju datuma početka novog projekta koji je napravljen iz kopije.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Rad (sati) | :heavy_check_mark: | :heavy_check_mark: | |
| Procijenjena cijena rada | :heavy_check_mark: | :heavy_check_mark: | |
| Procijenjena cijena troška | :heavy_check_mark: | :heavy_check_mark: | |
| Procijenjena cijena materijala | | :heavy_check_mark: | |

> [!NOTE]
> Projekt kopiranja dugotrajan je postupak. Kopiraju se i projektni zapisi, njihovi relevantni atributi i mnogi povezani entiteti. Zbog dugotrajnosti postupka, nakon započinjanja kopiranja, ciljna stranica projekta zaključava se kako se ne bi mogla uređivati dok se postupak kopiranja ne dovrši.

## <a name="work-breakdown-structure"></a>Strukturna analiza rada

Kada se projekt kopira, kopira se cijela strukturna analiza rada ispunjena resursima. Imenovani resursi mijenjaju se generičkim resursima. Ako imenovani resursi nemaju isto radno vrijeme kao generički resurs, raspored će se ponovno izračunati, a trajanje zadatka može se promijeniti.

## <a name="project-team-members"></a>Članovi projektnog tima

Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi. Zadaci generičkih resursa također se zadržavaju onakvi kakvi su bili u izvornom projektu. Imenovani resursi pretvorit će se u generičke članove tima.

> [!NOTE]
> Članovi tima i zadaci ne kopiraju se u programu Project za web.

## <a name="estimates"></a>Procjene

Kada se projekt kopira, redci procjene resursa, troškova i materijala kopiraju se iz izvornog projekta. 

Za informacije o načinu programskog pristupanja aplikaciji Copy Project, pogledajte odjeljak [Razvoj predložaka projekata s pomoću aplikacije Copy Project](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Ponude i ugovori

Ponude i ugovori nisu povezani s odredišnim projektom.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
