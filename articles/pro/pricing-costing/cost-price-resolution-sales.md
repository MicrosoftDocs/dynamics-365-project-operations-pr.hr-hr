---
title: Određivanje stopa troškova za procjene i stvarne vrijednosti projekata
description: Ovaj članak pruža informacije o tome kako se određuju stope troškova za procjene i stvarne vrijednosti projekata.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475222"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Određivanje stopa troškova za procjene i stvarne vrijednosti projekata

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Da bi odredio stope troškova za procjene i stvarne vrijednosti u Microsoftu Dynamics 365 Project Operations, sustav najprije koristi datum i valutu u dolaznoj procjeni ili stvarnom kontekstu za određivanje cjenika troškova. U stvarnom kontekstu posebno, sustav koristi **polje Datum** transakcije da bi odredio koji je cjenik primjenjiv. Vrijednost **datuma** transakcije dolazne procjene ili stvarne uspoređuje se s **vrijednostima Efektivni početak (nezavisna vremenska zona)** i **Efektivni kraj (neovisno o vremenskoj zoni)** na cjeniku. Nakon određivanja cjenika troškova, sustav određuje stopu troškova. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Određivanje stopa troškova u procijenjenom i stvarnom kontekstu za vrijeme

Kontekst procjene za **vrijeme** odnosi se na:

- Detalji retka ponude za **Vrijeme**.
- Detalji retka ugovora za **vrijeme**.
- Dodjele resursa na projektu.

Stvarni kontekst za **vrijeme** odnosi se na:

- Reci temeljnice stavke i ispravka za **vrijeme**.
- Reci temeljnice kreirani prilikom slanja stavke vremena.

Nakon određivanja cjenika troškova sustav dovršava sljedeće korake kako bi unio zadanu stopu troška.

1. Sustav odgovara kombinaciji **polja Uloga** i **Jedinica** resursa u procjeni ili stvarnom kontekstu za **Vrijeme** u odnosu na retke cijene uloge u cjeniku. Ovo podudaranje pretpostavlja da koristite standardne dimenzije određivanja cijena za troškove rada. Ako ste konfigurirali sustav tako da odgovara poljima koja nisu ili uz **jedinicu** uloga **i** resursa, za dohvaćanje odgovarajućeg retka cijene uloge koristi se drugačija kombinacija.
1. Ako sustav pronađe redak cijene uloge koji ima stopu troška za **kombinaciju Uloga** i **Jedinica** izvora, ta se stopa troška koristi kao zadana stopa troška.
1. Ako sustav ne može odgovarati **vrijednostima Jedinica** uloge **i** resursa, dohvaća retke cijene uloga koji imaju odgovarajuće vrijednosti za **polje Uloga**, ali null vrijednosti za **polje Resourcing Unit**. Nakon što sustav ima odgovarajući zapis cijene uloge, stopa troška iz tog zapisa koristit će se kao zadana stopa troška.

> [!NOTE]
> Ako konfigurirate različito određivanje prioriteta **polja Uloga** i **Jedinica** resursa ili ako imate druge dimenzije koje imaju veći prioritet, prethodno ponašanje promijenit će se u skladu s tim. Sustav dohvaća zapise cijena uloga koji imaju vrijednosti koje odgovaraju svakoj vrijednosti dimenzije određivanja cijena prema redoslijedu prioriteta. Reci koji imaju null vrijednosti za te dimenzije dolaze posljednji.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Određivanje stopa troškova za stvarne i procijenjene retke za trošak

Kontekst procjene troškova **odnosi** se na:

- Detalji retka ponude za **trošak**.
- Detalji retka ugovora za **trošak**.
- Procjene troškova za projekt.

Stvarni kontekst za **trošak** odnosi se na:

- Reci temeljnice stavke i ispravka za **trošak**.
- Reci temeljnice kreirani prilikom slanja stavke troškova.

Nakon određivanja cjenika troškova sustav dovršava sljedeće korake kako bi unio zadanu stopu troška.

1. Sustav odgovara kombinaciji polja Kategorija i Jedinica u procjeni ili stvarnom kontekstu **rashoda** **u odnosu na retke cijene kategorije u cjeniku.** **·**
1. Ako sustav pronađe redak cijene kategorije koji ima stopu troška za kombinaciju **Kategorija** i **Jedinica**, ta se stopa troška koristi kao zadana stopa troška.
1. Ako sustav ne može odgovarati **vrijednostima Kategorija** i **Jedinica**, cijena je prema zadanim postavkama postavljena na **0** (nula).
1. U kontekstu procjene, ako sustav može pronaći odgovarajuću liniju cijena kategorije, ali metoda određivanja cijena je nešto drugo osim **cijene po jedinici**, stopa troškova prema zadanim je postavkama postavljena na **0** (nula).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Određivanje stopa troškova za stvarne i procijenjene retke za materijal

Kontekst procjene za **Materijal** odnosi se na:

- Detalji retka ponude za **Materijal**.
- Detalji retka ugovora za **Materijal**.
- Materijalne procjene na projektu.

Stvarni kontekst za **Materijal** odnosi se na:

- Reci temeljnice stavki i ispravka za **Materijal**.
- Reci temeljnice kreirani prilikom slanja zapisnika korištenja materijala.

Nakon određivanja cjenika troškova sustav dovršava sljedeće korake kako bi unio zadanu stopu troška.

1. Sustav koristi kombinaciju **polja Proizvod** i **Jedinica** u procjeni ili stvarnom kontekstu za **Materijal** u odnosu na retke artikla cjenika u cjeniku.
1. Ako sustav pronađe redak artikla cjenika koji ima stopu troška za kombinaciju **Proizvod** i **Jedinica**, ta se stopa troška koristi kao zadana stopa troška.
1. Ako sustav ne može odgovarati **vrijednostima Proizvod** i **Jedinica**, jedinični trošak je prema zadanim postavkama postavljen na **0** (nula).
1. U procjeni ili stvarnom kontekstu, ako sustav može pronaći odgovarajući redak stavke cjenika, ali način određivanja cijena je nešto drugo osim **iznosa** valute, jedinični trošak je prema zadanim postavkama postavljen na **0**. To se događa zato što Project Operations podržava samo metodu **određivanja cijena iznosa** valute za materijale koji se koriste na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
