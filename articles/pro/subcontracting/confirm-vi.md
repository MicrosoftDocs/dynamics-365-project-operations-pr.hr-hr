---
title: Potvrda fakture dobavljača projekta
description: Ovaj tema objašnjava kako potvrditi fakturu dobavljača projekta u Microsoftu Dynamics 365 Project Operations i financijski učinak potvrde fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595719"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potvrda fakture dobavljača projekta

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Kada potvrdite sve retke na fakturi dobavljača u Microsoftu Dynamics 365 Project Operations, možete upotrijebiti akciju Potvrda da biste potvrdili fakturu dobavljača.

Kada na fakturi dobavljača odaberete **Potvrdi**, događa se sljedeće ponašanje:

1. Stanje fakture dobavljača obnavlja se u **Potvrđeno**.
2. Potvrđena faktura dobavljača i povezani zapisi postaju samo za čitanje i ne mogu se uređivati ili brisati.
3. Ako se bilo koji iznos troška odnosi na redak fakture dobavljača kao dio postupka podudaranja, sve stvarne troškove povezane s referentnim retkom fakture dobavljača storniraju se.
4. Novi iznosi troška kreiraju se pomoću podataka u retku fakture dobavljača.
5. Nakon što je faktura dobavljača potvrđena, više ne možete kreirati temeljnice ispravaka, opozive stavki vremena obrade ili stornirati odobravanje izvornog vremena, troška ili stvarnog materijala koje su stornirane.

> [!NOTE]
> Ako bilo koji redak na fakturi dobavljača ima status provjere koji nije **Dovršeno**, faktura dobavljača ne može se potvrditi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
