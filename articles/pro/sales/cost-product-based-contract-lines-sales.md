---
title: Određivanje cijene redaka ugovora utemeljenih na proizvodu
description: Ova tema pruža informacije o stvaranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4073619"
---
# <a name="costing-product-based-contract-lines"></a>Određivanje cijene redaka ugovora utemeljenih na proizvodu

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_


Redci ugovora koji se temelje na proizvodima u aplikaciji Dynamics 365 Project Operations uključuju polje **Cijena troška** u kojem je pohranjena cijena troška proizvoda za izračun nizvodne profitabilnosti.

Kada se za kataloški proizvod stvara redak ugovora koji se temelji na proizvodu, cijenu retka ugovora koji se temelji na proizvodu zadaje polje **Standardna cijena** iz kataloga proizvoda. Polje **Standardna cijena** u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove. Kada je jedinična cijena zadana retku ugovora, pretvara se u valutu prodaje u ugovoru.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jedinična cijena u retku ugovora koji se temelji na proizvodu

Postojanje jedinične cijene u retku ugovora koji se temelji na proizvodu omogućuje različite cijene proizvoda za svaku prodaju jedinice. Iako nisu uvijek nužni, postoje određeni scenariji u kojima dobavljač može klijentu sniziti troškove proizvoda. Razmotrite sljedeći scenarij:

Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum. Fabrikam pruža usluge ugradnje, ali robotske ruke nabavljaju se od tvrtke Trey Research. Ako instalacija robotskih ruku u tvrtki Adatum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey Research, za ovaj bi se posao mogao odobriti poseban popust tvrtki Fabrikam. U tom slučaju, Fabrikam stvara redak ugovora koji se temelji na proizvodu za tvrtku Robotic Arms i za taj ugovor unosi jediničnu cijenu koja se razlikuje od standardnih cijena robotskih ruku tvrtke Trey Research.
