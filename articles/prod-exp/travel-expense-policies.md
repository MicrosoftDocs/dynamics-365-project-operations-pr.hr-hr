---
title: Postavljanje pravila o troškovima
description: Možete postaviti pravila koja se odnose na troškove kojih se vaši radnici moraju pridržavati tijekom unosa i slanja izvješća o troškovima i putnih naloga u aplikaciji Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073535"
---
# <a name="set-up-expense-policies"></a>Postavljanje pravila o troškovima

[!include [banner](../includes/banner.md)]

Možete definirati pravila kojih se vaši radnici moraju pridržavati tijekom unosa i podnošenja izvješća o troškovima i putnih naloga.         
Uvođenje pravila koja reguliraju troškove može vam pomoći da učinkovito upravljate troškovima.         

Na primjer, možete postaviti pravila za hotelske troškove u Zagrebu, koja navode da trošak po noćenju ne smije premašiti 1.500,00 kn.       
Ako radnik podnese izvješće o trošku ili putni nalog u kojem cijena sobe prelazi taj iznos, sustav će obavijestiti        
radnika kako je prekoračen iznos iz pravila koja reguliraju troškove. Možete konfigurirati poruku koju će radnik primiti kada        
definirate pravila.      
        
Možete definirati tri vrste pravila:         
        
- Upozorenje – Omogućuje radniku da podnese izvješće o trošku ili putni nalog, ali će trošak biti označen za sve odobravatelje i        
  za kasnije izvješćivanje.        

- Pogreška – Zahtijeva od radnika da revidira trošak kako bi se uskladio s pravilima prije podnošenja izvješća o troškovima ili putnog naloga.       
 
 - Opravdanje – Zahtijeva od radnika ili voditelja da, prije podnošenja izvješća o troškovima ili putnog naloga, unese opravdani razlog za prekoračenje iznosa dozvoljenog pravilima.        

## <a name="policy-tips"></a>Savjeti za pravila
Evo nekoliko prijedloga koji vam mogu pomoći pri stvaranju novih pravila za upravljanje troškovima. 
* Pravila vrijede od određenog datuma i neće se primijeniti ako su stvorena s datumom koji je nastupio nakon datuma nastanka troška. Na primjer, ako danas stvorite novo pravilo kako biste uveli maksimalni trošak obroka od 50 USD, tada se svi postojeći troškovi uneseni od jučer neće provjeriti u skladu s ovim pravilom.
* Tijekom stvaranja pravila za kategoriju troškova koja se može specificirati, razmislite o dodavanju uvjeta za vrstu retka troška. Neka pravila, poput zahtjeva za računom, možda neće imati smisla za specificirane retke i trebala bi se primijeniti samo na zaglavlje ili nespecificirani redak. 
* Pravila upravljanja troškovima prema zadanim se postavkama vrednuju prema izvornom entitetu. Za scenarije među tvrtkama možete umjesto toga postaviti pravila koja će se ocjenjivati prema odredišnom entitetu (entitetu primatelju posudbe). Kako biste pokrenuli pravila prema odredišnom entitetu, uključite značajku „Procijeni pravila koja reguliraju troškove u odnosu na pravnu osobu primateljicu posudbe” u radnom prostoru **Upravljanje značajkama**.

## <a name="when-to-evaluate-policies"></a>Vrijeme za procjenu pravila

U parametrima upravljanja troškovima postoji mogućnost procjene pravila upravljanja troškovima ili kada se spremi redak ili kada se pošalje izvješće o troškovima. Ako se odlučite na procjenu kada se spremi redak to će korisnicima omogućiti da imaju raniji uvid u ono što trebaju učiniti kako bi odjednom dovršili svoje izvješće o troškovima. U suprotnom, možete odgoditi procjenu pravila i uštedjeti vrijeme ako do provjere valjanosti dolazi na kraju, tijekom slanja u tijek rada.
