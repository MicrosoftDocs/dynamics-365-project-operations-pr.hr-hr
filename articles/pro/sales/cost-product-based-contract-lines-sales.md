---
title: Cijena redaka ugovora koji se temelje na proizvodu – osnovna
description: Ova tema pruža informacije o stvaranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764450"
---
# <a name="cost-product-based-contract-lines---lite"></a>Cijena redaka ugovora koji se temelje na proizvodu – osnovna

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Redci ugovora koji se temelje na proizvodu u aplikaciji Dynamics 365 Project Operations uključuju polje **Cijena koštanja**, u kojem je pohranjena cijena koštanja proizvoda za izračun profitabilnosti u daljnjem tijeku.

Kada se za proizvod iz kataloga stvori redak ugovora koji se temelji na proizvodu, cijenu u retku zadaje polje **Standardni trošak** iz kataloga proizvoda. Polje **Standardna cijena** u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove. Kada je jedinična cijena zadana retku ugovora, pretvara se u valutu prodaje u ugovoru.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jedinična cijena u retku ugovora koji se temelji na proizvodu

Postojanje jedinične cijene u retku ugovora koji se temelji na proizvodu omogućuje različite cijene proizvoda za svaku prodaju jedinice. Iako nisu uvijek nužni, postoje određeni scenariji u kojima dobavljač može klijentu sniziti troškove proizvoda. Razmotrite sljedeći scenarij:

Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum. Fabrikam pruža usluge ugradnje, ali je tvrtka Robotic arms u sastavu tvrtke Trey Research. Ako instalacija robotskih ruku u tvrtki Adatum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey Research, za ovaj bi se posao mogao odobriti poseban popust tvrtki Fabrikam. U ovom slučaju, Fabrikam stvara redak ugovora koji se temelji na proizvodu za tvrtku Robotic Arms. U ovaj ugovor unosi se trošak po jedinici. Cijena se razlikuje od cijene tvrtke Robotic arms koja je u sastavu tvrtke Trey Research.
