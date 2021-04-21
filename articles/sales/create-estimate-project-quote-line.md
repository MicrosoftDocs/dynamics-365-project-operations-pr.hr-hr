---
title: Procjena retka ponude za projekt
description: U ovoj temi nalaze se informacije o načinu stvaranja procjene u retku ponude za projekt.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858779"
---
# <a name="estimate-a-project-quote-line"></a>Procjena retka ponude za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Redak ponude koji se temelji na projektu sadrži pojedinosti koje pomažu u procjeni troška i potencijalnih prihoda od posla potrebnog za isporuku retka ponude.

Kako biste procijenili redak ponude koji se temelji na projektu, u retku ponude odaberite karticu **Pojedinost retka ponude**. Postoje dva načina za stvaranje procjene u retku ponude koji se temelji na projektu:

   - Ručna izrada procjene izravno na retku ponude s pomoću pojedinosti retka ponude. 
   - Stvorite projekt i plan projekta, a zatim projekt i zadatke na projektu povežite s retkom ponude. Omogućit će se postupak uvoza procjena iz plana projekta u redak ponude koji se temelji na podacima koje ste naveli.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Stvaranje procjena izravno iz retka ponude koji se temelji na projektu

Kako biste stvorili procjene izravno na retku ponude koji se temelji na projektu, slijedite ove korake:

1. Kako biste stvorili procjenu iz retka ponude koji se temelji na projektu, odaberite karticu **Pojedinosti retka ponude**. Stavka retka koju stvarate na ovoj kartici sažet će ponuđenu vrijednost za ovaj redak ponude. 
2. Kako biste stvorili pojedinosti retka ponude, odaberite **Nove pojedinosti retka ponude** u podrešetki **Pojedinosti retka ponude**. Otvorit će se klizač za brzo stvaranje. Sljedeća polja na stranici **Redak ponude**.

| **Polje** | **Lokacija** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- | --- |
| Opis | Brzo stvaranje | Opis specifične procjene. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Razred transakcije | Brzo stvaranje | Ovaj padajući popis pruža klase transakcija koje su uključene u karticu **Općenito** retka ponude koji se temelji na projektu.  | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Odabir proizvoda | Brzo stvaranje | Primjenjuje se kada je klasa transakcije **Materijal**. Možete odabrati da navedete kako je ovaj redak procjene za **Postojeći** (kataloški) proizvod ili **Umetnut** proizvod. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Proizvod | Brzo stvaranje | ID proizvoda iz kataloga proizvoda. Ovo je polje omogućeno samo nakon što odaberete mogućnost **Postojeće** u polju **Odaberi proizvod**. ID se upotrebljava za dohvaćanje prodajne cijene iz cjenika za projekt u ponudi. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Upisani proizvod | Brzo stvaranje | Tekstni okvir za upisivanje naziva proizvoda. Ovo je polje omogućeno samo nakon što odaberete mogućnost **Umetni** u polju **Odaberi proizvod**.| Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Uloga | Brzo stvaranje | Uloga osobe koja će izvršiti ovaj posao ili snositi taj trošak. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Kategorija | Brzo stvaranje | Kategorija posla ili troška. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Datum početka | Brzo stvaranje | Datum početka posla. | Ovo je polje zadano za pojedinost retka ponude za trošak koji se automatski stvorio. |
| Datum završetka | Brzo stvaranje | Datum završetka posla. | Ovo je polje zadano za pojedinost retka ponude za trošak koji se automatski stvorio. |
| Tvrtka resursa | Brzo stvaranje | Tvrtka za resurse ili pravna osoba koja će snositi taj trošak i osigurati resurse za rad na njima. | Vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio i upotrijebio za dohvaćanje cijene koštanja. |
| Jedinica za resurse | Brzo stvaranje | Jedinica za resurse koja snosi taj trošak i osigurava resurse za rad na njima. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio i upotrijebio za dohvaćanje cijene koštanja. |
| Raspored jedinice | Brzo stvaranje | Grupa jedinica za rad, proizvod ili trošak. Jedinice koje pripadaju rasporedu jedinice ili grupi jedinica. Na primjer, milje i kilometri su jedinice koje pripadaju grupi jedinica koje opisuju udaljenost. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Jedinica | Brzo stvaranje | Jedinica za rad, proizvod ili trošak. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Količina | Brzo stvaranje | Količina rada, proizvoda ili troškova. | Ova je vrijednost zadana za pojedinost povezanog retka ponude za trošak koji se automatski stvorio. |
| Jedinična cijena | Brzo stvaranje |Cijena naplate uloge koja izvršava posao, jedinična cijena proizvoda ili prodajna cijena kategorije proizvoda ili troška. Zadana vrijednost za **Vrijeme** temelji se na kombinaciji vrijednosti veličina u retku cijene uloge cjenika za projekt koja vrijedi za datum početka. Za **Troškove**, zadana vrijednost dolazi iz postavke cijene za kategoriju transakcija u cjeniku za projekt koja vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije cijena po jedinici, nema zadane vrijednosti te ovo polje ostaje prazno. Za proizvode, zadana vrijednost za ovo polje temelji se na retku **Stavka cjenika** cjenika za projekta koji vrijedi za datum početka.| Cijena troška uloge koja izvršava posao, trošak po jedinici kategorije troška ili jedinični trošak proizvoda. Zadana vrijednost za **Vrijeme** temelji se na kombinaciji vrijednosti veličina u retku cijene uloge iz troškovnika priloženog ugovornoj jedinici koja vrijedi za datum početka. Za troškove, zadana se vrijednost temelji na retku cijene kategorije iz troškovnika priloženog ugovornoj jedinici koji vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije cijena po jedinici, nema zadane vrijednosti i ovo polje ostaje prazno. Za proizvode, zadana vrijednost ovog polja temelji se na retku **Stavke cjenika** iz troškovnika priloženog ugovornoj jedinici koji vrijedi za datum početka.|
| Procijenjeni porez | Brzo stvaranje | Možete ručno unijeti procijenjeni porez za ovaj rad ili trošak. | Ovo polje ne utječe na niže razine. |
| Iznos | Brzo stvaranje | U ovo polje možete ručno unijeti podatke ako polja **Količina** i **Cijena** ostaju prazna. Ako ta polja nisu prazna, ovo polje postaje polje samo za čitanje i izračunava se kao (Količina \* Jedinična cijena) + Porez. | Ovo polje ne utječe na niže razine. |

## <a name="update-prices-on-quote-line-details"></a>Ažuriranje cijena na pojedinostima retka ponude

Ako ste promijenili cijene na cjeniku projekta koji je priložen uz ponudu ili na popisu cijena koštanja ugovorne jedinice, možete odabrati **Preračunaj** na stranici **Ponuda** kako biste osvježili cijene na pojedinostima pojedinog retka ponude kako bi odražavale ovu promjenu. Kad odaberete **Preračunaj**, prikazuje se upozorenje koje vas izvješćuje da će se cijene na pojedinostima retka ponude, u svim redcima te ponude, vratiti na zadane. Odaberite **Da** kako biste osvježili cijene pojedinosti redaka ponude i prodaje i troška.

## <a name="access-quote-line-details-for-cost"></a>Pristup pojedinostima retka ponude za trošak

Kako biste pristupili pojedinostima retka ponude o trošku, slijedite ove korake:

1. Na kartici **Pojedinosti retka ponude** odaberite redak u rešetki kako biste omogućili radnje na alatnoj traci podrešetke. 
2. Odaberite **Pojedinosti otvorenog troška** kako biste vidjeli povezanu cijenu troška i iznos za taj redak ponude.

> [!NOTE]
> Izmjena vrijednosti resursne jedinice, količine, datuma, uloge ili kategorije na pojedinosti retka ponude promijenit će odgovarajuće vrijednosti na pojedinostima retka ponude za prodaju.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta pojedinostima retka ponude za trošak i prodaju

Valuta na pojedinosti retka ponuda za prodaju zadana je iz cjenika za projekt koji vrijedi za datum početka pojedinosti retka ponude.

Valuta na pojedinosti retka ponuda za trošak zadana je iz cjenika za ugovornu jedinicu ponude koja vrijedi za datum početka pojedinosti retka ponude o trošku.

> [!NOTE]
> Izračuni profitabilnosti pretvaraju iznos pojedinosti retka ponude za troškove i prodaju u osnovnu valutu okruženja kako bi se prijavila ukupna procijenjena marža ponude. Pogreške u zaokruživanju valuta i izmjena marži mogli bi se dogoditi zbog nedostatka tečajeva koji su na snazi na određeni datum. Upotrebljavajte ove izračune samo na ponudama za projekt, jer su to približni podaci i nisu stvarno propisani ili drugo izvještavanje koje zahtijeva veću preciznost zaokruživanja i svijest o učinkovitosti datuma za tečajeve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
