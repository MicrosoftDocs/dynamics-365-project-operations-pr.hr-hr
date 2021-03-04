---
title: Predujmovi i ugovori koji se temelje na akontaciji
description: U ovoj se temi nalaze informacije o ugovornim modelima koji se temelje na akontaciji i predujmovima u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1aee64bf683b7d8d0bcde284f2d5d484e689c4d2
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596093"
---
# <a name="advances-and-retainer-based-contracts"></a>Predujmovi i ugovori koji e temelje na povremenim plaćanjima


_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations podržava ugovore koji se temelje na akontacijama. Ugovor koji se temelji na akontaciji pregovarački je skup jednako raspoređenih plaćanja za koje će se klijentu fakturirati tijekom trajanja projekta. Ova vrsta ugovora obično se upotrebljava za modele naplate za vrijeme i materijal ili koji se temelje na potrošnji, gdje je klijentu potrebno dati predvidljivi račun i raspored plaćanja. Stvarni prihodi prikupljeni u svakom razdoblju usklađuju se s uplatom primljenom od klijenta na početku razdoblja. U skladu s konceptom modela naplate vremena i materijala, vrijednosti prihoda nastale u svakom razdoblju mogu se razlikovati ovisno o nastalim troškovima. Ako je ostvareni prihod veći od iznosa primljenog na početku razdoblja, tvrtka za dostavu projekata mogla bi:

- Klijentu fakturirajte samo višak 
- Odgoditi usklađivanje prihoda za sljedeće razdoblje fakturiranja i na kraju projekta napraviti jedan konačni račun za preostali neusuglašeni prihod

Glavna razlika između modela ugovora koji se temelji na akontaciji i modela ugovora s fiksnom cijenom u aplikaciji Project Operations je ta što u modelu ugovora s fiksnom cijenom iznos fakture nije povezan ili vezan s nastalim troškovima. Fakturiranje slijedi pristup koji se temelji na kontrolnim točkama i usklađen je s troškovima nastalim u tom razdoblju. U ugovoru koji se temelji na akontaciji, prihod koji se može fakturirati bilježi se na temelju načina naplate u retku ugovora. Kad je način naplate vrijeme i materijal, prihod koji se može fakturirati vezan je za troškove nastale u bilo kojem danom razdoblju i može se razlikovati od razdoblja do razdoblja. Međutim, klijentu se fakturira samo iznos periodične akontacije. Sustav upotrebljava drugu fakturu na kraju razdoblja za usklađivanje fakturiranog prihoda evidentiranog tijekom razdoblja u odnosu na iznos koji je klijentu fakturiran na početku razdoblja.

Prednost ovog načina je što troškovi klijenta postaju predvidivi u rasporedu akontacija, za razliku od uobičajenog modela vremena i materijala. Tvrtka ili ustanova koja dostavlja projekt također ima prostora za pokrivanje rizika povrata troškova nastalih uslijed bilo kakvog povećanja opsega, što im model fiksne cijene ne bi omogućio.

Uz periodični raspored koji se temelji na akontaciji, Project Operations mogu zabilježiti jednokratni predujam od klijenta i uskladiti ga s različitim komponentama troškova projekta.

Akontacija u aplikaciji Project Operations nije dostupna za uporabu dok se ne fakturira klijentu. To pokazuju sljedeća polja na podrešetki za predujmove i akontacije.

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| Dostupni iznos | Iznos koji je dostupan za uporabu na zapisu akontacije ili predujma. | Dok se predujam ili akontacija ne fakturiraju, nisu dostupni za uporabu, što znači da će dostupni iznos biti nula. |
| Iskorišteni iznos | Iznos koji je već upotrijebljen u akontaciji ili predujmu. | Predujam ili akontacija mogu se djelomično uskladiti na računu s pomoću stvarnih troškova koji će imati neki dio označen kao već upotrijebljen ili potrošen. Ostatak iznosa predujma ili akontacije dostupan je za usklađivanje na budućoj fakturi sa stvarnim troškovima. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]