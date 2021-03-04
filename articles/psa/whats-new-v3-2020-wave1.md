---
title: Novosti ili promjene u aplikaciji Project Service Automation, verzija 3.x val 1 2020
description: Ova tema pruža informacije o tome što je novo i promijenjeno u aplikaciji Project Service Automation, verzija 3. val1, 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150929"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novosti ili promjene u aplikaciji Project Service Automation, verzija 3, val 1, 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Ova tema ističe ključna razmatranja nadogradnje pri prelasku na najnovije izdanje aplikacije Project Service Automation (PSA), verzije 3.x, val 1, 2020.

## <a name="time-entry"></a>Unos vremena
Prošireno je iskustvo unosa vremena kako bi se pružile mogućnosti produljenja unosa vremena u više scenarija klijenta. To uključuje mogućnost dodavanja vrsta unosa koji sada upravljaju određenim ponašanjem na temelju naziva sheme polja **Postavke vremenskog unosa**, prikazane kao **Vremenski izvor**. Novo rješenje, pod nazivom Vrijeme, Trošak, Određivanje statusa i Odobrenja (TESA) dodano je da podrži ovu funkciju.

### <a name="upgrade-consideration"></a>Razmatranja nadogradnje
Kako bi se podržala ova funkcionalnost, uloge unutar PSA ažurirane su i uključuju nove ovlasti. Te ovlasti omogućuju pristup za čitanje novog entiteta, **Postavke unosa vremena**.

Korisnicima koji trebaju mogućnost prijavljivanja vremena treba, osim postojećih uloga, dodijeliti korisničku ulogu **Korisnik unosa vremena**. Ova uloga uključuje novu funkcionalnost i osigurava nastavak rada vremenskog unosa.

Uz to, ako imate neki prilagođeni modul aplikacije koji uključuje sve obrasce za entitet za unos vremena, od vas će se zatražiti uklanjanje **Obrasca za brzo stvaranje unosa vremena TESA** iz modula.

### <a name="currently-extended-time-entry-changes"></a>Trenutačno proširene promjene vremenskog unosa
Kako bi se umanjio utjecaj trenutačnih korisnika vremenskog unosa, ova promjena uloge jedini je osnovni zahtjev koji je potreban za nastavak uporabe vremenskog unosa. Ako ste stvorili prilagođene prikaze ili zasebna iskustva unosa vremena, morate postaviti polja **Postavljanje unosa vremena** na ispravnu vrijednost PSA.
