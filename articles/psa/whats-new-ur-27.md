---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 27, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 27, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ee7bbe888a982e3554ba524c67442437c9be9183a5ee0940ccc3261b4a4992e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985042"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 27. Broj izrade ove verzije jest V3.10.45.98, a ona je uglavnom dostupna putem samostalnog ažuriranja u siječnju 2021.

## <a name="update-release-27"></a>Izdanje ažuriranja 27

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Općenito**

Popravljeni su sljedeći problemi:

- Zapisnici generirani s pomoću dodataka u aplikaciji Project Service Automation nisu postavljeni na automatsko brisanje.
- Automatska nadogradnja ne uspijeva jer rješenje Project Service Automation sadrži naslijeđeni nulti NavBarArea i naslovni element.

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Rešetka **Unos vremena** prikazuje netočne podatke za ponašanje datuma **Neovisno o vremenskoj zoni** .
- Rešetka **Unos vremena** stvara netočno vrijeme za ponašanje datuma **Neovisno o vremenskoj zoni** .
- Traženje zadataka nije ograničeno na odabrani projekt na stranici **Uredi vremenski unos**.
- Odobrenje vremena za vremenske unose koji se ne odnose na projekt blokirano je jer sustav traži odobravatelja projekta.
- Ispravan unos u Stvarne podatke prikazuje neispravnu poruku o pogrešci.
- Kada zadatak sadrži nulu kao vrijednost stvarnog troška, a ukupni iznosi projekta se osvježavaju, dolazi do sljedeće pogreške „Dani ključ ne nalazi se u rječniku”.
- U određenim slučajevima, filtar **Grupiraj prema** na kartici **Procjena projekta** ne prikazuje procjene troškova.
- Interval **Ljetno računanje vremena** nije točan za vremenske unose.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Poboljšanja predmemoriranja, što poboljšava performanse povezane s učitavanjem stranice **Projekt**.
- Zastarjelo poslovno pravilo sprječava dovršavanje projektnih zadataka.
- Konture dodataka aplikacije Microsoft Project ne poštuju kalendar dodataka što rezultira netočnim zahtjevima za resursima.
- Stvaranje projekata iz predložaka pogrešno postavlja datume zadataka i sprječava mogućnost generiranja zahtjeva za resursima.
- Korisnik ne može pristupiti mogućnostima **Kategorija**, **Opis** i **Stanje** s pomoću tipkovnice.
- Stvarne prodajne vrijednosti projekta ne uključuju prodajne vrijednosti naknada i materijala.
- Zbrajanje stvarnih vrijednosti prodaje i troškova događa se pogrešno s različitim tečajevima.
- Opis u mogućnosti **Zadani predložak radnog** zavarava.
- Uvlačenje zadatka ne uklanja mogućnost **Kategorija** u korisničkom sučelju dok se ne osvježi.
- Nedostaje provjera valjanosti za osiguravanje premještanja projekta nakon njegova datuma završetka koje nije dopušteno.

**Sales**

Popravljeni su sljedeći problemi:

- Iznimka nulte reference generira se u retku ponude za projekt jer je **Uvoz iz procjene projekta** vidljiv kad projekt nije odabran.
- Sljedeća pogreška, „Referenca objekta nije postavljena na instancu objekta” događa se prilikom zatvaranja ponude kao **Dobivene**.
- Stanje prilagodbe nije postavljeno tijekom stvarnog storniranja za vrijeme dok se prekida veza s projektom iz retka ugovora.
- Kada su aplikacije Dynamics 365 Field Service i Project Service Automation instalirane, mogućnosti **Zaključaj cijene** i **Upotrijebi trenutačnu cijenu** ne prikazuju se istodobno na stranici **Faktura**.
- Za japanski jezik postoji nesklad prijevoda s ostalim stranicama koje se temelje na kalendaru.
- Mogućnosti **Aktiviraj** i **Deaktivira** uklonjene su iz entiteta **Povezani cjenici** u aplikaciji Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]