---
title: Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno
description: U ovom se članku nalaze informacije o postavljanju troškova i prodajnih stopa za artikle u katalogu proizvoda.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917383"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Postavljanje cijena za stavke iz kataloga proizvoda u aplikaciji Dynamics 365 Project Operations isto je kao i u aplikaciji Dynamics 365 Sales.

Budući da se proizvodi ne mogu procijeniti ili upotrijebiti na projektima u aplikaciji Project Operations, nije potrebno postavljati cijene proizvoda iz kataloga na cjenike za projekt za ponude i ugovore.

Upotrijebite polje **Cijena proizvoda** ponude, ugovora ili računa kako biste postavili cijena proizvoda iz kataloga. Nemojte postavljati cijene proizvoda iz kataloga u cjenike za projekt. Cjenici za projekt ekskluzivni su za aplikaciju Project Operations. Poslovna logika specifična za aplikaciju kopira cjenike iz ponude u ugovor. Rezultat je cjenik projekta specifičan za ugovor. Operacija kopiranja može odgoditi postupak usvajanja ponude ako cjenik za projekt na ponudi postane prevelik. Cjenici proizvoda ne kopiraju se kako bi stvorili prilagođene cjenike u ugovorima. Budući da nije uključeno kopiranje, to ne utječe na izvedbu postupka ponude.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]