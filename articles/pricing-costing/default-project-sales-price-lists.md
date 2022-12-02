---
title: Zadani cjenici
description: U ovom se članku navode informacije o zadanim prodajnim cjenicima i cjenicima troškova u aplikaciji Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410253"
---
# <a name="default-price-lists"></a>Zadani cjenici

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

## <a name="sales-price-lists"></a>Prodajni cjenici

Svaka projektna ponuda i ugovor u aplikaciji Dynamics 365 Project Operations sadrži zadani prodajni cjenik. 

### <a name="price-list-default-on-project-quotes"></a>Zadani cjenik za ponude projekata
Sustav dovršava sljedeći postupak kako bi odredio koji će cjenik zadati za ponudu projekta:

1. Sustav pregledava cjenike koji su priloženi cjenicima za projekt računa. 
1. Ako uz zapis računa nisu priloženi cjenici za projekt, sustav pregledava prodajne cjenike priložene uz parametre projekta koji se podudaraju s valutom ponude projekta.
1. Nadalje, sustav provjerava mjerodavnost datuma cjenika koji se podudara s datumskim rasponom ponude projekta. Osobito datum kada je stvorena ponuda.
1. Ako postoji više cjenika koji vrijede za datum ponude projekta, za ponudu projekta zadani su svi cjenici.
1. Ako na datum ponude projekta nema cjenika koji su na snazi, za ponudu projekta ne postoji zadani cjenik projekata. Na ponudi projekta pojavit će se poruka upozorenja. U poruci se navodi kako, budući da nisu priloženi cjenici za projekat, stvarni i procijenjeni podaci za projekt neće imati cijenu.

### <a name="price-list-default-on-project-contracts"></a>Zadani cjenik za ugovore o projektima 
Sustav dovršava sljedeći postupak kako bi odredio koji će cjenik zadati za ugovor o projektu:

1. Ako je ugovor izrađen iz ponude, cjenici za projekt na ponudi zasebno se kopiraju i prilažu uz ugovor o projektu.
1. Ako se ugovor stvara od samog početka, sustav pregledava cjenike koji su priloženi cjenicima za projekt računa. Ako uz zapis računa nisu priloženi cjenici za projekt, sustav pregledava prodajne cjenike priložene uz parametre projekta koji se podudaraju s valutom ugovora o projektu.
1. Nadalje, sustav provjerava mjerodavnost datuma cjenika koji se podudara s datumskim rasponom ugovora o projektu. Osobito datum kada je stvoren ugovor.
1. Ako postoji više cjenika koji vrijede za datum ugovora, za ugovor su zadani svi cjenici.
1. Ako na datum ugovora nema cjenika koji su na snazi, za ugovor ne postoji zadani cjenik za projekt. Na ugovoru o projektu pojavit će se poruka upozorenja. U poruci se navodi kako, budući da nisu priloženi cjenici projekata, stvarni i procijenjeni podaci za projekt neće imati cijenu.

## <a name="cost-price-lists"></a>Cjenici troškova

Cjenici troškova ne zadaju nijedan entitet u aplikaciji Project Operations. Utvrđivanje cjenika troškova koji će se upotrebljavati za troškove projekta uvijek se vrši na osnovni pojedine transakcije. Sustav dovršava sljedeći postupak kako bi odredio koji će cjenik upotrijebiti za troškove projekta:

1. Sustav pregledava cjenike koji su priloženi ugovornoj organizacijskoj jedinici projekta.
1. Sustav potom pregledava datum stupanja na snagu cjenika koji se podudara s datumom konteksta ulazne procjene ili konteksta stvarnih podataka.

    - *Kontekst procjene* odnosi se na bilo koji od tri konteksta procjene u aplikaciji Project Operations:

        - Redak procjene projekta
        - Pojedinost retka ponude
        - Pojedinosti retka ugovora

    - *Kontekst stvarnog podatka* odnosi se na bilo koji od tri izvora stvarnih podataka u aplikaciji Project Operations:

       - Ručno izrađeni redci temeljnice ili redci dnevnika ispravaka izrađeni u dnevniku ispravaka
       - Redci u dnevniku izrađeni tijekom podnošenja zapisnika o vremenu, trošku ili utrošenom materijalu
       - Pojedinost retka fakture

    Kada aplikacija Project Operations pronađe podudaranje datuma stupanja na snagu dolaznog retka u dnevniku ili pojedinosti retka fakture u *kontekstu stvarnog podatka*, upotrebljava polje **Datum transakcije**.

    - Ako je za datum konteksta ulazne procjene ili konteksta stvarnog podatka na snazi više cjenika, odabire se najnovije izrađeni cjenik.
    - Ako uz ugovornu organizacijsku jedinicu projekta nisu priloženi cjenici projekta, sustav pregledava cjenike troškova priložene uz parametre projekta koji se podudaraju s valutom projekta.

## <a name="enable-multi-currency-cost-price-list"></a>Omogući cjenik troškova u više valuta

Ovu postavku možete pronaći u **Postavke** \> **Parametri**. Zadana je vrijednost **Ne**.

Kada je ova postavka omogućena (to jest, njena vrijednost postavljena na **Da**), sustav se ponaša na sljedeći način:

- Omogućuje povezivanje cjenika troškova u bilo kojoj valuti s organizacijskom jedinicom. Na primjer, cjenik troškova u valuti EUR može se priložiti organizacijskoj jedinici u valuti USD. Sustav će nastaviti provjeravati da cjenici troškova koji su priloženi organizacijskoj jedinici nemaju preklapajuće datume stupanja na snagu.
- Potvrđuje da cjenici troškova koji su priloženi projektnim parametrima nemaju preklapajuće datume stupanja na snagu, čak i ako imaju različite valute. Ovo se ponašanje razlikuje od zadanog ponašanja (to jest, ponašanja kada je vrijednost postavljena na **Ne**). U zadanom ponašanju, za datume stupanja na snagu koji se ne preklapaju potvrđuju se samo cjenici troškova koji imaju **istu** valutu.
- Za kontekst dolazne transakcije, određuje cjenik troškova isključivo na temelju datuma stupanja na snagu. Ovo se ponašanje razlikuje od zadanog ponašanja gdje sustav odabire cjenik troškova koji odgovara i valuti projekta i datumu stupanja na snagu.

Zbog ovih promjena ponašanja, klijenti koji se koristi aplikacijom Project Operations moći će održavati globalni cjenik troškova koji će biti relevantan za cijelu tvrtku. Neće morati imati cjenike u svakoj valuti poslovanja. Globalni cjenik imat će datum stupanja na snagu i omogućit će postavljanje stopa troškova u bilo kojoj valuti za određenu kombinaciju vrijednosti cjenovne veličine. Valuta cjenika troškova koristi se samo za unos zadanih vrijednosti kada se izrađuju zapisi stavki **Cijene uloga**, **Cijene kategorije** i **Cjenik**. Neće se koristiti za određivanje cjenika.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
