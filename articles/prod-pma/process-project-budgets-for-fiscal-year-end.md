---
title: Prijenos proračuna projekata na kraju poslovne godine
description: U ovom članku nalaze se informacije o načinu prijenosa preostalog proračunskog iznosa u naredne godine i stvaranju pojedinosti proračunskog registra.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 74b2831a19688636f5c4863036adf7043c80d49829737b56c131abb6998d6cb3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007362"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Prijenos proračuna projekata na kraju poslovne godine

[!include [banner](../includes/banner.md)]

Kada radite na višegodišnjem projektu, možda ćete na kraju poslovne godine imati preostali proračun. Preostale proračunske iznose možete prenijeti u narednu godinu i stvoriti pojedinosti registra proračuna za iznose na povezanim računima glavne knjige. Prije nego što prenesete preostale iznose, pregledajte i analizirajte preostale proračunske iznose.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Pregled i analiza preostalih proračunskih iznosa

Dovršite sljedeće korake kako biste pregledali proračunske iznose za projekte na kraju godine, ali nemojte iznose prenositi dalje.

1. Idite na stavku **Upravljanje projektima i računovodstvo** > **Povremeno** > **Proračuni** > **Prenesi proračune**. 
2. Na stranici **Postupak prijenosa proračuna projekta**, na kartici **Mogućnosti na kraju godine**, provjerite da mogućnost **Prenesi preostale proračunske iznose projekta** nije omogućena.
3. Na kartici **Parametri**, u polju **Proračunska godina projekta**, odaberite poslovnu godinu za koji želite prikazati preostali proračunski iznos. 
4. U polju **Proračunska godina projekta**, odaberite poslovnu godinu za koji želite prikazati preostali proračunski iznos. 
5. U polju **Iz modela predviđanja** odaberite **Preostali proračun**. 
6. Kako biste uključili projekte koji ispunjavaju odabrane kriterije i nemaju preostali proračun, odaberite **Prikaži bez preostalog iznosa**.  
7. Na kartici **Odaberi proračune** odaberite **Dohvati sve proračune** kako biste učitali sve proračune koji se podudaraju s odabranim kriterijima, a zatim odaberite **Postupak**. 
8. Kako biste dizajnirali upit baze podataka koji učitava određeni skup proračuna u okno, odaberite **Dohvati odabrane proračune**.

Za više informacija o određenom retku u oknu odaberite redak, a zatim odaberite **Prikaži pojedinosti proračuna** ili **Prikaži račune**.

## <a name="carry-forward-remaining-budget-amounts"></a>Prijenos preostalih proračunskih iznosa 

Kada obrađujete preostale proračunske iznose, možete stvoriti transakcije u glavnoj knjizi za iznose koje prenosite. Kako biste stvorili transakcije glavne knjige, poduzmite korake navedene u odjeljku [Prijenos proračunskih iznosa i stvaranje transakcija glavne knjige](#carry-forward). 

> [!NOTE]
> Proračunski iznosi koji se prenose, prenose se na model predviđanja koji je odabran na stranici **Modeli predviđanja** kao model predviđanja za prijenos.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Prijenos proračunskih iznosa i stvaranje transakcija glavne knjige

1.  Odaberite **Upravljanje projektima i računovodstvo** > **Povremeno** > **Proračuni** > **Prenesi proračune**. 
2. Na stranici **Postupak prijenosa proračuna projekta** odaberite **Kraj godine**, a zatim omogućite **Prijenos preostalog proračunskog iznosa projekta** i **Stvaranje unosa u registar proračuna u glavnoj knjizi**. 
3. Na kartici **Parametri**, u grupi polja **Parametri projekta**, odaberite sljedeće:

   - **Proračunska godina projekta**: Odaberite početak poslovne godine za koji želite prikazati preostale iznose proračuna. 
   - **Dobit i gubitak**: Stvorite transakcija dobiti i gubitka u glavnoj knjizi. 
   -  **WIP**: Stvorite transakcije Rada u tijeku (WIP) u glavnoj knjizi.
   -  **Plaća**: Stvorite transakcije raspodjele plaća u glavnoj knjizi. 

5. U grupi polja **Glavna knjiga** navedite sljedeće informacije: 

   - U polju **Otvaranje poslovne godine** odaberite poslovnu godinu u koju želite prenijeti preostali proračunski iznos za projekt. Zadana vrijednost je jedna godina nakon vrijednosti u polju **Proračunska godina projekta**.
   -  U polju **Razdoblje prijenosa** odaberite razdoblje za koje želite stvoriti pojedinosti proračunskog registra u glavnoj knjizi. To je obično prvo razdoblje na otvaranju poslovne godine.

6. U grupi polja **Kopiraj iz/na** navedite sljedeće podatke:

   - U polju **Iz modela predviđanja** odaberite model predviđanja proračuna projekta povezan s preostalim proračunskim iznosima koje želite prenijeti za projekte. 
   - U polju **Proračunski model za glavnu knjigu** odaberite model proračuna za glavnu knjigu povezan s proračunskim iznosima koje želite prenijeti u glavnu knjigu. 
   -  Odaberite **Valuta prijenosa prodaje** kako biste valutu prodaje projekta upotrebljavali za transakcije glavne knjige koje se kreiraju kada prenesete proračunske iznose za projekte. Kad mogućnost nije odabrana, transakcije upotrebljavaju računovodstvenu valutu. 
   -  Odaberite **Prikaži bez preostalog iznosa** kako biste uključili projekte koji nemaju preostali iznos proračuna, ali zadovoljavaju ostale kriterije koje odaberete u projektima prikazanim u donjem oknu.

7. Na kartici **Odaberi proračune** odaberite **Dohvati sve proračune** kako biste učitali sve proračune koji se podudaraju s kriterijima koje ste odabrali. Ako biste željeli dizajnirati upit baze podataka koji učitava određeni skup proračuna projekta u okno, odaberite **Dohvati odabrane proračune**.
8. Za svaki projekt koji želite obraditi, odaberite mogućnost na početku retka za projekt.

    > [!TIP]
    > Kako biste odabrali sve ili većinu projekata, odaberite kvačicu u gornjem lijevom kutu. Kako biste isključili obradu nekog projekta, uklonite kvačicu za taj projekt.

9. Kako biste prenijeli preostale proračunske iznose za odabrane projekte u odabranu poslovnu godinu i stvorili pojedinosti proračunskog registra u glavnoj knjizi, odaberite **Postupak**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Prijenos proračunskih iznosa bez stvaranja transakcija glavne knjige

1. Idite na stavku **Upravljanje projektima i računovodstvo** > **Povremeno** > **Proračuni** > **Prenesi proračune**.
2. Na stranici **Postupak prijenosa proračuna projekta**, u polju **Mogućnosti na kraju godine**, odaberite mogućnost **Prenesi preostale iznose proračuna projekta**.
3. U grupi **Parametri**, u polju **Proračunska godina projekta**, odaberite poslovnu godinu za koju želite prikazati preostale iznose proračuna.
4. U grupi **Kopiraj iz/na** navedite sljedeće podatke:

   - U polju **Iz modela predviđanja** odaberite model predviđanja proračuna projekta koji je povezan s preostalim proračunskim iznosima koje želite prenijeti za projekte. 
   - Kako biste uključili projekte koji nemaju preostali proračun, ali ispunjavaju kriterije koje ste odabrali, odaberite **Prikaži bez preostalog iznosa**.
   - U grupi **Odaberi proračune** odaberite **Dohvati sve proračune** kako biste učitali sve proračune koji se podudaraju s kriterijima koje ste odabrali. Kako biste dizajnirali upit baze podataka koji učitava određeni skup proračuna projekta u okno, odaberite **Dohvati odabrane proračune**.

5. Za svaki projekt koji želite obraditi, odaberite mogućnost na početku retka za projekt. 
6. Odaberite **Postupak** za prijenos preostalih proračunskih iznosa za odabrane projekte na odabranu poslovnu godinu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]