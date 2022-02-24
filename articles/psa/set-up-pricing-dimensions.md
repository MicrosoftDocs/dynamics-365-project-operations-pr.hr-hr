---
title: Postavljanje prilagođenih polja kao cjenovnih veličina
description: Ovaj tema pruža informacije o postavljanju prilagođenih dimenzija cijena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150344"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Postavljanje prilagođenih polja kao cjenovnih veličina 

[!include [banner](../includes/psa-now-project-operations.md)]

Prije početka rada, ova tema podrazumijeva da ste dovršili postupke opisane u temama [Izrada prilagođenih polja i entiteta](create-custom-fields-entities.md) i [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](field-references.md). Ako niste dovršili te postupke, vratite se i dovršite ih, a zatim se vratite na ovu temu. 

Ovaj tema pruža informacije o postavljanju prilagođenih dimenzija cijena. Na web-sučelju programa Project Service, na stranici **Parametar**, na kartici **Dimenzije cijena na temelju iznosa** prikazuju se zapisi u entitetu dimenzije cijena. Prema zadanim postavkama, instalacijom programa Project Service stvaraju se 2 retka u rešetki na ovoj kartici:

- **msdyn_resourcecategory** (Uloga)
- **msdyn_OrganizationalUnit** (Organizacijska jedinica)

> [!IMPORTANT]
> Nemojte izbrisati te retke. No, ako ih ne trebate, možete im onemogućiti primjenu u određenom kontekstu postavljanjem vrijednosti za **Primjenjivo na trošak**, **Primjenjivo na prodaju** i **Primjenjivo na kupnju** na **Ne** Postavljanje vrijednosti tih atributa na **Ne** ima isti učinak kao da nemate polje kao dimenziju cijena.

Da bi polje postalo dimenzija cijena, ono mora biti:

- Stvoreno kao polje u entitetima **Cijena uloge** i **Provizija cijene uloge**. Više informacija kako to napraviti potražite u odjeljku [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](field-references.md).
- Stvoreno kao redak u tablici **Dimenzija cijena**. Na primjer, dodajte retke dimenzije cijena kao što je prikazano na slici u nastavku. 

![Dimenzije cijena utemeljene na iznosu](media/Amt-based-PD.png)

Primijetite da je radno vrijeme resursa **(** msdyn_resourceworkhours) dodano kao dimenzija utemeljena na proviziji te da je dodano u rešetku na kartici **Dimenzija cijena utemeljene na proviziji**.

![Reci dimenzije cijena utemeljene na proviziji](media/Markup-based-PD.png)

> [!IMPORTANT]
> Svaka izmjena podataka o dimenziji cijena u ovoj tablici, postojećih ili novih, prenosi se na poslovnu logiku određivanja cijena programa Project Service tek nakon osvježavanja predmemorije. Vrijeme osvježavanja predmemorije može trajati do 10 minuta. Pričekajte neko vrijeme dok se promjene ne prikažu u logici za postavljanje zadane cijene koja mora odražavati promjene u podacima dimenzije cijena.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Tablica atributa dimenzija cijena
Sljedeći odjeljci pružaju informacije o različitim atributima u tablici **Dimenzije cijena**.

### <a name="pricing-dimension-name"></a>Naziv dimenzije cijena
Ova bi vrijednost trebala točno odgovarati nazivu sheme polja koje je dodano u tablicu **Cijena uloge** za prilagođene dimenzije cijena. Dodatne informacije o dodavanju polja u tablicu **Cijena uloge** potražite u odjeljku [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](field-references.md).

### <a name="type-of-dimension"></a>Vrsta dimenzije
Postoje dvije vrste dimenzija cijena:
  
  - **Dimenzije utemeljene na iznosu**: vrijednosti dimenzije iz ulaznog konteksta podudaraju se s vrijednostima dimenzije u retku **Cijena uloge**, a cijena/trošak preuzete su kao zadane vrijednosti izravno iz tablice **Cijena uloge**.
  - **Dimenzije utemeljene na proviziji**: ovo su dimenzije za koje se u programu Project Service uvodi sljedeći postupak u 3 koraka da bi se došlo do cijene/troška.
 
    1. Project Service pronalazi vrijednosti dimenzija koje nisu utemeljene na proviziji iz ulaznog konteksta, a podudaraju se s retkom Cijena uloga da bi se dobila osnovna stopa.
    2. Project Service pronalazi sve vrijednosti dimenzija iz ulaznog konteksta koje odgovaraju retku **Provizija cijene uloge** da bi se dobio postotak provizije.
    3. Project Service primjenjuje postotak provizije iz drugog koraka u osnovnu stopu dobivenu iz tablice **Cijena uloga** u prvom koraku da bi se došlo do konačne cijene/troška.
   
   U sljedećoj tablici prikazan je izračun provizija cijena.
  
| Uloga        | Org. jedinica    |Radno mjesto      |Radno mjesto – standardno      |Radno vrijeme resursa      |  Provizija|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso, Indija|Na lokaciji            |                    |Prekovremeni rad                 |15     |
|             | Contoso, Indija|Lokalno             |                    |Prekovremeni rad                 |10     |
|             | Contoso US   |Lokalno             |                    |Prekovremeni rad                 |20     |


Ako je resurs iz tvrtke Contoso, Indija čija je osnovna stopa 100 USD radi na lokaciji, a oni bilježe 8 sati uobičajenog radnog vremena i 2 sata prekovremenog rada, program za određivanje cijena Project Service upotrebljava osnovnu stopu od 100 za 8 sati kako bi se zabilježilo 800 USD. Za 2 sata prekovremenog rada na osnovnu stopu od 100 primjenjuje se provizija od 15% da bi se dobila jedinična cijena od 115 USD te se bilježi ukupni trošak od 230 USD.

### <a name="applicable-to-cost"></a>Primjenjivo na trošak 
Ako je ovo polje postavljeno na **Da**, to znači da bi se vrijednost dimenzije iz ulaznog konteksta trebala upotrijebiti za podudaranje s recima **Cijena uloge** i **Provizija cijene uloge** prilikom dohvaćanja stopa troška i provizije.

### <a name="applicable-to-sales"></a>Primjenjivo na prodaju
Ako je ovo polje postavljeno na **Da**, to znači da bi se vrijednost dimenzije iz ulaznog konteksta trebala upotrijebiti za podudaranje s recima **Cijena uloge** i **Provizija cijene uloge** prilikom dohvaćanja stopa naplate i provizije.

### <a name="applicable-to-purchase"></a>Primjenjivo na kupnju
Ako je ovo polje postavljeno na **Da**, to znači da bi se vrijednost dimenzije iz ulaznog konteksta trebala upotrijebiti za podudaranje s recima **Cijena uloge** i **Provizija cijene uloge** prilikom dohvaćanja kupovne cijene. Project Service trenutačno ne podržava scenarije podugovaranja, pa da se ovo polje ne koristi. 

### <a name="priority"></a>Prioritet
Postavljanje prioriteta dimenzije omogućuje određivanje cijene u programu Project Service, čak i kada ne može pronaći točno podudaranje između vrijednosti ulazne dimenzije i vrijednosti iz tablice **Cijena uloge** ili **Provizija cijene uloge**. U ovom scenariju Project Service upotrebljava vrijednosti null za vrijednosti dimenzija koje se ne podudaraju kako bi se dimenzije ponderirale po redoslijedu prioriteta.

- **Prioritet troška**: vrijednost prioriteta troška dimenzije ukazuje na ponder te dimenzije kada se usporedi s postavkama cijena koštanja. Vrijednost **Prioritet troška** mora biti jedinstvena u različitim dimenzijama koje su označene kao **Primjenjivo na trošak**.
- **Prioritet prodaje**: vrijednost prioriteta prodaje dimenzije ukazuje na ponder te dimenzije kada se usporedi s postavkama cijena prodaje ili stopa naplate. Vrijednost **Prioritet prodaje** mora biti jedinstvena u različitim dimenzijama koje su označene kao **Primjenjivo na prodaju**.
