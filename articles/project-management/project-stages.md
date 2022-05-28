---
title: Faze projekta
description: U ovoj se temi nalaze informacije o fazama projekta koje su dostupne u aplikaciji Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a25f32badd8776c89ad6eb56ad77ff61ad0cccae
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586197"
---
# <a name="project-stages"></a>Faze projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Faze projekta dizajnirane su tako da odražavaju napredak projekta. Prilagodbe se mogu upotrebljavati za automatsko ažuriranje faza s tijekovima poslovnih procesa, uslugom Power Automate ili proširenjima dodataka.

Sljedeće su faze definirane u zadanom tijeku poslovnog procesa:

- Novo
- Ponuda
- Tarifa
- Dostavi
- Dovršeno
- Zatvaranje 

## <a name="new"></a>Novo

Kada stvorite projekt, faza projekta postavljena je na **Novo**. Ako je projekt stvoren na temelju predloška, možda sadrži raspored, procjenu i podatke o timu. U suprotnom, to je skica projekta, a preostale komponente moraju se unijeti.

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