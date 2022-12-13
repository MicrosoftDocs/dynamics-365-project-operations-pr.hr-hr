---
title: Određivanje cijene redaka ponude utemeljenih na proizvodu
description: U ovom se članku navode informacije o primjeni cijene koštanja na redak ponude koji se temelji na proizvodu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825602"
---
# <a name="costing-product-based-quote-lines"></a>Određivanje cijene redaka ponude utemeljenih na proizvodu

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Redci ponude koji se temelje na proizvodu u aplikaciji Dynamics 365 Project Operations također imaju polje **Cijena koštanja**. To se polje upotrebljava za praćenje cijene koštanja proizvoda na retku ponude i za izračun profitabilnosti na nižim razinama.

Kada se za kataloški proizvod stvara redak ponude koji se temelji na proizvodu, cijenu retka ponude koji se temelji na proizvodu zadaje polje **Standardni trošak** iz kataloga proizvoda. Polje standardnih troškova u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove. Zadani jedinični trošak u retku ponude koji se temelji na proizvodu pretvara se u valutu prodaje na ponudi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Jedinična cijena u retku ponude utemeljenom na proizvodu

Svrha jediničnog troška u retku ponude koji se temelji na proizvodu jest omogućivanje različitih troškova proizvoda za svaku prodaju. To nije uobičajen scenarij, ali dobavljač ponekad može sniziti cijenu proizvoda ovisno o krajnjem klijentu.

Na primjer:

Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum. Fabrikam pruža usluge ugradnje, ali robotske ruke nabavljaju se od tvrtke Trey robotics. Ako instalacija robotskih ruku u tvrtki A Datum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey, Trey bi mogao dati poseban popust za ovaj posao tvrtki Fabrikam.

U ovom slučaju, Fabrikam će stvoriti redak ponude koji se temelji na proizvodu za robotske ruke i unijeti posebnu jediničnu cijenu za ovu ponudu. Ta cijena razlikuje se od standardne cijene tvrtke Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
