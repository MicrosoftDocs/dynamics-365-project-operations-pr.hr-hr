---
title: Stvarni podaci
description: U ovom se članku navode informacije o radu sa stvarnim podacima u aplikaciji Microsoft Dynamics 365 Project Operations.
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

Stvarni podaci predstavljaju pregledani i odobreni financijski napredak i napredak rasporeda na projektu. Izrađuju se u trenutku odobravanja unosa vremena, troškova, utrošenog materijala te unosa i faktura dnevnika.

> [!IMPORTANT]
> Stvarni podaci ne smiju se uređivati niti brisati iz sustava. U protivnom, to bi moglo negativno utjecati na financijski integritet i bilo kakvu integraciju s drugim financijskim i računovodstvenim sustavima. Sustav Microsoft Dynamics 365 Project Operations omogućuje vam korištenje poništavanja i zamjene stvarnih podataka za uređivanje stvarnih podataka na različitim točkama u životnom ciklusu poslovnog procesa vaših projekata.

## <a name="recording-actuals-based-on-project-events"></a>Zapis stvarnih vrijednosti na temelju projektnih događaja

Aplikacija Project Operations bilježi financijske transakcije koje se odvijaju tijekom životnog ciklusa angažmana projekta u obliku stvarnih podataka. Izrada stvarnih podataka u okviru različitih događaja u životnom ciklusu varira, ovisno o tome primjenjuje li angažman projekta model naplate vremena i materijala ili model naplate po fiksnoj cijeni te je li u fazi pretprodaje ili je interni projekt.

U sljedećim člancima objašnjava se utjecaj na tablicu Stvarni podaci u okviru različitih događaja za različite varijacije:

- [Utjecaj stvarnih podataka na angažiranje vremena i materijala](ActualsonTM.md)
- [Utjecaj stvarnih podataka na angažiranje fiksne cijene](ActualonFP.md)
- [Utjecaj stvarnih podataka tijekom pretprodajne faze angažmana](ActualonPreSales.md)
- [Utjecaj stvarnih podataka za interni projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
