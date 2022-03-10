---
title: Novosti u svibnju 2021. – osnovna implementacija rješenja Project Operations
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju osnovne implementacije rješenja Project Operations u svibnju 2021. godine.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 14ff7f1f7374ffe885c511fd693cda5b7023c5beb53adb45042ddda1e932c93d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005967"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Novosti u svibnju 2021. – osnovna implementacija rješenja Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

   - Project Operations na verziji 4.10.0.186 okruženja platforme Dataverse.

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- [Načini planiranja](../../project-management/scheduling-modes.md): Voditelji projekata sada mogu definirati treba li projektom upravljati s pomoću fiksnog trajanja, fiksnog rada ili načina planiranja fiksnih jedinica.

## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2224568 | Dodana je logika za omogućivanje prilagodbi koje uključuju pozivanje dodatka za potvrdu računa. |
| Naplata i određivanje cijene | 2101098 | Poboljšana je logika zadanih polja za predračun. Ova polja obuhvaćaju **Adresa za naplatu**, **Ime/naziv onoga kome se naplaćuje** i **Uvjeti plaćanja**. Polja su sada zadana iz odgovarajućeg zapisa klijenta ugovora o projektu. |
| Naplata i određivanje cijene | 2021413 | Ažurirana su polja **Stvarni trošak** i **Prodaja** na entitetu **Zadatak** kako bi uključivala prodajne vrijednosti iz nenaplaćene i naplaćene troškove za zadatke. |
| Naplata i određivanje cijene | 2182110 | Pri kopiranju ugovora o projektu, ID retka ugovora generira se u ugovoru o odredišnom projektu kako bi se osiguralo da je jedinstven. |
| Upravljanje prilikama | 2186741 | Dodane su provjere valjanosti kako bi se osiguralo da se polje **Podrijetlo** i vrsta transakcije ne mogu ažurirati s postojećim pojedinostima retka ponude. |
| Upravljanje prilikama | 2191353 | Stvaranje kontrolne točke ne smije se dozvoliti u retku ugovora za vrijeme i materijal. |
| Upravljanje prilikama | 2216956 | Ispravljeni su problemi sa značajkom **Ažuriraj cijene**. |
| Planiranje i praćenje | 2182979 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje redaka procjene troškova s izvornog projekta. |
| Planiranje i praćenje | 2184144 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje naziva položaja resursa s izvornog projekta. |
| Planiranje i praćenje | 2184799 | Pooštrena je kontrola pri kopiranju projekta kako bi se osiguralo da se procijenjeni datum početka ne može promijeniti tijekom kopiranja. |
| Planiranje i praćenje | 2185134 | Tijekom kopiranja projekta, predviđeni datum početka odredišnog projekta postavljen je na današnji datum. |
| Planiranje i praćenje | 2196373 | Osigurajte da se zapisi voditelja projekta i članova tima ne dupliciraju u projektnom timu tijekom kopiranja projekta. |
| Planiranje i praćenje | 2211833 | Zadaci resursa kopiraju se iz izvornog projektnog zadatka u odredišni projekt. |
| Planiranje i praćenje | 2186541 | Popravljeni su problemi u rešetki **Procjene** do kojih je dolazilo pri grupiranju po **Resursu**. |
| Planiranje i praćenje | 2166906 | Kategorija transakcije iz zadatka mora se kopirati u entitet **Dodjela resursa**. |
| Upravljanje resursima | 2125362 | Ispravljeni su problemi do kojih je dolazilo tijekom stvaranja generičkog člana tima s pomoću načina raspodjele zasnovane na satima. |
| Vrijeme i trošak | 2113603 | Ispravljen je problem povezan s prilagodbom koji je uzrokovao uklanjanje atributa sa stranice **Vremenski unos**. Sustav provjerava postoji li na stranici atribut prije nego što mu pristupi s pomoću skripte. |
| Vrijeme i trošak | 2204377 | Kopirane vremenske tablice moraju se automatski prikazati kada odaberete **Kopiraj tjedan**. |
| Vrijeme i trošak | 2209059 | Polje **Stanje** moguće je uređivati za vremenske unose u aplikaciji Dynamics 365 Field Service. |
