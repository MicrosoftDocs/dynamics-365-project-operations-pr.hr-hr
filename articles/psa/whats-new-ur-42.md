---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 42, V3
description: U ovom se članku navode značajke i popravci dostupni u Microsoft Dynamics 365 Project Service Automation ažuriranju Izdanja 42, V3.
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912706"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za izdanje ažuriranja automatizacije usluge project servicea 42, V3. Ova verzija ima broj međuverzije V3.10.73.61 i uglavnom je dostupna putem samostalnog ažuriranja u travnju 2022. godine.

## <a name="update-release-42"></a>Izdanje ažuriranja 42

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**

- Kada se vremenski list odbije, korisnik koji ga je odbio pogrešno je identificiran kao **Sustav**.
- Prilikom uvoza **stavki vremena nedostaje vrijednost Kategorija** resursa.
- Odobravatelji projekata mogu odobriti prijavljene projekte kada njihove dozvole nisu posebno postavljene na **Može odobriti**.

**Prodaje**

- Kada se stvarni podaci evidentiraju na zadacima koji nisu korijenske razine, stvarni troškovi pogrešno se zbrajaju.
