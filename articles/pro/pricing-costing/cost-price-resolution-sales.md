---
title: Određivanje stopa troškova za procjene i stvarne vrijednosti projekata
description: Ovaj članak pruža informacije o tome kako se određuju stope troškova za procjene i stvarne vrijednosti projekata.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410140"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Određivanje stopa troškova za procjene i stvarne vrijednosti projekata

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Da bi odredio cjenik troškova i stope troškova u procjeni i stvarnim kontekstima, sustav koristi podatke u **poljima Datum**, **Valuta** i **Ugovorna jedinica** povezanog projekta.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Određivanje stopa troškova u procijenjenom i stvarnom kontekstu za vrijeme

Kontekst procjene za **vrijeme** odnosi se na:

- Detalji retka ponude za **Vrijeme**.
- Detalji retka ugovora za **vrijeme**.
- Dodjele resursa na projektu.

Stvarni kontekst za **vrijeme** odnosi se na:

- Reci temeljnice stavke i ispravka za **vrijeme**.
- Reci temeljnice kreirani prilikom slanja stavke vremena.

Nakon određivanja cjenika troškova sustav ispunjava sljedeće korake kako bi unio zadanu stopu troška.

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

Nakon određivanja cjenika troškova sustav ispunjava sljedeće korake kako bi unio zadanu stopu troška.

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

Nakon određivanja cjenika troškova sustav ispunjava sljedeće korake kako bi unio zadanu stopu troška.

1. Sustav koristi kombinaciju **polja Proizvod** i **Jedinica** u procjeni ili stvarnom kontekstu za **Materijal** u odnosu na retke artikla cjenika u cjeniku.
1. Ako sustav pronađe redak artikla cjenika koji ima stopu troška za kombinaciju **Proizvod** i **Jedinica**, ta se stopa troška koristi kao zadana stopa troška.
1. Ako sustav ne može odgovarati **vrijednostima Proizvod** i **Jedinica**, jedinični trošak je prema zadanim postavkama postavljen na **0** (nula).
1. U procjeni ili stvarnom kontekstu, ako sustav može pronaći odgovarajući redak stavke cjenika, ali način određivanja cijena je nešto drugo osim **iznosa** valute, jedinični trošak je prema zadanim postavkama postavljen na **0**. To se događa zato što Project Operations podržava samo metodu **određivanja cijena iznosa** valute za materijale koji se koriste na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
