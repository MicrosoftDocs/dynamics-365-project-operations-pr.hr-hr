---
title: Pregled izdatka
description: U ovoj temi nalaze se informacije o funkcioniranju troška u aplikaciji Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 7ba4d090e15bffa687d69d3d8e5733d2519668e2879249e1d6dc6aba26f7fbf6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988462"
---
# <a name="expense-home-page"></a>Početna stranica troška

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Dynamics 365 Project Operations podržava mogućnost obrade troškova. Obrada troškova događa se s projektima ili bez njih uporabom prilagodljivog tijeka rada pravila, kategorija transakcija i odobrenja.

U aplikaciji Project Operations postoje dva podržana modela implementacije troška: 

- **Potpuno**: Dostupno je potpuno raspoređivanje za **Project Operations za scenarije koji se temelje na resursima / bez zaliha** ili **Project Operations za scenarije koji se temelje na proizvodnim nalozima**.
- **Osnovno**: Osnovna implementacija dostupna je za **Project Operations za scenarije koji se temelje na resursima / bez zaliha** i **Jednostavna implementacija – od sklapanja posla do predračuna**.

## <a name="full"></a>Potpuni 
Potpuna implementacija troška omogućuje cjelovitu provedbu pravila koja obuhvaća i mogućnost stvaranja pravila, kao što su:

  - Ograničenja kategorija troška
  - Putovanja
  - Po danu
  - Uvoze kreditnih kartica
  - Primitak optičkog prepoznavanja znakova

## <a name="basic"></a>Osnovno 
Scenarij implementacije osnovnih troškova omogućuje vam samo bilježenje osnovnih troškova u odnosu na projekt. 

Dodatne informacije potražite u odjeljku [Unos troška (jednostavno)](basic-expense.md).

## <a name="determine-your-expense-deployment"></a>Određivanje implementacije troška
Kako biste utvrdili upotrebljavate li implementaciju upravljanja osnovnim troškovima, provjerite završava li URL adresa sljedećim izrazom **.crm.dynamics.com**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]