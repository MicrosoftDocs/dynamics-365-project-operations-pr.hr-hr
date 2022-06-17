---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 16, V3
description: U ovom se članku navode značajke i popravci dostupni u ažuriranju 16. izdanja automatizacije servisa project service update release 16, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926491"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, izdanje ažuriranja 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.  Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje i ažuriranje željenog rješenja](/dynamics365/project-service/upgrade-psa-home-page).
U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za PSA V3, Ažuriraj izdanje 16. Broj izrade ove verzije jest V3.10.6.34, a ona je uglavnom dostupna putem samostalnog ažuriranja u siječnju 2020.


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
