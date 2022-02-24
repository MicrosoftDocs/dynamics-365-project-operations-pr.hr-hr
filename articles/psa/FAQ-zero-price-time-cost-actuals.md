---
title: Zašto je zadana cijena u stvarnim podacima vrijeme – trošak nula?
description: Pronalaženje problema zbog kojeg je zadana cijena u stvarnim podacima vrijeme – trošak 0.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ffe915a48f088bde457121a323325ba490c24e45
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993047"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Zašto je zadana cijena u stvarnim podacima vrijeme – trošak nula?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova se najčešća pitanja primjenjuju na stvarne vrijednosti u slučajevima u kojima je klasa transakcije postavljena na Vrijeme, a vrsta transakcije je Trošak. Sljedeće tri provjere pomoći će vam utvrditi zašto je zadana cijena u stvarnim podacima vrijeme – trošak 0.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Provjera 1: identifikacija cjenika s cijenama koštanja za projekt

Pronađite projekt iz polja Projekt stvarnih podataka pa otvorite stranicu projekta. Kliknite vezu ugovorene jedinice u polju. Na stranici Ugovorena jedinica provjerite ima li ta ugovorena jedinica cjenik na rešetki Cjenici s cijenama koštanja.

Ako postoji više od jednog cjenika, utvrdili ste problem. Project Service podržava samo jedan cjenik po organizacijskoj jedinici. Uklonite sve cjenike iz tog entiteta dok rešetki Cjenici s cijenama koštanja organizacijske jedinice ne bude priložen samo jedan cjenik.

Ako toj organizacijskoj jedinici nije priložen nijedan cjenik, zabilježite koja je valuta te organizacijske jedinice. Idite na Project Service pa stavku Parametri pa otvorite karticu Cjenici. Provjerite nema li možda nijednog cjenika čiji je kontekst postavljen na Trošak, a valuta se podudara s valutom organizacijske jedinice.
 
Ako nijedan cjenik ne ispunjava te kriterije, utvrdili ste problem. Provjerite postoji li barem jedan cjenik čiji je kontekst postavljen na Trošak, a valuta se podudara s valutom ogranizacijske jedinice.

Ako više od jednog cjenika ispunjava te kriterije, nastavite čitati ovaj dokument da biste izvršili dodatne provjere.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Provjera 2: Je li ijedan od cjenika utvrđenih gore valjan za određeni datum u stvarnim podacima vrijeme – trošak?

Da bi servis Project Service pri postavljanju zadane cijene uzeo u obzir neki cjenik, taj cjenik mora biti primjenjiv za datum u stvarnim podacima vrijeme – trošak. Provjerite sljedeće da biste utvrdili jesu li cjenici utvrđeni gore primjenjivi:

- Uvjerite se da polja datuma početka i završetka na kartici Općenito za priložene cjenike nisu prazna. Ako su polja datuma početka i završetka na cjenicima utvrđenima gore prazna, utvrdili ste problem. 
- Zabilježite polje datuma početka u stvarnim podacima vrijeme – trošak i provjerite je li ijedan od utvrđenih cjenika primjenjiv za taj datum. Na primjer, datum u stvarnim podacima vrijeme – trošak mora biti između datuma početka i datuma završetka na cjeniku. 
    - Ako nijedan cjenik ne pokriva taj datum u stvarnim podacima vrijeme – trošak, utvrdili ste problem. Izmijenite datume početka i završetka cjenika da biste osigurali da cjenik pokriva datum iz stvarnih podataka vrijeme – trošak. 
    - Ako više od jednog cjenika pokriva datum iz stvarnih podataka vrijeme – trošak, utvrdili ste problem. Taj problem možete otkloniti tako da uredite datume početka i završetka cjenika tako da samo jedan cjenik pokriva datum iz stvarnih podataka vrijeme – trošak. 
    - Ako samo jedan cjenik pokriva taj datum iz stvarnh podataka vrijeme – trošak, prijeđite na sljedeću provjeru u dokumentu.
Nakon što dovršite potrebne popravke, ponovno stvorite Unos vremena, odobrite ga pa provjerite prikazuje li se valjana cijena u stvarnim podacima vrijeme – trošak.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Provjera 3: Postoji li cijena na cjeniku za dimenzije cijena u stvarnim podacima vrijeme – trošak?

Ako ste uspješno dovršili provjere 1 i 2, sada bi vam samo jedan cjenik trebao biti primjenjiv za taj datum u stvarnim podacima vrijeme – trošak. Otvorite ovaj Cjenik i otvorite karticu Cijene uloga. Uvjerite se da rešetka sadrži redak za dimenzije cijena u stvarnim podacima vrijeme – trošak.

Ako rešetka cijena uloga ne sadrži redak za dimenzije cijena u stvarnim podacima vrijeme – trošak, utvrdili ste problem. Na rešetki Cijene uloga stvorite redak za dimenzije cijena u stvarnim podacima vrijeme – trošak. Nakon što to dovršite, ponovno stvorite Unos vremena, odobrite ga pa provjerite prikazuje li se valjana cijena za stvarne podatke vrijeme – trošak.
 
Ako nakon tri gornje provjere u stvarnim podacima vrijeme – trošak i dalje nije prikazana valjana cijena, prijavite problem službi za podršku.





[!INCLUDE[footer-include](../includes/footer-banner.md)]