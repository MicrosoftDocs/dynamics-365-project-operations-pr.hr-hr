---
title: Konfigurirajte ploču rasporeda tako da prikaže radnike po ugovoru i podugovorne kapacitete
description: U ovom se članku opisuje kako konfigurirati ploču za raspored u Microsoftu Dynamics 365 Project Operations tako da prikazuje kapacitet resursa kooperanta prilikom zapošljavanja potreba za resursima projekta.
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

Ploča za raspored u Microsoftu Dynamics 365 Project Operations može se koristiti za traženje resursa na dva načina:

- Pretraživanje općih resursa bez konteksta bilo kojeg specifičnog zahtjeva resursa temeljenog na projektu.
- Pretraživanje resursa specifično za zahtjev ako će zahtjev za projekt pružiti kontekst predloženih resursa.

Da biste obavijestili odbor za raspored o kapacitetu resursa i ugovornim radnicima, morate ažurirati postavke ploče za raspored. Ta ažuriranja uključuju: 
- Ažurirajte postavke rasporeda ploče za opće pretraživanje resursa.
- Ažurirajte postavke ploče za raspored za pretraživanje resursa temeljeno na zahtjevima.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ažuriraj postavke rasporeda ploče za opće pretraživanje resursa
### <a name="update-filters-for-general-resource-search"></a>Ažuriranje filtara za opće pretraživanje resursa
Kada tražite resurs, filtre dostupne na ploči za raspored trebalo bi ažurirati tako da možete tražiti i vanjske resurse navodeći nešto ili sve od sljedećeg:
  - Vrsta radnika, bez obzira na to trebaju li prikazani resursi biti ugovorni radnici ili zaposlenici.
  - Poduzeće dobavljača kojem bi resurs trebao pripadati.
  - Resursi koji pripadaju određenom retku podugovaranja ili podugovaranja.
    
### <a name="update-retrieve-resource-query"></a>Ažuriraj upit o dovršavanju resursa
Upit koji se koristi za pretraživanje također bi trebalo ažurirati kako bi se koristili ti dodatni atributi filtra. Da biste ažurirali konfiguraciju rasporeda ploče za opće pretraživanje resursa, slijedite ove korake:  
1. Otvorite **Postavke** ploče za raspored za određenu ploču za raspored.
2. Otvorite karticu **Opće postavke** i pomaknite se do **odjeljka Ostale postavke**.
3. Na popisu postavki u ovom odjeljku ažurirajte **izgled** filtra na **Zadani izgled filtra za Project Operations Lite**.
4. Ažuriraj upit **za dohvaćanje resursa** u **zadani upit o resursima za dohvaćanje za projektne operacije Lite**.

![Ažuriraj postavke rasporeda ploče za opće pretraživanje resursa](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ažuriraj postavke rasporeda ploče za pretraživanje resursa utemeljeno na zahtjevima
### <a name="update-filters-for-requirement-specific-resource-search"></a>Ažuriranje filtara za pretraživanje resursa specifičnih za zahtjeve 
Kada tražite resurs, filtre dostupne na ploči za raspored trebalo bi ažurirati tako da možete tražiti i vanjske resurse navodeći nešto ili sve od sljedećeg:
 - Vrsta radnika, bez obzira na to trebaju li prikazani resursi biti ugovorni radnici ili zaposlenici.
 - Poduzeće dobavljača kojem bi resurs trebao pripadati.
 - Resursi koji pripadaju određenom retku podugovaranja ili podugovaranja.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ažuriranje upita dohvata resursa za pretraživanje resursa specifičnog za zahtjev 
Upit koji se koristi za pretraživanje također bi trebalo ažurirati kako bi se koristili ti dodatni atributi filtra. Da biste ažurirali konfiguraciju rasporedske ploče za pretraživanje resursa utemeljeno na zahtjevima, slijedite ove korake:

1. Otvorite **Postavke** ploče za raspored za određenu ploču za raspored, a zatim odaberite **Otvori zadane postavke** da biste otvorili postavke za pretraživanje specifično za zahtjev.
2. Otvorite karticu **Opće postavke** i pomaknite se do **odjeljka Ostale postavke**.
3. Na popisu postavki u ovom odjeljku ažurirajte **izgled** filtra na **Zadani izgled filtra za Project Operations Lite**.
4. Ažuriraj upit **za dohvaćanje resursa** u **zadani upit o resursima za dohvaćanje za projektne operacije Lite**.
5. Otvorite karticu **Vrste rasporeda** i otvorite **Project**.
6. U postavkama za Project ažurirajte upit o dohvaćanju resursa pomoćnika za **planiranje na** zadani upit o resursima za dohvaćanje za projektne operacije Lite **i ažuriraj** upit Za uređivanje ograničenja pomoćnika za raspored u **zadani** upit za dohvaćanje ograničenja za Project Operations Lite **.** **·**

![Ažuriraj postavke rasporeda ploče za pretraživanje resursa utemeljeno na zahtjevima](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
