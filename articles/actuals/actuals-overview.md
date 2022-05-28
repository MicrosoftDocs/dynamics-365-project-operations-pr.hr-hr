---
title: Stvarni podaci
description: U ovoj temi nalaze se informacije o radu sa stvarnim podacima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581275"
---
# <a name="actuals"></a>Stvarni podaci

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Stvarni podaci predstavljaju pregledani i odobreni financijski napredak i napredak rasporeda na projektu. Kreiraju se kada se odobravaju stavke vremena, troška i upotrebe materijala, stavke temeljnice i fakture.

> [!IMPORTANT]
> Stvarne vrijednosti ne bi trebalo uređivati ili brisati iz sustava. U suprotnom bi to moglo negativno utjecati na financijski integritet i svaku integraciju s drugim financijskim i računovodstvenim sustavima. Microsoft Dynamics 365 Project Operations vam omogućuje da koristite storniranje i zamjenu stvarnih vrijednosti za uređivanje stvarnih vrijednosti u različitim točkama životnog ciklusa poslovnih procesa vaših projekata.

## <a name="recording-actuals-based-on-project-events"></a>Zapis stvarnih vrijednosti na temelju projektnih događaja

Project Operations bilježi financijske transakcije koje se dogode tijekom životnog ciklusa angažmana projekta kao stvarne. Stvaranje stvarnih stvari na različitim događajima u životnom ciklusu varira, ovisno o tome koristi li angažman projekta model naplate vremena i materijala ili model naplate fiksne cijene i je li u fazi pretprodaje ili je interni projekt.

Sljedeće teme objašnjavaju utjecaj na tablicu Stvarni podaci na različitim događajima za različite varijacije:

- [Stvarni utjecaj u vremenu i angažmanu materijala](ActualsonTM.md)
- [Stvarni utjecaj u angažmanu s fiksnom cijenom](ActualonFP.md)
- [Stvarni učinak tijekom pretprodajne faze angažmana](ActualonPreSales.md)
- [Stvarni učinak za interni projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
