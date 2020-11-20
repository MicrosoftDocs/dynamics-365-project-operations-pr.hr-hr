---
title: Nadjačavanje prodajnih cjenika za projekt
description: U ovoj temi nalaze se informacije o stvaranju prilagođenih prodajnih cjenika.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130839"
---
# <a name="override-project-sales-price-lists"></a>Nadjačavanje prodajnih cjenika za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

## <a name="customer-specific-project-price-lists"></a>Cjenici za projekt specifični za klijenta

Ugovori o cijenama specifičnim za klijenta mogu se postaviti kao cjenici projekta na zapisu računa u aplikaciji Dynamics 365 Project Operations.

Kako biste postavili cjenik projekta specifičan za kupca, u području **Prodaja**, pomaknite se do zapisa računa.

1. Otvorite stranicu s popisom **Računi**.
2. Pronađite i dvaput kliknite zapis o klijentu kako biste otvorili stranicu s pojedinostima **Računa**.
3. Na kartici **Cjenici za projekt** odaberite **+ Novi cjenik za projekt^^.
4. Na stranici **Novi cjenik za projekt**, s padajućeg izbornika odaberite cjenik. Samo cjenici kojima je kontekst postavljen na **Prodaja** i čija se valuta podudara s valutom računa.
5. Ime i veza, a zatim odaberite **Spremi**. Stvoren je cjenik za projekt specifičan za klijenta. Ovaj će se cjenik upotrebljavati za zadavanje cijena za projekt na ponudama projekta ili ugovorima o projektu stvorenim za ovog klijenta ako datum stvaranja ponude ili ugovora o projektu pada unutar datuma kada je cjenik na snazi.

## <a name="custom-pricing-on-project-quotes"></a>Prilagođene cijene za ponude projekta

Na ponudama projekta možete imati cijene za projekt koje započinju sa zadanim standardnim cjenikom koji zadaje klijent ili parametri projekta.

Kada su vam potrebne prilagođene cijene za radove povezane s projektom na određenoj ponudi, to možete dobiti iz entiteta povezanog s cjenicima za projekt.

Dovršite sljedeće korake za postavljanje cijena projekata specifičnih za ponudu.

1. Otvorite ponudu projekta i odaberite karticu **Cjenici za projekt**.
2. U podrešetki odaberite **Stvori prilagođene cijene**.

Svi cjenici za projekt koji su priloženi uz ponudu, kopiraju se u nove cjenike. Nazivi novih cjenika odražavaju naziv ponude s oznakom datuma i vremena kada su ti cjenici stvoreni.

Možete upotrijebiti svaki od tih cjenika i ažurirati cijene rada (cijena uloge) i troškova (cijena kategorije). Ove cijene primjenjivat će se samo na ovu ponudu projekta.

## <a name="price-lists-on-a-project-contract"></a>Cjenici u ugovoru o projektu

Na ugovoru o projektu, cijene za projekt uvijek su zadane kao prilagođeni cjenik s nazivom ugovora i stvorenom oznakom datuma i vremena koja se dodaje nazivu. To vrijedi bez obzira je li ugovor stvoren kada je prihvaćena ponuda ili je ugovor stvoren od početka. Ako je potrebno, možete ukloniti ovu povezanost s prilagođenim cjenikom i umjesto toga s ugovorom o projektu povezati standardni cjenik.

Kada standardni cjenik povežete s projektnim cjenicima na ponudi ili ugovoru, sve promjene cijena u cjeniku utjecat će na sve ponude i ugovore koji upotrebljavaju cjenik.