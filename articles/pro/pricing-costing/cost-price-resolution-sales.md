---
title: Određivanje stopa troškova za procjene i stvarne podatke projekta
description: U ovom se članku navode informacije o tome kako se određuju stope troškova za procjene i stvarne podatke projekta.
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
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Određivanje stopa troškova za procjene i stvarne podatke projekta

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Za određivanje stopa troškova za procjene i stvarne podatke u sustavu Microsoft Dynamics 365 Project Operations, sustav prvo koristi datum i valutu u dolaznoj procjeni ili stvarnom kontekstu za određivanje cjenika troškova. Konkretno, u stvarnom kontekstu sustav upotrebljava polje **Datum transakcije** kako bi odredio koji je cjenik primjenjiv. Vrijednost ulazne procjene ili stvarni podatak polja **Datum transakcije** uspoređuje se s vrijednostima **Važeći početak (neovisno o vremenskoj zoni)** i **Važeći završetak (neovisno o vremenskoj zoni)** na cjeniku. Nakon određivanja cjenika troškova, sustav određuje stopu troška. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Određivanje cijena troškova u kontekstima procjene i stvarnih podataka za Vrijeme

Procijenjeni kontekst za **Vrijeme** odnosi se na:

- Pojedinosti redka ponude za **Vrijeme**.
- Pojedinosti redka ugovora za **Vrijeme**.
- Dodjelu resursa na projektu.

Kontekst stvarnog podatka za **Vrijeme** odnosi se na:

- Redke unosa i ispravaka u dnevniku za **Vrijeme**.
- Redke u dnevniku koji se stvaraju kad se pošalje unos vremena.

Nakon određivanja cjenika troška, sustav dovršava sljedeće korake za unos zadane stope troška.

1. Sustav uparuje kombinaciju polja **Uloga** i **Jedinica za resurse** u kontekstu procjene ili stvarnog podatka za **Vrijeme** s redcima cijene uloge na cjeniku. Ovo podudaranje pretpostavlja da upotrebljavate standardne veličine određivanja cijena za trošak rada. Ako ste sustav konfigurirali tako da se podudara s poljima koja nisu polja **Uloga** i **Jedinica za raspodjelu resursa** odnosno da se podudara i s nekim drugim poljima uz ta dva polja, za dohvaćanje podudarajućeg retka cijene uloge upotrebljava se drugačija kombinacija.
1. Ako sustav pronađe redak cijene uloge koji ima stopu troška za kombinaciju polja **Uloga** i **Jedinica za raspodjelu resursa**, ta se stopa troška primjenjuje kao zadana stopa troška.
1. Ako se sustav nije u mogućnosti podudariti s vrijednostima polja **Uloga** i **Jedinica za raspodjelu resursa**, dohvaća retke cijene uloge s vrijednostima koje se podudaraju za polje **Uloga**, no koji imaju nulte vrijednosti stavke **Jedinica za raspodjelu resursa**. Nakon što sustav pronađe podudarni zapis o cijeni uloge, stopa troška iz tog zapisa koristit će se kao zadana stopa troška.

> [!NOTE]
> Ako konfigurirate drugačije određivanje prioriteta za polja **Uloga** i **Jedinica resursa** ili ako imate druge dimenzije koje imaju veći prioritet, prethodno će se ponašanje u skladu s tim promijeniti. Sustav dohvaća zapise o cijenama uloga koji imaju vrijednosti koje odgovaraju svakoj vrijednosti dimenzije cijene prema redoslijedu prioriteta. Redci koji imaju vrijednost nula za te dimenzije su zadnji.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Određivanje cijena troškova na redcima stvarnih podataka i procjene za Trošak

Procijenjeni kontekst za **Trošak** odnosi se na:

- Pojedinosti redka ponude za **Trošak**.
- Pojedinosti redka ugovora za **Trošak**.
- Procjene troškova u projektu

Stvarni kontekst za **Trošak** odnosi se na:

- Redke unosa i ispravaka u dnevniku za **Trošak**.
- Redke u dnevniku koji se stvaraju kada se pošalje unos troška.

Nakon određivanja cjenika troška, sustav dovršava sljedeće korake za unos zadane stope troška.

1. Sustav uparuje kombinaciju polja **Kategorija** i **Jedinica** u kontekstu procjene ili stvarnog podatka za **Trošak** s redcima cijene kategorije na cjeniku.
1. Ako sustav pronađe redak cijene kategorije koji ima stopu troška za kombinaciju polja **Kategorija** i **Jedinica**, ta se stopa troška upotrebljava kao zadana stopa troška.
1. Ako sustav ne može upariti vrijednosti **Kategorija** i **Jedinica**, cijena se postavlja na **0** (nula) prema zadanim postavkama.
1. U kontekstu procjene, ako sustav može pronaći odgovarajući redak cijene kategorije, no metoda određivanja cijene nije **Cijena po jedinici** već neka druga, stopa troška postavlja se na **0** (nula) prema zadanim postavkama.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Određivanje stopa troška na redcima stvarnih podataka i procjena za materijal

Procijenjeni kontekst za **Materijal** odnosi se na:

- Pojedinosti redka ponude za **Materijal**.
- Pojedinosti redka ugovora za **Materijal**.
- Procjene materijala za projekt.

Stvarni kontekst za **Materijal** odnosi se na:

- Redke unosa i ispravka u dnevniku za **Materijal**.
- Redke u dnevniku koji se stvaraju kad se pošalje zapisnik uporabe Materijala.

Nakon određivanja cjenika troška, sustav dovršava sljedeće korake za unos zadane stope troška.

1. Sustav upotrebljava kombinaciju polja **Kategorija** i **Jedinica** u kontekstu procjene ili stvarnog podatka za **Materijal** s redcima stavke cjenika na cjeniku.
1. Ako sustav pronađe redak stavke cjenika koji ima stopu troška za kombinaciju polja **Kategorija** i **Jedinica**, ta se stopa troška upotrebljava kao zadana stopa troška.
1. Ako sustav ne može upariti vrijednosti **Proizvod** i **Jedinica**, jedinični trošak postavlja se na **0** (nula) prema zadanim vrijednostima.
1. U kontekstu procjene ili stvarnog podatka, ako sustav može pronaći odgovarajući redak stavka cjenika, no metoda određivanja cijene nije **Iznos valute** već neka druga, trošak jedinice postavlja se na **0** (nula) prema zadanim postavkama. Ovo se ponašanje događa jer Project Operations podržava samo metodu određivanja cijena **Valutni iznos** za materijale koji se upotrebljavaju na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
