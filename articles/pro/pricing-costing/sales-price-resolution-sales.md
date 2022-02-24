---
title: Rješavanje prodajnih cijena za procjene i stvarne podatke projekta
description: U ovoj temi nalaze se informacije o načinu rješavanja prodajnih cijena na procijenjenim i stvarnim podacima za projekt.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3bf4686b414300370e6b364834b33edad98b7f39
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877347"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Rješavanje prodajnih cijena za procjene i stvarne podatke projekta

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Kada se u aplikaciji Dynamics 365 Project Operations riješe prodajne cijene na procjenama i stvarnim vrijednostima, sustav prvo upotrebljava datum i valutu povezane ponude za projekt ili ugovora o projektu za rješavanje prodajnog cjenika. Nakon što se riješi prodajni cjenik, sustav rješava prodajnu cijenu ili cijenu naplate.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Rješavanje prodajnih cijena na redcima sa stvarnim i procijenjenim podacima za Vrijeme

U aplikaciji Project Operations, redci procjene za vrijeme upotrebljavaju se za označavanje pojedinosti retka ponude i retka ugovora za vrijeme i dodjelu resursa projektu.

Nakon što se riješi prodajni cjenik, sustav dovršava sljedeće korake za zadavanje cijene naplate.

1. Sustav upotrebljava polja **Uloga** i **Jedinica za raspodjelu resursa** u retku s procijenjenim podacima za Vrijeme kako bi uskladio retke s cijenama uloga u riješenom cjeniku. Ova podudarnost pretpostavlja uporabu gotovih dimenzija za cijene naplate koje se upotrebljavaju. Ako ste umjesto toga konfigurirali određivanje cijena na temelju nekog drugog polja ili dodatno za mogućnosti **Uloga** i **Jedinica za raspodjelu resursa**, tada je to druga kombinacija koja će se upotrebljavati za dohvaćanje odgovarajućeg retka cijene uloge.
2. Ako sustav pronađe redak cijene uloge koja ima cijenu naplate za kombinaciju polja **Uloga** i **Jedinica za raspodjelu resursa**, to je zadana ta cijena naplate.
3. Ako sustav nije u mogućnosti podudariti vrijednosti polja **Uloga** i **Jedinica za raspodjelu resursa**, tada dohvaća retke s cijenama uloga s pomoću odgovarajuće uloge, ali s praznom vrijednosti stavke **Jedinica za raspodjelu resursa**. Nakon što sustav pronađe podudarni zapis o cijeni uloge, iz tog će zapisa zadati obračun. Ovo podudaranje pretpostavlja gotovu konfiguraciju za relativni prioritet mogućnosti **Uloga** nasuprot **Jedinica za raspodjelu resursa** kao dimenzije određivanja prodajnih cijena.

> [!NOTE]
> Ako ste konfigurirali drugačije određivanje prioriteta za stavke **Uloga** i **Jedinica resursa**, ili ako imate druge dimenzije koje imaju veći prioritet, to će se ponašanje u skladu s tim promijeniti. Sustav dohvaća zapise cijena uloga s vrijednostima koje se podudaraju sa svakom vrijednošću dimenzije za određivanje cijene prema redoslijedu prioriteta, s redovima koji nemaju vrijednosti za one dimenzije koje dolaze posljednje.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Rješavanje prodajnih cijena na redcima sa stvarnim i procijenjenim podacima za trošak

U aplikaciji Project Operations, redci procjene za trošak upotrebljavaju se za označavanje pojedinosti retka ponude i retka ugovora za trošak i retke za procjenu troška na projektu.

Nakon što se riješi prodajni cjenik, sustav dovršava sljedeće korake za zadavanje jedinične prodajne cijene.

1. Sustav upotrebljava kombinaciju polja **Kategorija** i **Jedinica** u retku s procijenjenim podacima za trošak kako bi uskladio retke cijene kategorije na riješenom cjeniku.
2. Ako sustav pronađe redak cijene kategorije koji ima prodajnu cijenu za kombinaciju polja **Kategorija** i **Jedinica**, tada je prodajna cijena zadana.
3. Ako sustav pronađe podudarni redak cijene kategorije, metoda određivanja cijena može se upotrebljavati za zadavanje prodajne cijene. Sljedeća tablica u nastavku prikazuje zadano ponašanje cijene troška u aplikaciji Project Operations.

    | Kontekst | Način određivanja cijena | Zadana cijena |
    | --- | --- | --- |
    | Procjena | Jedin. cijena | Na temelju retka cjenovne kategorije |
    | &nbsp; | Uz trošak | 0.00 |
    | &nbsp; | Marža na trošak | 0.00 |
    | Stvarno | Jedin. cijena | Na temelju retka cjenovne kategorije |
    | &nbsp; | Uz trošak | Na temelju povezanih stvarnih troškova |
    | &nbsp; | Marža na trošak | Primjena oznake definirane retkom cjenovne kategorije na jediničnu cijenu troška povezanog stvarnog troška |

4. Ako sustav ne može podudarati vrijednosti polja **Kategorija** i **Jedinica**, prodajna cijena zadana je na nulu (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Rješavanje prodajnih cijena na stvarnim i procijenjenim redcima za materijal

Redci procjene materijala u aplikaciji Project Operations upotrebljavaju se za označavanje pojedinosti na pojedinosti retka ponude i retka ugovora za materijale i retke procjene materijala za projekt.

Nakon što se riješi prodajni cjenik, sustav dovršava sljedeće korake za zadavanje jedinične prodajne cijene.

1. Sustav upotrebljava kombinaciju polja **Proizvod** i **Jedinica** na retku procjene za materijal za podudaranje s redcima stavki cjenika u cjeniku koji je riješen.
2. Ako sustav pronađe redak stavke cjenika koji ima prodajnu cijenu za kombinaciju polja **Proizvod** i **Jedinica**, a način određivanja cijena je **Iznos valute**, upotrebljava se prodajna cijena navedena u retku cjenika.
3. Ako se vrijednosti polja **Proizvod** i **Jedinica** ne podudaraju, prodajna cijena zadaje se na nulu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
