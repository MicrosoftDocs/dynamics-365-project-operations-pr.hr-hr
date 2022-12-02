---
title: Cjenici proizvoda
description: U ovom se članku nalaze informacije o cjenicima u određivanju kataloških cijena koje se upotrebljavaju u ponudama za projekt i ugovore o projektu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 68203f5adf7bf41d97e662e335d481ccac959ed6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917613"
---
# <a name="product-price-lists"></a>Cjenici proizvoda

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

 **Cjenici proizvoda** u aplikaciji Project Operations i povezani entiteti stavke cjenika podržavaju funkcionalnost za određivanje cijena proizvoda na ponudama i redcima ugovora koji se temelje na proizvodu. Za proizvode koji se upotrebljavaju na projektima upotrebljavaju se zapisi stavki cjenika za cjenike projekata. 

Proizvodi se trebaju postaviti tako da sadrže zadani trošak i cjenike u katalogu proizvoda. Upotrebljavajte kataloške cijena, standardni trošak i trenutačni trošak kako biste konfigurirali zadani trošak i kataloških cijena. Zadane kataloške cijene koriste se u retku ponude ili u retku ugovora o projektu samo ako sustav ne može pronaći redak cjenika za taj proizvod u cjeniku proizvoda za ponudu ili ugovor o projektu.

Cijena koštanja redaka kataloga proizvoda može se promijeniti između ponuda. Ta je mogućnost važna jer ako ne pratite precizno troškove, ne možete odrediti operativnu dobit u projektnim angažmanima. Prema zadanim postavkama standardna cijena proizvoda upotrebljava se kao cijena koštanja. Međutim, zadana cijena koštanja može se ažurirati u retku ponude ako postoji drugačija cijena koštanja za tu ponudu.

## <a name="price-list-items"></a>Stavke cjenika

Proizvode iz kataloga proizvoda možete dodavati na različite cjenike. Reci cjenika za proizvode uvijek upućuju na određenu jedinicu. Cijena za proizvod u stavkama cjenika može se konfigurirati kao iznos valute. Ili se može konfigurirati kao funkcija kataloške cijene, trenutačnog troška ili standardnog troška.

Funkcionalnost određivanja cijena podržava različite mogućnosti zaokruživanja kada su cijene proizvoda konfigurirane kao funkcija kataloške cijene, standardnog ili trenutačnog troška. Uz iskorištavanje prednosti više načina određivanja cijena i mogućnosti zaokruživanja, popise popusta možete povezati sa stavkama cjenika. 

 
## <a name="default-product-price-list"></a>Zadani cjenik proizvoda
Svaki zapis klijenta sadrži polje **Zadani cjenik**, gdje možete navesti cjenik koji odgovara valuti klijenta. Zadana vrijednost ne unosi se automatski u ovo polje. Kada postoji prilagođeni ugovor o određivanju cijena s određenim klijentom, ovo polje možete koristiti za povezivanje cjenika s tim klijentom.

Entiteti Prilika, Ponuda i Ugovor o projektu koriste sljedeću ponudu za unos zadanih cjenika proizvoda. Ista ponuda upotrebljava se za cjenike za projekt.

1.  Ponuda
2.  Prilika
3.  Klijent
4.  Globalne postavke 

Prema zadanim postavkama polje **Proizvod** u retku ponude popisuje sve aktivne proizvode u cjeniku proizvoda ponude. Ako je proizvod neaktivan ili je skica proizvoda, ne navodi se na popisu, čak i ako je naveden u cjeniku. 

Reci kataloga proizvoda dodaju se kao reci fakture u prvoj fakturi koja se izrađuje za ugovor o projektu. U skici fakture ti se reci fakture mogu izbrisati. U tom će se slučaju reci prikazati u sljedećoj fakturi dok se ne fakturiraju ili dok se faktura ne pošalje klijentu. Ne možete fakturirati djelomičnu količinu retka fakture za proizvod. Kada se reci proizvoda iz ugovora o projektu fakturiraju, izrađuju se stvarni podaci. Međutim, ti stvarni podaci ne povezuju se s povezanim entitetom projekta. Drugim riječima, reci projekta temeljeni na proizvodu neovisni su o bilo kakvoj upotrebi temeljenoj na projektu. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
