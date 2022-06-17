---
title: Postavljanje cijena koštanja i prodaje za materijale
description: U ovom se članku navode informacije o postavljanju troškova i prodajnih stopa za materijale koji se koriste na projektima.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911771"
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
