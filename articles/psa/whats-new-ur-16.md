---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 16, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 1f3bb4442ce1d06807f264003c930dbbee19a5c7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280884"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, izdanje ažuriranja 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.  Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje i ažuriranje željenog rješenja](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 16. Broj izrade ove verzije jest V3.10.6.34, a ona je uglavnom dostupna putem samostalnog ažuriranja u siječnju 2020.


## <a name="update-release-16"></a>Izdanje ažuriranja 16

### <a name="bug-fixes"></a>Ispravke pogrešaka

-   Vrijeme i trošak

    -   Popravljeno: Korisnici koji pokušavaju poslati izbrisane unose vremena i troškova za odobrenja sada će primati odgovarajuće poruke o pogrešci.

-   Upravljanje projektom

    -   Popravljeno: Obrasci koji se primjenjuju na novi projekt uvažavaju jedinice za resurse koje su u predlošcima definirane za članove tima.

    -   Popravljeno: Poboljšano rukovanje ponovnim dodjeljivanjem vlasništva nad zapisima.

    -   Popravljeno: Projekti koji su u fazi kopiranja neće se moći kopirati dok se ne dovrše sve radnje kopiranja.

-   Upravljanje resursima

    -   Popravljeno: Produžene rezervacije sada ispravno upravljaju kratkim periodima i više ne stvara nula sati za produžene rezervacije.

    -   Popravljeno: Prikaz usklađivanja sada se prikazuje kada je vremenska zona projekta +5:30 GMT, a vremenska zona korisnika je drugačija.

-   Sales

    -   Popravljeno: Kada se ukloni projekt mapiran na redak ugovora i mapira se novi projekt, stvarni zapisi o novom projektu nisu preispitani na temelju pravila za naplatu i cijenu definiranih u retku ugovora. To je popravljeno u ovom izdanju. Cijene i stvarni zapisi novomapiranog projekta poništit će se i ponovno ispravno stvoriti na temelju pravila o cijenama i naplatama iz retka ugovora. Stvarni zapisi projekta koji nije mapiran također će se preispitati i posljedično ponovno stvoriti.

    -   Popravljeno: Dodatna provjera dodana je polju **Iznos** retka procjene kako bi se osiguralo da se ne zadrže nulte vrijednosti.

    -   Popravljeno: Kada su u projektu ažurirani stvarni podaci, glavnom obrascu projekta dodaje se gumb za osvježavanje kako bi se korisnicima omogućilo da ponovno sinkroniziraju stvarne podatke.

    -   Popravljeno: Kada korisnici izvrše nadogradnju s verzije 2.X na verziju 3.X, za naziv projekta dopušteni su projekti s vrijednošću NULL.



[!INCLUDE[footer-include](../includes/footer-banner.md)]