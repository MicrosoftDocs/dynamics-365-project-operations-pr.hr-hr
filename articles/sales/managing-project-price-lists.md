---
title: Upravljanje cjenicima za projekt u ponudi
description: U ovoj se temi nalaze se informacije o entitetu cjenika za projekt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 5fc8691984e22b2fa35e26b1a7d94cc56c25c26d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177187"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Upravljanje cjenicima za projekt u ponudi

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations proširuje entitet cjenika u aplikaciji Dynamics 365 Sales. 

## <a name="key-entities"></a>Ključni entiteti

Cjenik uključuje informacije koje pružaju četiri različita entiteta:

- **Cjenik**: Ovaj entitet pohranjuje informacije o kontekstu, valuti, datumu stupanja na snagu i vremenskoj jedinici za vrijeme određivanja cijena. Kontekst prikazuje izražava li cjenik cijene koštanja ili cijene prodaje. 
- **Valuta**: Ovaj entitet pohranjuje valutu cijena na cjenik. 
- **Datum**: Ovaj se entitet upotrebljava kada sustav pokuša unijeti zadanu cijenu na transakciju. Cjenik koji ima datum stupanja na snagu koji uključuje odabrani datum transakcije. Ako je pronađeno više od jednog cjenika koji je na snazi za datum transakcije i koji je priložen povezanoj ponudi, ugovoru ili organizacijskoj jedinici, onda nijedna cijena nije zadana. 
- **Vrijeme**: Ovaj entitet pohranjuje jedinicu vremena za koju su cijene izražene, kao što su dnevne ili po satu. 

Entitet Cjenik ima tri povezane tablice koje pohranjuju cijene:

  - **Cijena na temelju uloge**: Ova tablica pohranjuje cijenu za kombiniranje vrijednosti uloge i organizacijske jedinice te se upotrebljava za postavljanje cijena utemeljenih na ulogama za ljudske resurse.
  - **Cijena po kategoriji transakcije**: Ova tablica pohranjuje cijene po kategoriji transakcije i upotrebljava se za postavljanje cijena po kategoriji troška.
  - **Stavke cjenika**: Ova tablica pohranjuje cijene za kataloške proizvode.
 
Cjenik je službena cijena. Službena cijena je kombinacija entiteta Cjenik i povezanih redaka u tablicama Cijena na temelju uloge, Cijena po kategoriji transakcije i Stavke cjenika.

## <a name="resource-roles"></a>Uloge resursa

Pojam *Uloga resursa* odnosi se na skup vještina, kompetencija i certifikacija koje osoba mora imati za obavljanje određenog skupa zadataka na projektu.

Vrijeme ljudskog resursa navodi se na temelju uloge koju resurs ispunjava u određenom projektu. Vrijeme, troškovi i naplata ljudskog resursa temelje se na ulozi resursa. Vrijeme može biti naplaćeno u bilo kojoj jedinici u grupi jedinica **Vrijeme**.

Grupa jedinica **Vrijeme** stvara se kada instalirate aplikaciju Project Operations. Ima zadanu jedinicu **Sat**. Ne možete brisati, preimenovati ili uređivati atribute grupe jedinica **Vrijeme** ili jedinice **Sat**. Međutim, možete dodati druge jedinice u grupu jedinica **Vrijeme**. Ako pokušate izbrisati grupu jedinica **Vrijeme** ili jedinicu **Sat**, mogli biste uzrokovati pogreške u poslovnoj logici.
 
## <a name="transaction-categories-and-expense-categories"></a>Kategorije transakcija i kategorije troškova

Putni i ostali troškovi koje snose projektni savjetnici naplaćuju se klijentu. Određivanje cijena kategorija troškova dovršava se s pomoću cjenika. Zrakoplovne karte, hotel i najam automobila primjeri su za kategorije troškova. Svaki redak cjenika za troškove određuje određivanje cijena za određenu kategoriju troškova. Za određivanje cijena troškova upotrebljavaju se sljedeća tri načina:

- **Po cijeni**: Cijena troškova naplaćuje se klijentu i ne primjenjuje se marža.
- **Postotak marže**: Klijentu se naplaćuje postotak iznad stvarnih troškova. 
- **Cijena po jedinici**: Cijena naplate postavljena je za svaku jedinicu kategorije troškova. Iznos koji se naplaćuje klijentu izračunava se na temelju broja jedinica troškova koje savjetnik prijavljuje. Kilometraža koristi metodu određivanja cijena po jedinici. Na primjer, kategorija troškova kilometraže može se konfigurirati za 30 američkih dolara (USD) dnevno ili 2 USD po milji. Kada savjetnik prijavi kilometražu na projektu, iznos računa izračunava se na temelju broja milja koje je savjetnik prijavio.
 
## <a name="project-sales-pricing-and-overrides"></a>Određivanje cijena prodaje projekta i otpisi

Za ponude i ugovore projekta, cjenik projekta ima različit uzorak otpisa cijena od cjenika proizvoda. U retku ponude koji se temelji na katalogu proizvoda možete otpisati cijenu za uloge i kategorije izravno u retku ponude jer svaki redak ponude upućuje na točno jednu stavku kataloga. Međutim, u retku ponude koji se temelji na projektu ne možete otpisati cijenu za uloge i kategorije izravno u retku ponude. Upotrijebite cjenik za projekt kako biste podržali dva različita uzorka za zamjenu.

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

Na ugovoru o projektu, sljedeći je redoslijed prvenstva za automatsko postavljanje povezanih cjenika za projekt:

1. Ponuda
2. Prilika
3. Klijent 
4. Globalne postavke 

Ako je cjenik projekta unesen po zadanim postavkama, sustav provjerava odgovara li valuta valuti klijenta i imaju li zadani cjenici koji su uneseni kontekst **Prodaja**.

Entitete Klijent, Prilika, Ponuda i Ugovor o projektu možete povezati s nekoliko cjenika za projekt. Ova mogućnost podržava zadane cijene za određeni datum za ugovor o dugoročnom projektu, u kojem bi moglo biti potrebno više od jednog cjenika za ažuriranje cijena koje se pojavljuju zbog inflacije. Međutim, ako cjenici koje pridružujete entitetu Klijent, Prilika, Ponuda ili Ugovor o projektu imaju preklapajući datum stupanja na snagu, zadane cijene možda nisu točne. Stoga biste trebali osigurati da cjenici za projekt koji imaju preklapajući datum stupanja na snagu nisu povezani s tim entitetima.

### <a name="deal-specific-price-overrides"></a>Otpisi cijena koji su specifični za dogovor

Možete stvoriti zamjene koje su specifične za dogovor za odabrane cijene na cjenicima za projekt koji su uneseni prema zadanim postavkama u ponudu ili ugovor o projektu.

Prema zadanim postavkama, ugovor projekta uvijek dobiva kopiju glavnog prodajnog cjenika umjesto izravne veze do njega. To ponašanje pomaže jamčiti da se sporazumi o cijenama koji su sklopljeni s klijentom za izjavu o radu (SOW, Statement of work) ne mijenjaju ako je glavni cjenik promijenjen.

Međutim, u ponudi možete koristiti glavni cjenik. Alternativno, možete kopirati glavni cjenik i urediti ga za izradu prilagođenog cjenika koji se odnosi samo na tu ponudu. Da biste izradili novi cjenik koji je specifičan za ponudu, na stranici **Ponuda** odaberite **Izradi prilagođeno određivanje cijena**. Cjeniku projekta koji je specifičan za dogovor možete pristupiti samo iz ponude. 

Kada izrađujete prilagođeni cjenik projekta, kopiraju se samo komponente cjenika. Drugim riječima, novi cjenik izrađen kao kopija postojećeg cjenika projekta koji je priložen u ponudi, a ovaj novi cjenik ima samo povezane cijene na temelju uloge i cijene po kategoriji transakcije.
  
## <a name="tracking-costs"></a>Praćenje troškova

Project Operations prati troškove uporabe vremena ljudskog resursa na projektima. Također prati troškove za ostale izdatke koji su nastali tijekom projekta, kao što su putni troškovi.

Kao što je slučaj kod stopa naplaćivanja, stope troškova za ljudske resurse također se postavljaju s pomoću cjenika. Ovdje su glavne razlike u ponašanju cjenika troškova i cjenika prodaje:

- Stopa troškova resursa ne može se otpisati na određenom projektu, ugovoru ili ponudi. Međutim, stope naplaćivanja mogu se otpisati na temelju dogovora ako su izvršene promjene koje su specifične za prirodu dogovora. 

- Sljedeći redoslijed koristi se za rješavanje cjenika troškova:

    1. Cjenik troškova koji je priložen organizacijskoj jedinici.
    2. Cjenik troškova koji je priložen parametrima aplikacije Project Operations. Budući da se cjenik troškova u mnogim različitim valutama može priložiti parametrima, dovršavanje usklađivanja valute između valute ugovorne organizacijske jedinice projekta, ugovora ili ponude te valute cjenika troškova.
    3. Za troškove, načini određivanja cijena po troškovima i marži troškova ne primjenjuju se za cjenik troškova. Čak i ako se ti načini određivanja cijena koriste u recima cjenika troškova za postavljanje troškova po kategoriji transakcije, sustav ih ignorira i ne unosi se zadana cijena troška.


[!INCLUDE[footer-include](../includes/footer-banner.md)]