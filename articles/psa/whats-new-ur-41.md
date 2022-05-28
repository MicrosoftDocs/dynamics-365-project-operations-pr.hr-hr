---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 41, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 41, V3, sustava Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580907"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 41. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj međuverzije V3.10.62.162 i općenito je dostupna putem samostalnog ažuriranja iz ožujka 2022.

## <a name="update-release-41"></a>Izdanje ažuriranja 41

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Upravljanje projektom**
- Kada pokušate stvoriti projekt iz predloška koji se temelji na projektu stvorenom iz dodatka za stolna računala, prikazat će se sljedeća pogreška: "Provjera polja Planirani rad dodjele resursa: Datum završetka svakog vremena dodjele resursa S isječak ne smije biti raniji od datuma početka".

**Vrijeme i trošak**
- Kada pokušate izbrisati unos vremena, prikazuje se sljedeća poruka o pogrešci:"Iz ISV koda dolazi do neočekivane pogreške".

**Prodaje**
- Kada kreirate fakturu za prekretnicu s fiksnom cijenom, polja Opis **i** Vanjski opis **ne popunjavaju** se. 
