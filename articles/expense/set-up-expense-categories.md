---
title: Postavljanje kategorije izdatka
description: U ovoj temi nalaze se informacije o načinu postavljanja kategorije troškova i dijeljene kategorije za izvješća o troškovima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896677"
---
# <a name="set-up-expense-categories"></a>Postavljanje kategorije izdatka

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kad zaposlenici stvaraju izvješća o troškovima, svaki trošak koji evidentiraju mora biti povezan s kategorijom troška. Kategorije troškova izvedene su iz dijeljenih kategorija koje se mogu dijeliti između pravnih osoba u vašoj tvrtki ili ustanovi. Ovisno o tome kako je definirana vaša tvrtka ili ustanova, ove se kategorije troškova mogu dijeliti i u drugim područjima. Na temelju definicije vaše tvrtke ili ustanove i smjernica implementacijskog tima, morate odrediti hoće li se kategorije koje se upotrebljavaju u upravljanju troškovima upotrebljavati samo u upravljanju troškovima ili bi ih se trebalo dijeliti u drugim područjima.

> [!NOTE]
> Te se kategorije mogu dijeliti između Upravljanja projektima i računovodstva te Upravljanja troškovima tj. Upravljanja projektima i računovodstva te Proizvodnje. Međutim, ne mogu se dijeliti između Upravljanja troškovima i Proizvodnje.

Prije nego što započnete postupak postavljanja, za svaku kategoriju troškova moraju se donijeti sljedeće odluke:

- Što je kategorija troškova? Primjeri uključuju kategorije za letove, hotele ili kilometražu.
- Može li se kategorija troškova upotrebljavati i za Upravljanje projektima i računovodstvo? Ako može, morate također donijeti sljedeće odluke:

    - Koji će se računi za troškove upotrebljavati za sljedeće troškove?

        - Cijena
        - Raspodjela plaća
        - Vrijednost troškova WIP-a
        - Troškovna stavka
        - Vrijednosna stavka troškova WIP-a
        - Obračunani gubitak
        - Obračunani gubitak WIP-a

    - Koji će se računi prihoda upotrebljavati za sljedeće izvore prihoda?

        - Fakturirani prihod
        - Obračunani prihod – vrijednost prodaje
        - Prodajna vrijednost WIP-a
        - Obračunani prihod proizvodnje
        - Proizvodnja WIP-a
        - Obračunani prihod – dobit
        - Dobit WIP-a
        - Obračunani prihod – pretplata
        - Pretplata WIP-a

- Što je vrsta troškova?
- Koji je zadani način plaćanja za kategoriju troškova?
- Moraju li se razvrstati troškovi iz kategorije troškova?
- Koji je glavni zadani račun za kategoriju troškova?
- Koja je zadana stavka grupe poreza na promet za kategoriju troškova?
- Jesu li dodatni načini plaćanja dozvoljeni za kategoriju troškova? Ako jesu, koji su?
- Postoje li potkategorije u ovoj kategoriji troškova? Ako postoje potkategorije, morate također donijeti sljedeće odluke:

    - Je li neka od potkategorija izuzeta iz povrata poreza?
    - Koja je stavka grupe poreza na promet potkategorija?
