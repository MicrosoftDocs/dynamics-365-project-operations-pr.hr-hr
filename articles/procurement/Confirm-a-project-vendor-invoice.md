---
title: Potvrda fakture dobavljača na projektu
description: U ovom se članku objašnjava kako potvrditi fakturu dobavljača projekta u sustavu Microsoft Dynamics 365 Project Operations te se opisuje financijski učinak potvrđivanja fakture dobavljača projekta.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475464"
---
# <a name="confirm-project-vendor-invoices"></a>Potvrda fakture dobavljača na projektu

**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha

Kada je parametar **Potrebna je ručna potvrda upravitelja projekta** omogućen, status faktura dobavljača izrađenih na platformi Microsoft Dataverse glasi **Nacrt**. Fakture dobavljača izrađene na ovaj način moraju se pregledati i ručno potvrditi. Kada je parametar **Potrebna je ručna potvrda upravitelja projekta** onemogućen, fakture dobavljača izrađene na platformi Dataverse automatski se potvrđuju. Daljnje radnje nisu potrebne. 

Nakon što ste provjerili sve retke fakture dobavljača u sustavu Dynamics 365 Project Operations, odaberite **Potvrdi** za potvrdu fakture dobavljača.

Kada odaberete **Potvrdi** na fakturi dobavljača, događa se sljedeće:

1. Status fakture dobavljača ažurira se na **Potvrđeno**.
1. Potvrđena faktura dobavljača i s njom povezani zapisi postaju samo za čitanje te se ne mogu uređivati niti brisati.
1. Ako bilo koji stvarni podaci o troškovima upućuje na redak fakture dobavljača kao dio procesa uparivanja, svi stvarni podaci o troškovima koji su povezani s referenciranim retkom fakture dobavljača se poništavaju.
1. Novi stvarni podaci o troškovima izrađuju se primjenom informacija u retku fakture dobavljača.
1. Više ne možete izrađivati dnevnike ispravaka, obrađivati opozive unosa vremena ili otkazati odobrenje izvornog vremena, troška ili stvarnih podataka o materijalu koje je poništeno.
1. Vrijednost **Trošak projekta** se u sustavu Dynamics 365 Finance ažurira korištenjem dnevnika integracije projekta, a račun integracije nabave se *poništava* nakon što se objavi dnevnik integracije projekta.

> [!NOTE]
> Faktura dobavljača ne može se potvrditi ako status svih redaka fakture dobavljača ne glasi **Dovršeno**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
