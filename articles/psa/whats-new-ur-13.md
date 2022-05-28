---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 13, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 13, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: eb935d5bf3d2deb95db420f20a8102dae1864515
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596143"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation, izdanje ažuriranja 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 13. Broj izrade ove verzije jest V3.10.3.18, a ona je dostupna na sljedećem rasporedu:

- **Opća dostupnost (samostalno ažuriranje):** studeni 2019.
- **Automatsko ažuriranje:** prosinac 2019.


## <a name="update-release-13"></a>Izdanje ažuriranja 13 

### <a name="bug-fixes"></a>Ispravke pogrešaka

- Vrijeme i trošak

     - Popravljeno: Funkcionalnost pretraživanja na stranici **Odobravanje troška** ne radi tijekom pretraživanja po svrsi troška.

- Upravljanje resursima

     - Popravljeno: Brojevi u usklađivanju ažurirani su kako bi se ispravno poredali.
     - Popravljeno: Imenovani resursi ne mogu se dodijeliti zadacima putem kartice **Raspored**.

- Upravljanje projektom

     - Popravljeno: Iznimka nulte reference tijekom dodjeljivanja člana tima kada mogućnosti **VrstaTransakcije** nedostaje podataka o postavljanju za stavke **Jedinica** i **ZadanaGrupa**.

- Sales

     - Popravljeno: Dvostruki zapisi vrste transakcije vraćaju pogrešku kada se stvore zapisi o cijenama uloga.
     - Popravljeno: Dodatni gumbi za mogućnosti **Nova prilika**, **Ponuda**, **Redak narudžbe** i **Dodaj proizvod** vidljivi su u naredbama za Prilike, Ponude, Naručivanje proizvoda i podrešetki redaka koji se temelje na projektu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
