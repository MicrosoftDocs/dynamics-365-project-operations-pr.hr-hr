---
title: Zamjene cijena s datumom stupanja na snagu
description: U ovom se članku objašnjava način postavljanja zamjene cijena za određene cijene u cjeniku.
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
# <a name="date-effective-price-overrides"></a>Zamjene cijena s datumom stupanja na snagu 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

*Zamjene cijena s datumom stupanja na snagu* omogućuje način za zamjenu ili promjenu određenih cijena u cjeniku. Primjerice, imate standardni cjenik koji je na snazi od 1. siječnja 2022. do 31. prosinca 2022. Ovaj cjenik ima cijene za mnoge uloge. Cijena koja je postavljena za ulogu **Tehničar za mrežu** iznosi 100 američkih dolara (USD) po satu. Kada mrežni tehničar bilježi vrijeme između 1. siječnja 2022. i 31. prosinca 2022., cijena vremena iznosi 100 USD. 1. listopada 2022. morate prilagoditi cijenu *samo* za ulogu **Tehničar za mrežu**, i to s 100 USD po satu na 110 USD po satu. Značajka **Zamjena cijena s datumom stupanja na snagu** omogućuje vam da postavite ovu promjenu kao zamjenu retka za cijenu te određene uloge. Dakle, ne morate kopirati cijeli cjenik i mijenjati cijenu samo u tom jednom retku.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Zamjena cijena s datumom stupanja na snagu za cijene rada

Proces postavljanja zamjena cijena s datumom stupanja na snagu za radno vrijeme na projektu sastoji se od dva osnovna koraka.

1. Omogućite značajku **Zamjene cijena s datumom stupanja na snagu**.
1. Postavite zamjenu cijena s datumom stupanja na snagu.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Omogućavanje značajke Zamjene cijena s datumom stupanja na snagu

> [!NOTE]
> Nakon što se značajka **Zamjena cijena s datumom stupanja na snagu** omogući, ne može se onemogućiti.

Da biste omogućili značajku **Zamjena cijena s datumom stupanja na snagu**, slijedite ove korake.

1. Idite na **Postavke** \> **Parametri**.
1. Otvorite zapis **Parametri**.
1. U Oknu radnji, na kartici **Kontrola značajke**, odaberite **Omogući zamjenu cijene s datumom stupanja na snagu**.
1. U potvrdnom dijaloškom okviru kliknite **U redu**.
1. Osvježite preglednik nakon nekoliko trenutaka. Mogućnosti zamjene cijene s datumom stupanja na snagu sada bi trebale biti dostupne. Znat ćete da su te mogućnosti omogućene ako se opcija **Omogući zamjenu cijene s datumom stupanja na snagu** više ne pojavljuje u Oknu radnji.

### <a name="set-up-a-date-effective-price-override"></a>Postavljanje zamjene cijene s datumom stupanja na snagu

Zamjene cijene s datumom stupanja na snagu mogu se postaviti na cjenicima **Trošak**, **Prodaja** ili **Kupnja**.

> [!NOTE]
>Ponašanje značajke **Zamjene cijene s datumom stupanja na snagu** trenutno ima sljedeća ograničenja:
>
> - Značajka **Zamjena cijene s datumom stupanja na snagu** podržana je samo za cijene uloge i marže cijene uloge u aplikaciji Project Operations.
> - Kada kopirate cjenik s pomoću radnje **Kopiraj** na stranici **Detalji cjenika** i kada izradite cjenik projekta iz standardnog ili prilagođenog cjenika tijekom izrade ugovora, zamjene cijene s datumom stupanja na snagu **ne** kopiraju se iz izvornog cjenika.

Da biste postavili zamjenu cijene s datumom stupanja na snagu za cijenu uloge ili maržu cijene uloge, slijedite ove korake.

1. Otvorite stranicu za cjenik za koji želite postaviti zamjenu cijene s datumom stupanja na snagu.
1. Odaberite karticu **Cijene uloga**. U toj se kartici navode svi zapisi **Cijene uloge** u cjeniku.
1. Odaberite zapis **Cijene uloge** za koji želite postaviti novu zamjensku cijenu s datumom stupanja na snagu, a zatim dvaput dodirnite (ili dvaput kliknite) **Cijena uloge** da biste otvoriti stranicu **Pojedinosti o cijeni uloge**.
1. Odaberite karticu **Datum stupanja na snagu nadjačava**. Rešetka na ovoj kartici navodi sve promjene cijena s datumom na snagu za odabrani zapis **Cijena uloge**.
1. Na alatnoj traci iznad rešetke odaberite **Nova zamjena cijene uloge**. Otvara se klizač **Nova zamjena cijene uloge**.
1. Navedite datum stupanja na snagu, jedinicu i novu cijenu za zamjenu cijene. Zatim odaberite **Spremi** i zatvorite obrazac.

> [!NOTE]
> - Zamjena cijene s datumom stupanja na snagu za cijenu uloge ili maržu cijene uloge primjenjivo je na istu kombinaciju vrijednosti dimenzije cijene koja postoji u nadređenom retku **Cijena uloge** ili **Marža cijene uloge**.
> - Datum koji se odabere u polju **Na snazi od** treba biti unutar datuma stupanja na snagu matičnog cjenika. Zamjena cijene stupit će na snagu na datum koji je odabran u polju **Na snazi od** i primjenjivat će se do datuma završetka matičnog cjenika. Ako postavite još jednu zamjenu cijene s datumom stupanja na snagu za istu cijenu uloge, prva zamjena cijene stupit će na snagu na datum koji je odabran u polju **Na snazi od** i primjenjivat će se do početka druge zamjene.

## <a name="examples"></a>Primjeri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Primjer 1: određivanje datuma stupanja na snagu za cijenu uloge koja ima zamjene cijene uloge

Sljedeći primjer pokazuje kako se datum stupanja na snagu određuje za određenu cijenu uloge za koju su postavljene zamjene cijene uloge.

**Cjenik A: od 1. siječnja do 30. lipnja**

*Cijena uloge*

| Cijena uloge | Jedinica | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|---|
| Tehničar za mrežu | h | 100 | Ta će se cijena upotrebljavati za sve transakcije čiji je datum transakcije između 1. siječnja i 14. ožujka. |

*Zamjena cijene uloge*

| Na snazi od | Jedinica | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|---|
| Ožujak 15. | h | 110 | Ta će se cijena upotrebljavati za sve transakcije čiji je datum transakcije između 15. ožujka i 30. ožujka. |
| Travanj 1. | h | 120 | Ta će se cijena upotrebljavati za sve transakcije čiji je datum transakcije između 1. travnja i 30. lipnja. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Primjer 2: određivanje datuma stupanja na snagu za maržu cijene uloge koja ima zamjene marže cijene uloge

Sljedeći primjer pokazuje kako se datum stupanja na snagu određuje za određenu maržu cijene uloge za koju su postavljene zamjene marže cijene uloge.

**Cjenik A: od 1. siječnja do 30. lipnja**

*Cijena uloge*

| Cijena uloge | Radni sati | Jedinica | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|---|---|
| Tehničar za mrežu | Regularno | h | 100 | Ta će se cijena upotrebljavati za sve transakcije čiji je datum transakcije između 1. siječnja i 14. ožujka. |

*Marža cijene uloge*

| Organizacijska jedinica | Radni sati | Marža % |
|---|---|---|
| Contoso US | Prekovremeni rad | 10 % |

*Zamjena marže cijene uloge*

| Na snazi od | Cijena | Učinak na cijene za dolazne transakcije |
|---|---|---|
| Ožujak 15. | 20 % | Taj će se postotak marže upotrebljavati za sve transakcije čiji je datum transakcije između 15. ožujka i 30. ožujka. |
| Travanj 1. | 25 % | Ta će se marža upotrebljavati za sve transakcije čiji je datum transakcije između 1. travnja i 30. lipnja. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
