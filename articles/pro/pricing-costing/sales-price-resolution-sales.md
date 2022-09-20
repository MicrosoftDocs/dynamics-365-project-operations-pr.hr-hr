---
title: Određivanje prodajnih cijena za procjene i stvarne podatke projekta
description: U ovom se članku navode informacije o tome kako se određuju prodajne cijene za procjene i stvarne vrijednosti projekata.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475175"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Određivanje prodajnih cijena za procjene i stvarne podatke projekta

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Da bi odredio prodajne cijene na procjenama i stvarnim vrijednostima u Microsoftu Dynamics 365 Project Operations, sustav najprije koristi datum i valutu u dolaznoj procjeni ili stvarnom kontekstu za određivanje cjenika prodaje. U stvarnom kontekstu posebno, sustav koristi **polje Datum** transakcije da bi odredio koji je cjenik primjenjiv. Vrijednost **datuma** transakcije dolazne procjene ili stvarne uspoređuje se s **vrijednostima Efektivni početak (nezavisna vremenska zona)** i **Efektivni kraj (neovisno o vremenskoj zoni)** na cjeniku. Nakon određivanja prodajnog cjenika sustav određuje stopu prodaje ili računa.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Određivanje prodajnih stopa u stvarnim i procijenjenim recima za vrijeme

Kontekst procjene za **vrijeme** odnosi se na:

- Detalji retka ponude za **Vrijeme**.
- Detalji retka ugovora za **vrijeme**.
- Dodjele resursa na projektu.

Stvarni kontekst za **vrijeme** odnosi se na:

- Reci temeljnice stavke i ispravka za **vrijeme**.
- Reci temeljnice kreirani prilikom slanja stavke vremena.
- Detalji retka fakture za **Vrijeme**. 

Nakon određivanja cjenika za prodaju, sustav dovršava sljedeće korake da bi unio zadanu stopu računa.

1. Sustav odgovara kombinaciji **polja Uloga** i **Jedinica** resursa u procjeni ili stvarnom kontekstu za **Vrijeme** u odnosu na retke cijene uloge u cjeniku. Ovo podudaranje pretpostavlja da koristite gotove dimenzije cijena za cijene računa. Ako ste konfigurirali određivanje cijena tako da se temelji na poljima koja nisu ili uz **jedinicu** uloga **i** resursa, ta se kombinacija polja koristi za dohvaćanje odgovarajućeg retka cijene uloge.
1. Ako sustav pronađe redak cijene uloge koji ima stopu računa za **kombinaciju Uloga** i **Jedinica** izvora, ta se stopa računa koristi kao zadana stopa računa.
1. Ako sustav ne može odgovarati **vrijednostima Jedinica uloge** i **resursa**, dohvaća retke cijene uloga koji imaju odgovarajuće vrijednosti za **polje Uloga**, ali null vrijednosti za **polje Jedinica** resursa. Nakon što sustav pronađe odgovarajući zapis cijene uloge, stopa računa iz tog zapisa koristit će se kao zadana stopa računa. Ovo podudaranje pretpostavlja gotovu konfiguraciju za relativni prioritet Uloge u **odnosu na** jedinicu **resursa kao dimenziju prodajnih** cijena.

> [!NOTE]
> Ako konfigurirate različito određivanje prioriteta **polja Uloga** i **Jedinica** resursa ili ako imate druge dimenzije koje imaju veći prioritet, prethodno ponašanje promijenit će se u skladu s tim. Sustav dohvaća zapise cijena uloga koji imaju vrijednosti koje odgovaraju svakoj vrijednosti dimenzije određivanja cijena prema redoslijedu prioriteta. Reci koji imaju null vrijednosti za te dimenzije dolaze posljednji.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Određivanje stopa prodaje za stvarne i procijenjene retke za rashode

Kontekst procjene troškova **odnosi** se na:

- Detalji retka ponude za **trošak**.
- Detalji retka ugovora za **trošak**.
- Reci procjene troškova na projektu.

Stvarni kontekst za **trošak** odnosi se na:

- Reci temeljnice stavke i ispravka za **trošak**.
- Reci temeljnice kreirani prilikom slanja stavke troškova.
- Detalji retka fakture za **trošak**. 

Nakon određivanja cjenika za prodaju, sustav dovršava sljedeće korake da bi unio zadanu jediničnu prodajnu cijenu.

1. Sustav odgovara kombinaciji polja Kategorija i Jedinica u **retku procjene rashoda** **s recima cijene kategorije u cjeniku.** **·**
1. Ako sustav pronađe redak cijene kategorije koji ima stopu prodaje za **kombinaciju Kategorija** i **Jedinica**, ta se stopa prodaje koristi kao zadana stopa prodaje.
1. Ako sustav pronađe odgovarajući redak cijene kategorije, način određivanja cijena može se koristiti za unos zadane prodajne cijene. Sljedeća tablica prikazuje zadano ponašanje za cijene troškova u operacijama projekta.

    | Kontekst | Način određivanja cijena | Zadana cijena |
    | --- | --- | --- |
    | Procjena | Jedinična cijena | Na temelju retka cijene kategorije. |
    |        | Uz trošak | 0.00 |
    |        | Marža na trošak | 0.00 |
    | Stvarno | Jedinična cijena | Na temelju retka cijene kategorije. |
    |        | Uz trošak | Na temelju stvarnog povezanog troška. |
    |        | Marža na trošak | Marža se primjenjuje, kako je definirano retkom cijene kategorije, na stopu jediničnog troška povezanog stvarnog troška. |

1. Ako sustav ne može odgovarati **vrijednostima Kategorija** i **Jedinica**, stopa prodaje po zadanom je postavljena na **0** (nula).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Određivanje prodajnih stopa za stvarne i procijenjene retke za materijal

Kontekst procjene za **Materijal** odnosi se na:

- Detalji retka ponude za **Materijal**.
- Detalji retka ugovora za **Materijal**.
- Linije procjene materijala na projektu.

Stvarni kontekst za **Materijal** odnosi se na:

- Reci temeljnice stavki i ispravka za **Materijal**.
- Reci temeljnice kreirani prilikom slanja zapisnika korištenja materijala.
- Detalji retka fakture za **Materijal**. 

Nakon određivanja cjenika za prodaju, sustav dovršava sljedeće korake da bi unio zadanu jediničnu prodajnu cijenu.

1. Sustav odgovara kombinaciji polja Proizvod i Jedinica u **retku procjene za** Materijal **u odnosu na retke artikla cjenika u cjeniku**.**·**
1. Ako sustav pronađe redak artikla cjenika koji ima stopu prodaje za **kombinaciju Proizvod** i **Jedinica** te ako je **način određivanja cijena iznos** valute, koristi se prodajna cijena navedena u retku cjenika. 
1. Ako se **vrijednosti polja Proizvod** i **Jedinica** ne podudaraju ili ako je način određivanja cijena nešto drugo osim **iznosa** valute, stopa prodaje po zadanom je postavljena na **0** (nula). To se događa zato što Project Operations podržava samo metodu **određivanja cijena iznosa** valute za materijale koji se koriste na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
