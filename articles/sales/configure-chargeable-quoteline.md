---
title: Konfiguriranje naplative komponente retka ponude koji se temelji na projektu
description: U ovoj temi nalaze se informacije o uključenim, naplativim i nenaplativim komponentama u redcima ponude koji se temelje na projektu.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642534"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfiguriranje naplative komponente retka ponude koji se temelji na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Redak ponude koji se temelji na projektu može imati uključene komponente i naplative komponente.

Uključene komponente podliježu načinu naplate, podjelama kupca, ograničenjima koja se ne smiju prekoračiti i postavkama učestalosti računa definiranim u retku ponude koji se temelji na projektu.
Podskup uključenih komponenti može se označiti kao naplativ s pomoću stavke **Vrsta naplate**. Možete odabrati jednu od sljedećih mogućnosti u polju **Vrsta naplate** u kontekstu retka ponude:

   - Naplativo
   - Nenaplativo

Komponente koje se naplaćuju mogu se definirati u ulogama i kategorijama transakcija.

Naplativost koja je definirana u ulogama za redak ponude projekta odnosi se samo na klasu transakcije **Vrijeme**. Ako redak ponude projekta ima **Uključi vrijeme** = **Ne**, kartica **Naplative uloge** nije dostupna.

Naplativost koja je definirana u kategorijama transakcije za redak ponude projekta odnosi se samo na klasu transakcije **Trošak**. Ako redak ponude projekta ima **Uključi troškove** = **Ne**, kartica **Naplative kategorije** nije dostupna.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažuriranje uloge kako bi bila naplativa ili nenaplativa
U retku ponude koji se temelji na projektu uloga može biti naplativa ili nenaplativa. Vrsta naplate za ulogu može se konfigurirati na kartici **Naplative uloge** retka ponude koji se temelji na projektu. Kako biste to učinili, ažurirajte **Vrstu naplate** u podrešetki **Naplative uloge**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažuriranje kategorije transakcije kako bi bila naplativa ili nenaplativa
U retku ponude koji se temelji na projektu kategorija transakcije može biti naplativa ili nenaplativa. Vrsta naplate za transakciju može se konfigurirati na kartici **Naplative kategorije** retka ponude koji se temelji na projektu. Kako biste to učinili, ažurirajte polje **Vrsta naplate** u podrešetki **Naplative kategorije**. 

## <a name="resolve-chargeability"></a>Rješavanje naplativosti

Procjena ili stvarna vrijednost stvorena za vrijeme smatrat će se naplativom samo ako je vrijeme uključeno u redak ponude i ako je uloga konfigurirana kao naplativa.
Procjena ili stvarni podatak stvoren za trošak smatrat će se naplativim samo ako je trošak uključen u redak ponude i ako je kategorija transakcije u retku ponude konfigurirana kao naplativa. Sljedeća tablica prikazuje kako se naplativost zadaje za svaku stvarnu vrijednost. Zadane vrijednosti temelje se na uključenim komponentama i vrsti naplate koja je postavljena u retku ponude.

| Uključuje vrijeme | Uključuje trošak | Uloga | Kategorija | Zadatak |
| --- | --- | --- | --- | --- |
| Jest | Jest | Naplativo | Naplativo | Naplata za stvarno vrijeme: Naplativo </br>Vrsta naplate na stvarnom trošku: Naplativo |
| Jest | Jest | Nenaplativo | Naplativo | Naplata za stvarno vrijeme: Nenaplativo </br>Vrsta naplate na stvarnom trošku: Naplativo |
| Jest | Jest | Nenaplativo | Nenaplativo | Naplata za stvarno vrijeme: Nenaplativo </br>Vrsta naplate na stvarnom trošku: Nenaplativo |
| No | Jest | Nije moguće postaviti | Naplativo | Naplata za stvarno vrijeme: Nenaplativo </br>Vrsta naplate na stvarnom trošku: Naplativo |
| No | Jest | Nije moguće postaviti | Nenaplativo | Naplata za stvarno vrijeme: Nenaplativo </br>Vrsta naplate na stvarnom trošku: Nenaplativo |
| Jest | No | Naplativo | Nije moguće postaviti | Naplata za stvarno vrijeme: Naplativo </br>Vrsta naplate na stvarnom trošku: Nenaplativo |
| Jest | No | Nenaplativo | Nije moguće postaviti | Naplata za stvarno vrijeme: Nenaplativo </br> Vrsta naplate na stvarnom trošku: Nenaplativo |


[!INCLUDE[footer-include](../includes/footer-banner.md)]