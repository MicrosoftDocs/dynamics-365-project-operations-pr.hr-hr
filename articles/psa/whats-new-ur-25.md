---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 25, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183534"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 25, V3

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi navode se značajke i popravci koji su novi ili promijenjeni za aplikaciju Project Service Automation V3, izdanje ažuriranja 25. Ova verzija ima broj međuverzije V 3.10.43.76 i općenito je dostupna putem samoažuriranja u listopadu 2020.

## <a name="update-release-25"></a>Izdanje ažuriranja 25

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljen je sljedeći profil:

- Grafikon unosa vremena koji prikazuje dodatne podatke na temelju prevelikog intervala koji se dohvaća.

**Upravljanje resursima**

Popravljen je sljedeći profil:

- Dodan je kod za alat Package deployer kako bi se preskočio uvoz zakrpe za aplikaciju Universal Resource Scheduling ako već postoji zakrpa više verzije.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Ispravljena neusklađenost zaokruživanja i tečajne razlike koja je rezultirala netočnim planiranim troškovima u rešetki za praćenje projekta.
- Podrška mogućnosti prikaza dvije ili više rešetki za reakciju na obrascu **Projekt**.
- Pod uvjetom da se provjera valjanosti odnosi na mogućnost dodijele zadatka nakon datuma završetka kalendara, što rezultira neuspjelom dodjelom resursa.
- Poboljšano rukovanje pogreškama za rješavanje iznimke reference vrijednosti jednake nuli generirane iz sljedećeg:

    - Programski dodatak **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** kada se projektni zadatak stvori bez povezanog projekta
    - Programski dodatak **PreProjectTeamMemberCreate**
    - Programski dodatak **PostProjectTeamMemberDelete**
    - Programski dodatak **PreValidateProjectTaskDelete**

**Sales**

Popravljeni su sljedeći problemi:

- Poboljšano rukovanje pogreškama za rješavanje iznimki reference koja ima vrijednost jednaku nuli generiranih iz **Kopiraj projekt: Upravljanje procjenama pomoćnih resursa**.
- **Nije spremno za fakturiranje** na **Zaostatak naplate vremena i materijala** ne čisti status naplate.
- Ispravljeno pogrešno označavanje gumba **Cijene** na karticama **Cijena uloge** i **Predmeti iz kataloga**.