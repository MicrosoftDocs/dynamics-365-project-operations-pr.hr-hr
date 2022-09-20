---
title: Potvrda faktura dobavljača projekta
description: U ovom se članku objašnjava kako potvrditi fakturu dobavljača projekta u Microsoftu Dynamics 365 Project Operations i opisuje financijski učinak potvrde fakture dobavljača projekta.
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
# <a name="confirm-project-vendor-invoices"></a>Potvrda faktura dobavljača projekta

**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha

Kada je parametar Ručna **potvrda prema PM-u obavezna**, fakture dobavljača kreirane u Microsoft Dataverse sustavu imaju **status Skica**. Tako kreirane fakture dobavljača moraju se pregledati i ručno potvrditi. Kada je parametar Ručna **potvrda prema PM-u obavezan** onemogućen, fakture dobavljača kreirane u sustavu Dataverse automatski se potvrđuju. Daljnje radnje nisu potrebne. 

Kada potvrdite sve retke na fakturi dobavljača u Dynamics 365 Project Operations sustavu, odaberite **Potvrdi** da biste potvrdili fakturu dobavljača.

Kada na fakturi dobavljača odaberete **Potvrdi**, događa se sljedeće ponašanje:

1. Status fakture dobavljača obnavlja se u **Potvrđeno**.
1. Potvrđena faktura dobavljača i povezani zapisi postaju samo za čitanje i ne mogu se uređivati ili brisati.
1. Ako se bilo koji iznos troška odnosi na redak fakture dobavljača kao dio postupka podudaranja, sve stvarne troškove povezane s referentnim retkom fakture dobavljača storniraju se.
1. Novi iznosi troška kreiraju se pomoću podataka u retku fakture dobavljača.
1. Više ne možete kreirati temeljnice ispravaka, obrađivati opozive stavki vremena ili stornirati odobravanje izvornog vremena, troškova ili stvar materijala koje su stornirane.
1. U Dynamics 365 Finance **vrijednost troška** projekta ažurira se pomoću temeljnice integracija projekta, a račun integracije s nabavom stornira *se* nakon knjiženja temeljnice integracije projekta.

> [!NOTE]
> Ako bilo koji redak na fakturi dobavljača ima status provjere koji nije **Dovršeno**, faktura dobavljača ne može se potvrditi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
