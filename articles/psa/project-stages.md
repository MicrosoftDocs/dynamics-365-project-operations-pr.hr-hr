---
title: Vrste faza projekta
description: Ova tema pruža informacije o fazama projekta.
author: ruhercul
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
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996877"
---
# <a name="project-stage-types"></a>Vrste faza projekta 

[!include [banner](../includes/psa-now-project-operations.md)]

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

Kada projekt povežete s projektom ili ponudom ili kada stvorite projekt na temelju ponude, faza projekta postavljena je na mogućnost **Ponuda**, a procijenjeni datumi početka i završetka ažuriraju se. Kada je projekt u fazi **Ponuda**, pojedinosti o ponudi prikazuju se na kartici **Prodaja** na stranici **Entitet projekta**.

## <a name="plan"></a>Plan

Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze **Ugovor**, faza projekta ažurira se na **Plan**. Kada je projekt u fazi **Plan**, stranica **Entitet projekta** prikazuje pojedinosti o ugovoru.

## <a name="deliver"></a>Isporuka

Kada se plan projekta dovrši i spremni ste započeti projekt, upravitelj projekta trebao bi ažurirati fazu projekta na **Isporuka** da bi se prikazalo da je projekt započeo.

## <a name="complete"></a>Dovršetak 

Kada se posao projekta dovrši, upravitelj projekta može ažurirati fazu na **Dovršetak**. Ažuriranjem faze projekta na **Dovršetak** upravitelj projekta označava da je rad 100 posto dovršen, no projekt ostaje otvoren kako bi se unosi vremena ili troškova na čekanju mogli zabilježiti.

## <a name="close"></a>Zatvori

Kada se zabilježe sve transakcije za projekt, upravitelj projekta može ažurirati fazu na **Zatvaranje**. U tom trenutku nije moguće bilježiti transakcije, a projekt je postavljen samo za čitanje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]