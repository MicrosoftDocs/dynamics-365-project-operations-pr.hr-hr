---
title: Troškovi unutar tvrtke
description: U ovoj temi nalaze se informacije o načinu uporabe troškova unutar tvrtke za dodjelu troškova radnika pravnoj osobi za koju je posao obavljen.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005062"
---
# <a name="intercompany-expenses"></a>Međukompanijski troškovi

Radnik koji je zaposlen u jednoj pravnoj osobi u tvrtki ili ustanovi može obavljati posao za drugu pravnu osobu u istoj tvrtki ili ustanovi. Možete upotrijebiti troškove unutar tvrtke za dodjelu troškova radnika pravnoj osobi za koju je posao obavljen. Pravna osoba koja zapošljava radnika naziva se pravnom osobom koja posuđuje. Pravna osoba kojoj radnik stvara troškove naziva se pravnom osobom koja se zadužuje. 

Prije nego što radnik može stvoriti i poslati troškove unutar tvrtke, morate omogućiti retke za troškove unutar tvrtke. U pravnoj osobi koja posuđuje, na stranici **Parametri za upravljanje troškovima**, odaberite mogućnost **Omogući redak troškova unutar tvrtke**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Knjiženje poreza za troškove unutar kompanije

[!include [banner](../includes/banner.md)]

Prije nego što u svom izvješću o troškovima možete upotrijebiti porezne grupe povezane s pravnom osobom koja posuđuje (izvor) umjesto pravne osobe koja se zadužuje (odredište), morate omogućiti funkciju u postavci poreza na promet Glavne knjige. Kada je parametar **Pravna osoba za knjiženje poreza unutar tvrtke** postavljen na **Izvor**, a stavka **Primijeni pravilo oporezivanja poreza na promet** postavljena na **Ne**, upotrebljava se porezna kombinacija za pravnu osobu koja posuđuje. Kada je isti parametar postavljen na **Odredište**, koristit će se porezna kombinacija za zaduženu pravnu osobu. Za pravne osobe u SAD-u, kada je parametar postavljen na **Izvor**, polje **Potraživanje od poreza na promet** također mora biti konfigurirano na novoj stranici **Grupe za knjiženje u glavnu knjigu**. Računovodstveni mehanizam upotrijebit će podatke iz ovog polja za računovodstveno knjiženje u vezi s porezom.   
Ponašanje je u skladu s redcima troškova knjiženim s projektom ili bez njega.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]