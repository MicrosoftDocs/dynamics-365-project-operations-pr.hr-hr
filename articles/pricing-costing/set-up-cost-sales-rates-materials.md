---
title: Postavljanje cijena koštanja i prodaje za materijale
description: U ovoj temi nalaze se informacije o načinu postavljanja cijena troška i prodaje za materijale koji se upotrebljavaju na projektima.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1b1b679f15662d922804deefb6372adcdf4d4839
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576859"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Postavljanje cijena koštanja i prodaje za materijale

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Možete postaviti cijenu koštanja i prodaje za proizvode u aplikaciji Dynamics 365 Project Operations. Cijena koštanja i prodajne cijene proizvoda mogu se navesti samo u jednoj valuti, koja mora biti valuta u zaglavlju cjenika.

Kako biste postavili cijene koštanja i prodajne cijene proizvoda, poduzmite sljedeće korake. 

1. Idite na **Prodaja** > **Klijenti** > **Cjenici** i odaberite **Novi** za stvaranje novog cjenika. 
2. Na stavci **Stavke cjenika**, na izborniku podrešetke, odaberite **Nova stavka cjenika**. 
3. Na stranici **Brzo stvaranje** unesite proizvod i jedinicu za koje stvarate novu cijenu.

Dodatne informacije o definiranju cijena za stavke kataloga potražite u člancima [Definiranje određivanja cijena proizvoda cjenicima i stavkama cjenika](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) te [Decimalna preciznost u valuti i cijenama](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations ne podržava sve metode određivanja cijena za proizvode kao Dynamics 365 Sales. Jedini način određivanja cijena podržan za proizvode koji će se koristiti na projektima je *iznos valute*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
