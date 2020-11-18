---
title: Zašto je zadana cijena nula u stvarnim vrijednostima vremena i prodaje?
description: Rješavanje problema zbog kojeg je zadana cijena 0 u stvarnim vrijednostima vremena i prodaje.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c886c4a53b4ba47e381b891fe22a565ad8fd1ac6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073512"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Zašto je zadana cijena nula u stvarnim vrijednostima vremena i prodaje?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova se često postavljena pitanja primjenjuju na stvarne vrijednosti u slučajevima u kojima je razred transakcije postavljen na Vrijeme, a vrsta transakcije je Nenaplaćena prodaja. Sljedeće tri provjere pomoći će vam utvrditi zašto je zadana cijena (stopa naplate) 0 u stvarnim vrijednostima vremena i prodaje.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Provjera 1: identificiraj cjenik prodaje za projekt

Pronađite projekt u polju projekta stvarne vrijednosti i otvorite stranicu projekta. Zatim otvorite karticu Prodaja i na rešetki Reci ugovora projekta kliknite vezu u polju Ugovor projekta. Otvorit će se stranica projekta Ugovor. Na stranici projekta Ugovor, otvorite karticu Cjenici projekta. Provjerite je li tu priložen barem jedan cjenik. Ako rešetki Cjenici projekta stranice Ugovor projekta nije priložen nijedan cjenik, utvrdili ste problem. Priložite jedan cjenik rešetki Cjenici projekta. Da bi se cjenici mogli tu priložiti, njihovo polje konteksta mora biti postavljeno na Prodaja, a polje valute na cjeniku mora se podudarati s poljem valute na stranici Ugovor projekta. Nakon što ste izvršili potrebne popravke, ponovno izradite Unos vremena, odobrite ga pa provjerite prikazuje li se valjana cijena za stvarnu vrijednost nenaplaćene prodaje. 

Ako ste rešetki Cjenici projekta stranice Ugovor projekta priložili jedan ili više cjenika, prijeđite na sljedeću provjeru u dokumentu.

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
