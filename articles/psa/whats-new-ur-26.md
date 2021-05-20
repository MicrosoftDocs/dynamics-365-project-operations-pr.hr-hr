---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 26, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948815"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, izdanje ažuriranja 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 26. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj izrade V3.10.44.59 i općenito je dostupna putem samostalnog ažuriranja u prosincu 2020.

## <a name="update-release-26"></a>Izdanje ažuriranja 26

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Korisnici mogu promijeniti zadatak na unosu vremena koji je odobren/poslan.
- Pogreška „Referenca objekta nije postavljena” prilikom spremanja unosa vremena.
- Uvoz unosa vremena iz zadataka resursa stvara unose vremena s netočnim vrijednostima DateTime.
- Kada su instalirane obje aplikacije, i Project Service Automation i Field Service, gumb **Novi** dvaput se prikazuje na naredbenoj traci za unose vremena u aplikaciji Field Service.
- Ažuriranje ćelija **Omogući jedinicu** i **Grupa jedinica** sada rade na rešetki **Procjene troškova**.
- Obrazac **Ažuriranje uređivanja unosa vremena** uključuje **Vremensku traku**.
- Odobrenje vremena za vremenske unose koji se ne odnose na projekt blokira sustav tijekom traženja uloge odobravatelja projekta.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:

- Dodana je provjera valjanosti u programski dodatak **PostProjectCreate** za provjeru primarnog zahtjeva prije stvaranja.
- Obrazac za brzo stvaranje **Član projektnog tima** izbacuje iznimku nulte vrijednosti reference ako se iz obrasca uklone polja.
- Generiranje zahtjeva za 12 sati tijekom jedne godine neće uspjeti.
- Poboljšana poruka o pogrešci za iznimku nulte vrijednosti reference tijekom stvaranja zahtjeva za resursom.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Poboljšana provjera valjanosti za rješavanje iznimke nulte vrijednosti reference generirane u programskom dodatku **PreProjectUpdate**.
- Projekti koje je objavio programski dodatak radnog područja aplikacije Microsoft Project brišu neraspoređene zadatke.
- Dodana je nova provjera valjanosti kada je referenca projekta zadatka nevaljana zbog iznimke nulte vrijednosti reference u programskom dodatku **PreValidateProjectTaskUpdate**.
- Rešetka člana tima ne prikazuje različite zadatke u zapisu člana tima.
- Dodane su nove provjere valjanosti i poruke o pogrešci zbog iznimke nulte vrijednosti reference u programskom dodatku **PreProjectTaskDelete**.

**Sales**

Popravljeni su sljedeći problemi:

- Pri odabiru retka koji se temelji na projektu u ponudi ili ugovoru, gumb **Prijedlog** bi trebao biti vidljiv samo pri odabiru retka koji se temelji na proizvodu povezanog s postojećim proizvodom.
- Razdvojite ovlast **Stvori_proizvod** od **Stvori_UgovoroProjektu**.
- Brisanje retka fakture uzrokuje neuspješnu vrijednost reference jednaku nuli na **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]