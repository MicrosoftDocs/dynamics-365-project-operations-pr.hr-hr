---
title: Analiza ponuda projekta
description: Ova tema pruža informacije o analizi ponuda projekta.
author: rumant
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012442"
---
# <a name="analysis-of-project-quotes"></a>Analiza ponuda projekta

[!include [banner](../includes/psa-now-project-operations.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]