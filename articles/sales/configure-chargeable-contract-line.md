---
title: Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu
description: U ovoj temi nalaze se informacije o uključenim komponentama koje se naplaćuju i onima koje se ne naplaćuju na redcima ugovora.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d6f67d5dc6b94148d437b3399229c1235c702c6a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128679"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Redak ugovora koji se temelji na projektu ima koncept uključenih, naplativih i nenaplativih komponenti.

Uključene komponente podliježu načinu naplate, podjelama klijenta, ograničenjima koja ne smiju premašiti i postavkama učestalosti računa definiranim na retku ugovora koji se temelji na projektu.

Podskup uključenih komponenti može se označiti kao naplativ ažuriranjem polja **Vrsta naplate**.

Komponente koje se naplaćuju mogu se definirati u ulogama i kategorijama transakcija.

Za redak ugovora o projektu, naplata definirana u ulozi odnosi se samo na klasu transakcije **Vrijeme**. Ako je postavka **Uključi vrijeme** postavljena na **Ne** na retku ugovora o projektu, kartica **Naplative uloge** nije dostupna.

Mogućnost naplate definirana je u kategorijama transakcije za redak ugovora o projektu i primjenjuje se samo na klasu transakcije **Trošak**. Ako je postavka **Uključi troškove** postavljena na **Ne** na retku ugovora o projektu, kartica **Naplative kategorije** nije dostupna.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažuriranje uloge kako bi bila naplativa ili nenaplativa

Uloga može biti naplativa ili nenaplativa na određenom retku ugovora koji se temelji na projektu.

Na kartici **Naplative uloge** retka ugovora koji se temelji na projektu, na podrešetki **Naplative kategorije**, u polju **Vrsta naplate**, ažurirajte vrstu naplate za ulogu.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažuriranje kategorije transakcije kako bi bila naplativa ili nenaplativa

Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ugovora koji se temelji na projektu.

Na kartici **Naplative kategorije** retka ugovora koji se temelji na projektu, na podrešetki **Naplative kategorije**, u polju **Vrsta naplate**, ažurirajte vrstu naplate za transakciju.

### <a name="resolve-chargeability"></a>Rješavanje naplativosti

Procijenjeno ili stvarno stvoreno vrijeme smatrat će se naplativima samo ako je vrijeme uključeno u redak ugovora i ako je uloga konfigurirana kao naplativa u retku ugovora.

Procijenjeni ili stvarno stvoreni troškovi smatrat će se naplativima samo ako je trošak uključen u redak ugovora i ako je kategorija transakcije konfigurirana kao naplativa u retku ugovora.

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