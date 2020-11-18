---
title: Zadani cjenici
description: U ovoj temi nalaze se informacije o zadanim prodajnim cjenicima i cjenicima troškova u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073267"
---
# <a name="default-price-lists"></a>Zadani cjenici

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

## <a name="sales-price-lists"></a>Prodajni cjenici

Svaka ponuda i ugovor za projekt u aplikaciji Dynamics 365 Project Operations sadrži zadani prodajni cjenik. 

### <a name="price-list-default-on-project-quotes"></a>Zadani cjenik za ponude projekata
Sustav dovršava sljedeći postupak kako bi odredio koji će cjenik zadati za ponudu projekta:

1. Sustav pregledava cjenike koji su priloženi cjenicima projekta računa. 
2. Ako su uz zapis računa priloženi cjenici projekta, sustav pregledava prodajne cjenike priložene uz parametre projekta koji se podudaraju s valutom ponude projekta.
3. Nadalje, sustav provjerava mjerodavnost datuma cjenika koji se podudara s datumskim rasponom ponude projekta. Osobito datum kada je stvorena ponuda.
4. Ako postoji više cjenika koji vrijede za datum ponude projekta, za ponudu projekta zadani su svi cjenici.
5. Ako na datum ponude projekta nema cjenika koji su na snazi, za ponudu projekta ne postoji zadani cjenik projekata. Na ponudi projekta pojavit će se poruka upozorenja. U poruci se navodi kako, budući da nisu priloženi cjenici projekata, stvarni i procijenjeni podaci za projekt neće imati cijenu.

### <a name="price-list-default-on-project-contracts"></a>Zadani cjenik za ugovore o projektima 
Sustav dovršava sljedeći postupak kako bi odredio koji će cjenik zadati za ugovor o projektu:

1. Ako je ugovor izrađen iz ponude, cjenici projekta na ponudi zasebno se kopiraju i prilažu uz ugovor o projektu.
2. Ako se ugovor stvara od samog početka, sustav pregledava cjenike koji su priloženi cjenicima projekta računa. Ako uz zapis računa nisu priloženi cjenici projekta, sustav pregledava prodajne cjenike priložene uz parametre projekta koji se podudaraju s valutom ugovora o projektu.
4. Nadalje, sustav provjerava mjerodavnost datuma cjenika koji se podudara s datumskim rasponom ugovora o projektu. Osobito datum kada je stvoren ugovor.
5. Ako postoji više cjenika koji vrijede za datum ugovora, za ugovor su zadani svi cjenici.
6. Ako na datum ugovora nema cjenika koji su na snazi, za ugovor ne postoji zadani cjenik projekata. Na ugovoru o projektu pojavit će se poruka upozorenja. U poruci se navodi kako, budući da nisu priloženi cjenici projekata, stvarni i procijenjeni podaci za projekt neće imati cijenu.

## <a name="cost-price-lists"></a>Cjenici troškova

Cjenici troškova ne zadaju nijedan entitet u aplikaciji Project Operations. Utvrđivanje cjenika troškova koji će se upotrebljavati za troškove projekta uvijek se vrši u trenutku. Sustav dovršava sljedeći postupak kako bi odredio koji će cjenik upotrijebiti za troškove projekta:

1. Sustav prvo pregledava cjenike koji su priloženi ugovornoj organizacijskoj jedinici projekta.
2. Zatim sustav pregledava datum mjerodavnosti cjenika koji se podudaraju s datumom retka ulazne procjene ili stvarnih podataka. U ovoj situaciji *redak procjene* odnosi se na sva tri konteksta procjene u aplikaciji Project Operations:

    - Redak procjene projekta
    - Pojedinost retka ponude
    - Pojedinosti retka ugovora
  
3. Ako postoji više cjenika koji vrijede za datum na ulaznoj procjeni ili stvarnim podacima, odabire se najnoviji izrađeni cjenik.
4. Ako uz ugovornu organizacijsku jedinicu projekta nisu priloženi cjenici projekta, sustav pregledava cjenike troškova priložene uz parametre projekta koji se podudaraju s valutom ponude projekta.
5. Nadalje, sustav pregledava datum mjerodavnosti cjenika koji se podudaraju s datumom retka ulazne procjene ili stvarnih podataka. 
6. Ako postoji više cjenika koji vrijede za datum na ulaznoj procjeni ili stvarnim podacima, odabire se najnoviji izrađeni cjenik.
7. Ako uz parametre projekta nisu priloženi cjenici troškova koji se podudaraju s valutom i datumom stupanja na snagu, sustav za redak ulazne procjene ili stvarnog podatka zadaje cijene koštanja na nulu (0).