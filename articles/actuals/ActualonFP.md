---
title: Utjecaj stvarnih podataka na angažiranje fiksne cijene
description: U ovom se članku navode informacije o utjecaju na tablicu Stvarni podaci u okviru različitih događaja tijekom životnog ciklusa angažmana po fiksnoj cijeni u sustavu Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918119"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Utjecaj stvarnih podataka na angažiranje fiksne cijene

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U sljedećoj tablici navode se stvarni podaci različitih vrsta transakcija izrađeni u okviru različitih događaja u angažmanu po fiksnoj cijeni.

| Događaj | Stvarna vrijednost troškova | Stvarni podatak o nenaplaćenim prodajama | Stvarni podatak o naplaćenim prodajama | Primjer |
|---|---|---|---|---|
| Izrađuje se stavka Vrijeme. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | <p>Bob Kozack, iz organizacijske jedinice Fabrikam US koja ima stopu troška od 100 američkih dolara (100 USD) po satu, radi na projektu naziva "Ugradnja kraka u postrojenju Adatum". Za taj je projekt na retku ugovora određena metoda naplate s fiksnom cijenom. Ovo je primjer unosa vremena Boba Kozaka:</p><p>Bob Kozack – 8 sati</p> |
| Vrijeme podneseno. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | Redak u dnevniku troška izrađuje se za svaki unos vremena. Zadana stopa trošak unosi se u dnevnički unos. |
| Unos vremena opozove se prije nego što se odobri. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | |
| Vrijeme je odobreno. | Izrađuje se stvarni podatak troška. | Nije primjenjivo | Nije primjenjivo | <p>Novi stvarni podatak koji je izrađen:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD</li></ul> |
| Odobrenje vremena je poništeno. | <p>Status prilagodbe stvarnog podatka troška ažurira se na **Prilagođeno**.</p><p>Izrađuje se stvarni podatak poništenog troška koji ima status prilagodbe **Nije moguće prilagoditi**.</p> | Nije primjenjivo | Nije primjenjivo | <p>Postojeći stvarni podatak koji se ažurira:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD, *Prilagođeno*</li></ul><p>Novi stvarni podataka koji se izrađuje radi poništavanja prethodnog financijskog učinka:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, (8 sati), (800 USD), *Nije moguće prilagoditi*</li></ul> |
| Unos vremena opozove se nakon što se odobri. | <p>Status prilagodbe stvarnog podatka troška ažurira se na **Prilagođeno**.</p><p>Izrađuje se stvarni podatak poništenog troška koji ima status prilagodbe **Nije moguće prilagoditi**.</p> | Nije primjenjivo | Nije primjenjivo | <p>Postojeći stvarni podatak koji se ažurira:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD, *Prilagođeno*</li></ul><p>Novi stvarni podataka koji se izrađuje radi poništavanja prethodnog financijskog učinka:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, (8 sati), (800 USD), *Nije moguće prilagoditi*</li></ul> |
| Ugovor je potvrđen. | <p>Status prilagodbe starih stvarnih podataka troška ažurira se na **Prilagođeno**.</p><p>Izrađuju se stvarni podaci poništenja troška čiji status prilagodbe status glasi **Nije moguće prilagoditi**.</p><p>Novi stvarni podaci troška izrađuju se nakon ponovne procjene ugovornih pravila.</p> | Nije primjenjivo | Nije primjenjivo | <p>Postojeći stvarni podatak koji se ažurira:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD, *Prilagođeno*</li></ul><p>Novi stvarni podataka koji se izrađuje radi poništavanja prethodnog financijskog učinka:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, (8 sati), (800 USD), *Nije moguće prilagoditi*</li></ul><p>Novi stvarni podatak koji se izrađuje za ponovno procijenjeni financijski učinak:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD</li></ul> |
| Izrađuje se fakture. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | |
| Faktura se potvrđuje kontrolnom točkom. | Nije primjenjivo | Nije primjenjivo | Izrađuju se novi stvarni podaci naplaćene prodaje temeljeni na kontrolnoj točki. | <p>Postojeći stvarni podatak koji ostaju nepromijenjen:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD</li></ul><p>Novi stvarni podatak koji je izrađen radi bilježenja vrijednosti naplaćene prodaje:</p><ul><li>**Stvarni podatak naplaćene prodaje:** Kontrolna točka, USD 5.000</li></ul> |
| Faktura se ispravlja kako bi se knjižila kontrolna točka. | Nije primjenjivo | Nije primjenjivo | Izrađuju se stvarni podaci storniranja naplaćene prodaje. | <p>Postojeći stvarni podatak koji ostaju nepromijenjen:</p><ul><li>**Stvarni podatak troška:** Bob Kozack, 8 sati, 800 USD</li></ul><p>Postojeći stvarni podatak koji se ažurira:</p><ul><li>**Stvarni podatak naplaćene prodaje:** Kontrolna točka, 5.000 USD, *Prilagođeno*</li></ul><p>Novi stvarni podatak koji je izrađen radi storniranja vrijednosti prethodno naplaćene prodaje:</p><ul><li>**Stvarni podatak naplaćene prodaje:** Kontrolna točka, (5.000 USD), *Nije moguće prilagoditi*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
