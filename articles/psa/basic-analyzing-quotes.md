---
title: Analiza ponuda projekta
description: Ova tema pruža informacije o analizi ponuda projekta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127014"
---
# <a name="analysis-of-project-quotes"></a>Analiza ponuda projekta

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analizira ponude projekta za procjenu profitabilnosti. Također analizira koliko je dobro ponuda usklađena s očekivanjima klijenta o datumu isporuke ili datumu završetka i o proračunu.

## <a name="profitability-analysis"></a>Analiza profitabilnosti

Project Service Automation analizira profitabilnost s pomoću bruto marže i prilagođene bruto marže.

- Bruto marže izračunavaju se s pomoću sljedeće formule:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Prilagođena bruto marža izračunava se s pomoću sljedeće formule:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Ako vrijednosti za bruto maržu i prilagođenu bruto maržu znatno odstupaju, velik dio rada u ponudi klasificira se kao nenaplativ.

## <a name="analysis-of-customer-expectations"></a>Analiza očekivanja klijenta

Možete analizirati ponude i generirati grafikone za očekivanja klijenta o rasporedu i proračunu ako unesete vrijednosti za sljedeća polja:

- Polje **Traženi datum isporuke** u zaglavlju ponude.
- Polje **Proračun klijenta** za svaki redak ponude (za retke koji se temelje na projektu i retke koji se temelje na proizvodu).

Analiza očekivanja klijenta o rasporedu provodi se uspoređivanjem najnovijeg datuma završetka detalja retka ponude s traženim datumom isporuke u svim recima ponude u ponudi.

Analiza očekivanja klijenta o proračunu provodi se uspoređivanjem zbroja ukupnog proračuna klijenta s navedenim iznosom u svim recima ponude.
