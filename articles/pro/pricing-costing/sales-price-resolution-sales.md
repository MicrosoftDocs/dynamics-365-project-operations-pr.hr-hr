---
title: Određivanje prodajnih cijena za procjene i stvarne podatke projekta
description: U ovom se članku navode informacije o tome kako se određuju prodajne cijene za procjene i stvarne podatke projekta.
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

Za određivanje cijena troškova za procjene i stvarne podatke u sustavu Microsoft Dynamics 365 Project Operations sustav prvo upotrebljava datum i valutu u dolaznoj procjeni ili kontekst stvarnog podatka za određivanje cjenika prodaje. Konkretno, u stvarnom kontekstu sustav upotrebljava polje **Datum transakcije** kako bi odredio koji je cjenik primjenjiv. Vrijednost ulazne procjene ili stvarni podatak polja **Datum transakcije** uspoređuje se s vrijednostima **Važeći početak (neovisno o vremenskoj zoni)** i **Važeći završetak (neovisno o vremenskoj zoni)** na cjeniku. Nakon što se odredi prodajni cjenik, sustav određuje prodajnu cijenu ili cijenu naplate.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Određivanje prodajnih cijena u redcima sa stvarnim i procijenjenim podacima za Vrijeme

Procijenjeni kontekst za **Vrijeme** odnosi se na:

- Pojedinosti redka ponude za **Vrijeme**.
- Pojedinosti redka ugovora za **Vrijeme**.
- Dodjelu resursa na projektu.

Kontekst stvarnog podatka za **Vrijeme** odnosi se na:

- Redke unosa i ispravaka u dnevniku za **Vrijeme**.
- Redke u dnevniku koji se stvaraju kad se pošalje unos vremena.
- Pojedinosti redka fakture za **Vrijeme**. 

Nakon što se odredi prodajni cjenik, sustav dovršava sljedeće korake kako bi se dodala zadana cijena naplate.

1. Sustav uparuje kombinaciju polja **Uloga** i **Jedinica za resurse** u kontekstu procjene ili stvarnog podatka za **Vrijeme** s redcima cijene uloge na cjeniku. U ovom se uparivanju pretpostavlja da upotrebljavate gotove dimenzije za cijene naplate. Ako ste konfigurirali određivanje cijena tako da se temelji na nekim drugim poljima umjesto ili pored polja **Uloga** i **Jedinica za resurse**, tada se ta kombinacija polja upotrebljava za dohvaćanje odgovarajućeg redka cijene uloge.
1. Ako sustav pronađe redak cijene uloge koja ima cijenu naplate za kombinaciju polja **Uloga** i **Jedinica za raspodjelu resursa**, ta cijena naplate upotrebljava se kao zadana cijena naplate.
1. Ako se sustav ne može upariti s vrijednostima polja **Uloga** i **Jedinica za raspodjelu resursa**, dohvaća redke cijene uloge s vrijednostima koje se podudaraju za polje **Uloga**, no koji imaju nulte vrijednosti stavke **Jedinica za resurse**. Nakon što sustav pronađe podudarni zapis o cijeni uloge, stopa naplate iz tog zapisa upotrebljavat će se kao zadana stopa naplate. Ovo podudaranje pretpostavlja gotovu konfiguraciju za relativni prioritet polja **Uloga** nasuprot polja **Jedinica za raspodjelu resursa** kao dimenzije određivanja prodajnih cijena.

> [!NOTE]
> Ako konfigurirate drugačije određivanje prioriteta za polja **Uloga** i **Jedinica resursa** ili ako imate druge dimenzije koje imaju veći prioritet, prethodno će se ponašanje u skladu s tim promijeniti. Sustav dohvaća zapise o cijenama uloga koji imaju vrijednosti koje odgovaraju svakoj vrijednosti dimenzije cijene prema redoslijedu prioriteta. Redci koji imaju vrijednost nula za te dimenzije su zadnji.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Određivanje prodajnih cijena u redcima sa stvarnim i procijenjenim podacima za Trošak

Procijenjeni kontekst za **Trošak** odnosi se na:

- Pojedinosti redka ponude za **Trošak**.
- Pojedinosti redka ugovora za **Trošak**.
- Redke procjena troškova u projektu.

Stvarni kontekst za **Trošak** odnosi se na:

- Redke unosa i ispravaka u dnevniku za **Trošak**.
- Redke u dnevniku koji se stvaraju kada se pošalje unos troška.
- Pojedinosti redka fakture za **Trošak**. 

Nakon što se odredi prodajni cjenik, sustav dovršava sljedeće korake kako bi unio zadane jedinične prodajne cijene.

1. Sustav uparuje kombinaciju polja **Kategorija** i **Jedinica** u redku koji sadržava procijenjene podatke za **Trošak** s redcima cjenovne kategorije na cjeniku.
1. Ako sustav pronađe redak cjenovne kategorije koji ima prodajnu cijenu za kombinaciju polja **Kategorija** i **Jedinica**, ta prodajna cijena upotrebljava se kao zadana.
1. Ako sustav pronađe podudarni redak cjenovne kategorije, metoda određivanja cijena može se upotrebljavati za unos zadane prodajne cijene. Sljedeća tablica prikazuje zadano ponašanje cijena troška u aplikaciji Project Operations.

    | Kontekst | Način određivanja cijena | Zadana cijena |
    | --- | --- | --- |
    | Procjena | Jedinična cijena | Na temelju redka cjenovne kategorije. |
    |        | Uz trošak | 0.00 |
    |        | Marža na trošak | 0.00 |
    | Stvarno | Jedinična cijena | Na temelju redka cjenovne kategorije. |
    |        | Uz trošak | Na temelju povezanih stvarnih troškova. |
    |        | Marža na trošak | Provizija definirana redkom cjenovne kategorije primjenjuje se na jediničnu cijenu troška povezanog stvarnog troška. |

1. Ako sustav ne može upariti vrijednosti **Kategorija** i **Jedinica**, prodajna cijena postavlja se na **0** (nula) prema zadanim postavkama.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Utvrđivanje prodajnih cijena na stvarnim i procijenjenim redcima za Materijal

Procijenjeni kontekst za **Materijal** odnosi se na:

- Pojedinosti redka ponude za **Materijal**.
- Pojedinosti redka ugovora za **Materijal**.
- Redke procjene materijala za projekt.

Stvarni kontekst za **Materijal** odnosi se na:

- Redke unosa i ispravka u dnevniku za **Materijal**.
- Redke u dnevniku koji se stvaraju kad se pošalje zapisnik uporabe Materijala.
- Pojedinosti redka fakture za **Materijal**. 

Nakon što se odredi prodajni cjenik, sustav dovršava sljedeće korake kako bi unio zadane jedinične prodajne cijene.

1. Sustav uparuje kombinaciju polja **Proizvod** i **Jedinica** u redku procjene za **Materijal** s redcima stavki cjenika u cjeniku.
1. Ako sustav pronađe redak stavke cjenika koji ima prodajnu cijenu za kombinaciju polja **Proizvod** i **Jedinica**, a ako je način određivanja cijena **Valutni iznos**, upotrebljava se prodajna cijena navedena u redku cjenika. 
1. Ako se vrijednosti polja **Proizvod** i **Jedinica** ne podudaraju ili ako je metoda određivanja cijene nešto drugo osim polja **Valutni iznos**, prodajna cijena postavlja se na **0** (nula) prema zadanim postavkama. Ovo se ponašanje događa jer Project Operations podržava samo metodu određivanja cijena **Valutni iznos** za materijale koji se upotrebljavaju na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
