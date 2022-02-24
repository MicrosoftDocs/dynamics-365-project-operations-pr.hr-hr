---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 31, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945526"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 31. Ova verzija ima broj međuverzije V3.10.52.77 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2021. godine.

## <a name="update-release-31"></a>Izdanje ažuriranja 31

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Naredbeni gumbi kontrole vremenskog unosa na stranici **Resursi koji se mogu rezervirati** bili su zbunjujući.
- Iznimka nulte reference generirana je u **Project.SetTrackingFields** tijekom odobravanja vremenskog unosa.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:

- **Stvori člana tima** ne prikazuje ispravno postavke metapodataka za postavljanje rezervacije za **Stanje izvršene zadane rezervacije**.
- Pri nadogradnji s PSA 1.X na 3.X, postupak nadogradnje ne uspijeva na **UpgradeResourceRequirements**.


**Prodaja**

Popravljeni su sljedeći problemi:

- Stvarni prihod pretvara iznose u valutu projekta u rešetki za praćenje.
- Zadana valuta nije jasna pri stvaranju redaka dnevnika, ponuda i ugovora u scenarijima kada se osnovna valuta tvrtke ili ustanove razlikuje od valute projekta.
- Upit **Provjera valjanosti ispravka dnevnika na čekanju** ne filtrira se po projektu.
- Preostala prodaja netočno se izračunava na projektu.
- Ponude zasnovane na kontaktu ne uspijevaju kada se stvaraju bez cjenika.
- Pri odabiru mogućnosti **Potvrdi fakturu** ne prikazuje se okretni gumb.
- Pri odabiru mogućnosti **Stvori fakturu** ne prikazuje se okretni gumb.
- Zatvaranje ponude kao izgubljene ne otkazuje rezervacije.







