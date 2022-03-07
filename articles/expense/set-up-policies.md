---
title: Definiranje pravila koja reguliraju troškove
description: Možete definirati pravila koja reguliraju troškove kojih se vaši radnici moraju pridržavati tijekom unosa i podnošenja izvješća o troškovima i putnih naloga.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d29b1a9c1a935b933f403f78279b74577d11089007ce1d1090c361075822263a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986347"
---
# <a name="define-expense-policies"></a>Definiranje pravila koja reguliraju troškove

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Možete definirati pravila kojih se vaši radnici moraju pridržavati tijekom unosa i podnošenja izvješća o troškovima i putnih naloga.         
Uvođenje pravila koja reguliraju troškove može vam pomoći da učinkovito upravljate troškovima.         

Na primjer, možete postaviti pravila za hotelske troškove u Zagrebu, koja navode da trošak po noćenju ne smije premašiti 1.500,00 kn.       
Ako radnik podnese izvješće o trošku ili putni nalog u kojem cijena sobe prelazi taj iznos, sustav će obavijestiti         
radnika kako je prekoračen iznos iz pravila koja reguliraju troškove. Možete konfigurirati poruku koju će radnik primiti kada        
definirate pravila.      
        
Možete definirati tri vrste pravila:         
        
- **Upozorenje**: Omogućuje radniku da podnese izvješće o trošku ili putni nalog, ali će trošak biti označen za sve odobravatelje i         
  za kasnije izvješćivanje.        

- **Pogreška**: Zahtijeva od radnika da revidira trošak kako bi se uskladio s pravilima prije podnošenja izvješća o troškovima ili putnog naloga.        
 
 - **Opravdanje**: Zahtijeva od radnika ili voditelja da, prije podnošenja izvješća o troškovima ili putnog naloga, unese opravdani razlog za prekoračenje iznosa dozvoljenog pravilima.        

## <a name="policy-tips"></a>Savjeti za pravila
Evo nekoliko prijedloga koji vam mogu pomoći pri stvaranju novih pravila za upravljanje troškovima: 

- Pravila vrijede od određenog datuma, što znači da se neće primijeniti ako su stvorena s datumom koji je nastupio nakon datuma nastanka troška. Na primjer, danas stvorite novo pravilo kojim se propisuje maksimalni trošak obroka od 300,00 kn. Svi postojeći troškovi uneseni za jučerašnji dan neće se provjeravati u skladu s ovim pravilom.
- Tijekom stvaranja pravila za kategoriju troškova koja se može specificirati, razmislite o dodavanju uvjeta za vrstu retka troška. Neka pravila, poput zahtijevanja računa, možda nemaju smisla za specificirane retke. U toj se situaciji pravilo primjenjuje samo na redak zaglavlja ili nespecificiran redak. 
- Pravila upravljanja troškovima prema zadanim se postavkama vrednuju prema izvornom entitetu. Za scenarije među tvrtkama možete umjesto toga postaviti pravila koja će se ocjenjivati prema odredišnom entitetu (entitetu primatelju posudbe). Kako biste pokrenuli pravila prema odredišnom entitetu, uključite značajku **Procijeni pravila koja reguliraju troškove u odnosu na pravnu osobu primateljicu posudbe** u radnom prostoru **Upravljanje značajkama**.

## <a name="when-to-evaluate-policies"></a>Vrijeme za procjenu pravila

U parametrima upravljanja troškovima možete odabrati procjenu pravila upravljanja troškovima kada je redak spremljen ili izvješće o troškovima podneseno. Ako odlučite na procjenu kada se redak spremi, korisnici će imati raniji uvid u ono što trebaju učiniti kako bi odjednom dovršili svoje izvješće o troškovima. U suprotnom, možete odgoditi procjenu pravila i uštedjeti vrijeme provjerom valjanosti na kraju, tijekom slanja u tijek rada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]