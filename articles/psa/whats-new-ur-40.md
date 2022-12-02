---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 40, V3
description: U ovom članku navode se značajke i popravci koji su dostupni u aplikaciji Microsoft Dynamics 365 Project Service Automation, izdanje ažuriranja 40, V3.
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912783"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku navode se značajke i ispravci koji su novi ili izmijenjeni u aplikaciji Project Service Automation, izdanje ažuriranja 40, V3. Ova verzija ima broj izrade V3.10.61.61 i općenito je dostupna putem samostalnog ažuriranja u veljači 2022.

## <a name="update-release-40"></a>Izdanje ažuriranja 40

### <a name="features"></a>Značajke
Faza 1 nadogradnje s aplikacije Project Service Automation na Project Operations – Lite bit će objavljena u veljači 2022. za sve korisnike. Da biste provjerili ispunjavanje uvjeta, pogledajte [Nadogradnja s aplikacije Project Service Automation na Project Operations](upgrade-project-operations-non-stocked.md). Ako se aplikacija ne pojavi u vašoh instanci u administratorskom centru Power Platform, kontaktirajte podršku i zatražite da let bude omogućen za vaša okruženja. Vaš zahtjev mora sadržavati popis ID-ova okruženja u kojima let treba biti omogućen.

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**
- Unos bilješke nedostaje kada je unos vremena odbijen ili poništen. 

**Prodaje**

- Kada ažurirate procjene troškova ili prodaje s pomoću dodataka spremnih za uporabu, pogrešno vam je dopušteno slanje JSON sadržaja koji nije valjan izvan korisničkog sučelja.
- Kada ažurirate retke ponude s pomoću brzog pregleda, dopušteno vam je aktivirati ponude.
