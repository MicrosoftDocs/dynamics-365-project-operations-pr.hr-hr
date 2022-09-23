---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 47, V3
description: U ovom se članku navode značajke i popravci dostupni u Microsoft Dynamics 365 Project Service Automation ažuriranju izdanja 47, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477277"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 47, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za izdanje 45. izdanja ažuriranja automatizacije usluge project servicea, V3. Ova verzija ima broj izdanja V3.10.78.8 i općenito je dostupna putem samostalnog ažuriranja u srpnju 2022. godine.

## <a name="update-release-47"></a>Izdanje ažuriranja 47

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Upravljanje resursima**
- Provjera valjanosti ažurirana je kako bi se osiguralo da korisnici ne mogu pokrenuti nultu referentnu iznimku pri pokušaju stvaranja člana projektnog tima bez resursa koji **se može rezervirati**.
