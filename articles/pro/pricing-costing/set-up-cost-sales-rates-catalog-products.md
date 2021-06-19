---
title: Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova i prodajnih cijena za stavke u katalogu proizvoda.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004305"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Postavljanje cijena za stavke iz kataloga proizvoda u aplikaciji Dynamics 365 Project Operations isto je kao i u aplikaciji Dynamics 365 Sales.

Budući da se proizvodi ne mogu procijeniti ili upotrijebiti na projektima u aplikaciji Project Operations, nije potrebno postavljati cijene proizvoda iz kataloga na cjenike za projekt za ponude i ugovore.

Upotrijebite polje **Cijena proizvoda** ponude, ugovora ili računa kako biste postavili cijena proizvoda iz kataloga. Nemojte postavljati cijene proizvoda iz kataloga u cjenike za projekt. Cjenici za projekt ekskluzivni su za aplikaciju Project Operations. Poslovna logika specifična za aplikaciju kopira cjenike iz ponude u ugovor. Rezultat je cjenik projekta specifičan za ugovor. Operacija kopiranja može odgoditi postupak usvajanja ponude ako cjenik za projekt na ponudi postane prevelik. Cjenici proizvoda ne kopiraju se kako bi stvorili prilagođene cjenike u ugovorima. Budući da nije uključeno kopiranje, to ne utječe na izvedbu postupka ponude.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]