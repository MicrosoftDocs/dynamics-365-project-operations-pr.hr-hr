---
title: Objavljivanje izvješća o izdatku
description: U ovom se članku objašnjava način knjiženja izvješća o troškovima.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524860"
---
# <a name="post-expense-reports"></a>Objavljivanje izvješća o izdatku

Nakon što se odobri izvješće o troškovima i prenese u opću temeljnicu, može se knjižiti. Kada objavite izvješće o troškovima, identificiraju se troškovi koji ispunjavaju uvjete za povrat poreza na dodanu vrijednost (PDV). Zadatak provjere i povrata plaćenog PDV-a dodjeljuje se zaposleniku koji je odgovoran za provjeru valjanosti izvješća o troškovima.

Ako se troškovima iz izvješća o troškovima tereti tvrtka koja nije tvrtka koja zapošljava zaposlenika, morate provjeriti valjanost i tvrtke koja duguje za te troškove i tvrtku kojoj se duguje. Na primjer, zaposlenik koji je predao izvješće o trošku radi za tvrtku DAT, ali je tvrtki DIR naplatio trošak. U ovom je slučaju DAT tvrtka kojoj se duguje trošak, a DIR tvrtka koja duguje za trošak. Nakon što provjerite valjanost ovih redaka temeljnice, retke troškova možete knjižiti u glavnu knjigu.

Kako biste knjižili izvješće o troškovima, na stranici **Odobrena izvješća o troškovima** odaberite izvješće o troškovima, a zatim na oknu radnji odaberite **Knjiži**.

Također možete istodobno knjižiti sva izvješća o troškovima na popisu. Odaberite sva izvješća o troškovima, a zatim odaberite **Knjiži**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Omogućivanje Mogućnosti knjiženja obveze troškova u valuti dobavljača za značajku gotovinskog načina plaćanja

Značajka **Mogućnost knjiženja obveza za troškove u valuti dobavljača za način gotovinskog plaćanja** omogućuje knjiženje izvješća o troškovima u valuti dobavljača za način gotovinskog plaćanja.

Kada podnosite gotovinske troškove, izvješća o troškovima trenutačno se knjiže u računovodstvenoj valuti. Zbog pretvorbe iznosa valute transakcije, obračunske valute i valute dobavljača dobavljačima se plaća netočan iznos ako su tečajevi na datum transakcije troška i stvarni datum plaćanja različiti.

Ova će značajka osigurati da se saldo dobavljača knjiži u valuti dobavljača kada se knjiži izvješće o troškovima.

1. Idite na **Radni prostori** \> **Upravljanje značajkama**.
2. Na popisu pronađite i odaberite **Mogućnost knjiženja obveza za troškove u valuti dobavljača za način gotovinskog plaćanja**, a zatim odaberite **Omogući sada**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
