---
title: Rješavanje cijena troškova za procijenjene i stvarne podatke
description: U ovoj temi nalaze se informacije o načinu rješavanja cijena troškova za procijenjene i stvarne podatke.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003672"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Rješavanje cijena troškova za procijenjene i stvarne podatke

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Za rješavanje cijena troška i cjenika troškova za procijenjene i stvarne podatke sustav upotrebljava podatke u poljima **Datum**, **Valuta** i **Ugovorna jedinica** povezanog projekta. Nakon rješavanja cjenika troškova, aplikacija rješava cijenu troška.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rješavanje cijena troškova na redcima sa stvarnim i procijenjenim podacima za Vrijeme

Redci s procijenjenim podacima za Vrijeme odnose se na pojedinosti redaka ponude i ugovora za dodjele vremena i resursa za projekt.

Nakon rješavanja cjenika troškova, sustav upotrebljava polja **Uloga**, **Tvrtka za raspodjelu resursa** i **Jedinica za raspodjelu resursa** u retku s procijenjenim podacima za Vrijeme kako bi uskladio retke s cijenama uloga u cjeniku. Ova podudarnost pretpostavlja uporabu gotovih dimenzija za određivanje cijene troška radne snage. Ako ste umjesto toga konfigurirali sustav tako da pristaje poljima ili dodatno za mogućnosti **Uloga**, **Tvrtka resursa** i **Jedinica resursa**, tada će se upotrebljavati druga kombinacija za dohvaćanje odgovarajućeg retka cijene uloge. Ako aplikacija pronađe redak cijene uloge koja ima cijenu troška za kombinaciju **Uloga**, **Tvrtka resursa** i **Jedinica resursa**, to je zadana cijena troška. Ako se aplikacija ne može točno podudarati s kombinacijom vrijednosti **Uloga**, **Tvrtka za resurse** i **Jedinica za resurse**, dohvatit će retke s cijenama uloga s odgovarajućom vrijednošću uloge, ali ima praznu vrijednosti za stavke **Jedinica za resurse** i **Tvrtka za resurse**. Nakon pronalaska podudarnosti zapisa cijene uloge s odgovarajućom vrijednošću cijene uloge, cijena troška zadaje se iz tog zapisa. 

> [!NOTE]
> Ako konfigurirate drugačije određivanje prioriteta za stavke **Uloga**, **Tvrtka resursa** i **Jedinica resursa** ili ako imate druge dimenzije koje imaju veći prioritet, to će se ponašanje u skladu s tim promijeniti. Sustav dohvaća zapise cijene uloge s vrijednostima koje se podudaraju sa svakom vrijednošću veličine za određivanje cijene prema redoslijedu prioriteta s redovima koji imaju praznu vrijednost za one veličine koje su posljednje u redoslijedu prioriteta.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rješavanje cijena troškova na redcima sa stvarnim i procijenjenim podacima za Trošak

Redci s procijenjenim podacima za Trošak odnose se na pojedinosti redaka ponude i ugovora za troškove i retke troškova za projekt.

Nakon rješavanja cjenika troškova, sustav upotrebljava kombinaciju polja **Kategorija** i **Jedinica** u retku s procijenjenim podacima za trošak kako bi uskladio retke **Cijena kategorije** na riješenom cjeniku. Ako sustav pronađe redak cijene kategorije koja ima cijenu troška za kombinaciju polja **Kategorija** i **Jedinica**, cijena troška je zadana. Ako se sustav ne može podudariti vrijednosti stavki **Kategorija** i **Jedinica** ili ako može pronaći podudarni redak cijene kategorije, ali način određivanja cijena nije **Jedinična cijena**, cijena troška zadaje se na nulu (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rješavanje cijene troška na stvarnim i procijenjenim redcima za materijal

Redci procjene materijala odnose se na pojedinosti ponude i retka ugovora za materijale i retke procjene materijala za projekt.

Nakon rješavanja troškovnika, sustav upotrebljava kombinaciju polja **Proizvod** i **Jedinica** na retku procjene za procjenu materijala koja se podudara s redcima **Stavki cjenika** na riješenom cjeniku. Ako sustav pronađe redak cijene proizvoda koja ima cijenu troška za kombinaciju polja **Proizvod** i **Jedinica**, cijena troška je zadana. Ako se sustav ne može podudarati vrijednosti **Proizvod** i **Jedinica**, jedinični trošak zadaje se na nulu. Ova zadana vrijednost dogodit će se i ako postoji podudarni redak stavke cjenika, ali se način određivanja cijena temelji na standardnom ili trenutačnom trošku koji nije definiran u proizvodu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
