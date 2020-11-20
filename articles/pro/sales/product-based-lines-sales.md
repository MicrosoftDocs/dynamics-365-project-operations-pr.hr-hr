---
title: Redci prilike koji se temelje na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o stavkama retka prilike koji se temelji na proizvodu u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176312"
---
# <a name="product-based-opportunity-lines---lite"></a>Redci prilike koji se temelje na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Redci prilike koji se temelje na proizvodu stavke su retka u Prilici. Ti se redci dostavljaju klijentu kao zasebne stavke retka na konačnom računu bez ikakvih drugih usluga s dodanom vrijednosti. Povezani trošak i potrošnja ne prate se na zadacima bilo kojih povezanih projekata.

Redci koji se temelje na proizvodu mogu biti stavke iz kataloga ili proizvodi koji se upisuju. Većina funkcionalnosti na redcima prilike koji se temelje na proizvodu slijedi funkcionalnost koju pruža aplikacija Dynamics 365 Sales. Dodatne informacije o redcima prilike koji se temelje na proizvodima potražite u članku [Dodavanje proizvoda prilici](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

Jedan koncept o redcima prilike koji se temelje na proizvodu koji je specifičan za priliku koja se temelji na projektu jest **Proračun klijenta**. Ovo polje upotrebljavajte za praćenje iznosa koji je klijent spreman platiti za stavku retka.

Ako je metoda prihoda sažetka Prilike postavljena na **Izračunao sustav**, proračunske vrijednosti klijenta u svim redcima koji se temelje na proizvodu i projektu sažete su kako bi se izračunao procijenjeni prihod.
