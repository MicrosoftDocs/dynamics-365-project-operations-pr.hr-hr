---
title: Faze projekta
description: Ova tema pruža informacije o fazama projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750099"
---
# <a name="project-stages"></a>Faze projekta 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faze projekta ažuriraju se kako bi odražavale napredak projekta. Zadani tijek poslovnog procesa automatski ažurira neke faze projekta dok druge faze ručno ažurira upravitelj projekta. 

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
