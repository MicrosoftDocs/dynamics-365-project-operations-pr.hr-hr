---
title: Načini troška za završetak
description: U ovoj temi nalaze se informacije o načinima s pomoću kojih se izračunava trošak za završetak projekta.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531382"
---
# <a name="cost-to-complete-methods"></a>Načini troška za završetak

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o načinima s pomoću kojih se izračunava trošak za završetak projekta. Postoji više načina s pomoću kojih možete izračunati trošak za završetak projekta. 

Kada stvarate procjenu za projekt, na stranici **Stvori procjenu**, u polju **Način troška za završetak**, možete odabrati jedan od sljedećih načina troška za završetak.

| Način troška za završetak    | Opis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ukupni stvarni trošak            | Ručno unesite procjenu troškova u polja **Ukupni trošak** ili **Ukupna količina** s pomoću gumba **Procjena troška** na **Stranici procjene**. Sustav oduzima stvarne troškove od ukupnih unosa koje ste unijeli. Ukupni iznos je trošak za završetak projekta. Ovaj način ne upotrebljava procjene troškova i dodjele resursa koji su uneseni u aplikaciju Project Operations izgrađenu unutar aplikacije Microsoft Dataverse. Ukupni trošak ili ukupna količina mogu se po potrebi ažurirati ručno.  |
| Ukupno predviđanje – stvarno        | Dodjele resursa i procjene troškova upotrebljavaju se za određivanje ukupnog iznosa predviđenog za projekt. Stvarni se troškovi uspoređuju s ovim predviđanjem kako bi se izračunao trošak za dovršetak projekta.                                                                                                                                                                                                                                                                          |
| Kao prethodna procjena         | Ovdje se upotrebljavaju isti načini procjene koji su se ovdje upotrebljavali u prethodnom razdoblju. Za ovaj način potreban je model predviđanja ako je prethodno razdoblje zahtijevalo model predviđanja.                                                                                                                                                                                                                                                                                                                           |
| Postavljanje troška za završetak na nulu | Ovaj se način obično upotrebljava prije uklanjanja procjene projekta i podudara ukupne procjene s proknjiženim stvarnim transakcijama te briše stupac **Troškovi za završetak**. Kad se završi, rezultat je uvijek 100 posto. Za svaki redak troška koji stvarate, briše se potvrdni okvir **Predviđanje**, a ukupna se procjena kopira iz prethodne procjene troškova. Stvarna potrošnja za razdoblje procjene oduzima se od troška za završetak projekta.              |
| Iz predloška troška           | Način troškova za završetak koji je postavljen u predlošku troškova povezanom s odabranom procjenom projekta.                                                                                                                                                                                                                                                                                                                                                                          |
