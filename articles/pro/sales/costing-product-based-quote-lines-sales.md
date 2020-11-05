---
title: Određivanje cijene redaka ponude utemeljenih na proizvodu
description: U ovoj temi nalaze se informacije o primjeni cijene koštanja na redak ponude koji se temelji na proizvodu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073291"
---
# <a name="costing-product-based-quote-lines"></a>Određivanje cijene redaka ponude utemeljenih na proizvodu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_


Redci ponude koji se temelje na proizvodu u programu Dynamics 365 Project Operations također imaju polje **Cijena koštanja**. To se polje upotrebljava za praćenje cijene koštanja proizvoda na retku ponude i za izračun profitabilnosti na nižim razinama.

Kada se za kataloški proizvod stvara redak ponude koji se temelji na proizvodu, cijenu retka ponude koji se temelji na proizvodu zadaje polje **Standardni trošak** iz kataloga proizvoda. Polje standardnih troškova u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove. Zadani jedinični trošak u retku ponude koji se temelji na proizvodu pretvara se u valutu prodaje na ponudi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Jedinična cijena u retku ponude utemeljenom na proizvodu

Svrha jediničnog troška u retku ponude koji se temelji na proizvodu jest omogućivanje različitih troškova proizvoda za svaku prodaju. To nije uobičajen scenarij, ali dobavljač ponekad može sniziti cijenu proizvoda ovisno o krajnjem kupcu.

Na primjer:

Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum. Fabrikam pruža usluge ugradnje, ali robotske ruke nabavljaju se od tvrtke Trey robotics. Ako instalacija robotskih ruku u tvrtki A Datum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey, Trey bi mogao dati poseban popust za ovaj posao tvrtki Fabrikam.

U ovom slučaju, Fabrikam će stvoriti redak ponude koji se temelji na proizvodu za robotske ruke i unijeti posebnu jediničnu cijenu za ovu ponudu. Ta cijena razlikuje se od standardne cijene tvrtke Trey Robotic Arms.
