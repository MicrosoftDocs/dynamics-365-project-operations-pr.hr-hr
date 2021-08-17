---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 34, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009747"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 34. Ova verzija ima broj izdanja V3.10.55.38 i općenito je dostupna putem samostalnog ažuriranja u srpnju 2021. godine.

## <a name="update-release-34"></a>Izdanje ažuriranja 34

### <a name="bug-fixes"></a>Ispravke pogrešaka
Popravljeni su sljedeći problemi.

**Općenito**

- Ažuriranja koja proveo izdavač ne aktiviraju novi suvremeni tijek rada odobrenja.
- Atributi **Status cilja** i **Vrsta radnje** nedostaju na glavnoj stranici **Skup odobrenja**.

**Vrijeme i trošak**

- Nije moguće odobriti zahtjev za opoziv s pomoću suvremenog tijeka odobrenja.
- Kopiranje tjednih vremenskih unosa ne funkcionira tijekom kopiranja unosa koji nisu povezani s prijavljenim korisnikom.

**Planiranje projekta**

- Konture dodjeljivanja resursa oštećene su pri uvozu iz dodatka radne površine Microsoft Project.

**Upravljanje resursima**

- Kada objavite projekt iz dodatka klijenta radne površine Microsoft Project, mijenja se datum završetka postojećih preduvjeta.
- Decimalna preciznost premašuje dva decimalna mjesta u dijaloškom okviru za potvrdu produženja rezervacija.

**Prodaje**

- Kada ugovoru o projektu dodate redak koji se temelji na proizvodu s postojećim proizvodom, prikazuje se iznimka **ključ nije pronađen u rječniku**.
- Potencijalni klijenti ne mogu se kvalificirati kada se vrsta narudžbe mapira iz potencijalnog klijenta u priliku.
