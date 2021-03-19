---
title: Ispravljene fakture
description: U ovoj se temi nalaze informacije o ispravljenim fakturama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287814"
---
# <a name="corrected-invoices"></a>Ispravljene fakture

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Potvrđene fakture mogu se urediti. Kada uređujete potvrđenu fakturu, stvara se skica ispravljene fakture. Budući da se pretpostavlja kako želite poništiti sve transakcije i količine iz izvorne fakture, ispravljena faktura uključuje sve transakcije iz izvorne fakture, a sve količine navedene u njoj iznose nula (0).

Kada transakcije ne treba ispravljati, možete ih ukloniti iz skice ispravljene fakture. Kako biste poništili ili vratili samo djelomičnu količinu, polje Količina možete urediti u pojedinosti retka. Ako otvorite pojedinost retka fakture, možete vidjeti izvornu količinu fakture. Zatim možete urediti trenutačnu količinu fakture tako da je manja ili veća od izvorne količine fakture.

Kada potvrdite ispravljenu fakturu, izvorni naplaćeni stvarni podatak o prodaji mijenja se i stvara se novi naplaćeni stvarni podatak o prodaji. Ako je količina manja, razlika će dovesti i do stvaranja novog nenaplaćenog stvarnog podatka o prodaji. Na primjer, ako je izvorna naplaćena prodaja obuhvaćala osam sati, a pojedinost retka ispravljene fakture sadrži manju količinu od šest sati, vraća se izvorni redak naplaćene prodaje i stvaraju se dva nova stvarna podatka:

- Naplaćeni stvarni podatak o prodaji za šest sati.
- Nenaplaćeni stvarni podatak o prodaji za preostala dva sata. Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, ovisno o pregovorima s klijentom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]