---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 19, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143597"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, izdanje ažuriranja 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 19. Ova verzija ima broj međuverzije V3.10.30.41 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2020. godine.

## <a name="update-release-19"></a>Izdanje ažuriranja 19

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi: 

- Pogreške proizašle iz uvoza unosa vremena nisu se ispravno prikazale.
- Rešetka za unos vremena ne podržava ponašanje polja **Samo datum**.
- Resursi projekta ne mogu stvoriti trošak s pomoću projekta.

**Upravljanje projektom**

Popravljeni su sljedeći problemi: 

-  Zadatak podređenog uzrokuje pogrešnu procjenu napora tijekom dovršavanja (EAC) izračuna.

**Sales**

Popravljeni su sljedeći problemi: 

- Radnja **Ponovni izračun** ne funkcionira s pojedinostima retka ugovora o troškovima ili retka ponude.
- **Ažuriraj cijene** nedostaje za procjenu troškova.
-  Klijenti ne mogu odabrati razloge statusa prilagođenog ugovora na stranici **Ugovor o projektu**.
- Klijenti imaju smanjene performanse pri izradi prilagođenog cjenika iz ponude.
- Klijenti doživljavaju nedosljednost zadanih postavki **jedinice** na stranicama **Pojedinosti retka ponude** i **Pojedinosti retka ugovora**.
- Dodavanje stavki iz kategorije nenaplativih transakcija u naplativi redak ugovora neće poštovati vrstu naplate kategorije transakcije **Nenaplativo**.
- Klijenti ne mogu upotrijebiti novododane uloge i kategoriju na prethodno stvorenim ugovorima.
- Klijenti imaju smanjenu učinkovitost značajke Nepotrebno preuzimanje u PreValidateProjectTeamMemberUpdate.cs
- Uloge postavljene na popis **Kategorije resursa** kao nenaplative treba dodati na karticu **Naplative uloge** kao **Nenaplative** na retku ugovora za projekt.
- Klijenti mogu imati smanjene performanse pri stvaranju projekta jer **GetBookableResourceIdFromUser** dohvaća sve stupce resursa koji se mogu rezervirati, a ne samo primarnog ID-a.
- Entitetu **Vrsta transakcije** nedostaje dodatak za ažuriranje prethodne provjere valjanosti kako bi se spriječilo korisnike da uđu u **Jedinice** i **Grupe jedinica** koji nisu valjani za vrste transakcija.
- Korak **Ukloni** ne funkcionira za uvoz unosa vremena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]