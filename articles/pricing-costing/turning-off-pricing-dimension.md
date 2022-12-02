---
title: Isključivanje cjenovne veličine
description: U ovom se članku nalaze informacije o načinu isključivanja cjenovnih veličina.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4a13074e20d3005873c28fb95b7443b6ffc84140
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924283"
---
# <a name="turning-off-a-pricing-dimension"></a>Isključivanje cjenovne veličine

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Možda ćete morati pregledati i ažurirati svoju strategiju određivanja cijena svakih nekoliko godina. Za ažuriranja koja izvršite možda bude potrebno da isključite postojeću dimenziju cijena i stvorite novu. Na primjer, možda ste prethodno određivali cijenu po dimenziji **Uloga**, ali sada ste odlučili određivati cijenu po dimenziji **Radno iskustvo**. To od vas može zatražiti da isključite **Ulogu** kao cjenovnu veličinu i kao novu cjenovnu veličinu stvorite **Radno iskustvo**. 

Isključivanje dimenzije cijena, bez obzira na to je li unaprijed pripremljena ili prilagođena, možete provesti postavljanjem polja **Primjenjivo na trošak** i **Primjenjivo na prodaju** za dimenzije cijena na **Ne**.

Međutim, kada to učinite, možda ćete dobiti poruku o pogrešci **Cjenovna veličina ne može se ažurirati ili izbrisati ako postoje povezani podaci o cijenama.**

![Vjerojatnost pogreške poslovnog procesa kad se isključi dimenzija cijena.](media/Business-Process-Error.png)

Ta poruka o pogrešci ukazuje na to da postoje zapisi cijena koji su prethodno postavljeni za dimenziju koja se isključuje. Svi zapisi u recima **Cijena uloge** i **Provizija cijene uloge** koji se odnose na dimenziju moraju se izbrisati prije postavljanja primjenjivosti dimenzije na **Ne**. Ovo se pravilo odnosi na unaprijed pripremljene dimenzije cijena i na prilagođene dimenzije cijena koje ste izradili. Ova provjera valjanosti provodi se zbog toga što svaki zapis **Cijena uloge** mora imati jedinstvenu kombinaciju veličina. Na primjer, u cjeniku pod nazivom **Cijene koštanja za SAD, 2018.**, imate sljedeće retke **Cijena uloge**. 

| Radno mjesto – standardno         | Org. jedinica    |Jedinica   |Cijena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Inženjer sustava|Contoso US|Hour| 100|USD|
| Viši inženjer sustava|Contoso US|Hour| 150| USD|


Kada kao cjenovnu veličinu isključite **Standardni naslov**, a cjenovna veličina i modul za određivanje cijene pretražuje cijenu, upotrebljava se samo vrijednost **Org. jedinica** iz konteksta unosa. Ako je **Org. jedinica** ulaznog konteksta „Contoso US”, rezultat će biti neodređen jer se oba retka podudaraju. Kako biste to izbjegli, kada stvorite zapise **Cijena uloge**, sustav provjerava je li kombinacija veličina jedinstvena. Ako je dimenzija isključena nakon stvaranja zapisa **Cijena uloge**, ovo ograničenje može biti prekršeno. Stoga je potrebno da prije nego što isključite dimenziju izbrišete sve retke **Cijena uloge** i **Provizija cijene uloge** koji imaju tu vrijednost dimenzije.


[!INCLUDE[footer-include](../includes/footer-banner.md)]