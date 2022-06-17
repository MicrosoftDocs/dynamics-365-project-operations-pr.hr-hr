---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 41, V3
description: U ovom se članku navode značajke i popravci dostupni u Microsoft Dynamics 365 Project Service Automation ažuriranju izdanja 41, V3.
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930539"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za izdanje ažuriranja automatizacije usluge project service 41, V3. Ova verzija ima broj međuverzije V3.10.62.162 i općenito je dostupna putem samostalnog ažuriranja iz ožujka 2022.

## <a name="update-release-41"></a>Izdanje ažuriranja 41

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Upravljanje projektom**
- Kada pokušate stvoriti projekt iz predloška koji se temelji na projektu stvorenom iz dodatka za stolna računala, prikazat će se sljedeća pogreška: "Provjera polja Planirani rad dodjele resursa: Datum završetka svakog vremena dodjele resursa S isječak ne smije biti raniji od datuma početka".

**Vrijeme i trošak**
- Kada pokušate izbrisati unos vremena, prikazuje se sljedeća poruka o pogrešci:"Iz ISV koda dolazi do neočekivane pogreške".

**Prodaje**
- Kada kreirate fakturu za prekretnicu s fiksnom cijenom, polja Opis **i** Vanjski opis **ne popunjavaju** se. 
