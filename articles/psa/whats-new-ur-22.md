---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 22, V3
description: Ovaj članak navodi značajke i ispravke dostupne u aplikaciji Project Service Automation, izdanje ažuriranja 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 733ee6e0d3583f21d0f58f9651920be3e3fd8cb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930631"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, izdanje ažuriranja 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku navode se značajke i ispravci koji su novi ili izmijenjeni u aplikaciji Project Service Automation V3, izdanje ažuriranja 22. Ova verzija ima broj međuverzije V 3.10.33.48 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.

## <a name="update-release-22"></a>Izdanje ažuriranja 22

### <a name="bug-fixes"></a>Ispravke pogrešaka



**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- **Vremenski unosi** ne dodaju se automatski u raspored vremenskih unosa nakon uvoza.
- Alat za odabir datuma rešetke **Vremenski unos** ne prepoznaje regionalne postavke korisnika.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:

- U ručnom načinu rada, promjene obrisa **Dodjela resursa** ne prepoznaju se pri generiranju mogućosti **Preduvjeti za resurse**.
- **Zahtjevi za resursima** ne podržavaju statuse prilagođenih zahtjeva.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- S pomoću dvostrukog klika na EstimateGridControl neće se pravilno raščlaniti brojevi holandskog formata.
- Zadani sati ne ažuriraju se ispravno kad se zadaci mijenjaju s pomoću dodatka za klijent radne površine aplikacije Microsoft Project.
- Rešetke za praćenje i procjene projekta prikazuju pogrešan kôd valute prodaje kada je ugovorena valuta različita od valute klijenta, a tvrtka ili ustanova konfigurirana je za prikaz kodova valuta umjesto simbola valuta.
- Datum završetka člana Tima dodati će jedan dan ako je raspored sati rada 24 sata dnevno.
- U Projektnom rasporedu, dodavanje Transakcijske kategorije zadatku ne aktivira automatsko spremanje.
- Sljedeća greška prikazuje se tijekom dodavanja člana tima u predložak projekta: „Preduvjeti za resurse ne mogu se povezati s predlošcima projekta”. 
- Skripta pravila vrpce „msdyn.Approval.CanApproveOrReject” prikazuje pogrešku vremenskog ograničenja.

**Sales**

Popravljeni su sljedeći problemi:

- Poruka o pogrešci provjere ne prikazuje se kada je u pretraživanju cjenika na obrascu „Nova ponuda cjenika projekta” odabran cjenik.
- Zatvaranje prihvaćene ponude ne prelazi na stvoreni ugovor ako je BPF u prilogu ponude u završnoj fazi.
- Storniranje **Nenaplaćene prodaje** povezano je s izvornim troškom kad se opozove unos vremena.
- Nakon odabira gumba **Potvrdi**, status fakture se ne mijenja u **Potvrđen** sve dok se faktura ne osvježi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
