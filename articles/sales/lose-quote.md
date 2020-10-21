---
title: Kopiranje ponuda koje se temelje na projektu
description: U ovoj temi nalaze se informacije o načinu kopiranja ponuda koje se temelje na projektu u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7234958d542dec4cba55cb0516f1222937389e1
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928551"
---
# <a name="copy-project-based-quotes"></a>Kopiranje ponuda koje se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Možete jednostavno stvoriti novu ponudu projekta kopiranjem postojeće. 

- Kako biste kopirali ponudu projekta, na stranici s popisom **Ponude projekata** ili stranici s pojedinostima **Ponude projekata**, odaberite ponudu projekta koju želite kopirati, a zatim odaberite **Kopiraj**.

Otvorit će se dijaloška stranica na kojoj možete unijeti parametre kopije. Sljedeća tablica navodi polja koja su uključena u dijalošku stranicu. Ovisno o odabranim vrijednostima, postupak kopiranja može se promijeniti.

| **Polje** | **Relevantnost, svrha i smjernice** | **Utjecaj na niže razine** |
| --- | --- | --- |
| Tema | Unesite odgovarajuću temu ili naziv ciljne ponude. Kad se otvori dijaloški okvir, sustav će ga postaviti na temu izvorne ponude sa stavkom **–kopija** dodanom uz njega. | |
| Potencijalni klijent | Upućivanje na zapis tvrtke ili računa klijenta. Kad se otvori dijaloški okvir, sustav će ga postaviti na račun na izvornoj ponudi. | Ovo je polje primarni klijent na ponudi. |
| Ugovorena jedinica | Organizacijska jedinica koja je odgovorna za isporuku projekata povezanih s ovim poslom.
Kad se otvori dijaloški okvir, sustav će ga postaviti na ugovornu jedinicu izvorne ponude. | Ugovorna jedinica odjel je tvrtke koji će izvršiti projekte nakon zaključenja posla. Svaka ugovorna jedinica ima valutu. Valuta se upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima koji su nastali tijekom izvršenja projekta. |
| Valuta | To je valuta u kojoj se transakcija posla obavlja. Kad se otvori dijaloški okvir, sustav će ga postaviti na valutu izvorne ponude. To se može izmijeniti, pa ako se izmijeni, polje **Kopiraj cijenu** uvijek se postavlja na **Ne**. To je zato što cjenici na izvornoj ponudi više nisu relevantni. | Valuta se upotrebljava za zadavanje cjenika, za izradu financijske procjene na ponudi i na kraju za fakturiranje klijentu kada je posao dobiven. |
| Zatraženi datum dostave | Ovo je datum isporuke koji je klijent zatražio. | Upotrebljava se kao datum završetka tijekom stvaranja datuma fakturiranja uz određenu učestalost. |
| Kopiranje cijena | Vrijednost Da/Ne označava treba li cijenu na ponudi kopirati iz izvorne ponude. | Ako se odabere **Da**, referentni cjenici projekta i proizvoda kopiraju se iz izvorne ponude u ciljanu ponudu. Ako se odabere **Ne**, cjenici se ponovno zadaju na temelju posljednjih cjenika koji su postavljeni na parametrima računa ili projekta. |

Kad odaberete **U redu** na dijaloškoj stranici, sustav stvara kopiju ponude projekta na temelju parametara odabranih u dijaloškom okviru. Otvara se nova ponuda projekta. 

> [!NOTE]
> Sljedeće se informacije ne kopiraju iz izvorne u ciljanu ponudu:
>
> - Rasporedi fakturiranja
> - Klijenti ponude i retka ponude
> - Referenca projekta na redcima ponude koji se temelje na projektima – Podaci o proračunu klijenta
>
>Budući da su ove informacije vrlo specifične za svaku ponudu, ta se polja i zapisi ne kopiraju. Kopiraju se redci ponude za projekte i proizvode, procjene pojedinosti redaka ponude i vrijednosti koje ne smiju premašiti na razini ponude. Zadane postavke cijene i troška ovise o mogućnosti **Kopiraj cijene** odabranoj na dijaloškoj stranici **Kopiraj parametre**.
