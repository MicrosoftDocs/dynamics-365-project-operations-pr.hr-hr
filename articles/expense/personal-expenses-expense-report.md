---
title: Rad s osobnim troškovima na izvješću o troškovima
description: U ovoj temi nalaze se informacije o načinu rada s osobnim troškovima zaposlenih za putovanja u poslovne svrhe.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025675"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Rad s osobnim troškovima na izvješću o troškovima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Tijekom poslovnog putovanja zaposlenik može platiti osobne troškove svojom korporativnom kreditnom karticom. Ako postupak nije određen za rukovanje osobnim troškovima, postupak odobravanja izvješća o troškovima mogao bi biti poremećen kad zaposlenik pošalje svoje podrobno izvješće o troškovima.

Dva su načina s pomoću kojih možete raditi s osobnim troškovima zaposlenika:

  - **Plaća zaposlenik**: Vaša tvrtka ili ustanova ne plaća osobne troškove koji se prikazuju za naplatu po kreditnoj kartici poduzeća. Umjesto toga, zaposlenik izravno plaća dobavljača kreditne kartice za troškove. 
  - **Plaća tvrtka** : Vaša tvrtka ili ustanova plaća puni račun za korporativnu kreditnu karticu, a zatim tereti račun radnika za osobne troškove.

Način koji vaša tvrtka ili ustanova upotrebljava možete odabrati na stranici **Parametri upravljanja troškovima**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Omogućivanje funkcije podijeljenog troška kada polje osobnog iznosa ima definiranu vrijednost

Značajka **Omogući funkciju podijeljenog troška kada polje osobnog iznosa ima definiranu vrijednost** odnosi se samo na izvješća o troškovima koja su odobrena s pomoću tijeka rada na razini retka. Izvješća se odobravaju odlaskom na **Obradi izvješća o troškovima** > **Izvješća o troškovima dodijeljena meni** > **Otvori izvješće o troškovima**. 

Kako biste omogućili ovu značajku, idite na mogućnost **Radni prostori** > **Upravljanje značajkama**, odaberite **Omogući funkciju podijeljenog troška kada polje osobni iznos ima definiranu vrijednost**, a zatim odaberite **Omogući odmah**. 

Kada je značajka omogućena, redci troškova koji upotrebljavaju ovu funkciju generiraju dva retka kada se šalje izvješće. Generiraju se dva retka tako da odobravatelj može odobriti svaki redak zasebno.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
