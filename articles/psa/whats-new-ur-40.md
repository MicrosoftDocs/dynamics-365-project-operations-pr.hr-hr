---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 40, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 40, V3, sustava Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588635"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 40. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj izrade V3.10.61.61 i općenito je dostupna putem samostalnog ažuriranja u veljači 2022.

## <a name="update-release-40"></a>Izdanje ažuriranja 40

### <a name="features"></a>Značajke
Faza 1 nadogradnje s automatizacije projektnih usluga na projektne operacije - Lite će biti objavljena u veljači 2022. svim kupcima. Da biste provjerili ispunjava li uvjete, pročitajte članak [Nadogradnja s automatizacije projektnih usluga na projektne operacije](upgrade-project-operations-non-stocked.md). Ako se aplikacija ne pojavi u vašoj instanci u Power Platform centru za administratore, obratite se službi za podršku i zatražite da let bude omogućen za vaša okruženja. Vaš zahtjev mora sadržavati popis ID-ova okruženja u kojima let treba omogućiti.

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**
- Stavka bilješke nedostaje kada je unos vremena odbijen ili otkazan. 

**Prodaje**

- Kada ažurirate procjene troškova ili prodaje pomoću gotovih dodataka, pogrešno vam je dopušteno slati JSON korisne terete koji nisu valjani izvan korisničkog sučelja.
- Kada ažurirate retke ponude pomoću brzog prikaza, dopušteno vam je aktivirati ponude.
