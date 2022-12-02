---
title: Najčešća pitanja o upravljanju resursima
description: Ovaj članak pruža odgovore na najčešća pitanja o upravljanju resursima.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 6610098737b79d76b38c3d467135b9118c2a8ec7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913335"
---
# <a name="resource-management-faq"></a>Najčešća pitanja o upravljanju resursima

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Koja je razlika između člana tima i preduvjeta resursa?

Član projektnog tima može se dodijeliti zadacima, biti rezerviran ili prekomjerno rezerviran te se postaviti kao odobravatelj. Preduvjet resursa može postojati bez člana projektnog tima, kao skica bilješke o potražnji. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Koja je razlika između predloženih i promjenjivo rezerviranih sati?

Predloženi sati i promjenjivo rezervirani sati razlikuju se u vidljivosti. Predloženi sati vidljivi su samo upraviteljima resursa i voditelju projekta koji je pokrenuo potražnju pomoću zahtjeva za resurs. Promjenjivo rezervirani sati vidljivi su svakome tko ima pristup ploči s rasporedom.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Kako mogu vidjeti promjenjivo rezervirane sate za resurse u timu?

Promjenjive rezervacije moguće su prilikom rezerviranja preduvjeta resursa. Resursi koji su promjenjivo rezervirani u projektnom timu prikazuju se kao članovi tima koji imaju promjenjivo rezervirane sate. Prikazuju se i na ploči s rasporedom.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Kako promijeniti potrebne sate te datume početka i završetka za resurs (generički ili imenovani) koji sam rezervirao?

Nakon što se resursi rezerviraju, odaberite **Zadrži rezervacije** da biste uveli sve potrebne promjene.

## <a name="what-resources-types-does-project-service-automation-support"></a>Koje vrste resursa podržava Project Service Automation?

**Korisnik** i **Kontakt** jedine su vrste resursa koje su podržane u aplikaciji Dynamics 365 Project Service Automation. Iako možete stvoriti druge vrste resursa (na primjer, **Oprema** i **Grupa**), za njih nije podržan nijedan slučaj sveobuhvatne upotrebe.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Koja je razlika između dodjele i rezervacije?

Dodjele predstavljaju dodjelu resursa zadacima projekta u rasporedu projekta. Resursi mogu biti pravi ili generički resursi. Rezervacije mogu imati fiksno ili promjenjivo dodjeljivanje resursa projektu. Fiksne rezervacije iskorištavaju kapacitet resursa. Rezervacije i dodjele za prave resurse trebale bi se podudarati jer se ne razlikuju. No u PSA-u to podudaranje nije obavezno. U prikazu Usklađivanje možete vidjeti mjesta voditelja projekta gdje se rezervacija i dodjele resursa ne podudaraju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
