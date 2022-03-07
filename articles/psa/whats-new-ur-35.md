---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 35, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 35, V3, sustava Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473256"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 35. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj izdanja V3.10.56.110 i općenito je dostupna putem samostalnog ažuriranja u rujnu 2021. godine.

## <a name="update-release-35"></a>Izdanje ažuriranja 35

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**

- Odobravatelj projekta prima pogrešku ovlasti za čitanje kada odobri unose troška s ulogom **Odobravatelj projekta**.
- Odobravatelj projekta prima pogrešku ovlasti za pisanje na **msdyn_projectapproval** kada otkaže odobreni vremenski unos s pomoću uloge **Odobravatelj projekta**.
- Kad u vremenskom unosu odaberete **Kopiraj tjedan** u aplikaciji Dynamics 365 za telefon – modul aplikacije Središte resursa projekta, dolazi do sljedeće pogreške: "...\ OfficeProductivity_RibbonRules.js.map: HTTP pogreška: statusni kod 404, net:: ERR_HTTP_RESPONSE_CODE_FAILURE."
- Pravilo **Pokušaj ponovno** automatski odobrava unose koji su prethodno odbijeni.
- Podrešetka **Skupovi odobrenja** prikazuje neprimjenjive radnje na vrpci.
- Ikone nedostaju za **Zadatak projekta** i **Uloga resursa** na entitetu **Vremenski unos**.
- Kada uvozite dodjele resursa, uvezeni vremenski unosi nemaju ispravno trajanje za dodjele koje su stvorene putem zadataka ručnog načina.
- **Izbriši** nedostaje na stranici **Napredno pretraživanje zapisa vremenskog unosa**.
- **Spremi** nedostaje na stranici **Podaci o vremenskom unosu**. Ovaj problem sprječava spremanje promjena kada je stranica zatvorena.

**Planiranje projekta**

- Rešetke **Dodjela resursa** i **Usklađivanje resursa** ne sortiraju grupirane atribute po abecedi.
- Zadaci se ne mogu stvoriti ako je ponašanje datuma prilagođeno na **Samo datum**.

**Upravljanje resursima**

- Ako su instalirani i Dynamics 365 Field Service i Project Service Automation, do problema s preklapanjem dolazi kada je **Povezani prikaz preduvjeta za resurs** povezan s glavnom stranicom.
- Dvostrukim klikom na mogućnost **Spremi** u dijaloškom okviru **Brzo stvaranje člana tima** sprječava se stvaranje preduvjeta za resurs.

**Prodaje**

- Iznimka se prikazuje ako izbrišete zadatak koji je povezan s ponudom koja ima status **Ostvarena**.
