---
title: Pregled izdatka
description: U ovoj temi nalaze se informacije o funkcioniranju troška u aplikaciji Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276564"
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