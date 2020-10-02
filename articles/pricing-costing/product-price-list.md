---
title: Cjenici proizvoda
description: U ovoj se temi nalaze informacije o cjenicima u određivanju kataloških cijena koje se upotrebljavaju u ponudama za projekt i ugovore o projektu.
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
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898162"
---
# <a name="product-price-lists"></a>Cjenici proizvoda

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Cjenici i entiteti stavki cjenika podržavaju određivanje cijena kataloga proizvoda. Ova se funkcija uglavnom upotrebljava za retke temeljene na katalogu u ponudama projekata i ugovorima o projektu.

Za retke temeljene na projektu ugovor nakon sklapanja predstavlja dogovor. Budući da sklapanju ugovora obično prethodi postupak pregovoranja, cijena pridružena ponudi uvijek se kopira kakva jest u novi cjenik i prilaže se ugovoru. Taj novi cjenik ne može se promijeniti izvan opsega ugovora. To ograničenje pomaže zaštititi ispregovaranu cijenu od promjena cijena koje se pojavljuju u glavnom cjeniku.

Proizvodi se trebaju postaviti tako da sadrže zadani trošak i cjenike u katalogu proizvoda. Upotrebljavajte kataloške cijena, standardni trošak i trenutačni trošak kako biste konfigurirali zadani trošak i kataloških cijena. Zadane kataloške cijene koriste se u retku ponude ili u retku ugovora o projektu samo ako sustav ne može pronaći redak cjenika za taj proizvod u cjeniku proizvoda za ponudu ili ugovor o projektu.

Cijena koštanja redaka kataloga proizvoda može se promijeniti između ponuda. Ta je mogućnost važna jer ako ne pratite precizno troškove, ne možete odrediti operativnu dobit u projektnim angažmanima. Prema zadanim postavkama standardna cijena proizvoda upotrebljava se kao cijena koštanja. Međutim, zadana cijena koštanja može se ažurirati u retku ponude ako postoji drugačija cijena koštanja za tu ponudu.

## <a name="price-list-items"></a>Stavke cjenika

Proizvode iz kataloga proizvoda možete dodavati na različite cjenike. Reci cjenika za proizvode uvijek upućuju na određenu jedinicu. Cijena za proizvod u stavkama cjenika može se konfigurirati kao iznos valute. Ili se može konfigurirati kao funkcija kataloške cijene, trenutačnog troška ili standardnog troška.

PSA podržava različite mogućnosti zaokruživanja kada su cijene konfigurirane kao funkcija kataloške cijene, trenutačnog troška ili standardnog troška. Uz iskorištavanje prednosti više načina određivanja cijena i mogućnosti zaokruživanja, popise popusta možete povezati sa stavkama cjenika. 

Kada stvarate novi prilagođeni cjenik za ponudu odabirom mogućnosti **Stvori prilagođeno određivanje cijena** na stranici **Ponuda za projekt**, napravljena je kopija cjenika, a polje **Entitet** u zaglavlju novog cjenika postavlja se na **Prodajni entitet**. Naziv novog cjenika dodaje se s nazivom ponude i vremenskom oznakom. Također možete koristiti naziv novog cjenika i naziv ponude u prilagođenim tijekovima rada za pokretanje dodatnog pregleda i odobrenja za ponude koje koriste prilagođeno određivanje cijena.

 
## <a name="default-product-price-list"></a>Zadani cjenik proizvoda
Svaki zapis klijenta sadrži polje **Zadani cjenik**, gdje možete navesti cjenik koji odgovara valuti klijenta. Zadana vrijednost ne unosi se automatski u ovo polje. Kada postoji prilagođeni ugovor o određivanju cijena s određenim klijentom, ovo polje možete koristiti za povezivanje cjenika s tim klijentom.

Entiteti Prilika, Ponuda i Ugovor o projektu koriste sljedeću ponudu za unos zadanih cjenika proizvoda. Ista ponuda koristi se za cjenike projekta.

1.  Ponuda
2.  Prilika
3.  Klijent
4.  Globalne postavke 

Prema zadanim postavkama polje **Proizvod** u retku ponude popisuje sve aktivne proizvode u cjeniku proizvoda ponude. Ako je proizvod neaktivan ili je skica proizvoda, ne navodi se na popisu, čak i ako je naveden u cjeniku. 

Reci kataloga proizvoda dodaju se kao reci fakture u prvoj fakturi koja se izrađuje za ugovor o projektu. U skici fakture ti se reci fakture mogu izbrisati. U tom će se slučaju reci prikazati u sljedećoj fakturi dok se ne fakturiraju ili dok se faktura ne pošalje klijentu. Ne možete fakturirati djelomičnu količinu retka fakture za proizvod. Kada se reci proizvoda iz ugovora o projektu fakturiraju, izrađuju se stvarni podaci. Međutim, ti stvarni podaci ne povezuju se s povezanim entitetom projekta. Drugim riječima, reci projekta temeljeni na proizvodu neovisni su o bilo kakvoj upotrebi temeljenoj na projektu. Potrošnju materijala u projektima se ne prati.
