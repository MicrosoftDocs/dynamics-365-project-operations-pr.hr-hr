---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 37, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 37, V3, sustava Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593465"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 37. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj međuverzije V3.10.58.120 i općenito je dostupna putem samostalnog ažuriranja u studenom 2021.

## <a name="update-release-37"></a>Izdanje ažuriranja 37

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**
- Korisnici ne mogu izbrisati vremenski unos brisanjem ćelije.
- Prikaz **Moja neuspjela odobrenja** sadrži samo odobrenja projekta sa statusom **Poslano**.

**Upravljanje projektima**
- Korisnici dobivaju pogrešku iznimke nulte reference tijekom otvaranja projekta u Microsoftovu dodatku za radnu površinu ako je naziv položaja člana projektnog tima prazan.
- Ne postoji gumb **Spremi** na stranici **Projektni zadatak** tako da korisnici ne mogu spremati promjene u zapise zadatka.
- Korisnici ne mogu izbrisati projekt koji ima zadatak povezan s ponudom sa statusom **Osvojeno**.

**Prodaje**
- Polje **Valuta** na stranici **Projekt** ažurirano je kako bi odgovaralo valuti primijenjenog predloška.
- Trošak se pogrešno izračunava za zadatke koji imaju više valuta.
