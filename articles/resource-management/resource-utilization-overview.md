---
title: Prikaz korištenja resursa
description: U ovoj temi nalaze se informacije o iskoristivosti resursa u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401367"
---
# <a name="resource-utilization-overview"></a>Prikaz korištenja resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Resursi mogu imati ciljanu naplativu upotrebu. Ova ciljna iskoristivost definira se kao atribut u zadanoj ulozi resursa ili je postavljena na zapisu pojedinačnog resursa koji se može rezervirati. Izračuni upotrebe temelje se na stvarnim satima koje su resursi prijavili pomoću odobrenih vremenskih unosa.

Formule u nastavku služe za izračun upotrebe:

  - Naplativa upotreba = naplativi stvarni sati ÷ kapacitet resursa
  - Nenaplativa upotreba = stvarno vrijeme s ID-om vrste naplate = nenaplativo, besplatno ili nije dostupno ÷ kapacitet resursa
  - Interno = stvarno vrijeme bez prodajnog ugovora ÷ kapacitet resursa
  - Kapacitet resursa = radno vrijeme resursa – izvan ureda – neradni dani

Prikaz **Upotreba resursa** možete pronaći u oknu **Resursi**.

Svaka ćelija u rešetki predstavlja postotak naplative upotrebe resursa u razdoblju, kao što je dan, tjedan ili mjesec. Formule u nastavku služe za označavanje ćelija bojom:

  - **Zelena**: Naplativa iskoristivost >= Ciljna iskoristivost resursa
  - **Žuta**: Ciljna iskoristivost – 20 <= Naplativa iskoristivost < Ciljna iskoristivost.
  - **Crvena**: Naplativa iskoristivost < Ciljna iskoristivost – 20

Budući da se prikaz **Upotreba resursa** temelji na ploči s rasporedom, možete filtrirati rezultate pomoću mogućnosti filtriranja na ploči s rasporedom.

U rešetki je potrebno postaviti ciljnu upotrebu za svaku ulogu ili pojedinačni resurs. Kako biste to učinili, idite na mogućnost **Resursi** > **Uloge resursa**.

Osim toga, svakom resursu koji se može rezervirati potrebno je dodijeliti zadanu ulogu. Idite na mogućnost **Resursi** > **Resursi**. Na kartici **Project Service** provjerite je li definirana uloga resursa i je li polje **Zadano je** postavljeno na **Da**. Možete dodati dodatne uloge ako je polje **Zadano je** = **Ne**. Uloga u kojoj se polje **Zadano je** = **Da** upotrebljava za procjenu iskoristivosti resursa u odnosu na cilj za tu ulogu.

Na kartici **Project Service** možete postaviti i pojedinačnu ciljnu upotrebu za resurs. Izračun upotrebe zatim upotrebljava ciljnu upotrebu da bi se procijenio cilj resursa, a ne cilj zadane uloge resursa.

Iskoristivost se prikazuje za resurs samo ako taj resurs ima odobreno naplativo vrijeme tijekom razdoblja prikazanog u rešetki.


[!INCLUDE[footer-include](../includes/footer-banner.md)]