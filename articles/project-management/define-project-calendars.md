---
title: Definiranje kalendara projekata
description: U ovom se članku nalaze informacije o primjeni predloška kalendara na projekt za praćenje rasporeda projekta.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e195cdb0dc5acc2ea816fadce40811675a855de2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933529"
---
# <a name="define-project-calendars"></a>Definiranje kalendara projekata

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Kako biste stvorili projekt i upravljali njime, na projekt morate primijeniti predložak kalendara. Predložak kalendara definira sljedeće atribute projekta:

- Radno vrijeme, uključujući vrijeme početka i završetka
- Radni dani
- Iznimke kalendara poput neradnih dana

Predložak kalendara koji se primjenjuje na projekt kopija je predloška kalendara definiranog u postavkama vaše tvrtke ili ustanove.

> [!NOTE]
> Ako promijenite predložak kalendara, te se promjene neće proširiti na radno vrijeme projekta. Kako biste promijenili radno vrijeme projekta, morate primijeniti novi obrazac.

Dva su osnovna zahtjeva za stvaranje predloška kalendara za vašu tvrtku ili ustanovu:

- Definirajte željeno radno vrijeme predloška s pomoću novog ili postojećeg resursa koji se može rezervirati.
- Stvorite novi predložak kalendara i povežite ga s resursom koji se može rezervirati.

**Definiranje radnog vremena predloška**

1. Otvorite **Resursi** \> **Resursi**.
2. Stvorite novi resurs za referencu u predlošku kalendara ili odaberite postojeći.
3. Odaberite karticu **Radno vrijeme** resursa i dovršite upute iz članka [Postavljanje radnog vremena za resurs](/dynamics365/field-service/set-work-hours-resource) kako biste konfigurirali pravila kalendara.

**Stvaranje novog predloška kalendara**

1. Idite na **Postavke** \> **Predložak kalendara**.
2. Odaberite **Novi** i unesite naziv, opis i resurs predloška.

> [!NOTE]
> Kada se u predlošku kalendara upućuje na resurs, kopija kalendara resursa povezuje se s predloškom kalendara. Ako se promijeni radno vrijeme kopiranog predloška, te se promjene neće proširiti na predložak kalendara.

Sada možete povezati predložak rada s predloškom kalendara projekta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

