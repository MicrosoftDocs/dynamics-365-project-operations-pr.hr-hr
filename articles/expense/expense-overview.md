---
title: Pregled izdatka
description: U ovom se članku nalaze informacije o funkciji Trošak u projektnim operacijama.
author: stsporen
ms.date: 10/06/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 935998adda4a967285d68016b4dad0bc2b0c56dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917889"
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