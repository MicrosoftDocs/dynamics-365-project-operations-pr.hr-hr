---
title: Rješavanje cijena troškova na procijenjenim i stvarnim podacima
description: U ovoj temi nalaze se informacije o načinu rješavanja cijena troškova na procijenjenim i stvarnim podacima.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bad8f4b95ac5803d3f334e1b306d2a9d27a6645d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073298"
---
# <a name="resolving-cost-prices-on-estimates-and-actuals"></a>Rješavanje cijena troškova na procijenjenim i stvarnim podacima

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Za rješavanje cijena troška i cjenika troškova za procijenjene i stvarne podatke sustav upotrebljava podatke u poljima **Datum** , **Valuta** i **Ugovorna jedinica** povezanog projekta. Nakon rješavanja cjenika troškova, aplikacija rješava cijenu troška.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rješavanje cijena troškova na redcima sa stvarnim i procijenjenim podacima za Vrijeme

Redci s procijenjenim podacima za Vrijeme odnose se na pojedinosti redaka ponude i ugovora za dodjele vremena i resursa za projekt.

Nakon rješavanja cjenika troškova, sustav upotrebljava polja **Uloga** i **Jedinica resursa** u retku s procijenjenim podacima za Vrijeme kako bi uskladio retke s cijenama uloga u cjeniku. Ova podudarnost pretpostavlja uporabu gotovih dimenzija za određivanje cijene troška radne snage. Ako ste umjesto toga konfigurirali sustav tako da pristaje poljima ili dodatno za mogućnosti **Uloga** i **Jedinica resursa** , tada će se upotrebljavati druga kombinacija za dohvaćanje odgovarajućeg retka cijene uloge. Ako aplikacija pronađe redak cijene uloge koja ima cijenu troška za kombinaciju **Uloga** i **Jedinica resursa** , to je zadana cijena troška. Ako se aplikacija ne može podudariti s vrijednostima **Uloga** i **Jedinica resursa** , tada dohvaća retke s cijenama uloga s pomoću odgovarajuće uloge, ali s praznom vrijednosti stavke **Jedinica resursa**. Nakon što dobije zapis o cijeni odgovarajuće uloge, cijena troška zadaje se iz tog zapisa. 

> [!NOTE]
> Ako konfigurirate drugačije određivanje prioriteta za stavke **Uloga** i **Jedinica resursa** , ili ako imate druge dimenzije koje imaju veći prioritet, to će se ponašanje u skladu s tim promijeniti. Sustav dohvaća zapise cijena uloga s vrijednostima koje se podudaraju sa svakom vrijednošću dimenzije za određivanje cijene prema redoslijedu prioriteta, s redovima koji nemaju vrijednosti za one dimenzije koje dolaze posljednje.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rješavanje cijena troškova na redcima sa stvarnim i procijenjenim podacima za Trošak

Redci s procijenjenim podacima za Trošak odnose se na pojedinosti redaka ponude i ugovora za troškove i retke troškova za projekt.

Nakon rješavanja cjenika troškova, sustav upotrebljava kombinaciju polja **Kategorija** i **Jedinica** u retku s procijenjenim podacima za trošak kako bi uskladio retke **Cijena kategorije** na riješenom cjeniku. Ako sustav pronađe redak cijene kategorije koja ima cijenu troška za kombinaciju polja **Kategorija** i **Jedinica** , cijena troška je zadana. Ako se sustav ne može podudariti vrijednosti stavki **Kategorija** i **Jedinica** ili ako može pronaći podudarni redak cijene kategorije, ali način određivanja cijena nije **Jedinična cijena** , cijena troška zadaje se na nulu (0).