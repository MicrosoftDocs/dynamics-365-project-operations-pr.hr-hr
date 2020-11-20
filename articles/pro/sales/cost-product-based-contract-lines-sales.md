---
title: Cijena redaka ugovora koji se temelje na proizvodu – osnovna
description: Ova tema pruža informacije o stvaranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177232"
---
# <a name="cost-product-based-contract-lines---lite"></a>Cijena redaka ugovora koji se temelje na proizvodu – osnovna

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Redci ugovora koji se temelje na proizvodima u aplikaciji Dynamics 365 Project Operations uključuju polje **Cijena troška** u kojem je pohranjena cijena troška proizvoda za izračun nizvodne profitabilnosti.

Kada se za kataloški proizvod stvara redak ugovora koji se temelji na proizvodu, cijenu retka ugovora koji se temelji na proizvodu zadaje polje **Standardna cijena** iz kataloga proizvoda. Polje **Standardna cijena** u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove. Kada je jedinična cijena zadana retku ugovora, pretvara se u valutu prodaje u ugovoru.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jedinična cijena u retku ugovora koji se temelji na proizvodu

Postojanje jedinične cijene u retku ugovora koji se temelji na proizvodu omogućuje različite cijene proizvoda za svaku prodaju jedinice. Iako nisu uvijek nužni, postoje određeni scenariji u kojima dobavljač može klijentu sniziti troškove proizvoda. Razmotrite sljedeći scenarij:

Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum. Fabrikam pruža usluge ugradnje, ali robotske ruke nabavljaju se od tvrtke Trey Research. Ako instalacija robotskih ruku u tvrtki Adatum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey Research, za ovaj bi se posao mogao odobriti poseban popust tvrtki Fabrikam. U tom slučaju, Fabrikam stvara redak ugovora koji se temelji na proizvodu za tvrtku Robotic Arms i za taj ugovor unosi jediničnu cijenu koja se razlikuje od standardnih cijena robotskih ruku tvrtke Trey Research.
