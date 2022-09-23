---
title: Sigurnost i odobrenja
description: U ovom se članku nalaze informacije o sigurnosnom postavljanju za rad s odobrenjima u programu Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525401"
---
# <a name="security-and-approvals"></a>Sigurnost i odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Microsoft Dynamics 365 Project Operations koristi dvije sigurnosne uloge da bi omogućio odobravanje unosa vremena, troškova i materijala:

- Odobravatelj projekta
- Administrator odobravatelja projekta

## <a name="project-approver"></a>Odobravatelj projekta

Da biste odobrili **vrijeme projekta, troškove i stavke materijala, morate imati sigurnosna uloga odobravatelja** projekta. Također morate imati pristup relevantnim povezanim entitetima, kao **što je Project**. Taj pristup može dodijeliti netko tko ima ulogu upravitelja **projekta**. Osim toga, morate biti član tima projekta i označeni kao odobravatelj.

Da biste odobrili stavke koje nisu projektne, morate biti upravitelj podnositelja zahtjeva.

## <a name="project-approver-admin"></a>Administrator odobravatelja projekta

> [!NOTE]
> Značajka Skupovi [odobrenja](approval-sets.md) mora biti omogućena da biste mogli koristiti funkciju administratora odobravatelja projekta.

Administrator projekta **sigurnosna** uloga omogućuje korisnicima da zaobiđu pravila i omogućuje odobravanje unosa u svim projektima. Dodjela ove uloge zaobići će logiku provjere valjanosti koja zahtijeva članstvo u timu i označavanje kao odobravatelja. Morate imati pristup relevantnim povezanim entitetima, kao **što je Project**. Taj pristup može dodijeliti netko tko ima ulogu upravitelja **projekta**.

Kontekst korisnika SUSTAVA zaobilazi provjere valjanosti na isti način kao i sigurnosna uloga administratora odobravatelja projekta.
