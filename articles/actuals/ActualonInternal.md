---
title: Stvarni učinak za interni projekt
description: Ova tema pruža informacije o utjecaju na tablicu Stvarne na različitim događajima za interni projekt u Microsoftu Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579757"
---
# <a name="actuals-impact-for-an-internal-project"></a>Stvarni učinak za interni projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U sljedećoj su tablici navedene stvarne vrijednosti različitih vrsta transakcija koje se kreiraju na različitim događajima u internom angažmanu projekta.

| Događaj | Stvarna vrijednost troškova | Primjer |
|---|---|---|
| Vrijeme se stvara. | Nije primjenjivo | <p>Bob Kozack, iz američke organizacijske jedinice Fabrikam koja ima stopu troškova od 100 američkih dolara (100 USD) po satu, radi na projektu koji nosi naziv "Arm Installation at Adatum". Ovaj projekt mapiran je na način naplate fiksne cijene u retku ugovora. Evo oglednog vremenskog unosa Boba Kozaka:</p><p>Bob Kozack - 8 sati</p> |
| Vrijeme se šalje. | Nije primjenjivo | Za stavku vremena kreira se redak temeljnice troškova. Zadana stopa troška unosi se u stavku temeljnice. |
| Unos vremena se opoziva prije nego što bude odobren. | Nije primjenjivo | |
| Vrijeme je odobreno. | Stvara se stvarni trošak. | <p>Stvoreno je novo stvarno:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul> |
| Odobrenje vremena je otkazano. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul> |
| Unos vremena opozvan je nakon što je odobren. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | <p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li></ul><p>Nova stvarna stvar stvorena za preokretanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
