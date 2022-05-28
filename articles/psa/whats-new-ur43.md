---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 43, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 43, V3, sustava Microsoft Dynamics 365 Project Service Automation.
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710123"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilan je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 43. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj međuverzije V3.10.74.200 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2022. godine.

## <a name="update-release-43"></a>Izdanje ažuriranja 43

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.


**Vrijeme i trošak**

- Prilikom uvoza vremenskih unosa iz rezervacija ili dodjela resursa ne zadržava se upućivanje na povezani resurs koji se može rezervirati.
- Kada se rešetka za unos vremena proširi na cijeli zaslon, navigacija rešetkom pomoću tipke tabulatora ne funkcionira.
- Prilikom slanja vremenske stavke koju je stvorio drugi korisnik, **polje Poslano po** neispravno se popunjava korisnikom koji je stvorio vremenski list.
