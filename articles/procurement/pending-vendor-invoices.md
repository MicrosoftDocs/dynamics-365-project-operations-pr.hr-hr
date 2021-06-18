---
title: Kupnja materijala koji nisu na zalihama s pomoću fakture dobavljača na čekanju
description: U ovoj se temi objašnjava način bilježenja faktura dobavljača na čekanju.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993774"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Kupnja materijala koji nisu na zalihama s pomoću fakture dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kako tvrtka za projekt nabavlja materijale koji nisu na zalihi, troškovi se mogu odmah evidentirati u odnosu na projekt. 

Na primjer, Contoso Robotics US izvodi projekt obnove opreme i treba softverske licence. Te se licence nabavljaju od dobavljača koji je treća srana.  S pomoću aplikacije Dynamics 365 Finance, službenik za dugovanja evidentira dokument fakture dobavljača na čekanju i pripisuje troškove licence izravno na projekt obnove opreme. 

> [!IMPORTANT]
> Prije nego što upotrijebite funkcionalnost opisanu u ovoj temi, pregledajte i primijenite potrebne konfiguracije. Dodatne informacija potražite u članku [Omogućivanje materijala koji nisu na zalihi i fakture dobavljača na čekanju](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Knjiženje fakture dobavljača na čekanju povezane s projektom 

Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**). Poduzmite sljedeće korake za knjiženje fakture dobavljača na čekanju u vezi s projektom:

1. Idite na **Dugovanja** > **Fakture** i odaberite **Nova**. 
2. U polju **Račun fakture** odaberite dobavljača, a u polje **Broj** unesite identifikaciju fakture dobavljača.
3. Dodajte redak fakturi dobavljača i u polju **Broj stavke** odaberite stavku koja nije na zalihi kupljenu od dobavljača. 

    > [!NOTE]
    > Redci fakture dobavljača koji se temelje na kategoriji nabave ne mogu se evidentirati u projektu. 
    
5. Dodajte kupljenu količinu. Sustav će popuniti jediničnu cijenu na temelju konfiguracije cijene stavke koja nije na zalihi. 
6. U retku provjerite ukupan iznos i ostale potrebne pojedinosti.
7. Na pojedinostima retka, na kartici **Projekt**, odaberite ID projekta na koji će se evidentirati ova stavka.
8. Po želji odaberite broj aktivnosti i ažurirajte kategoriju projekta i svojstvo retka.
9. Knjiženje fakture dobavljača na čekanju. Kada se faktura proknjiži, sustav bilježi:
    
    - Iznos salda dobavljača.
    - Iznos poreza na promet.
    - Trošak u odnosu na projekt evidentira se na račun integracije nabave.
    - Stvarna transakcija projekta na platformi Dataverse. Ova se transakcija dalje obrađuje s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md). Knjiženjem ovog dnevnika premješta se iznos s računa integracije nabave na račun troškova projekta.