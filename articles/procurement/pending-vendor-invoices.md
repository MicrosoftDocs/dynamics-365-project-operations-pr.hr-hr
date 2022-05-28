---
title: Kupnja nespremljenih materijala ili kategorija nabave pomoću fakture dobavljača na čekanju
description: U ovoj se temi objašnjava način bilježenja faktura dobavljača na čekanju.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612648"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Kupnja nespremljenih materijala ili kategorija nabave pomoću fakture dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Budući da tvrtka nabavlja ne-opskrbljene materijale ili kategorije nabave za projekt, troškovi se mogu odmah zabilježiti u odnosu na projekt. 

Na primjer, Contoso Robotics US izvršava projekt obnove opreme i potrebne su mu licence za softver. Te se licence nabavljaju od dobavljača koji je treća srana.  Koristeći Dynamics 365 Finance, službenik koji plaća račune bilježi dokument o fakturi dobavljača na čekanju i troškove licence pripisuje izravno projektu obnove opreme. 

> [!IMPORTANT]
> Prije nego što upotrijebite funkcionalnost opisanu u ovoj temi, pregledajte i primijenite potrebne konfiguracije. Dodatne informacije potražite u člancima [Omogućivanje nespremljenih materijala i faktura dobavljača na čekanju te](configure-materials-nonstocked.md) Korištenje kategorija nabave [s narudžbenicama za projekt i fakturama dobavljača na čekanju](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Knjiženje fakture dobavljača na čekanju povezane s projektom 

Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**). Poduzmite sljedeće korake za knjiženje fakture dobavljača na čekanju u vezi s projektom:

1. Otvorite Računi **koji se** > **plaćaju** i odaberite **Novo**. 
1. U polje Račun fakture **odaberite dobavljača, a zatim u** polje Broj **unesite identifikaciju fakture** dobavljača.
1. Dodajte redak fakturi dobavljača, a zatim u **polju Broj** artikla odaberite neutemeljeni artikl nabavljen od dobavljača. U polju Kategorija **Nabava** odaberite kategoriju nabave kupljenu od dobavljača.   
1. Dodajte količinu koja je kupljena. Sustav popunjava jediničnu cijenu na temelju konfiguracije cijena artikla koja nije opskrbljena. 
1. U retku provjerite ukupan iznos i ostale potrebne pojedinosti.
1. U detaljima retka na **kartici Projekt** odaberite ID projekta u koji će stavka biti zabilježena.
1. Neobavezno: Odaberite broj aktivnosti i ažurirajte kategoriju projekta i svojstvo retka.
1. Proknjižite fakturu dobavljača na čekanju. Kada se faktura proknjiži, sustav bilježi sljedeće podatke:
    
    - Iznos salda dobavljača.
    - Iznos poreza na promet.
    - Trošak u odnosu na projekt evidentira se na račun integracije nabave.
    - Transakcija stvarnih troškova projekta u aplikaciji Dataverse.  Ova se transakcija dalje obrađuje s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md). Knjiženjem ovog dnevnika premješta se iznos s računa integracije nabave na račun troškova projekta. 
    - Kupnje koje se klijentu projekta naplaćuju s pomoću metode naplate vremena i materijala. Osim toga, u aplikaciji Dataverse stvaraju se neplaćene prodajne transakcije za kupnje. Cjenik proizvoda u aplikaciji Dataverse upotrebljava se za prodajne cijene i iznose za nenaplaćene prodajne transakcije.
