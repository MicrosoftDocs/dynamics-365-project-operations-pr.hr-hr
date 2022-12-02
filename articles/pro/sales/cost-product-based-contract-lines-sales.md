---
title: Cijena redaka ugovora koji se temelje na proizvodu – osnovna
description: U ovom se članku navode informacije o izradi
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922903"
---
# <a name="cost-product-based-contract-lines---lite"></a>Cijena redaka ugovora koji se temelje na proizvodu – osnovna

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Redci ugovora koji se temelje na proizvodu u aplikaciji Dynamics 365 Project Operations uključuju polje **Cijena koštanja**, u kojem je pohranjena cijena koštanja proizvoda za izračun profitabilnosti u daljnjem tijeku.

Kada se za proizvod iz kataloga stvori redak ugovora koji se temelji na proizvodu, cijenu u retku zadaje polje **Standardni trošak** iz kataloga proizvoda. Polje **Standardna cijena** u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove. Kada je jedinična cijena zadana retku ugovora, pretvara se u valutu prodaje u ugovoru.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jedinična cijena u retku ugovora koji se temelji na proizvodu

Postojanje jedinične cijene u retku ugovora koji se temelji na proizvodu omogućuje različite cijene proizvoda za svaku prodaju jedinice. Iako nisu uvijek nužni, postoje određeni scenariji u kojima dobavljač može klijentu sniziti troškove proizvoda. Razmotrite sljedeći scenarij:

Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum. Fabrikam pruža usluge ugradnje, ali je tvrtka Robotic arms u sastavu tvrtke Trey Research. Ako instalacija robotskih ruku u tvrtki Adatum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey Research, za ovaj bi se posao mogao odobriti poseban popust tvrtki Fabrikam. U ovom slučaju, Fabrikam stvara redak ugovora koji se temelji na proizvodu za tvrtku Robotic Arms. U ovaj ugovor unosi se trošak po jedinici. Cijena se razlikuje od cijene tvrtke Robotic arms koja je u sastavu tvrtke Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]