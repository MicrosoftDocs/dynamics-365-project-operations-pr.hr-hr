---
title: Nabava materijala koji nisu na zalihama ili nabavnih kategorija pomoću fakture dobavljača na čekanju
description: U ovom se članku objašnjava način evidentiranja faktura dobavljača na čekanju.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921983"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nabava materijala koji nisu na zalihama ili nabavnih kategorija pomoću fakture dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kako tvrtka za projekt nabavlja materijale koji nisu na zalihama ili nabavne kategorije, troškovi projekta mogu se odmah evidentirati. 

Na primjer, Contoso Robotics US izvršava projekt obnove opreme i potrebne su mu licence za softver. Te se licence nabavljaju od dobavljača koji je treća srana.  Upotrebom sustava Dynamics 365 Finance računovođa evidentira dokument fakture dobavljača na čekanju i pripisuje troškove licencije izravno na projekt obnove opreme. 

> [!IMPORTANT]
> Prije nego što upotrijebite funkcionalnost opisanu u ovom članku, pregledajte i primijenite potrebne konfiguracije. Za više informacija pogledajte [Omogućite materijale koji nisu na zalihama i fakture dobavljača na čekanju](configure-materials-nonstocked.md) i [Koristite nabavne kategorije s narudžbenicama za projekt i fakturama dobavljača na čekanju](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Knjiženje fakture dobavljača na čekanju povezane s projektom 

Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**). Poduzmite sljedeće korake za knjiženje fakture dobavljača na čekanju u vezi s projektom:

1. Idite na **Dugovanja** > **Fakture** i odaberite **Nova**. 
1. U polju **Račun fakture** odaberite dobavljača, a zatim u polje **Broj** unesite broj fakture dobavljača.
1. Dodajte redak na fakturi dobavljača i u polju **Broj stavke** odaberite stavku kupljenu od dobavljača koja nije na zalihi. Umjesto toga u polju **Kategorija nabave** odaberite nabavu kategoriju koja je kupljena od dobavljača.   
1. Dodajte kupljenu količinu. Sustav popunjava jediničnu cijenu na temelju konfiguracije cijene stavke koja nije na zalihi. 
1. U retku provjerite ukupan iznos i ostale potrebne pojedinosti.
1. Na pojedinostima retka, na kartici **Projekt** odaberite ID projekta za koji će se evidentirati ova stavka.
1. Možete odabrati broj aktivnosti i ažurirati kategoriju projekta i svojstvo retka.
1. Knjiženje fakture dobavljača na čekanju. Kad je faktura proknjižena, sustav evidentira sljedeće podatke:
    
    - Iznos salda dobavljača.
    - Iznos poreza na promet.
    - Trošak u odnosu na projekt evidentira se na račun integracije nabave.
    - Transakcija stvarnih troškova projekta u aplikaciji Dataverse.  Ova se transakcija dalje obrađuje s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md). Knjiženjem ovog dnevnika premješta se iznos s računa integracije nabave na račun troškova projekta. 
    - Kupnje koje se klijentu projekta naplaćuju s pomoću metode naplate vremena i materijala. Osim toga, u aplikaciji Dataverse stvaraju se neplaćene prodajne transakcije za kupnje. Cjenik proizvoda u aplikaciji Dataverse upotrebljava se za prodajne cijene i iznose za nenaplaćene prodajne transakcije.
