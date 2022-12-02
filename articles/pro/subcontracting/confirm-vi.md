---
title: Potvrda fakture dobavljača projekta
description: U ovom se članku objašnjava kako potvrditi fakturu dobavljača projekta u sustavu Microsoft Dynamics 365 Project Operations, kao i financijski učinak potvrđivanja fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261502"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potvrda fakture dobavljača projekta

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Nakon što ste provjerili sve retke fakture dobavljača u sustavu Microsoft Dynamics 365 Project Operations, radnjom Potvrdi možete potvrditi fakturu dobavljača.

Kada odaberete **Potvrdi** na fakturi dobavljača, događa se sljedeće:

1. Stanje fakture dobavljača ažurira se na **Potvrđeno**.
2. Potvrđena faktura dobavljača i s njom povezani zapisi postaju samo za čitanje te se ne mogu uređivati niti brisati.
3. Ako bilo koji stvarni podaci o troškovima upućuje na redak fakture dobavljača kao dio procesa uparivanja, svi stvarni podaci o troškovima koji su povezani s referenciranim retkom fakture dobavljača se poništavaju.
4. Novi stvarni podaci o troškovima izrađuju se primjenom informacija u retku fakture dobavljača.
5. Nakon potvrđivanja fakture dobavljača više ne možete izrađivati dnevnike ispravaka, obrađivati opozive unosa vremena ili otkazati odobrenje izvornog vremena, troška ili stvarnih podataka o materijalu koje je poništeno.

> [!NOTE]
> Faktura dobavljača ne može se potvrditi ako status svih redaka fakture dobavljača ne glasi **Dovršeno**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
