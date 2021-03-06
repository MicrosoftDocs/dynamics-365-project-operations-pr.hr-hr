---
title: Postavljanje tijekova rada za upravljanje troškovima
description: Možete postaviti postupak tijeka rada koji se upotrebljava za pregled i odobravanje dokumenata o putovanju i troškovima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896542"
---
# <a name="set-up-workflows-for-expense-management"></a>Postavljanje tijekova rada za upravljanje troškovima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Možete postaviti postupak tijeka rada za pregled i odobravanje dokumenata o putovanju i troškovima. Možete definirati tijekove rada za izvješća o troškovima, putne naloge i zahtjeve za predujmom gotovine.

Tijek rada predstavlja poslovni proces i definira način prolaska dokumenta kroz sustav. Tijek rada također ukazuje na to tko mora izvršiti zadatak ili odobriti dokument. Nekoliko je blagodati uporabe sustava tijeka rada u vašoj tvrtki ili ustanovi:

- **Dosljedni procesi**: Možete definirati postupak odobrenja za određene dokumente, poput zahtjeva za kupnju i izvješća o troškovima. Uporaba sustava tijeka rada osigurava da se dokumenti obrađuju i odobravaju na dosljedan i učinkovit način.
- **Vidljivost procesa**: Možete pratiti mjerne podatke statusa, povijesti i učinkovitosti određene instance tijeka rada. To vam pomaže utvrditi trebaju li se unijeti promjene u tijek rada kako bi se poboljšala učinkovitost.
- **Centralizirani popis posla**: Korisnici mogu pregledavati centralizirani popis posla kako bi vidjeli zadatke tijeka rada i odobrenja koja su im dodijeljena. 

## <a name="workflow-types"></a>Vrste tijekova rada

Sljedeća tablica navodi vrste tijekova rada u kojima možete stvoriti u mogućnosti **Upravljanje troškovima**.


|              <strong>Vrsta</strong>              |                   <strong>Ovu vrstu upotrijebite za</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatsko odobrenje izvješća o trošku</strong> |            Stvorite tijekove rada odobrenja za izvješća o troškovima.             |
|  <strong>Automatsko objavljivanje izvješća o trošku</strong>   |        Stvorite tijekove rada za automatsko objavljivanje izvješća o troškovima.        |
|       <strong>Stavka retka troška</strong>        |     Stvorite tijekove rada odobrenja za stavke retka izvješća o troškovima.      |
| <strong>Automatsko knjiženje stavke retka troška</strong> | Stvorite tijekove rada za automatsko objavljivanja stavki retka izvješća o troškovima. |
|       <strong>Putni nalog</strong>       |          Stvorite tijekove rada odobrenja za putne naloge.           |
|      <strong>Zahtjev za gotovinski predujam</strong>      |         Stvorite tijekove rada odobrenja zahtjeva za gotovinski predujam.          |
|        <strong>Povrat PDV-a</strong>        | Stvorite tijekove rada odobrenja za povrat poreza na dodanu vrijednost (PDV).  |
