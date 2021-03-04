---
title: Zašto je zadana cijena u u stvarnim podacima troškovi – prodaja nula?
description: Sljedeće tri provjere pomoći će vam utvrditi zašto je zadana cijena u stvarnim podacima troškovi – prodaja 0.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d4910d3727085a45036f3b438ecd69abc3e99836
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146294"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Zašto je zadana cijena u stvarnim podacima troškovi – prodaja nula?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ova se najčešća pitanja primjenjuju na stvarne troškove u slučajevima u kojima je klasa transakcije postavljena na Trošak, a vrsta transakcije je Nenaplaćena prodaja. Sljedeće tri provjere pomoći će vam utvrditi zašto je zadana cijena (stopa naplate) u stvarnim podacima troškovi – prodaja 0.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Provjera 1: identifikacija cjenika prodaje za projekt

Pronađite projekt iz polja Projekt stvarnih podataka i otvorite stranicu projekta. Zatim otvorite karticu Prodaja. Na rešetki Retci ugovora projekta kliknite vezu u polju Ugovor projekta. Otvorit će se stranica Ugovor projekta. Na stranici Ugovor o projektu otvorite karticu cjenici za projekt. Provjerite je li tu priložen barem jedan cjenik.

Ako rešetki Cjenici za projekt Ugovora o projektu nije priložen nijedan cjenik, učinite sljedeće:

- Priložite cjenik rešetki Cjenici za projekt. Da bi se cjenici mogli tu priložiti, njihovo polje konteksta mora biti postavljeno na Prodaja, a polje valute na cjeniku mora se podudarati s poljem valute na stranici Ugovor projekta. Nakon što izvršite potrebne popravke, ponovno stvorite unos troška, odobrite ga pa provjerite prikazuje li se valjana cijena za stvarnu nenaplaćenu prodaju.
- Ako ste rešetki Cjenici za projekt stranice Ugovora o projektu priložili jedan ili više cjenika, prijeđite na provjeru 2:

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Provjera 2: Je li ijedan od cjenika utvrđenih gore valjan za određeni datum iz stvarnih troškova?

Da bi servis Project Service pri postavljanju zadane cijene uzeo u obzir neki cjenik, taj cjenik mora biti primjenjiv za datum u stvarnim podacima troškovi – prodaja. Provjerite sljedeće da biste utvrdili jesu li cjenici utvrđeni gore primjenjivi:

- Najprije se uvjerite da polja datuma početka i završetka na kartici Općenito za priložene cjenike nisu prazna. Ako su polja datuma početka i završetka na cjenicima utvrđenima gore prazna, utvrdili ste problem. 
- Zabilježite polje datuma početka u stvarnim podacima troškovi – prodaja i provjerite je li ijedan od utvrđenih cjenika primjenjiv za taj datum. Na primjer, datum stvarnih troškova mora biti između datuma početka i datuma završetka na cjeniku. 
    - Ako nijedan cjenik ne pokriva taj datum u stvarnim podacima troškovi – prodaja, utvrdili ste problem. Izmijenite datume početka i završetka cjenika da biste osigurali da cjenik pokriva datum iz stvarnih troškova. 
    - Ako više od jednog cjenika pokriva taj datum u stvarnim podacima troškovi – prodaja, utvrdili ste problem. Uredite datume početka i završetka cjenika tako da samo jedan cjenik pokriva datum stvarnih troškova. 
    - Ako samo jedan cjenik pokriva taj datum iz stvarnih troškova, prijeđite na provjeru 3.
Nakon što dovršite potrebne popravke, ponovno stvorite unos troška, odobrite ga pa provjerite prikazuje li se valjana cijena za stvarnu nenaplaćenu prodaju.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Provjera 3: Postoji li valjana cijena za kategoriju troška na primjenjivom cjeniku projekta? 

Ako ste uspješno dovršili provjere 1 i 2, sada bi vam samo jedan cjenik projekta trebao biti primjenjiv za taj datum iz stvarnih vrijednosti troškovi – prodaja. Otvorite ovaj Cjenik projekta i otvorite karticu Cijene kategorije. Uvjerite se da rešetka sadrži redak za određenu kategoriju troška u stvarnim troškovima.
 
- Ako nema retka, utvrdili ste problem. Stvorite redak na rešetki Cijena kategorije za tu kategoriju u stvarnim troškovima. Zatim ponovno stvorite unos troška, odobrite ga pa provjerite prikazuje li se valjana cijena za stvarnu nenaplaćenu prodaju. 
- Ako na rešetki cijena kategorije postoji redak za kategoriju troška, provjerite ima li valjanu cijenu.

Da biste utvrdili koja je valjana cijena, upotrijebite sljedeće metode:

- Ako je vrijednost polja Način određivanja cijena u retku Cijena kategorije postavljena na Uz trošak, zadana jedinična cijena u vašim stvarnim podacima troškovi – prodaja bit će vrijednost u stavci Trošak.
- Ako je vrijednost polja Način određivanja cijena u retku Cijena kategorije postavljena na Postotak provizije, provjerite je li postavljena valjana vrijednost u polju Postotak. Zadana jedinična cijena u vašim stvarnim podacima troškovi – prodaja određuje se primjenom tog postotka provizije na cijenu u stavci Trošak.
- Ako je vrijednost polja Način određivanja cijena u retku Cijena kategorije postavljena na Cijena po jedinici, provjerite je li postavljena valjana vrijednost u polju Cijena. Zadana jedinična cijena u vašim stvarnim podacima troškovi – prodaja bit će iznos valute koji je naveden u polju Cijena.

Ako postavljanje cijene za kategoriju troška nije valjano, utvrdili ste problem. Rješenje je urediti redak cijene kategorije unošenjem valjane cijene za kategoriju troška u skladu s gornjim pravilima. Nakon što to učinite, ponovno stvorite unos troška, odobrite ga pa provjerite prima li stvarna nenaplaćena prodaja valjanu cijenu.

Ako se ni nakon tri gornje provjere i dalje ne prikazuje valjana cijena stvarnih troškova prodaje, prijavite problem službi za podršku.




[!INCLUDE[footer-include](../includes/footer-banner.md)]