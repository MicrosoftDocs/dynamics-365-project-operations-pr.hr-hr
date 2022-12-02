---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 23, V3
description: Ovaj članak navodi značajke i ispravke dostupne u aplikaciji Project Service Automation, izdanje ažuriranja 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913020"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, izdanje ažuriranja 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku navode se značajke i ispravci koji su novi ili izmijenjeni u aplikaciji Project Service Automation V3, izdanje ažuriranja 23. Broj izrade ove verzije jest V 3.10.34.30, a ona je uglavnom dostupna putem samostalnog ažuriranja u kolovozu 2020.

## <a name="update-release-23"></a>Izdanje ažuriranja 23

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:
- Obradite rubni slučaj u mogućnosti **Izbriši člana projektnog tima** kako biste omogućili značajnu iznimku.
- Uvoz zadataka rezultira praznim zaslonom za uklanjanje.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:

- **Kartica resursa mreže za uporabu resursa** prikazuje netočne podatke kada je vremenska ljestvica dulja od pet dana.
- Kada klijenti stvarju resurs koji se može rezervirati, dodatak povremeno ne uspijeva automatski dodati resurs u grupu sustava Microsoft Office 365.
- Prikaz **Usklađivanje** pogrešno prikazuje ručne konture u prikazu **Tjedan** ili **Mjesec**.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Prekomjerni broj entiteta **Dohvati više za korisničke postavke** uzrokuju pogoršanje značajki za odobravanje projekata i ostalih operacija.
- Pretraživanje rešetke resursa **Planiranje zadataka** ograničen je na prikaz samo do pet članova iz projektnog tima. 
- Pretraživanje rešetke resursa **Planiranje zadataka** ne filtrira neaktivne resurse.
- Ručni način rada ne radi prema očekivanjima u strukturnoj analizi rada na planiranju projekta.
- Rešetka **Planiranje zadataka** prikazuje **Kategorije neaktivnih transakcija**.
- Rešetka **Dodjela resursa** pogrešno se zaokružuje kada projekt ima više zadataka.
- Vrijednosti zaokruživanja razlikuju se između planiranog i stvarnog troška za jedan zadatak.

**Sales**

Popravljeni su sljedeći problemi:

- Dvostrukim klikom mogućnosti **Dohvati sve kategorije transakcija** stvara se više redaka.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
