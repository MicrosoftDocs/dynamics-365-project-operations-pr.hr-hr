---
title: Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova i prodajnih cijena za stavke u katalogu proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176692"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Postavljanje cijena za stavke kataloga proizvoda u aplikaciji Dynamics 365 Project Operations isto je kao i u aplikaciji Dynamics 365 Sales.

Budući da se proizvodi ne mogu procijeniti ili upotrijebiti na projektima u aplikaciji Project Operations, nije potrebno postavljati cijene kataloga proizvoda na cjenike za projekt za ponude i ugovore.

Cijene kataloga proizvoda trebaju se postaviti u polje **Cijena proizvoda** ponude, ugovora ili računa. Nemojte postavljati cijene kataloga proizvoda u cjenike za projekt za te entitete. Cjenici za projekt ekskluzivni su za aplikaciju Project Operations. Postoji poslovna logika specifična za aplikaciju, koja cjenike kopira iz ponude u ugovor. Rezultat je cjenik projekta specifičan za ugovor. Operacija kopiranja može odgoditi postupak usvajanja ponude ako cjenik za projekt na ponudi postane prevelik. Cjenici proizvoda ne kopiraju se kako bi stvorili prilagođene cjenike u ugovorima. To znači da cjenici proizvoda ne utječu na učinkovitost postupka usvajanja ponude.
