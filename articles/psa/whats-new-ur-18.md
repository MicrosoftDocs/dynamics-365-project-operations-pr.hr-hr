---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 18, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073342"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, izdanje ažuriranja 18, V3

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 18. Ova verzija ima broj međuverzije V3.10.8.12 i uglavnom je dostupna putem samostalnog ažuriranja u travnju 2020. godine.

## <a name="update-release-18"></a>Izdanje ažuriranja 18

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

- Rješeno: Mogućnosti **Podsjetnik** , **Zahtjev** i **Otkaži odobrenje** odbacuju iznimke s nejasnim porukama o pogrešci.
- riješeno: Kada mogućnost **Otkaži odobrenje** ne uspije za trošak, relevantna se pogreška iznimke ne odbacuje.
- Riješeno: Rešetka vremenskog unosa pogrešno obrađuje neradne dane u Australiji nakon prebacivanja ljetnog računanja vremena (DST) u listopadu.
- Riješeno: Nepravilna zadana logika sprječava slanje troškova.
- Riješeno: Kad odobrenje unosa ne uspije, odobrenje ostaje u stanju **U tijeku**.
- Riješeno: SQL pogreške na skupnim odobrenjima (zastoj / vremensko ograničenje).
- Riješeno: Značajni problemi koje su korisnici imali s performansama uzrokovani su ažuriranjem članova tima tijekom odobravanja vremenskih unosa.

**Upravljanje projektom**

- Riješeno: Obavijest o vremenskoj zoni premještena je s prikaza **Usklađivanje** na glavni obrazac **Projekt**.
- Riješeno: Predložak kalendara nije se ispravno zadao kada se otvara novi obrazac projekta.
- Riješeno: Za preglednike koji se temelje na kromu korisnici ne mogu lako odabrati prethodne zadatke za brisanje.
- Riješeno: Stvaranje ili kopiranje mogućnosti **Projekt iz praznog predloška** dobiva nepovezane zadatke.
- Riješeno: U specifičnim rubnim slučajevima, stvaranje novog zadatka iz rešetke zadatka pravi dvostruke zapise.
- Riješeno: U ručnom načinu rada korisnici ne mogu ažurirati datume početka zadatka tako da budu kasniji od spremljenog trenutačnog datuma.

**Upravljanje resursima**

- Riješeno: Redak međuzbroja prikaza **Usklađivanje** pogrešno izračunava odstupanje rezervacije nakon produženja rezervacije.
- Rješeno: Prikaz mogućnosti **Usklađivanje** pogrešno prikazuje dodjele resursa kada resurs koji se može rezervirati ima kalendar koji se ne poklapa s kalendarom projekta.

**Sales**

- Riješeno: Kada se vremenski unosi ponovno odobre ( **Odobri > Odustani >** odobri ponovno), stvara se dvostruki nenaplativi trenutak.