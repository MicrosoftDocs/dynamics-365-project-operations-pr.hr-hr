---
title: Postavljanje prodajnog cjenika
description: U ovoj temi nalaze se informacije o prodajnim cjenicima za određivanje cijena za projekte.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 952d518fb58b5be46c4b1cf4ed57b2494fdfdad85e7fe6fb0d622367bc071b5f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997597"
---
# <a name="set-up-a-sales-price-list"></a>Postavljanje prodajnog cjenika

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Za ponude i ugovore projekta, cjenik projekta ima različit uzorak otpisa cijena od cjenika proizvoda. U retku ponude koji se temelji na katalogu proizvoda možete otpisati cijenu za uloge i kategorije izravno u retku ponude jer svaki redak ponude upućuje na točno jednu stavku kataloga. Međutim, u retku ponude koji se temelji na projektu ne možete otpisati cijenu za uloge i kategorije izravno u retku ponude. Možete upotrijebiti cjenik za projekt kako biste radili s dva različita uzorka za zamjenu.

> [!NOTE]
> Preporučujemo da imate zaseban cjenik za svoje projektne resurse i artikle kataloga zbog razlika u ponašanju između njih kada otpisujete cijene.

Svaki od sljedećih entiteta može imati jedan ili više pridruženih prodajnih cjenika za određivanje cijena projekta:

- Klijent (račun) 
- Prilika 
- Ponuda 
- Ugovor o projektu

Pridruživanje tih entiteta cjeniku naznačeno je cjenikom za projekt. Jedan ili više cjenika možete prudružiti prodajnim entitetima Klijent, Prilika, Ponuda i Ugovor o projektu.

Zadani cjenik projekta ne unosi se automatski u zapis klijenta. Međutim, cjenik projekta možete ručno priložiti zapisu klijenta. Ipak, trebate ručno priložiti cjenik projekta samo kada imate prilagođeni ugovor o određivanju cijena s klijentom. 

Kada se cjenik projekta prilaže entitetu prodaje, provjeravaju se sljedeći podaci:

- Cjenik ima kontekst **Prodaja**. 
- Valuta cjenika podudara se s valutom klijenta. 

Na ugovoru o projektu, sljedeći redoslijed prvenstva upotrebljava se za automatsko postavljanje povezanih cjenika za projekt:

1. Ponuda
2. Prilika
3. Klijent 
4. Globalne postavke 

Ako je cjenik projekta unesen po zadanim postavkama, sustav provjerava odgovara li valuta valuti klijenta i imaju li zadani cjenici koji su uneseni kontekst **Prodaja**.

Entitete Klijent, Prilika, Ponuda i Ugovor o projektu možete povezati s nekoliko cjenika za projekt. Ova mogućnost podržava zadane cijene za određeni datum za ugovor o dugoročnom projektu, u kojem bi moglo biti potrebno više od jednog cjenika za ažuriranje cijena koje se pojavljuju zbog inflacije. Međutim, ako cjenici koje pridružujete entitetu Klijent, Prilika, Ponuda ili Ugovor o projektu imaju preklapajući datum stupanja na snagu, zadane cijene možda nisu točne. Stoga biste trebali osigurati da cjenici za projekt koji imaju preklapajući datum stupanja na snagu nisu povezani s tim entitetima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]