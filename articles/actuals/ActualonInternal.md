---
title: Utjecaj stvarnih podataka za interni projekt
description: U ovom se članku navode informacije o utjecaju na tablicu Stvarni podaci u okviru različitih događaja za interni projekt u sustavu Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921339"
---
# <a name="actuals-impact-for-an-internal-project"></a>Utjecaj stvarnih podataka za interni projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Sljedeća tablica navodi stvarne podatke različitih vrsta transakcija izrađenih u okviru različitih događaja u internom projektnom angažmanu.

| Događaj | Stvarna vrijednost troškova | Primjer |
|---|---|---|
| Izrađuje se stavka Vrijeme. | Nije primjenjivo | <p>Bob Kozack, iz organizacijske jedinice Fabrikam US koja ima stopu troška od 100 američkih dolara (100 USD) po satu, radi na projektu naziva "Ugradnja kraka u postrojenju Adatum". Za taj je projekt na retku ugovora određena metoda naplate s fiksnom cijenom. Ovo je primjer unosa vremena Boba Kozaka:</p><p>Bob Kozack – 8 sati</p> |
| Vrijeme podneseno. | Nije primjenjivo | Redak u dnevniku troška izrađuje se za svaki unos vremena. Zadana stopa trošak unosi se u dnevnički unos. |
| Unos vremena opozove se prije nego što se odobri. | Nije primjenjivo | |
| Vrijeme je odobreno. | Izrađuje se stvarni podatak troška. | <p>Novi stvarni podatak koji je izrađen:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD</li></ul> |
| Odobrenje vremena je poništeno. | <p>Status prilagodbe stvarnog podatka troška ažurira se na **Prilagođeno**.</p><p>Izrađuje se stvarni podatak poništenog troška koji ima status prilagodbe **Nije moguće prilagoditi**.</p> | <p>Postojeći stvarni podatak koji se ažurira:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD, *Prilagođeno*</li></ul><p>Novi stvarni podataka koji se izrađuje radi poništavanja prethodnog financijskog učinka:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, (8 sati), (800 USD), *Nije moguće prilagoditi*</li></ul> |
| Unos vremena opozove se nakon što se odobri. | <p>Status prilagodbe stvarnog podatka troška ažurira se na **Prilagođeno**.</p><p>Izrađuje se stvarni podatak poništenog troška koji ima status prilagodbe **Nije moguće prilagoditi**.</p> | <p>Postojeći stvarni podatak koji se ažurira:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD, *Prilagođeno*</li></ul><p>Novi stvarni podataka koji se izrađuje radi poništavanja prethodnog financijskog učinka:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, (8 sati), (800 USD), *Nije moguće prilagoditi*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
