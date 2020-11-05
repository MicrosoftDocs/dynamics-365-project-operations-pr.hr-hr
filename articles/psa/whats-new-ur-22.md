---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 22, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073336"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, izdanje ažuriranja 22, V3

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 22. Ova verzija ima broj međuverzije V 3.10.33.48 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.

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
- Rešetke za praćenje i procjene projekta prikazuju pogrešan kôd valute prodaje kada je ugovorena valuta različita od valute kupca, a tvrtka ili ustanova konfigurirana je za prikaz kodova valuta umjesto simbola valuta.
- Datum završetka člana Tima dodati će jedan dan ako je raspored sati rada 24 sata dnevno.
- U Projektnom rasporedu, dodavanje Transakcijske kategorije zadatku ne aktivira automatsko spremanje.
- Sljedeća greška prikazuje se tijekom dodavanja člana tima u predložak projekta: „Preduvjeti za resurse ne mogu se povezati s predlošcima projekta”. 
- Skripta pravila vrpce „msdyn.Approval.CanApproveOrReject” prikazuje pogrešku vremenskog ograničenja.

**Sales**

Popravljeni su sljedeći problemi:

- Poruka o pogrešci provjere ne prikazuje se kada je u pretraživanju cjenika na obrascu „Nova ponuda cjenika projekta” odabran cjenik.
- Zatvaranje prihvaćene ponude ne prelazi na stvoreni ugovor ako je BPF u prilogu ponude u završnoj fazi.
- Storniranje **Nenaplaćene prodaje** povezano je s izvornim troškom kad se opozove unos vremena.
- Nakon odabira gumba **Potvrdi** , status fakture se ne mijenja u **Potvrđen** sve dok se faktura ne osvježi.
