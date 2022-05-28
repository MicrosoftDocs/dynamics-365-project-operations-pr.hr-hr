---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 28, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 28, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: b3afeaf131c8bab25e1ed3a9eb3b41cb3059f711
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586795"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi navode se značajke i popravci koji su novi ili promijenjeni za aplikaciju Project Service Automation V3, izdanje ažuriranja 28. Ova verzija ima broj međuverzije V 3.10.46.32 i općenito je dostupna putem samoažuriranja u siječnju 2021.

## <a name="update-release-28"></a>Izdanje ažuriranja 28

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Korisnici mogu upotrijebiti **Skupno uređivanje** za ažuriranje vremenskih zapisa koji su odobreni i poslani.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- U slučajevima kada se GUID zadatka tumači kao broj, zadaci se ne mogu otvoriti za uređivanje s pomoću mogućnosti **Uredi zadatak** s vrpce na stranici **Strukturna analiza rada**.

**Sales**

Popravljeni su sljedeći problemi:

- Iznimka nulte reference generira se kada se pozove dodatak **GetEstimatesForProject**.
- Mogućnost **Označi spremnim za fakturiranje** na rešetki kontrolne točke samo djelomično ažurira atribute, osim atributa **Status fakture**, koji se ažurira.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
