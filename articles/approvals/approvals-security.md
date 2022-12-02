---
title: Sigurnost i odobrenja
description: U ovom se članku navode informacije o sigurnosnim postavkama za rad s odobrenjima u sustavu Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709388"
---
# <a name="security-and-approvals"></a>Sigurnost i odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Sustav Microsoft Dynamics 365 Project Operations koristi dvije sigurnosne uloge kako bi omogućio odobrenje unosa vremena, troškova i materijala:

- Odobravatelj projekta
- Administrator odobravatelja projekta

## <a name="project-approver"></a>Odobravatelj projekta

Sigurnosna uloga **Odobravatelj projekta** mora vam biti dodijeljena da biste mogli odobravati unose vremena, troškova i materijala projekta. Također morate imati pristup relevantnim povezanim entitetima, npr. entitetu **Projekt**. Taj pristup može dodijeliti osoba kojoj je dodijeljena uloga **Voditelj projekta**. Osim toga, morate biti član tima projekta i označeni kao odobravatelj.

Da biste odobrili unose koji se ne odnose na projekt, morate biti upravitelj podnositelja.

## <a name="project-approver-admin"></a>Administrator odobravatelja projekta

> [!NOTE]
> Značajka [Skupovi odobrenja](approval-sets.md) mora biti omogućena prije nego što se možete koristiti funkcijom Administrator odobravatelja projekta.

Sigurnosna uloga **Administrator odobravatelja projekta** omogućuje korisnicima zaobilaženje pravila i omogućuje odobravanje unosa u svim projektima. Dodjeljivanjem ove uloge zaobići će se logika provjere valjanosti koja zahtijeva da je osoba član tima te da je označena kao odobravatelj. Morate imati pristup relevantnim povezanim tablicama, kao što je **Projekt**, putem sigurnosnih uloga koje su vam dodijeljene.

Kontekst korisnika SUSTAVA zaobilazi provjere valjanosti na isti način kao i sigurnosna uloga Administrator odobravatelja projekta.
