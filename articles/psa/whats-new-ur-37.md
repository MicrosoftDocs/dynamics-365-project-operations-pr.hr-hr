---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 37, V3
description: U ovom se članku navode značajke i popravci dostupni u ažuriranju Microsoft Dynamics 365 Project Service Automation izdanja 37, V3.
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
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922489"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za izdanje ažuriranja automatizacije usluge Project Service Update Release 37, V3. Ova verzija ima broj međuverzije V3.10.58.120 i općenito je dostupna putem samostalnog ažuriranja u studenom 2021.

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
