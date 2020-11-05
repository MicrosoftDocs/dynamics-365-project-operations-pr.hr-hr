---
title: Procjena retka ponude utemeljenog na projektu
description: U ovoj temi nalaze se informacije o načinu stvaranja procjene retka ponude koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073292"
---
# <a name="estimating-a-project-based-quote-line"></a>Procjena retka ponude utemeljenog na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Redak ponude koji se temelji na projektu sadrži pojedinosti koje pomažu u procjeni troška i potencijalnih prihoda od posla potrebnog za isporuku retka ponude.

Za procjenu retka ponude koji se temelji na projektu, na retku ponude koji se temelji na projektu odaberite karticu **Pojedinosti retka ponude**. Postoje dva načina za stvaranje procjene na retku ponude koji se temelji na projektu:

- Ručna izrada procjene izravno na retku ponude s pomoću pojedinosti retka ponude 
- Stvorite projekt i plan projekta, a zatim projekt i zadatke na projektu povežite s retkom ponude. Omogućit će se postupak uvoza procjena iz plana projekta u redak ponude koji se temelji na podacima koje ste naveli.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Stvaranje procjena izravno iz retka ponude koji se temelji na projektu

Kako biste stvorili procjenu iz retka ponude koji se temelji na projektu, odaberite karticu **Pojedinosti retka ponude**. Stavka retka koju stvarate na ovoj kartici sažet će ponuđenu vrijednost za ovaj redak ponude. 

Kako biste stvorili pojedinosti retka ponude, odaberite **+ Nova pojedinost retka ponude** na podrešetki **Pojedinosti retka ponude**. Otvorit će se klizač za brzo stvaranje. Sljedeća polja na obrascu **Redak ponude** :

| **Polje** | **Mjesto** | **Relevantnost, svrha i smjernice** | **Utjecaj na niže razine** |
| --- | --- | --- | --- |
| Opis | Brzo stvaranje | Opis specifične procjene. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Razred transakcije | Brzo stvaranje | Ovaj padajući popis pruža klase transakcija koje su uključene u karticu **Općenito** retka ponude koji se temelji na projektu.  | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Uloga | Brzo stvaranje | Osoba koja će obaviti ovaj posao ili snositi taj trošak. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Kategorija | Brzo stvaranje | Kategorija posla ili troška. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Datum početka | Brzo stvaranje | Datum početka posla. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Datum završetka | Brzo stvaranje | Datum završetka posla. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Jedinica za resurse | Brzo stvaranje | Resursna jedinica koja će snositi ovaj trošak i osigurati resurs za rad na tome. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. Ovo se polje također upotrebljava za pronalaženje cijene koštanja. |
| Raspored jedinice | Brzo stvaranje | Grupa jedinica rada ili troška. Jedinice koje pripadaju rasporedu jedinice ili grupi jedinica. Na primjer, milje i kilometri jedinice su koje pripadaju grupi jedinica koje opisuju udaljenost. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Jedinica | Brzo stvaranje | Jedinica rada ili troška. | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Količina | Brzo stvaranje | Količina rada ili troška | Ovo se polje prema zadanim postavkama odnosi na pojedinosti retka ponude za trošak koji se automatski stvara. |
| Jedinična cijena | Brzo stvaranje | Cijena plaćanja uloge koja izvršava posao ili prodajna cijena kategorije troška. Ovo polje zadaje vrijednost za Vrijeme koje se temelji na ulozi i kombinaciji resursne jedinice na cjeniku projekta koji vrijedi za datum početka. Za troškove, ovo se polje zadaje iz postavke cijene za kategoriju transakcije u cjeniku projekta koji vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije cijena po jedinici, nema zadane vrijednosti te ovo polje ostaje prazno. | Cijena troška uloge koja izvršava posao ili trošak po jedinici kategorije troška. Ovo polje zadaje vrijednost za Vrijeme koje se temelji na ulozi i kombinaciji resursne jedinice na cijeni ugovorne jedinice cjenika ponude koji vrijedi za datum početka. Za troškove, ovo se polje zadaje iz postavke cijene za kategoriju transakcije u cjeniku troškova ugovorne jedinice koji vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije cijena po jedinici, nema zadane vrijednosti te ovo polje ostaje prazno. |
| Procijenjeni porez | Brzo stvaranje | Možete ručno unijeti procijenjeni porez za ovaj rad ili trošak. | Nema utjecaja ovog polja na niže razine. |
| Iznos | Brzo stvaranje | U ovo polje možete ručno unijeti podatke ako polja **Količina** i **Cijena** ostaju prazna. Ako ta polja nisu prazna, ovo polje postaje polje samo za čitanje i izračunava se kao (Količina \* Jedinična cijena) + Porez. | Nema utjecaja ovog polja na niže razine. |

## <a name="update-prices-on-quote-line-details"></a>Ažuriranje cijena na pojedinostima retka ponude

Ako ste promijenili cijene na cjeniku projekta koji je priložen uz ponudu ili na popisu cijena koštanja ugovorne jedinice, možete odabrati **Preračunaj** na stranici **Ponuda** kako biste osvježili cijene na pojedinostima pojedinog retka ponude kako bi odražavale ovu promjenu. Kad odaberete **Preračunaj** prikazuje se upozorenje koje vas izvješćuje kako će se cijene na pojedinostima retka ponude za sve retke ponude iz ove ponude poništiti. Odaberite **Da** kako biste osvježili cijene pojedinosti redaka ponude i prodaje i troška.

## <a name="access-quote-line-details-for-cost"></a>Pristup pojedinostima retka ponude za trošak

Na kartici **Pojedinosti retka ponude** odaberite redak u rešetki kako biste omogućili neke radnje na alatnoj traci podrešetke. Prva radnja na alatnoj traci podrešetke kada se odabere pojedinost retka ponude je **Pojedinost otvorenog troška**. Odaberite **Pojedinosti otvorenog troška** kako biste vidjeli povezanu cijenu troška i iznos za taj redak ponude.

> [!NOTE]
> Izmjena vrijednosti resursne jedinice, količine, datuma, uloge ili kategorije na pojedinosti retka ponude promijenit će odgovarajuće vrijednosti na pojedinostima retka ponude za prodaju.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta pojedinostima retka ponude za trošak i prodaju

Valuta pojedinosti retka ponude za zadane vrijednosti prodaje iz cjenika projekta koji vrijedi za datum početka pojedinosti retka ponude.

Valuta pojedinosti retka ponude za zadane vrijednosti troška iz cjenika ugovorne jedinice ponude koji vrijedi za datum početka pojedinosti retka ponude za trošak.

Izračuni profitabilnosti pretvaraju iznos pojedinosti retka ponude za troškove i prodaju u osnovnu valutu okruženja kako bi se prijavila ukupna procijenjena marža ponude.

To bi moglo rezultirati pogreškama pri zaokruživanju valute i promjenom marži zbog nedostatka tečajeva koji vrijede na određeni datum. Ove izračune upotrijebite na ponudama projekta samo kao približne vrijednosti, a ne stvarno zakonsko ili drugo izvješćivanje koje zahtijeva veću preciznost zaokruživanja i saznanje o tečajevima koji vrijede na određeni datum.
