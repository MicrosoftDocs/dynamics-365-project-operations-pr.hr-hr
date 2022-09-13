---
title: Zadani cjenici
description: U ovom se članku nalaze informacije o zadanim cjenicima prodaje i troškova u operacijama projekta.
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
1. Ako zapisu računa nisu pridruženi cjenici projekta, sustav pregledava cjenike prodaje povezane s parametrima projekta koji odgovaraju valuti ponude projekta.
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

Cjenici troškova ne zadaju nijedan entitet u aplikaciji Project Operations. Određivanje cjenika troškova koji će se koristiti za troškove projekta uvijek se vrši po transakciji. Sustav dovršava sljedeći postupak kako bi odredio koji će cjenik upotrijebiti za troškove projekta:

1. Sustav pregledava cjenike koji su povezani s jedinicom ugovorne organizacije projekta.
1. Zatim sustav razmatra efektivnost datuma cjenika koji odgovaraju datumu konteksta dolazne procjene ili stvarnog konteksta.

    - *Kontekst* procjene odnosi se na bilo koji od tri konteksta procjene u projektnim operacijama:

        - Redak procjene projekta
        - Pojedinost retka ponude
        - Pojedinosti retka ugovora

    - *Stvarni kontekst* odnosi se na bilo koji od tri izvora za stvarne slučajeve u projektnim operacijama:

       - Reci temeljnice stavki koji su ručno kreirani ili reci temeljnice ispravaka kreirani u temeljnici ispravaka
       - Reci temeljnice kreirani tijekom slanja zapisnika o vremenu, troškovima ili korištenju materijala
       - Pojedinost retka fakture

    Kada operacije projekta podudaraju s efektivnošću datuma retka ulazne temeljnice ili retka fakture u *stvarnom kontekstu*, koristi **polje Datum** transakcije.

    - Ako više cjenika stupa na snagu za datum konteksta dolazne procjene ili stvarnog konteksta, odabire se posljednji kreirani cjenik.
    - Ako jedinici ugovorne organizacije projekta nisu priloženi cjenici, sustav pregledava cjenike troškova koji su povezani parametrima projekta koji odgovaraju valuti projekta.

## <a name="enable-multi-currency-cost-price-list"></a>Omogući cjenik troškova u više valuta

Ova postavka može se pronaći na Parametri **postavki** \> **·**. Zadana je vrijednost **Ne**.

Kada je ova postavka omogućena (to jest, vrijednost je postavljena na **Da**), sustav se ponaša na sljedeći način:

- Omogućuje da se cjenici troškova u bilo kojoj valuti povežu s organizacijskom jedinicom. Na primjer, cjenik troškova u valuti EUR može se priložiti organizacijskoj jedinici u valuti USD. Sustav će i dalje provjeravati da cjenici troškova koji su povezani s organizacijskom jedinicom nemaju preklapajuću efektivnost datuma.
- Potvrđuje da cjenici troškova koji su povezani s parametrima projekta nemaju preklapajuću efektivnost datuma, čak i ako imaju različite valute. Takvo se ponašanje razlikuje od zadanog ponašanja (to jest, ponašanja kada je vrijednost postavljena na **Ne**). U zadanom ponašanju provjeravaju se samo cjenici troškova koji imaju istu **valutu** za efektivnost datuma koja se ne preklapa.
- Za kontekst dolazne transakcije određuje cjenik troškova samo na temelju efektivnosti datuma. Takvo se ponašanje razlikuje od zadanog ponašanja, gdje sustav odabire cjenik troškova koji odgovara valuti projekta i efektivnosti datuma.

Zbog tih promjena u ponašanju, kupci Project Operationsa moći će održavati globalni cjenik troškova koji će biti relevantan za cijelu tvrtku. Neće morati imati cjenike u svakoj valuti poslovanja. Globalni cjenik imat će efektivnost datuma i omogućit će postavljanje stopa troškova u bilo kojoj valuti za određenu kombinaciju vrijednosti dimenzije određivanja cijena. Valuta cjenika troškova koristi se samo za unos zadanih vrijednosti kada **se kreiraju cijene** uloga, **cijene** kategorija i **zapisi stavki cjenika**. Neće se koristiti za određivanje cjenika.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
