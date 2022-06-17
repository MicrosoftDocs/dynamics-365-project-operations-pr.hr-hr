---
title: Stvarni podaci
description: U ovom se članku nalaze informacije o radu sa stvarnim stvarima u sustavu Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924789"
---
# <a name="actuals"></a>Stvarni podaci

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Stvarni podaci predstavljaju pregledani i odobreni financijski napredak i napredak rasporeda na projektu. Kreiraju se kada se odobravaju stavke vremena, troška i upotrebe materijala, stavke temeljnice i fakture.

> [!IMPORTANT]
> Stvarne vrijednosti ne bi trebalo uređivati ili brisati iz sustava. U suprotnom bi to moglo negativno utjecati na financijski integritet i svaku integraciju s drugim financijskim i računovodstvenim sustavima. Microsoft Dynamics 365 Project Operations vam omogućuje da koristite storniranje i zamjenu stvarnih vrijednosti za uređivanje stvarnih vrijednosti u različitim točkama životnog ciklusa poslovnih procesa vaših projekata.

## <a name="recording-actuals-based-on-project-events"></a>Zapis stvarnih vrijednosti na temelju projektnih događaja

Project Operations bilježi financijske transakcije koje se dogode tijekom životnog ciklusa angažmana projekta kao stvarne. Stvaranje stvarnih stvari na različitim događajima u životnom ciklusu varira, ovisno o tome koristi li angažman projekta model naplate vremena i materijala ili model naplate fiksne cijene i je li u fazi pretprodaje ili je interni projekt.

Sljedeći članci objašnjavaju utjecaj na tablicu Stvarni podaci na različitim događajima za različite varijacije:

- [Stvarni utjecaj u vremenu i angažmanu materijala](ActualsonTM.md)
- [Stvarni utjecaj u angažmanu s fiksnom cijenom](ActualonFP.md)
- [Stvarni učinak tijekom pretprodajne faze angažmana](ActualonPreSales.md)
- [Stvarni učinak za interni projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
