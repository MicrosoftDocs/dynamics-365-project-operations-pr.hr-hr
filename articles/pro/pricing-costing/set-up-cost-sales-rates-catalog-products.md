---
title: Postavljanje troškova i prodajnih cijena za kataloške proizvode
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova i prodajnih cijena za stavke u katalogu proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073455"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Postavljanje troškova i prodajnih cijena za kataloške proizvode

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_


Postavljanje cijena za stavke kataloga proizvoda u aplikaciji Dynamics 365 Project Operations isto je kao i u aplikaciji Dynamics 365 Sales.

Budući da se proizvodi ne mogu procijeniti ili upotrijebiti na projektima u aplikaciji Project Operations, nije potrebno postavljati cijene kataloga proizvoda na cjenike projekata za ponude i ugovore.

Cijene kataloga proizvoda trebaju se postaviti u polje **Cijena proizvoda** ponude, ugovora ili računa. Nemojte postavljati cijene kataloga proizvoda u cjenike projekta za te entitete. Cjenici projekta ekskluzivni su za aplikaciju Project Operations. Postoji poslovna logika specifična za aplikaciju, koja cjenike kopira iz ponude u ugovor. Rezultat je cjenik projekta specifičan za ugovor. Operacija kopiranja može odgoditi postupak usvajanja ponude ako cjenik za projekt na ponudi postane prevelik. Cjenici proizvoda ne kopiraju se kako bi stvorili prilagođene cjenike u ugovorima. To znači da cjenici proizvoda ne utječu na učinkovitost postupka usvajanja ponude.
