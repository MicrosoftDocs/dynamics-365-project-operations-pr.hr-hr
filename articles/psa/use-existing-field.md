---
title: Korištenje postojećeg polja u aplikaciji Project Service kao dimenzije određivanja cijena
description: Ova tema pruža informacije o korištenju postojećih polja u aplikaciji Project Service kao dimenzija određivanja cijena.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008077"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Korištenje postojećeg polja u aplikaciji Project Service kao dimenzije određivanja cijena

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) ima mnogo polja u entitetu **Stvarni podaci** koja se mogu koristiti kao dimenzije određivanja cijena za određivanje cijene na temelju resursa u tvrtkama ili ustanovama projekta. Na primjer, uobičajeno je polje **Resurs koji se može rezervirati**. Manje tvrtke koje imaju manje od 20 do 30 naplativih resursa mogu otkriti da je korištenje računa i stopa troškova specifičnih za svaki resurs jednostavniji pristup. Budući da se naplativa radna snaga povećava, posebne bi cijene mogle postati nerealne za održavanje jer trošak resursa i cijene naplate počinju varirati kako se resursi unapređuju, stječu više iskustva ili različite skupove vještina. Budući da je taj pristup i dalje dobar za tvrtke određene veličine, pogledajte odjeljak [Uporaba resursa koji se može rezervirati kao veličine za određivanje cijene](bookable-resource-pricing-dimension.md) kako biste razumjeli kako se postojeće polje aplikacije Project Service može upotrebljavati kao veličina za određivanje cijene.

Drugi je primjer kategorija transakcije. Klijenti i implementatori koristili su kategoriju transakcije u aplikaciji PSA da klasificiraju rad i koriste polje do cijene i troška na temelju kategorije rada. Za dodatne informacije pogledajte članak [Korištenje kategorije transakcije kao dimenzije određivanja cijena](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]