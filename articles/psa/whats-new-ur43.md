---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 43, V3
description: U ovom članku navode se značajke i popravci koji su dostupni u aplikaciji Microsoft Dynamics 365 Project Service Automation, izdanje ažuriranja 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915299"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je s aplikacijom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku navode se značajke i ispravci koji su novi ili izmijenjeni u aplikaciji Project Service Automation, izdanje ažuriranja 43, V3. Ova verzija ima broj međuverzije V3.10.74.200 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2022. godine.

## <a name="update-release-43"></a>Izdanje ažuriranja 43

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.


**Vrijeme i trošak**

- Prilikom uvoza unosa vremena iz rezervacija ili dodjela resursa, upućivanje na povezani resurs koji se može rezervirati ne zadržava se.
- Kada je rešetka za unos vremena proširena na cijeli zaslon, navigacija rešetkom s pomoću tipke tab ne funkcionira.
- Prilikom slanja unosa vremena koji je izradio drugi korisnik, polje **Poslao** netočno je popunjeno korisnikom koji je kreirao vremenski list.
