---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 45, V3
description: U ovom se članku navode značajke i popravci dostupni u Microsoft Dynamics 365 Project Service Automation ažuriranju izdanja 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169175"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za izdanje 45. izdanja ažuriranja automatizacije usluge project servicea, V3. Ova verzija ima broj izdanja V3.10.76.168 i općenito je dostupna putem samostalnog ažuriranja u srpnju 2022. godine.

## <a name="update-release-45"></a>Izdanje ažuriranja 45

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Prodaje**

- Korisnici ne mogu uspješno kreirati fakture nakon što pokušaju stvoriti fakturu bez ikakve neplaćene prodaje, ako također pregledavaju istu instancu stranice i ne osvježavaju je.

**Vrijeme i trošak**

- Kada je omogućena moderna odobrenja i odobrenje opozvanog projekta odobreno, faza zapisa pogrešno se ažurira u odobreni **zahtjev za opoziv**.
- Kada su omogućena moderna odobrenja i tokovi oblaka neaktivni, postupak odobravanja nije uspješan, a korisnici koji podnose ili odobravaju nisu obaviješteni.
