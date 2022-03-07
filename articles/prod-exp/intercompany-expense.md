---
title: Troškovi unutar tvrtke
description: U ovoj temi nalaze se informacije o načinu uporabe troškova unutar tvrtke za dodjelu troškova radnika pravnoj osobi za koju je posao obavljen.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001197"
---
# <a name="intercompany-expenses"></a>Međukompanijski troškovi

Radnik koji je zaposlen u jednoj pravnoj osobi u tvrtki ili ustanovi može obavljati posao za drugu pravnu osobu u istoj tvrtki ili ustanovi. Možete upotrijebiti troškove unutar tvrtke za dodjelu troškova radnika pravnoj osobi za koju je posao obavljen. Pravna osoba koja zapošljava radnika naziva se pravnom osobom koja posuđuje. Pravna osoba kojoj radnik stvara troškove naziva se pravnom osobom koja se zadužuje. 

Prije nego što radnik može stvoriti i poslati troškove unutar tvrtke, morate omogućiti retke za troškove unutar tvrtke. U pravnoj osobi koja posuđuje, na stranici **Parametri za upravljanje troškovima**, odaberite mogućnost **Omogući redak troškova unutar tvrtke**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Knjiženje poreza za troškove unutar kompanije

[!include [banner](../includes/banner.md)]

Prije nego što u svom izvješću o troškovima možete upotrijebiti porezne grupe povezane s pravnom osobom koja posuđuje (izvor) umjesto pravne osobe koja se zadužuje (odredište), morate omogućiti funkciju u postavci poreza na promet Glavne knjige. Kada je parametar **Pravna osoba za knjiženje poreza unutar tvrtke** postavljen na **Izvor**, a stavka **Primijeni pravilo oporezivanja poreza na promet** postavljena na **Ne**, upotrebljava se porezna kombinacija za pravnu osobu koja posuđuje. Kada je isti parametar postavljen na **Odredište**, koristit će se porezna kombinacija za zaduženu pravnu osobu. Za pravne osobe u SAD-u, kada je parametar postavljen na **Izvor**, polje **Potraživanje od poreza na promet** također mora biti konfigurirano na novoj stranici **Grupe za knjiženje u glavnu knjigu**. Računovodstveni mehanizam upotrijebit će podatke iz ovog polja za računovodstveno knjiženje u vezi s porezom.   
Ponašanje je u skladu s redcima troškova knjiženim s projektom ili bez njega.  

## <a name="new-expense-expression-builder"></a>Novi alat za izradu izraza troška

Novi alat za izradu izraza troška rješava probleme sa scenarijima troška među poduzećima unutar tvrtke koji koriste projekte. Ova značajka osigurava da se pri stvaranju troška među poduzećima unutar tvrtke politika troška ispravno vrednuje u odnosu na projekt odabran u retku troška te da se izvješće o trošku može uspješno poslati.

Kako bi značajka alata za izradu izraza troška funkcionirala, mora se uključiti. Osim toga, treba postaviti politiku troška koja ima ID projekta.

Ako ste već konfigurirali pravila koja potvrđuju ID projekta u retku troška, ta se pravila moraju povući. Zatim možete uključiti značajku i ponovno konfigurirati pravila.

Kako biste uključili značajku, slijedite ove korake.

1. Idite na **Radni prostori** \> **Upravljanje značajkama**.
2. S popisa odaberite **Novi alat za izradu izraza troška za rješavanje problema sa scenarijima troška među poduzećima unutar tvrtke koji koriste projekte**. Zatim odaberite **Omogući odmah**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
