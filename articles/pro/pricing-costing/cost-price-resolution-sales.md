---
title: Rješavanje cijena koštanja na procjenama i stvarnim podacima – jednostavno
description: U ovoj temi nalaze se informacije o načinu rješavanja cijena troškova na procijenjenim i stvarnim podacima.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274540"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Rješavanje cijena koštanja na procjenama i stvarnim podacima – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Za rješavanje cijena troška i cjenika troškova za procijenjene i stvarne podatke sustav upotrebljava podatke u poljima **Datum**, **Valuta** i **Ugovorna jedinica** povezanog projekta. Nakon rješavanja cjenika troškova, aplikacija rješava cijenu troška.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rješavanje cijena troškova na redcima sa stvarnim i procijenjenim podacima za Vrijeme

Redci s procijenjenim podacima za Vrijeme odnose se na pojedinosti redaka ponude i ugovora za dodjele vremena i resursa za projekt.

Nakon rješavanja cjenika troškova, polja **Uloga** i **Jedinica resursa** u retku procjene za vrijeme podudaraju se s redcima cijena uloga u cjeniku. Ovo podudaranje pretpostavlja da upotrebljavate standardne veličine određivanja cijena za trošak rada. Ako ste umjesto toga konfigurirali sustav tako da pristaje poljima ili dodatno za mogućnosti **Uloga** i **Jedinica resursa**, tada će se upotrebljavati druga kombinacija za dohvaćanje odgovarajućeg retka cijene uloge. Ako aplikacija pronađe redak cijene uloge koja ima cijenu troška za kombinaciju **Uloga** i **Jedinica resursa**, to je zadana cijena troška. Ako se aplikacija ne može podudariti s vrijednostima **Uloga** i **Jedinica resursa**, tada dohvaća retke s cijenama uloga s pomoću odgovarajuće uloge, ali s praznom vrijednosti stavke **Jedinica resursa**. Nakon što dobije zapis o cijeni odgovarajuće uloge, cijena troška zadaje se iz tog zapisa. 

> [!NOTE]
> Ako konfigurirate drugačije određivanje prioriteta za stavke **Uloga** i **Jedinica resursa**, ili ako imate druge dimenzije koje imaju veći prioritet, to će se ponašanje u skladu s tim promijeniti. Sustav dohvaća zapise cijena uloga s vrijednostima koje se podudaraju sa svakom vrijednošću dimenzije za određivanje cijene prema redoslijedu prioriteta, s redcima koji nemaju vrijednosti za one dimenzije koje dolaze posljednje.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rješavanje cijena troškova na redcima sa stvarnim i procijenjenim podacima za Trošak

Redci s procijenjenim podacima za Trošak odnose se na pojedinosti redaka ponude i ugovora za troškove i retke troškova za projekt.

Nakon rješavanja cjenika troškova, sustav upotrebljava kombinaciju polja **Kategorija** i **Jedinica** u retku procjene troškova kako bi se podudarila s redcima **Cijena kategorije** na riješenom cjeniku. Ako sustav pronađe redak cijene kategorije koja ima cijenu troška za kombinaciju polja **Kategorija** i **Jedinica**, cijena troška je zadana. Ako se sustav ne može podudariti s vrijednostima **Kategorija** i **Jedinica** ili ako je u mogućnosti pronaći podudarni redak cijene, ali metoda određivanja cijene nije **Cijena po jedinici**, cijena troška zadaje se na nulu (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]