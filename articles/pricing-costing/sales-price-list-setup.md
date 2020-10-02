---
title: Postavljanje prodajnog cjenika
description: U ovoj temi nalaze se informacije o prodajnim cjenicima za određivanje cijena za projekte.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896452"
---
# <a name="sales-price-list-setup"></a>Postavljanje prodajnog cjenika

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Za ponude i ugovore projekta, cjenik projekta ima različit uzorak otpisa cijena od cjenika proizvoda. U retku ponude koji se temelji na katalogu proizvoda možete otpisati cijenu za uloge i kategorije izravno u retku ponude jer svaki redak ponude upućuje na točno jednu stavku kataloga. Međutim, u retku ponude koji se temelji na projektu ne možete otpisati cijenu za uloge i kategorije izravno u retku ponude. Možete upotrijebiti cjenik za projekt kako biste radili s dva različita uzorka za zamjenu.

> [!NOTE]
> Preporučujemo da imate zaseban cjenik za svoje projektne resurse i artikle kataloga zbog razlika u ponašanju između njih kada otpisujete cijene.

Svaki od sljedećih entiteta može imati jedan ili više pridruženih prodajnih cjenika za određivanje cijena projekta:

- Klijent (račun) 
- Prilika 
- Ponuda 
- Ugovor o projektu

Pridruživanje tih entiteta cjeniku naznačeno je cjenikom projekta. Jedan ili više cjenika možete prudružiti prodajnim entitetima Klijent, Prilika, Ponuda i Ugovor o projektu.

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

Entitete Klijent, Prilika, Ponuda i Ugovor projekta možete povezati s nekoliko cjenika projekta. Ova mogućnost podržava zadane cijene za određeni datum za ugovor o dugoročnom projektu, u kojem bi moglo biti potrebno više od jednog cjenika za ažuriranje cijena koje se pojavljuju zbog inflacije. Međutim, ako cjenici koje pridružujete entitetu Klijent, Prilika, Ponuda ili Ugovor o projektu imaju preklapajući datum stupanja na snagu, zadane cijene možda nisu točne. Stoga biste trebali osigurati da cjenici projekta koji imaju preklapajući datum stupanja na snagu nisu pridruženi tim entitetima.
