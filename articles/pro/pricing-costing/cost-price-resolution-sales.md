---
title: Rješavanje cijena koštanja na procijenjenim i stvarnim podacima za projekt
description: U ovoj temi nalaze se informacije o tome kako se rješavaju cijene koštanja na procijenjenim i stvarnim podacima za projekt.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997552"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Rješavanje cijena koštanja na procijenjenim i stvarnim podacima za projekt 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rješavanje cijena troška na stvarnim i procijenjenim redcima za materijal

Redci procjene materijala odnose se na pojedinosti ponude i retka ugovora za materijale i retke procjene materijala za projekt.

Nakon rješavanja troškovnika, sustav upotrebljava kombinaciju polja **Proizvod** i **Jedinica** na retku procjene za procjenu materijala koja se podudara s redcima **Stavki cjenika** na riješenom cjeniku. Ako sustav pronađe redak cijene proizvoda koja ima cijenu troška za kombinaciju polja **Proizvod** i **Jedinica**, cijena troška je zadana. Ako se sustav ne može podudarati s vrijednostima **Proizvod** i **Jedinica** ili ako je u mogućnosti pronaći podudarni redak stavke cjenika, ali metoda određivanja cijene temelji se na Standardnom ili Trenutačnom trošku i nijedna nije definirana na proizvodu, jedinični trošak zadan je na nulu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
