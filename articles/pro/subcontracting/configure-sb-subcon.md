---
title: Konfigurirajte ploču rasporeda tako da prikaže radnike po ugovoru i podugovorne kapacitete
description: U ovom se članku opisuje kako konfigurirati ploču rasporeda u sustavu Microsoft Dynamics 365 Project Operations za prikaz kapaciteta podugovorenih resursa prilikom dodjeljivanja osoba prema zahtjevima za resursima projekta.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262207"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurirajte ploču rasporeda tako da prikaže radnike po ugovoru i podugovorne kapacitete 

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ploča rasporeda u sustavu Microsoft Dynamics 365 Project Operations može se koristiti za pretraživanje izvora na dva načina:

- Općenito pretraživanje resursa bez konteksta bilo kojeg specifičnog zahtjeva za resursima koji se temelji na projektu.
- Pretraživanje resursa specifičnog za zahtjev gdje će projektni zahtjev pružiti kontekst za predložene resurse.

Da biste obavijestili ploču rasporeda o kapacitetima podugovorenih resursa i ugovornim radnicima, trebate ažurirati postavke ploče rasporeda. Ta ažuriranja uključuju: 
- Ažurirajte postavke ploče rasporeda za općenito pretraživanje resursa.
- Ažurirajte postavke ploče rasporeda za pretraživanje resursa temeljno na zahtjevu.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ažuriranje postavki ploče rasporeda za općenito pretraživanje resursa
### <a name="update-filters-for-general-resource-search"></a>Ažuriranje filtara za općenito pretraživanje resursa
Kada tražite resurs, filtri dostupni na ploči rasporeda trebali bi se ažurirati tako da možete pretraživati i vanjske resurse navođenjem bilo kojeg ili svih od sljedećeg:
  - Vrsta radnika, trebaju li prikazani resursi biti ugovorni radnici ili zaposlenici.
  - Tvrtka dobavljača kojoj bi resurs trebao pripadati.
  - Resursi koji pripadaju određenom podugovoru ili retku podugovora.
    
### <a name="update-retrieve-resource-query"></a>Upit za ažuriranje dohvaćanja resursa
Upit koji se koristi za pretraživanje također treba ažurirati za korištenje ovih dodatnih atributa filtra. Slijedite sljedeće korake za ažuriranje konfiguracije ploče rasporeda za općenito pretraživanje resursa:  
1. Otvorite **Postavke ploče rasporeda** za određenu ploču rasporeda.
2. Otvorite karticu **Opće postavke** i pomaknite se do stavke **Ostale postavke**.
3. Na popisu postavki u ovom odjeljku ažurirajte postavku **Raspored filtra** na **Zadani izgled filtra za aplikaciju Project Operations Lite**.
4. Ažurirajte **Dohvati upit za resurse** na **Zadani upit za dohvaćanje resursa za aplikaciju Project Operations Lite**.

![Ažuriranje postavki ploče rasporeda za općenito pretraživanje resursa](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ažuriranje postavki ploče rasporeda za pretraživanje resursa temeljno na zahtjevu
### <a name="update-filters-for-requirement-specific-resource-search"></a>Ažuriranje filtara za općenito pretraživanje resursa 
Kada tražite resurs, filtri dostupni na ploči rasporeda trebali bi se ažurirati tako da možete pretraživati i vanjske resurse navođenjem bilo kojeg ili svih od sljedećeg:
 - Vrsta radnika, trebaju li prikazani resursi biti ugovorni radnici ili zaposlenici.
 - Tvrtka dobavljača kojoj bi resurs trebao pripadati.
 - Resursi koji pripadaju određenom podugovoru ili retku podugovora.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ažuriranje upita za dohvaćanje resursa za pretraživanje resursa temeljeno na zahtjevu 
Upit koji se koristi za pretraživanje također treba ažurirati za korištenje ovih dodatnih atributa filtra. Slijedite sljedeće korake za ažuriranje konfiguracije ploče rasporeda za pretraživanje resursa temeljeno na zahtjevu:

1. Otvorite **Postavke ploče rasporeda** za određenu ploču rasporeda, a zatim odaberite **Otvori zadane postavke** da biste otvorili postavke za pretraživanje temeljeno na zahtjevu.
2. Otvorite karticu **Opće postavke** i pomaknite se do stavke **Ostale postavke**.
3. Na popisu postavki u ovom odjeljku ažurirajte postavku **Raspored filtra** na **Zadani izgled filtra za aplikaciju Project Operations Lite**.
4. Ažurirajte **Dohvati upit za resurse** na **Zadani upit za dohvaćanje resursa za aplikaciju Project Operations Lite**.
5. Otvorite karticu **Vrste rasporeda** i idite na **Projekt**.
6. Pod postavkama za **Projekt**, stavku **Upit za dohvaćanje resursa pomoćnika za raspored** ažurirajte na **Zadani upit za dohvaćanje resursa za aplikaciju Project Operations Lite**, a stavku **Upit za dohvaćanje ograničenja pomoćnika za raspored** na **Zadani upit za dohvaćanje ograničenja za Project Operations**.

![Ažuriranje postavki ploče rasporeda za pretraživanje resursa temeljno na zahtjevu](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
