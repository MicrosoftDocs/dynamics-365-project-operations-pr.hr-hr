---
title: Novosti u travnju 2021. – osnovna implementacija rješenja Project Operations
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju osnovne implementacije rješenja Project Operations u travnju 2021. godine.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9498636d8c5f72b7544be4ec30f399d5e0311
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598111"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Novosti u travnju 2021. – osnovna implementacija rješenja Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations na verziji 4.9.0.221 okruženja platforme Dataverse 

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Materijali za projekte koji nisu na zalihama. Ključne mogućnosti uključuju:
  - Procjena i određivanje cijene materijala koji nije na zalihama tijekom prodajnog ciklusa za projekt. Dodatne informacije potražite u odjeljku [Postavljanje cijena koštanja i prodaje za kataloške proizvode – osnovno](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Praćenje uporabe materijala koji nisu na zalihama tijekom isporuke projekta. Dodatne informacije potražite u odjeljku [Bilježenje uporabe materijala na projektima i projektnim zadacima](../../material/material-usage-log.md).
  - Fakturiranje troškova za upotrijebljen materijal koji nije na zalihama. Dodatne informacije potražite u odjeljku [Upravljanje zaostalim naplatama – osnovno](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Novi API-ji u aplikaciji Dynamics 365 Dataverse omogućuju stvaranje, ažuriranje i brisanje operacija s pomoću značajke **Entiteta za planiranje**. Dodatne informacije potražite u odjeljku [Uporaba API-ja rasporeda za izvođenje operacija s pomoću entiteta planiranja](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2224568 | Dodana je logika za omogućivanje prilagodbi koje uključuju pozivanje dodatka za potvrdu računa. |
| Naplata i određivanje cijene | 2101098 | Poboljšana je logika zadanih polja predračuna: **Adresa naplate**, **Naziv naplate** i **Uvjeti plaćanja** sada se zadaju iz odgovarajućeg zapisa o klijentu u ugovoru o projektu. |
| Naplata i određivanje cijene | 2021413 | Ažurirana su polja **Stvarni trošak** i **Prodaja** na entitetu **Zadatak** kako bi uključivala prodajne vrijednosti iz nenaplaćene i naplaćene troškove za zadatke. |
| Naplata i određivanje cijene | 2182110 | Pri kopiranju ugovora o projektu, ID retka ugovora generira se u ugovoru o odredišnom projektu kako bi se osiguralo da je jedinstven. |
| Upravljanje prilikama | 2186741 | Dodane su provjere valjanosti kako bi se osiguralo da se polja **Podrijetlo** i **Vrsta transakcije** ne može ažurirati s postojećim pojedinostima retka ponude. |
| Upravljanje prilikama | 2191353 | Kontrole točke ne smiju se stvarati na retku ugovora za vrijeme i materijal. |
| Upravljanje prilikama | 2216956 | Ispravljeni problemi sa značajkom **Ažuriraj cijene**. |
| Planiranje i praćenje | 2182979 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje redaka procjene troškova s izvornog projekta. |
| Planiranje i praćenje | 2184144 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje naziva položaja resursa s izvornog projekta. |
| Planiranje i praćenje | 2184799 | Kopija projekta: Pooštrena je kontrola kako bi se osiguralo da se procijenjeni datum početka ne može promijeniti tijekom kopiranja. |
| Planiranje i praćenje | 2185134 | Kopija projekta: Predviđeni datum početka odredišnog projekta postavljen je na današnji datum. |
| Planiranje i praćenje | 2196373 | Kopija projekta: Osigurano je da se zapisi voditelja projekta i članova tima ne dupliciraju u projektnom timu. |
| Planiranje i praćenje | 2211833 | Kopija projekta: Zadaci resursa kopiraju se iz izvornog projektnog zadatka u odredišni projekt. |
| Planiranje i praćenje | 2186541 | Popravljeni su problemi u rešetki **Procjene** do kojih je dolazilo pri grupiranju po resursu. |
| Planiranje i praćenje | 2166906 | Kategorija transakcije iz zadatka mora se kopirati u entitet **Dodjela resursa**. |
| Upravljanje resursima | 2125362 | Ispravljeni su problemi do kojih je dolazilo tijekom stvaranja generičkog člana tima s pomoću načina raspodjele zasnovane na satima. |
| Vrijeme i trošak | 2113603 | Ispravljen je problem povezan s prilagodbom koji je uzrokovao uklanjanje atributa sa stranice **Vremenski unos**. Sustav sada provjerava postoji li atribut na stranici prije nego što im pristupi s pomoću skripte. |
| Vrijeme i trošak | 2204377 | Kopirane vremenske tablice moraju se automatski prikazati kada odaberete **Kopiraj tjedan** tijekom vremenskog unosa. |
| Vrijeme i trošak | 2209059 | Polje **Stanje** može se uređivati za vremenske unose u aplikaciji Dynamics 365 Field Service. |
