---
title: Određivanje cijene projekta
description: Ova tema sadrži informacije o tome kako funkcionira određivanje cijene u aplikaciji Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: 176b84671ca0b5b998c44be4f306d1f8f5200c72
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148904"
---
# <a name="project-pricing"></a>Određivanje cijene projekta 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation proširuje entitet Cjenik u sustavu Dynamics 365 Sales. 

## <a name="key-entities"></a>Ključni entiteti

Cjenik uključuje informacije koje pružaju četiri različita entiteta:

- **Cjenik** - Ovaj entitet pohranjuje informacije o kontekstu, valuti, datumu stupanja na snagu i vremenskoj jedinici za vrijeme određivanja cijena. Kontekst prikazuje izražava li cjenik stope troškova ili stope prodaje. 
- **Valuta** - Ovaj entitet pohranjuje valutu cijena na cjenik. 
- **Datum** – Ovaj se entitet koristi kada sustav pokuša unijeti zadanu cijenu na transakciju. PSA određivanje cijene odabire cjenik koji sadrži datum stupanja na snagu koji uključuje datum transakcije. Ako PSA određivanje cijene pronađe više od jednog cjenika koji stupa na snagu za datum transakcije koji je pridružen povezanoj ponudi, ugovoru ili organizacijskoj jedinici, onda nijedna cijena nije zadana. 
- **Vrijeme** -Ovaj entitet pohranjuje jedinicu vremena za koju su cijene izražene, kao što su dnevne ili po satu. 

Entitet Cjenik ima tri povezane tablice koje pohranjuju cijene:

  - **Cijena na temelju uloge** - Ova tablica pohranjuje stopu za kombiniranje vrijednosti uloge i organizacijske jedinice te se koristi za postavljanje cijena utemeljenih na ulogama za ljudske resurse.
  - **Cijena po kategoriji transakcije** -Ova tablica pohranjuje cijene po kategoriji transakcije i koristi se za postavljanje cijena po kategoriji troška.
  - **Stavke cjenika** - Ova tablica pohranjuje cijene za kataloške proizvode.

> ![Konfiguriranje cijena koristeći cjenik](media/basic-guide-12.png)
 
Cjenik je službena cijena. Službena cijena je kombinacija entiteta Cjenik i povezanih redaka u tablicama Cijena na temelju uloge, Cijena po kategoriji transakcije i Stavke cjenika.

## <a name="resource-roles"></a>Uloge resursa

Pojam *Uloga resursa* odnosi se na skup vještina, kompetencija i certifikacija koje osoba mora imati za obavljanje određenog skupa zadataka na projektu.

Vrijeme ljudskog resursa obično se navodi na temelju uloge koju resurs ispunjava u određenom projektu. Za vrijeme ljudskog resursa, PSA podržava troškove i naplatu koji se temelje na ulozi resursa. Vrijeme može biti naplaćeno u bilo kojoj jedinici u grupi jedinica **Vrijeme**.

Grupa jedinica **Vrijeme** izrađuje se prilikom instalacije PSA. Ima zadanu jedinicu **Sat**. Ne možete brisati, preimenovati ili uređivati atribute grupe jedinica **Vrijeme** ili jedinice **Sat**. Međutim, možete dodati druge jedinice u grupu jedinica **Vrijeme**. Ako pokušate izbrisati grupu jedinica **Vrijeme** ili jedinicu **Sat**, mogli biste uzrokovati greške u poslovnoj logici sustava PSA.

> ![Konfiguriranje cijena po ulozi](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Kategorije transakcija i kategorije troškova

Putni i ostali troškovi koje snose projektni savjetnici obično se naplaćuju klijentu. PSA podržava određivanje cijena kategorija troškova s pomoću cjenika. Zrakoplovne karte, hotel i najam automobila primjeri su za kategorije troškova. Svaki redak cjenika za troškove određuje određivanje cijena za određenu kategoriju troškova. Za određivanje cijena kategorija troškova, PSA podržava sljedeća tri načina određivanja cijena:

- **Po cijeni** - Cijena troška naplaćuje se klijentu i ne primjenjuje se marža.
- **Postotak marže** - Postotak izvan stvarnih troškova naplaćuje se klijentu. 
- **Cijena po jedinici** - Cijena naplate postavljena je za svaku jedinicu kategorije troškova. Iznos koji se naplaćuje klijentu izračunava se na temelju broja jedinica troškova koje savjetnik prijavljuje. Kilometraža koristi metodu određivanja cijena po jedinici. Na primjer, kategorija troškova kilometraže može se konfigurirati za 30 američkih dolara (USD) dnevno ili 2 USD po milji. Kada savjetnik prijavi kilometražu na projektu, iznos računa izračunava se na temelju broja milja koje je savjetnik prijavio.

> ![Konfiguriranje cijena za kategorije troškova](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Određivanje cijena prodaje projekta i otpisi

Za ponude i ugovore projekta, cjenik projekta ima različit uzorak otpisa cijena od cjenika proizvoda. U retku ponude koji se temelji na katalogu proizvoda možete otpisati cijenu za uloge i kategorije izravno u retku ponude jer svaki redak ponude upućuje na točno jednu stavku kataloga. Međutim, u retku ponude koji se temelji na projektu ne možete otpisati cijenu za uloge i kategorije izravno u retku ponude. Da bi podržao dva različita uzorka otpisa, PSA je uveo novo pridruživanje cjenika, cjenik projekta.

> [!NOTE]
> Preporučujemo da imate zaseban cjenik za svoje projektne resurse i artikle kataloga zbog razlika u ponašanju između njih kada otpisujete cijene.

Svaki od sljedećih entiteta može imati jedan ili više pridruženih prodajnih cjenika za određivanje cijena projekta:

- Klijent (račun) 
- Prilika 
- Ponuda 
- Ugovor o projektu

Pridruživanje tih entiteta cjeniku naznačeno je cjenikom za projekt. Jedan ili više cjenika možete prudružiti prodajnim entitetima Klijent, Prilika, Ponuda i Ugovor o projektu.

Zadani cjenik projekta ne unosi se automatski u zapis klijenta. Međutim, cjenik projekta možete ručno priložiti zapisu klijenta. Ipak, trebate ručno priložiti cjenik projekta samo kada imate prilagođeni ugovor o određivanju cijena s klijentom. 

Kada se cjenik projekta prilaže prodajnom entitetu, PSA provjerava sljedeće informacije:

- Cjenik u kontekstu **Prodaje**. 
- Valuta cjenika podudara se s valutom klijenta. 

Na ugovoru o projektu, PSA koristi sljedeći redoslijed prvenstva za automatsko postavljanje povezanih cjenika za projekt:

1. Ponuda
2. Prilika
3. Klijent 
4. Globalne postavke za PSA

Ako je cjenik projekta unesen po zadanim postavkama, PSA provjerava odgovara li valuta valuti klijenta i imaju li zadani cjenici koji su uneseni kontekst **Prodaje**.

Entitete Klijent, Prilika, Ponuda i Ugovor o projektu možete povezati s nekoliko cjenika za projekt. Ova mogućnost podržava zadane cijene za određeni datum za ugovor o dugoročnom projektu, u kojem bi moglo biti potrebno više od jednog cjenika za ažuriranje cijena koje se pojavljuju zbog inflacije. Međutim, ako cjenici koje pridružujete entitetu Klijent, Prilika, Ponuda ili Ugovor o projektu imaju preklapajući datum stupanja na snagu, zadane cijene možda nisu točne. Stoga biste trebali osigurati da cjenici za projekt koji imaju preklapajući datum stupanja na snagu nisu pridruženi tim entitetima.

### <a name="deal-specific-price-overrides"></a>Otpisi cijena koji su specifični za dogovor

U PSA možete izraditi otpise koji su specifični za dogovor za odabrane cijene na cjenicima za projekt koji su uneseni prema zadanim postavkama u ponudu ili ugovor o projektu.

Prema zadanim postavkama, ugovor projekta uvijek dobiva kopiju glavnog prodajnog cjenika umjesto izravne veze do njega. To ponašanje pomaže jamčiti da se sporazumi o cijenama koji su sklopljeni s klijentom za izjavu o radu (SOW) ne mijenjaju ako je glavni cjenik promijenjen.

Međutim, u ponudi možete koristiti glavni cjenik. Alternativno, možete kopirati glavni cjenik i urediti ga za izradu prilagođenog cjenika koji se odnosi samo na tu ponudu. Da biste izradili novi cjenik koji je specifičan za ponudu, na stranici **Ponuda** odaberite **Izradi prilagođeno određivanje cijena**. Cjeniku projekta koji je specifičan za dogovor možete pristupiti samo iz ponude. 

Kada izrađujete prilagođeni cjenik projekta, kopiraju se samo komponente cjenika. Drugim riječima, novi cjenik izrađen kao kopija postojećeg cjenika projekta koji je priložen u ponudi, a ovaj novi cjenik ima samo povezane cijene na temelju uloge i cijene po kategoriji transakcije.

> ![Pregledavanje i konfiguriranje prilagođenih određivanja cijena za ugovor o projektu](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Praćenje troškova

PSA prati troškove za korištenje vremena ljudskog resursa na projektima. Također prati troškove za ostale troškove koji su nastali tijekom projekta, kao što su putni troškovi.

Kao što je slučaj kod stopa naplaćivanja, stope troškova za ljudske resurse također se postavljaju s pomoću cjenika. Ovdje su glavne razlike u ponašanju cjenika troškova i cjenika prodaje:

- Stopa troškova resursa ne može se otpisati na određenom projektu, ugovoru ili ponudi. Međutim, stope naplaćivanja mogu se otpisati na temelju dogovora ako su izvršene promjene koje su specifične za prirodu dogovora. 

- Sljedeći redoslijed koristi se za rješavanje cjenika troškova:

    1. Cjenik troškova koji je priložen organizacijskoj jedinici.
    2. Cjenik troškova koji je priložen parametrima usluge projekta. Budući da se cjenik troškova u mnogim različitim valutama može priložiti parametrima usluge projekta, PSA provodi podudarnost valuta između valute ugovorne organizacijske jedinice projekta, ugovora ili ponude te valute cjenika troškova.
    3. Za troškove, načini određivanja cijena po troškovima i marži troškova ne primjenjuju se za cjenik troškova. Čak i ako se ti načini određivanja cijena koriste u recima cjenika troškova za postavljanje troškova po kategoriji transakcije, sustav ih ignorira i ne unosi se zadana cijena troška.


[!INCLUDE[footer-include](../includes/footer-banner.md)]