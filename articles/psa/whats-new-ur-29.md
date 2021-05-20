---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 29, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948607"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 29. Ova verzija ima broj izrade V3.10.47.7 i općenito je dostupna putem samostalnog ažuriranja u veljači 2021.

## <a name="update-release-29"></a>Izdanje ažuriranja 29

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Korisnici ne mogu vidjeti radno vrijeme zabilježeno neradnim danima u rešetki vremenskog unosa.
- Odobreni unosi troškova mogu se uređivati na rešetki.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Nedostaje logika provjere valjanosti kako bi se osiguralo da sati rada resursa na zadatku ne mogu biti negativni.
- Prilagođena radnja, **AssignResourcesForTask** ažurira sva polja, a ne samo promijenjena.
- Pri kopiranju projekta u okruženje s dodacima ili tijekovima rada koji su registrirani na događaju **CreateProject**, atribut **msdyn_bulkgenerationstatus** ne ažurira se ako **CopyWBSToProject** ne uspije.
- Kada proširite kalendar projekta, radni dani se ne sortiraju uzlazno, što uzrokuje neuspjeh ažuriranja nekih projektnih zadataka.
- Promjena Voditelja projekta na postojećem projektu pokreće zadanu logiku organizacijske jedinice.

**Prodaja**

Popravljeni su sljedeći problemi:

- Kartica **Izvršenje ugovora** na stranici **Ugovor** nečujno ne uspijeva tijekom inicijalizacije ako ne postoje redci ugovora.