---
title: Vrste faza projekta
description: Ova tema pruža informacije o fazama projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 521bf4b3090473a603626a99fded53906b644a7a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073439"
---
# <a name="project-stage-types"></a>Vrste faza projekta 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faze projekta dizajnirane su tako da odražavaju napredak projekta. Prilagodbe se mogu upotrebljavati za automatsko ažuriranje faza s tijekovima poslovnih procesa, uslugom Power Automate ili proširenjima dodataka.

Sljedeće su faze definirane u zadanom BPF-u:

- Novo
- Ponuda
- Plan
- Isporuka
- Dovršetak
- Zatvori 

## <a name="new"></a>Novo

Kada stvorite projekt, faza projekta postavljena je na **Novo**. Ako je projekt stvoren na temelju predloška, možda sadrži raspored, procjenu i podatke o timu. U suprotnom, to je samo skica projekta, a preostale komponente moraju se unijeti.

## <a name="quote"></a>Ponuda

Kada projekt povežete s projektom ili ponudom ili kada stvorite projekt na temelju ponude, faza projekta postavljena je na mogućnost **Ponuda** , a procijenjeni datumi početka i završetka ažuriraju se. Kada je projekt u fazi **Ponuda** , pojedinosti o ponudi prikazuju se na kartici **Prodaja** na stranici **Entitet projekta**.

## <a name="plan"></a>Plan

Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze **Ugovor** , faza projekta ažurira se na **Plan**. Kada je projekt u fazi **Plan** , stranica **Entitet projekta** prikazuje pojedinosti o ugovoru.

## <a name="deliver"></a>Isporuka

Kada se plan projekta dovrši i spremni ste započeti projekt, upravitelj projekta trebao bi ažurirati fazu projekta na **Isporuka** da bi se prikazalo da je projekt započeo.

## <a name="complete"></a>Dovršetak 

Kada se posao projekta dovrši, upravitelj projekta može ažurirati fazu na **Dovršetak**. Ažuriranjem faze projekta na **Dovršetak** upravitelj projekta označava da je rad 100 posto dovršen, no projekt ostaje otvoren kako bi se unosi vremena ili troškova na čekanju mogli zabilježiti.

## <a name="close"></a>Zatvori

Kada se zabilježe sve transakcije za projekt, upravitelj projekta može ažurirati fazu na **Zatvaranje**. U tom trenutku nije moguće bilježiti transakcije, a projekt je postavljen samo za čitanje.
