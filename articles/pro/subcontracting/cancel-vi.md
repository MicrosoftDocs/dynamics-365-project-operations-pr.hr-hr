---
title: Opoziv fakture dobavljača projekta
description: U ovom se članku objašnjava kako otkazati fakturu dobavljača projekta u sustavu Microsoft Dynamics 365 Project Operations, kao i financijski učinak otkazivanja fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261081"
---
# <a name="cancel-a-project-vendor-invoice"></a>Opoziv fakture dobavljača projekta

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Nakon što se faktura dobavljača potvrdi, više se ne može uređivati ili izbrisati. Ako je došlo do pogreške na fakturi dobavljača koja je potvrđena, možete upotrijebiti radnju Odustani za poništavanje utjecaja fakture dobavljača i izradu nove fakture dobavljača.

Kada odaberete **Otkaži** na fakturi dobavljača, događa se sljedeće:

1. Stanje fakture dobavljača ažurira se na **Otkazano**.
2. Otkazana faktura dobavljača i s njom povezani zapisi postaju samo za čitanje te se ne mogu uređivati niti brisati.
3. Bilo koji stvarni podaci o trošku izrađeni na temelju redaka fakture dobavljača kao dio potvrde fakture dobavljača se poništavaju.
4. Ako su bilo koji stvarni podaci o trošku bili povezani s recima fakture dobavljača kao dio procesa uparivanja, originalna potvrda fakture dobavljača ih je poništila. Tijekom otkazivanja fakture dobavljača, ti se stvarni podaci o trošku ponovno kreiraju. Podrijetlo ukazuje na unose vremena, troškova ili upotrebe materijala.
5. Nakon otkazivanja fakture dobavljača, ponovno možete izrađivati dnevnike ispravaka, obrađivati opozive unosa vremena ili otkazati odobrenje izvornog vremena, troška ili stvarnih podataka o materijalu koje je poništeno.

> [!NOTE]
> Samo potvrđene fakture dobavljača projekta mogu se poništiti Fakture dobavljača čija stanja glase drugačije ne mogu se poništiti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
