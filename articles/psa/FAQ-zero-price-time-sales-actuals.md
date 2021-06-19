---
title: Zašto je zadana cijena nula u stvarnim vrijednostima vremena i prodaje?
description: Rješavanje problema zbog kojeg je zadana cijena 0 u stvarnim vrijednostima vremena i prodaje.
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
ms.openlocfilehash: e32b4c8113afdc18d9b220b1a8daf5007be93ac8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011632"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Zašto je zadana cijena nula u stvarnim vrijednostima vremena i prodaje?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova se često postavljena pitanja primjenjuju na stvarne vrijednosti u slučajevima u kojima je razred transakcije postavljen na Vrijeme, a vrsta transakcije je Nenaplaćena prodaja. Sljedeće tri provjere pomoći će vam utvrditi zašto je zadana cijena (stopa naplate) 0 u stvarnim vrijednostima vremena i prodaje.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Provjera 1: identificiraj cjenik prodaje za projekt

Pronađite projekt u polju projekta stvarne vrijednosti i otvorite stranicu projekta. Zatim otvorite karticu Prodaja i na rešetki Reci ugovora projekta kliknite vezu u polju Ugovor projekta. Otvorit će se stranica projekta Ugovor. Na stranici Ugovor o projektu idite na karticu Cjenici za projekt. Provjerite je li tu priložen barem jedan cjenik. Ako rešetki Cjenici za projekt Ugovora o projektu nije priložen nijedan cjenik, utvrdili ste problem. Priložite cjenik rešetki Cjenici za projekt. Da bi se cjenici mogli tu priložiti, njihovo polje konteksta mora biti postavljeno na Prodaja, a polje valute na cjeniku mora se podudarati s poljem valute na stranici Ugovor projekta. Nakon što ste izvršili potrebne popravke, ponovno izradite Unos vremena, odobrite ga pa provjerite prikazuje li se valjana cijena za stvarnu vrijednost nenaplaćene prodaje. 

Ako ste rešetki Cjenici za projekt Ugovora o projektu priložili jedan ili više cjenika, prijeđite na sljedeću provjeru u dokumentu.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Provjera 2: Je li ijedan od cjenika koji su utvrđeni gore valjan za određeni datum stvarne vrijednosti vremena i prodaje?

Da bi program Project Service pri postavljanju zadane cijene uzeo u obzir neki cjenik, taj cjenik mora biti primjenjiv za datum na stvarnoj vrijednosti vremena i prodaje. Provjerite sljedeće da biste utvrdili jesu li cjenici utvrđeni gore primjenjivi:
- Uvjerite se da polja datuma početka i završetka na kartici Općenito za priložene cjenike nisu prazna. Ako su polja datuma početka i završetka na cjenicima utvrđenima gore prazna, utvrdili ste problem. 
- Zabilježite polje datuma početka na stvarnoj vrijednosti vremena i prodaje i provjerite je li ijedan od utvrđenih cjenika primjenjiv za taj datum. Na primjer, datum stvarne vrijednosti vremena i prodaje mora se nalaziti između datuma početka i datuma završetka na cjeniku. 
    - Ako nijedan cjenik ne pokriva taj datum na stvarnoj vrijednosti vremena i prodaje, utvrdili ste problem. Izmijenite datume početka i završetka cjenika da biste osigurali da cjenik pokriva datum stvarne vrijednosti vremena i prodaje. 
    - Ako više od jednog cjenika pokriva datum na stvarnoj vrijednosti vremena i prodaje, utvrdili ste problem. Taj problem možete riješiti uređivanjem datuma početka i završetka cjenika, tako da samo jedan cjenik pokriva datum stvarne vrijednosti vremena i prodaje. 
    - Ako samo jedan cjenik pokriva taj datum stvarne vrijednosti vremena i prodaje, idite na provjeru 3.
Nakon što ste izvršili potrebne popravke, ponovno izradite Unos vremena, odobrite ga pa provjerite prikazuje li stvarna vrijednost vremena i prodaje valjanu cijenu.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Provjera 3: Postoji li cijena na cjeniku za dimenzije određivanja cijena na stvarnoj vrijednosti vremena i prodaje?

Ako ste uspješno dovršili provjere 1 i 2, sada bi vam samo jedan cjenik trebao biti primjenjiv za datum stvarne vrijednosti vremena i prodaje. Otvorite ovaj Cjenik i navigirajte do kartice Cijene uloge. Provjerite sadrži li rešetka redak za dimenzije određivanja cijena na stvarnoj vrijednosti vremena i prodaje.

Ako rešetka cijena uloga ne sadrži redak za dimenzije određivanja cijena na stvarnoj vrijednosti vremena i prodaje, utvrdili ste problem. Na rešetki Cijene uloga izradite redak za dimenzije određivanja cijena na stvarnoj vrijednosti vremena i prodaje. Nakon što to izvršite, ponovno izradite Unos vremena, odobrite ga pa provjerite prikazuje li stvarna vrijednost vremena i prodaje valjanu cijenu.

Ako nakon tri gornje provjere na stvarnoj vrijednosti vremena i prodaje i dalje nije prikazana valjana cijena, prijavite problem službi za podršku. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]