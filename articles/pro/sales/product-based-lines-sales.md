---
title: Redci prilike koji se temelje na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o stavkama retka prilike koji se temelji na proizvodu u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764945"
---
# <a name="product-based-opportunity-lines---lite"></a>Redci prilike koji se temelje na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Redci prilike koji se temelje na proizvodu stavke su retka u Prilici. Te se različite stavke redaka nalaze na konačnoj fakturi koja se daje klijentu. Faktura ne uključuje neke druge dodatne usluge. Povezani trošak i potrošnja ne prate se na zadacima bilo kojih povezanih projekata.

Redci koji se temelje na proizvodu mogu biti stavke iz kataloga ili proizvodi koji se upisuju. Većina funkcionalnosti na redcima prilike koji se temelje na proizvodu slijedi funkcionalnost koju pruža aplikacija Dynamics 365 Sales. Dodatne informacije o redcima prilike koji se temelje na proizvodima potražite u članku [Dodavanje proizvoda prilici](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

**Proračun klijenta** je koncept specifičan za retke prilika koji se temelje na projektu. Polje **Proračun klijenta** prati iznos koji je klijent spreman platiti za stavku.

Kada je metoda prihoda sažetka Prilike **Izračunao sustav**, vrijednosti proračuna klijenta u redcima prilika zbrojene su kako bi se izračunao procijenjeni prihod. 

