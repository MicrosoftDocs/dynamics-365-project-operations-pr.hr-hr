---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 42, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 42, V3, sustava Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589187"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 42. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj međuverzije V3.10.73.61 i uglavnom je dostupna putem samostalnog ažuriranja u travnju 2022. godine.

## <a name="update-release-42"></a>Izdanje ažuriranja 42

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**

- Kada se vremenski list odbije, korisnik koji ga je odbio pogrešno je identificiran kao **Sustav**.
- Prilikom uvoza **stavki vremena nedostaje vrijednost Kategorija** resursa.
- Odobravatelji projekata mogu odobriti prijavljene projekte kada njihove dozvole nisu posebno postavljene na **Može odobriti**.

**Prodaje**

- Kada se stvarni podaci evidentiraju na zadacima koji nisu korijenske razine, stvarni troškovi pogrešno se zbrajaju.
