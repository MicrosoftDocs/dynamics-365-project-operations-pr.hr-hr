---
title: Stvarni utjecaj u angažmanu s fiksnom cijenom
description: Ova tema pruža informacije o utjecaju na tablicu Actuals na različitim događajima tijekom životnog ciklusa fiksnog cjenovnog angažmana u Microsoftu Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579219"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Stvarni utjecaj u angažmanu s fiksnom cijenom

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U sljedećoj su tablici navedene stvarne vrijednosti različitih vrsta transakcija koje se kreiraju na različitim događajima u angažmanu s fiksnom cijenom.

| Događaj | Stvarna vrijednost troškova | Stvarni podatak o nenaplaćenim prodajama | Stvarna naplaćena prodaja | Primjer |
|---|---|---|---|---|
| Vrijeme se stvara. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | <p>Bob Kozack, iz američke organizacijske jedinice Fabrikam koja ima stopu troškova od 100 američkih dolara (100 USD) po satu, radi na projektu koji nosi naziv "Arm Installation at Adatum". Ovaj projekt mapiran je na način naplate fiksne cijene u retku ugovora. Evo oglednog vremenskog unosa Boba Kozaka:</p><p>Bob Kozack - 8 sati</p> |
| Vrijeme se šalje. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | Za stavku vremena kreira se redak temeljnice troškova. Zadana stopa troška unosi se u stavku temeljnice. |
| Unos vremena se opoziva prije nego što bude odobren. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | |
| Vrijeme je odobreno. | Stvara se stvarni trošak. | Nije primjenjivo | Nije primjenjivo | <p>Stvoreno je novo stvarno:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul> |
| Odobrenje vremena je otkazano. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | Nije primjenjivo | Nije primjenjivo | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul> |
| Unos vremena opozvan je nakon što je odobren. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | Nije primjenjivo | Nije primjenjivo | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul> |
| Ugovor je potvrđen. | <p>Status prilagodbe starih iznosa troškova obnavlja se u **Prilagođeno**.</p><p>Kreiraju se stvarni troškovi storniranja koji imaju status prilagodbe **nepravomoćno**.</p><p>Nove stvarne troškove stvaraju se nakon ponovne procjene ugovornih pravila.</p> | Nije primjenjivo | Nije primjenjivo | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul><p>Nova stvarna vrijednost stvorena za ponovno procijenjeni financijski učinak:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul> |
| Kreira se faktura. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | |
| Račun je potvrđen prekretnicom. | Nije primjenjivo | Nije primjenjivo | Kreiraju se nove naplaćene prodajne stvarne vrijednosti temeljene na ključnim etapama. | <p>Postojeća stvarna vrijednost koja ostaje nepromijenjena:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul><p>Novo stvarno stvoreno za bilježenje naplaćenih vrijednosti prodaje:</p><ul><li>**Stvarna naplaćena prodaja:** Prekretnica, USD 5,000</li></ul> |
| Račun je ispravljen kako bi se pripisala prekretnica. | Nije primjenjivo | Nije primjenjivo | Kreiraju se naplaćene vrijednosti prodaje storniranja. | <p>Postojeća stvarna vrijednost koja ostaje nepromijenjena:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, 800 USD</li></ul><p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarna naplaćena prodaja:** prekretnica, USD 5,000, *prilagođeno*</li></ul><p>Novo stvarno stvoreno za storniranje prethodnih naplaćenih prodajnih vrijednosti:</p><ul><li>**Stvarna naplaćena prodaja:** Prekretnica, (5,000 USD), *Nepravomoćno*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
