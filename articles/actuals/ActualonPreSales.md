---
title: Stvarni učinak tijekom pretprodajne faze angažmana
description: U ovom se članku navode informacije o utjecaju na tablicu Stvarne na različitim događajima dok je zaplet u fazi pretprodaje u Microsoftu Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922351"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Stvarni učinak tijekom pretprodajne faze angažmana

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U sljedećoj su tablici navedene stvarne vrijednosti različitih vrsta transakcija kreirane na različitim događajima tijekom pretprodajne faze angažmana projekta.

| Događaj | Stvarna vrijednost troškova | Primjer |
|---|---|---|
| Vrijeme se stvara. | Nije primjenjivo | <p>Bob Kozack, iz američke organizacijske jedinice Fabrikam koja ima stopu troškova od 100 američkih dolara (100 USD) po satu, radi na projektu koji nosi naziv "Arm Installation at Adatum". Ovaj projekt mapiran je na način naplate fiksne cijene u retku ugovora. Evo oglednog vremenskog unosa Boba Kozaka:</p><p>Bob Kozack - 8 sati</p> |
| Vrijeme se šalje. | Nije primjenjivo | Za stavku vremena kreira se redak temeljnice troškova. Zadana stopa troška unosi se u stavku temeljnice. |
| Unos vremena se opoziva prije nego što bude odobren. | Nije primjenjivo | |
| Vrijeme je odobreno. | Stvara se stvarni trošak. | <p>Stvoreno je novo stvarno:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul> |
| Odobrenje vremena je otkazano. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul> |
| Unos vremena opozvan je nakon što je odobren. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul> |
| Ponuda je osvojena i kreira se ugovor. | <p>Status prilagodbe starih iznosa troškova obnavlja se u **Prilagođeno**.</p><p>Kreiraju se stvarni troškovi storniranja koji imaju status prilagodbe **nepravomoćno**.</p><p>Nove stvarne troškove stvaraju se nakon ponovne procjene ugovornih pravila.</p> | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul><p>Nove stvarne vrijednosti kreirane za ponovno procijenjeni financijski učinak prilikom osvojene ponude i stvaranja ugovora:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li><li>**Nenaplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
