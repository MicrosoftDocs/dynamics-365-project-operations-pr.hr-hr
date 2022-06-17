---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 34, V3
description: U ovom se članku navode značajke i popravci dostupni u ažuriranju ažuriranja automatizacije usluga programa Project Service 34, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928653"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za automatizaciju usluge Project Service V3, Ažuriraj izdanje 34. Ova verzija ima broj izdanja V3.10.55.38 i općenito je dostupna putem samostalnog ažuriranja u srpnju 2021. godine.

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
