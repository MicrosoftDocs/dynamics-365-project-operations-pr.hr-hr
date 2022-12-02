---
title: Postavljanje prilagođenih polja kao cjenovnih veličina
description: U ovom se članku nalaze informacije o načinu postavljanja cjenovnih veličina s pomoću prilagođenih polja.
author: rumant
ms.date: 09/18/2020
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
ms.openlocfilehash: 0c0c43e483ebcb016747e533d685f13fd5dd8700
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917567"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Postavljanje prilagođenih polja kao cjenovnih veličina

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Prije početka rada, u ovom se članku podrazumijeva da ste dovršili postupke opisane u člancima [Izrada prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md) i [Dodavanje obveznih prilagođenih polja entitetima za postavljanje cijena i transakcije](add-custom-fields-price-setup-transactional-entities.md). Ako niste dovršili te postupke, vratite se i dovršite ih, a zatim se vratite na ovaj članak. 

Ovaj članak pruža informacije o postavljanju prilagođenih cjenovnih veličina. Na stranici **Parametri** kartica **Cjenovne veličine utemeljene na količini** prikazuje zapise u entitetima cjenovne veličine. Prema zadanim postavkama, u rešetci ove kartice nalaze se dva retka:

- **msdyn_resourcecategory** (Uloga)
- **msdyn_OrganizationalUnit** (Organizacijska jedinica)

> [!IMPORTANT]
> Nemojte izbrisati te retke. No, ako ih ne trebate, možete im onemogućiti primjenu u određenom kontekstu postavljanjem vrijednosti za **Primjenjivo na trošak**, **Primjenjivo na prodaju** i **Primjenjivo na kupnju** na **Ne** Postavljanje vrijednosti tih atributa na **Ne** ima isti učinak kao da nemate polje kao dimenziju cijena.

Da bi polje postalo dimenzija cijena, ono mora biti:

- Stvoreno kao polje u entitetima **Cijena uloge** i **Provizija cijene uloge**. Više informacija kako to napraviti potražite u odjeljku [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](add-custom-fields-price-setup-transactional-entities.md).

- Stvoreno kao redak u tablici **Dimenzija cijena**. Na primjer, dodajte retke dimenzije cijena kao što je prikazano na slici u nastavku. 

![Redci veličine za određivanje cijena koji se temelje na iznosu.](media/Amt-based-PD.png)

Radno vrijeme resursa (**msdyn_resourceworkhours**) dodano je kao veličina utemeljena na proviziji i dodana je u rešetku na kartici **Cjenovna veličina utemeljena na proviziji**.

![Redci veličine za određivanje cijena koji se temelje na proviziji.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Svaka izmjena podataka o dimenziji cijena u ovoj tablici, postojećih ili novih, prenosi se na poslovnu logiku određivanja cijena tek nakon osvježavanja predmemorije. Vrijeme osvježavanja predmemorije može trajati do 10 minuta. Pričekajte neko vrijeme dok se promjene ne prikažu u logici za postavljanje zadane cijene koja mora odražavati promjene u podacima dimenzije cijena.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Tablica atributa dimenzija cijena
Sljedeći odjeljci pružaju informacije o različitim atributima u tablici **Dimenzije cijena**.

### <a name="pricing-dimension-name"></a>Naziv dimenzije cijena
Ova bi vrijednost trebala točno odgovarati nazivu sheme polja koje je dodano u tablicu **Cijena uloge** za prilagođene dimenzije cijena. Dodatne informacije o dodavanju polja u tablicu **Cijena uloge** potražite u odjeljku [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Vrsta dimenzije
Postoje dvije vrste dimenzija cijena:
  
  - **Dimenzije utemeljene na iznosu**: vrijednosti dimenzije iz ulaznog konteksta podudaraju se s vrijednostima dimenzije u retku **Cijena uloge**, a cijena/trošak preuzete su kao zadane vrijednosti izravno iz tablice **Cijena uloge**.
  - **Veličine utemeljene na proviziji**: To su veličine za koje se upotrebljava sljedeći postupak u tri koraka kako bi se došlo do cijene/troška:
 
    1. Vrijednosti veličine koje nisu utemeljene na proviziji iz konteksta unosa podudaraju se s retkom Cijene uloge kako bi se dobila osnovna cijena.
    2. Vrijednosti veličine iz konteksta unosa podudaraju se s retkom **Provizija cijene uloge** kako bi se dobio postotak provizije.
    3. Postotak provizije iz drugog koraka primjenjuje se na osnovnu cijenu dobivenu iz tablice **Cijena uloge** u prvom koraku kako bi se došlo do konačne cijene/troška.
   
   U sljedećoj tablici prikazan je izračun provizija cijena.
  
| Uloga        | Org. jedinica    |Radno mjesto      |Radno mjesto – standardno      |Radno vrijeme resursa      |  Provizija|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso, Indija|Na lokaciji            |                    |Prekovremeni rad                 |15     |
|             | Contoso, Indija|Lokalno             |                    |Prekovremeni rad                 |10     |
|             | Contoso US   |Lokalno             |                    |Prekovremeni rad                 |20     |


Ako je resurs iz tvrtke Contoso Indija čija je osnovna stopa za rad na lokaciji 600,00 kn, a oni na unosu radnog vremena bilježe 8 sati redovitog i 2 sata prekovremenog rada, modul za određivanje cijena upotrebljava osnovnu cijenu od 600,00 kn za 8 sati kako bi se zabilježilo 4.800,00 kn. Za 2 sata prekovremenog rada na osnovnu stopu od 100 primjenjuje se provizija od 15% da bi se dobila jedinična cijena od 115 USD te se bilježi ukupni trošak od 230 USD.

### <a name="applicable-to-cost"></a>Primjenjivo na trošak 
Ako je ovo polje postavljeno na **Da**, to znači da bi se vrijednost dimenzije iz ulaznog konteksta trebala upotrijebiti za podudaranje s recima **Cijena uloge** i **Provizija cijene uloge** prilikom dohvaćanja stopa troška i provizije.

### <a name="applicable-to-sales"></a>Primjenjivo na prodaju
Ako je ovo polje postavljeno na **Da**, to znači da bi se vrijednost dimenzije iz ulaznog konteksta trebala upotrijebiti za podudaranje s recima **Cijena uloge** i **Provizija cijene uloge** prilikom dohvaćanja stopa naplate i provizije.

### <a name="applicable-to-purchase"></a>Primjenjivo na kupnju
Ako je ovo polje postavljeno na **Da**, to znači da bi se vrijednost dimenzije iz ulaznog konteksta trebala upotrijebiti za podudaranje s recima **Cijena uloge** i **Provizija cijene uloge** prilikom dohvaćanja kupovne cijene. Scenariji podugovaranja nisu podržani, pa se ovo polje ne upotrebljava. 

### <a name="priority"></a>Prioritet
Postavljanje prioriteta veličine omogućuje alatu za određivanje cijene da napravi cijenu, čak i kada ne može pronaći točno podudaranje između vrijednosti ulazne veličine i vrijednosti iz tablice **Cijena uloge** ili **Provizija cijene uloge**. U ovom scenariju vrijednosti nule upotrebljavaju se za vrijednosti veličine koje se ne podudaraju kako bi se dimenzije ponderirale po redoslijedu prioriteta.

- **Prioritet troška**: vrijednost prioriteta troška dimenzije ukazuje na ponder te dimenzije kada se usporedi s postavkama cijena koštanja. Vrijednost **Prioritet troška** mora biti jedinstvena u različitim dimenzijama koje su označene kao **Primjenjivo na trošak**.
- **Prioritet prodaje**: vrijednost prioriteta prodaje dimenzije ukazuje na ponder te dimenzije kada se usporedi s postavkama cijena prodaje ili stopa naplate. Vrijednost **Prioritet prodaje** mora biti jedinstvena u različitim dimenzijama koje su označene kao **Primjenjivo na prodaju**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]