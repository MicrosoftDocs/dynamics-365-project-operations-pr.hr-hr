---
title: Konfiguriranje ploče rasporeda za prikaz ugovornih radnika i kooperantske sposobnosti
description: Ovaj tema opisuje kako konfigurirati Schedule Board u Dynamics 365 Project Operations Microsoftu za prikaz kooperantskog kapaciteta resursa prilikom osoblja u zahtjevima za resurse projekta.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903633"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfiguriranje ploče rasporeda za prikaz ugovornih radnika i kooperantske sposobnosti 

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Schedule Board u Dynamics 365 Project Operations Microsoftu može se koristiti za traženje resursa na dva načina:

- Opće pretraživanje resursa bez konteksta bilo kojeg specifičnog zahtjeva za resursima temeljenim na projektu.
- Pretraživanje resursa specifično za zahtjeve u kojima će zahtjev projekta pružiti kontekst za predložene resurse.

Da biste obavijestili odbor za raspored podugovorenog kapaciteta resursa i ugovornih radnika, morate ažurirati postavke odbora za planiranje rasporeda. Ta ažuriranja uključuju: 
- Ažurirajte postavke ploče rasporeda za opće pretraživanje resursa.
- Ažurirajte postavke ploče rasporeda za pretraživanje resursa utemeljeno na zahtjevima.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ažuriranje postavki ploče rasporeda za opće pretraživanje resursa
### <a name="update-filters-for-general-resource-search"></a>Ažuriranje filtara za opće pretraživanje resursa
Kada tražite resurs, filtre dostupne na ploči s rasporedom treba ažurirati tako da možete tražiti vanjske resurse navođenjem bilo kojeg ili svih sljedećih načina:
  - Vrsta radnika, trebaju li prikazani resursi biti ugovorni radnici ili zaposlenici.
  - Tvrtka dobavljač kojoj resurs treba pripadati.
  - Resursi koji pripadaju određenom retku kooperanta ili kooperanta.
    
### <a name="update-retrieve-resource-query"></a>Ažuriraj upit s dohvaćanjem resursa
Upit koji se koristi za pretraživanje također treba ažurirati kako bi se koristili ti dodatni atributi filtra. Da biste ažurirali konfiguraciju ploče rasporeda za opće pretraživanje resursa, slijedite ove korake:  
1. Otvorite **Postavke ploče** rasporeda za određenu ploču s rasporedom.
2. Otvorite **karticu Opće postavke** i pomaknite se do **odjeljka Ostale postavke**.
3. Na popisu postavki u ovom odjeljku **ažurirajte izgled filtra** na **Zadani izgled filtra za Operacije projekta Lite**.
4. Ažurirajte **upit dohvaćanja resursa** u **zadani upit dohvaćanja resursa za projektne operacije Lite**.

![Ažuriranje postavki ploče rasporeda za opće pretraživanje resursa](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ažuriranje postavki ploče rasporeda za pretraživanje resursa utemeljeno na zahtjevima
### <a name="update-filters-for-requirement-specific-resource-search"></a>Ažuriranje filtara za pretraživanje resursa specifično za zahtjev 
Kada tražite resurs, filtre dostupne na ploči s rasporedom treba ažurirati tako da možete tražiti vanjske resurse navođenjem bilo kojeg ili svih sljedećih načina:
 - Vrsta radnika, trebaju li prikazani resursi biti ugovorni radnici ili zaposlenici.
 - Tvrtka dobavljač kojoj resurs treba pripadati.
 - Resursi koji pripadaju određenom retku kooperanta ili kooperanta.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ažuriranje upita dohvaćanja resursa za pretraživanje resursa specifično za zahtjev 
Upit koji se koristi za pretraživanje također treba ažurirati kako bi se koristili ti dodatni atributi filtra. Da biste ažurirali konfiguraciju ploče s rasporedom za pretraživanje resursa utemeljeno na zahtjevima, slijedite ove korake:

1. Otvorite **Postavke ploče** rasporeda za određenu ploču s rasporedom, a zatim odaberite **Otvori zadane** postavke da biste otvorili postavke za pretraživanje specifično za zahtjev.
2. Otvorite **karticu Opće postavke** i pomaknite se do **odjeljka Ostale postavke**.
3. Na popisu postavki u ovom odjeljku **ažurirajte izgled filtra** na **Zadani izgled filtra za Operacije projekta Lite**.
4. Ažurirajte **upit dohvaćanja resursa** u **zadani upit dohvaćanja resursa za projektne operacije Lite**.
5. Otvorite **karticu Vrste rasporeda** i idite na **Project**.
6. Pod postavkama projekta ažurirajte Upit **za** **dohvaćanje resursa pomoćnika za planiranje** u **Zadani upit s resursima za dohvaćanje za projektne operacije Lite** i ažurirajte Upit ograničenja **dohvaćanja pomoćnika za planiranje** na **Zadani upit s ograničenjima dohvaćanja za projektne operacije Lite**.

![Ažuriranje postavki ploče rasporeda za pretraživanje resursa utemeljeno na zahtjevima](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
