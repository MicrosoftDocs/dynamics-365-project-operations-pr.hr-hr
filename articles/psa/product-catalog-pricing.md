---
title: Određivanje cijena kataloga proizvoda
description: Ova tema pruža informacije o tome kako funkcionira određivanje cijena kataloga proizvoda u sustavu Dynamics 365 Project Service Automation (PSA).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 148f52f74ee64c2ee218dda3b09e1188e70217b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009202"
---
# <a name="product-catalog-pricing"></a>Određivanje cijena kataloga proizvoda 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Cjenici i entiteti stavki cjenika podržavaju određivanje cijena kataloga proizvoda. Ova se funkcija uglavnom upotrebljava za retke temeljene na katalogu u ponudama projekata i ugovorima o projektu.

Za retke temeljene na projektu ugovor nakon sklapanja predstavlja dogovor. Budući da sklapanju ugovora obično prethodi postupak pregovoranja, cijena pridružena ponudi uvijek se kopira kakva jest u novi cjenik i prilaže se ugovoru. Taj novi cjenik ne može se promijeniti izvan opsega ugovora. To ograničenje pomaže zaštititi ispregovaranu cijenu od promjena cijena koje se pojavljuju u glavnom cjeniku.

Proizvodi se trebaju postaviti tako da sadrže zadani trošak i cjenike u katalogu proizvoda. Morate koristiti katalošku cijenu, standardni trošak i trenutačni trošak za konfiguriranje zadanih troškova i kataloških cijena. Zadane kataloške cijene koriste se u retku ponude ili u retku ugovora o projektu samo ako sustav ne može pronaći redak cjenika za taj proizvod u cjeniku proizvoda za ponudu ili ugovor o projektu.

Cijena koštanja redaka kataloga proizvoda može se promijeniti između ponuda. Ta je mogućnost važna jer ako ne pratite precizno troškove, ne možete odrediti operativnu dobit u projektnim angažmanima. Prema zadanim postavkama standardna cijena proizvoda upotrebljava se kao cijena koštanja. Međutim, zadana cijena koštanja može se ažurirati u retku ponude ako postoji drugačija cijena koštanja za tu ponudu.

## <a name="price-list-items"></a>Stavke cjenika

Proizvode iz kataloga proizvoda možete dodavati na različite cjenike. Reci cjenika za proizvode uvijek upućuju na određenu jedinicu. Cijena za proizvod u stavkama cjenika može se konfigurirati kao iznos valute. Ili se može konfigurirati kao funkcija kataloške cijene, trenutačnog troška ili standardnog troška.

PSA podržava različite mogućnosti zaokruživanja kada su cijene konfigurirane kao funkcija kataloške cijene, trenutačnog troška ili standardnog troška. Uz iskorištavanje prednosti više načina određivanja cijena i mogućnosti zaokruživanja, popise popusta možete povezati sa stavkama cjenika. 

> ![Dodavanje proizvoda iz kataloga u različite cjenike](media/basic-guide-16.png)

Kada izradite novi prilagođeni cjenik za ponudu odabirom mogućnosti **Izradi prilagođeno određivanje cijena** na stranici **Ponuda projekta**, PSA izrađuje kopiju cjenika, a polje **Entitet** u zaglavlju novog cjenika postavlja se na **Prodajni entitet**. Naziv novog cjenika dodaje se s nazivom ponude i vremenskom oznakom. Također možete koristiti naziv novog cjenika i naziv ponude u prilagođenim tijekovima rada za pokretanje dodatnog pregleda i odobrenja za ponude koje koriste prilagođeno određivanje cijena.

 
## <a name="default-product-price-list"></a>Zadani cjenik proizvoda
Svaki zapis klijenta sadrži polje **Zadani cjenik**, gdje možete navesti cjenik koji odgovara valuti klijenta. U PSA-u zadana vrijednost ne unosi se automatski u ovo polje. Kada postoji prilagođeni ugovor o određivanju cijena s određenim klijentom, ovo polje možete koristiti za povezivanje cjenika s tim klijentom.

Entiteti Prilika, Ponuda i Ugovor o projektu koriste sljedeću ponudu za unos zadanih cjenika proizvoda. Ista ponuda upotrebljava se za cjenike za projekt.

1.  Ponuda
2.  Prilika
3.  Klijent
4.  Globalne postavke za PSA

Prema zadanim postavkama polje **Proizvod** u retku ponude popisuje sve aktivne proizvode u cjeniku proizvoda ponude. Ako je proizvod neaktivan ili je skica proizvoda, ne navodi se na popisu, čak i ako je naveden u cjeniku. 

Reci kataloga proizvoda dodaju se kao reci fakture u prvoj fakturi koja se izrađuje za ugovor o projektu. U skici fakture ti se reci fakture mogu izbrisati. U tom će se slučaju reci prikazati u sljedećoj fakturi dok se ne fakturiraju ili dok se faktura ne pošalje klijentu. U PSA-u ne možete fakturirati djelomičnu količinu retka fakture za proizvod. Kada se reci proizvoda iz ugovora o projektu fakturiraju, izrađuju se stvarni podaci. Međutim, ti stvarni podaci ne povezuju se s povezanim entitetom projekta. Drugim riječima, reci projekta temeljeni na proizvodu neovisni su o bilo kakvoj upotrebi temeljenoj na projektu. PSA ne prati potrošnju materijala u projektima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]