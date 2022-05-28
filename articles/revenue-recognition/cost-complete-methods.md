---
title: Načini troška za završetak
description: U ovoj temi nalaze se informacije o načinima s pomoću kojih se izračunava trošak za završetak projekta.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 244afa919e5fbc16be8f905acce2e2354c7da974
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601653"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]