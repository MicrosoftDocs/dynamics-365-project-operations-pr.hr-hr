---
title: Datum na snazi nadjačavanja cijena
description: U ovom se članku objašnjava kako postaviti nadjačavanje cijena za određene cijene u cjeniku.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445998"
---
# <a name="date-effective-price-overrides"></a>Datum na snazi nadjačavanja cijena 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

*Nadjačavanja* cijena s datumskom učinkovitošću omogućuju nadjačavanje ili promjenu određenih cijena u cjeniku. Na primjer, imate standardni cjenik koji stupa na snagu od 1. siječnja 2022. do 31. prosinca 2022. Ovaj cjenik ima cijene za mnoge uloge. Cijena koja je postavljena za ulogu mrežnog tehničara **je** 100 američkih dolara (USD) po satu. Kada mrežni tehničar zabilježi vrijeme između 1. siječnja 2022. i 31. prosinca 2022., cijena mu je 100 USD. Dana 1. listopada 2022. morate prilagoditi cijenu *samo* za ulogu mrežnog **tehničara**, od 100 USD po satu do 110 USD po satu. Značajka efektivne **cijene datumskog nadjačavanja** omogućuje vam postavljanje ove promjene kao poništenja retka za tu određenu cijenu uloge. Stoga ne morate kopirati cijeli cjenik i mijenjati cijenu samo tog jednog retka.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Datum na snazi za nadjačavanje cijena za cijene rada

Proces postavljanja datuma efektivnih nadjačavanja cijena za radno vrijeme na projektu sastoji se od dva osnovna koraka.

1. Omogući **značajku efektivnih nadjačavanja** cijena datuma.
1. Postavite poništenje cijene na datumskom učinkovitošću.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Omogućivanje značajke datumskih efektivnih nadjačavanja cijena

> [!NOTE]
> Nakon što je omogućena **značajka datumskog efektivnog nadjačavanja** cijena, ona se ne može onemogućiti.

Da biste omogućili **značajku nadjačavanja cijena na datum, slijedite** ove korake.

1. Otvorite **Parametri postavki** \> **·**.
1. **Otvorite zapis Parametri**.
1. U oknu akcije na **kartici Kontrola** značajki odaberite **Omogući nadjačavanje** cijena na datum.
1. U potvrdnom dijaloškom okviru kliknite **U redu**.
1. Nakon nekoliko trenutaka osvježite preglednik. Mogućnosti za nadjačavanje cijena na datum stupanja na snagu sada bi trebale biti dostupne. Znat ćete da su te mogućnosti omogućene ako **se u oknu akcije više ne pojave mogućnosti Omogući poništenja** cijena s datumom.

### <a name="set-up-a-date-effective-price-override"></a>Postavljanje nadjačavanja cijene na datumsku snagu

Datumski efektivna poništenja cijena mogu se postaviti na **cjenicima troškova**, **prodaje** ili **Nabave**.

> [!NOTE]
>Ponašanje datuma efektivnih **nadjačavanja** cijena trenutno ima sljedeća ograničenja:
>
> - Samo cijene uloga i oznake cijena uloga podržavaju **značajku datuma efektivnog nadjačavanja** cijena u operacijama projekta.
> - Kada kopirate cjenik pomoću **akcije Kopiraj** na **stranici s detaljima cjenika** i kada kreirate cjenik projekta iz standardnog ili prilagođenog cjenika tijekom stvaranja ugovora, datumski efektivna povećanja cijena ne **kopiraju se** iz izvornog cjenika.

Da biste postavili poništenje cijene koja stupa na snagu datuma za cijenu uloge ili oznaku cijene uloge, slijedite ove korake.

1. Otvorite stranicu cjenika za koji želite postaviti poništenje cijene na datum.
1. Odaberite karticu **Cijene** uloga. Ova kartica prikazuje sve zapise **cijena** Uloga u cjeniku.
1. **Odaberite zapis cijene** uloge za koji želite postaviti novu cijenu nadjačavanja koja stupa na snagu datuma, a zatim dvaput dodirnite (ili dvokliknite) **cijenu** uloge da biste otvorili **stranicu Detalji o** cijeni uloge.
1. Odaberite karticu **Efektivna poništenja** datuma. Rešetka na ovoj kartici navodi sva nadjačavanja cijena na datumskom efektivu za odabrani **zapis cijene** uloge.
1. Na alatnoj traci iznad rešetke odaberite **Novo nadjačavanje** cijene uloge. Otvorit će se **klizač Nadjačavanje** cijene nove uloge.
1. Navedite datum stupanja na snagu, jedinicu i novu cijenu za nadjačavanje cijene. Zatim odaberite **Spremi** i zatvorite obrazac.

> [!NOTE]
> - Datumsko povećanje cijene za cijenu uloge ili oznaku cijene uloge primjenjuje se na istu kombinaciju vrijednosti dimenzije određivanja cijena koja postoji u nadređenoj **cijeni** uloge ili **retku cijene** Role.
> - Datum odabran u polju Stupa na **snagu iz** trebao bi biti unutar datuma stupanja na snagu nadređenog cjenika. Nadjačavanje cijena stupit će na snagu na datum koji je odabran u **polju Stupi na snagu iz** i primjenjivat će se do kraja datuma završetka nadređenog cjenika. Ako postavite drugo nadjačavanje cijene na datum na snagu za istu cijenu uloge, prvo nadjačavanje cijene stupit će na snagu na datum koji je odabran u **polju Stupi na snagu iz** i primjenjivat će se do početka drugog poništenja.

## <a name="examples"></a>Primjeri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Primjer 1: Određivanje efektivnosti datuma za cijenu uloge koja ima nadjačavanje cijene uloge

Sljedeći primjer pokazuje kako se određuje efektivnost datuma za određenu cijenu uloge za koju su postavljena nadjačavanja cijena uloge.

**Cjenik A: od 1. siječnja do 30. lipnja**

*Cijena uloge*

| Cijena uloge | Jedinica | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|---|
| Mrežni tehničar | h | 100 | Ta će se cijena koristiti za sve transakcije u kojima je datum transakcije između 1. siječnja i 14. ožujka. |

*Nadjačavanje cijene uloge*

| Efektivno od | Jedinica | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|---|
| Ožujak 15. | h | 110 | Ta će se cijena koristiti za sve transakcije u kojima je datum transakcije između 15. i 30. ožujka. |
| Travanj 1. | h | 120 | Ta će se cijena koristiti za sve transakcije u kojima je datum transakcije između 1. travnja i 30. lipnja. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Primjer 2:Određivanje efektivnosti datuma za oznaku cijene uloge koja ima nadjačavanje oznake cijene uloge

Sljedeći primjer pokazuje kako se određuje efektivnost datuma za određenu oznaku cijene uloge za koju su postavljena nadjačavanja cijene role.

**Cjenik A: od 1. siječnja do 30. lipnja**

*Cijena uloge*

| Cijena uloge | Radni sati | Jedinica | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|---|---|
| Mrežni tehničar | Redovan | h | 100 | Ta će se cijena koristiti za sve transakcije u kojima je datum transakcije između 1. siječnja i 14. ožujka. |

*Oznaka cijene uloge*

| Organizacijska jedinica | Radni sati | Obilježi % |
|---|---|---|
| Contoso US | Prekovremeni rad | 10 % |

*Nadjačavanje oznake cijene uloge*

| Efektivno od | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|
| Ožujak 15. | 20 % | Taj postotak marže koristit će se za sve transakcije u kojima je datum transakcije između 15. i 30. ožujka. |
| Travanj 1. | 25 % | Ta će se marža koristiti za sve transakcije u kojima je datum transakcije između 1. travnja i 30. lipnja. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
