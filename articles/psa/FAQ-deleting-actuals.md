---
title: Zašto ne mogu izbrisati zapise iz entiteta stvarnih vrijednosti?
description: Ova tema pruža informacije o tome zašto ne možete izbrisati zapise iz entiteta stvarnih vrijednosti.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286059"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Zašto ne mogu izbrisati zapise iz entiteta stvarnih vrijednosti?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne dozvoljava brisanje stvarnih vrijednosti jer služe kao izvor istine za transakcije koje imaju financijske implikacije na daljnje sustave, kao što je glavna knjiga. Kad bi se stvarne vrijednosti mogle izbrisati, cjelovitost transakcija financijskog izvješćivanja bila bi upitna. Da bi se uspostavila kontrola knjiženja, klijenti bi trebali koristiti dnevnike za izradu kompenzirajućih transakcija.



[!INCLUDE[footer-include](../includes/footer-banner.md)]