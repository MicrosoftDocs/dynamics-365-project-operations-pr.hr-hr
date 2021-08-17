---
title: Tijek rada upravljanja troškovima
description: U ovoj temi objašnjava se način uporabe sustava tijeka rada u aplikaciji Microsoft Dynamics 365 Finance za postavljanje postupka pregleda izvješća o troškovima u Upravljanju troškovima.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001287"
---
# <a name="expense-management-workflow"></a>Tijek rada upravljanja troškovima

Možete upotrebljavati sustav tijeka rada za postavljanje postupka pregleda izvješća o troškovima u Upravljanju troškovima. Možete postaviti tijek rada koji upotrebljava sljedeće kriterije za određivanje osobe koja odobrava izvješća o troškovima:

- Hijerarhija izvješćivanja zaposlenika i unaprijed definirana ograničenja odobrenja
- Odobravanje na više razina koje podržava privremene odobravatelje i konačnog odobravatelja
- Financijske dimenzije i odgovornost projekta
- Dodjela određenim korisnicima ili grupama korisnika

Odobrenja tijeka rada mogu se stvoriti za izvješća o troškovima, putne naloge, gotovinske predujmove i povrat poreza na dodanu vrijednost (PDV).

**Primjer**

Sljedeći je postupak primjer tijeka rada upravljanja troškovima za izvješće o troškovima.

1. Zaposlenik stvara i sprema izvješće o troškovima.
2. Zaposlenik šalje izvješće o troškovima na odobrenje. Odobravatelj se identificira na temelju pravila koja su definirana kada je postavljen tijeka rada.
3. Odobravatelj prima obavijest da je izvješće o troškovima spremno za odobrenje. Odobravatelj pregledava izvješće o troškovima i provjerava jesu li ispunjeni sljedeći uvjeti:

    - Troškovi ne krše nikakva pravila o troškovima. Ako trošak krši pravila, odobravatelj provjerava uključuje li izvješće o troškovima valjano poslovno opravdanje.
    - Elektronički računi priloženi su izvješću o troškovima.

4. Odobravatelj odobrava izvješće o troškovima.
5. Izvješće o troškovima dodjeljuje se koordinatoru za knjiženje Dugovanja.
6. Događa se jedan od sljedećih koraka, ovisno o tome je li konfigurirano automatsko knjiženje:

    - Ako je konfigurirano automatsko knjiženje, izvješće o trošku obrađuje se za plaćanje i ažurira se status izvješća o troškovima.
    - Ako automatsko knjiženje nije konfigurirano, koordinator Dugovanja provjerava jesu li predani svi izvorni računi te jesu li računi usklađeni s troškovima u izvješću o troškovima. Ispravnost svih poreznih kodova koji se unose u izvješće o troškovima također mora biti provjerena.

Nakon provjere ovih preduvjeta knjiži se izvješće o troškovima.

Nakon što se proknjiži izvješće o troškovima, autorizira se plaćanje izvješća o troškovima, a zaposleniku se vraća naknada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]