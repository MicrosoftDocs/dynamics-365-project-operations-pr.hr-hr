---
title: Aktivacija i revidiranje projektne ponude
description: U ovom se članku navode informacije o aktiviranju i revidiranju ponuda u sustavu Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410367"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktivacija i revidiranje projektne ponude

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Mogućnosti aktivacije i revizije pomažu vam u praćenju verzija za ponude temeljene na projektu tijekom faza procjene i pregovora. Kada se nacrt ponude aktivira, on postaje samo za čitanje.

Mogućnosti aktivacije i revizije omogućuju vam obavljanje sljedećih zadataka:

- Osvajanje ili gubitak ponude tek nakon aktivacije.
- Revidirajte ponudu kako biste promijenili postojeću ponudu ili izradili novu verziju.

> [!NOTE]
> Nakon što se značajka za aktivaciju i reviziju ponude omogući, ne može se onemogućiti.

Da biste uključili mogućnost aktiviranja i revizije ponuda temeljenih na projektu, slijedite ove korake.

1. Idite na **Postavke** \> **Parametri**.
1. Otvorite zapis **Parametri**.
1. U oknu s radnjama, na kartici **Kontrola značajki**, odaberite **Omogući aktivaciju i reviziju ponuda**.
1. U potvrdnom dijaloškom okviru kliknite **U redu**.
1. Osvježite preglednik nakon nekoliko trenutaka. Mogućnosti aktivacije i revizije sada bi trebale biti dostupne. Znat ćete da su te mogućnosti omogućene ako gumb **Omogući aktivacije i revizije za ponude** više nije vidljiv u oknu radnji.

## <a name="activating-a-quote"></a>Aktiviranje ponude

Nakon omogućavanja značajke za aktivaciju i reviziju ponuda, u oknu s radnjama gumbi **Zatvori ponudu kao dobivenu** i **Zatvori ponudu kao izgubljenu** neće biti dostupni za ponude nacrta projekta. Dostupni su samo nakon aktivacije ponude.

Aktivacija predstavlja fazu u procesu ponude kada želite spriječiti daljnje izmjene ponude. U ovoj fazi ponuda se šalje na interni pregled ili kupcu.

Gumbi **Zatvori ponudu kao dobivenu** i **Zatvori ponudu kao izgubljenu** u oknu radnji dostupni su za aktivirane ponude. Ovisno o ishodu internog pregleda ili pregleda kupca, možete upotrijebiti jedan od tih gumba za zatvaranje aktivirane ponude. Odabirom stavke **Revidiraj ponudu** omogućuju se pregovori i izmjene aktiviranih ponuda.

## <a name="revising-a-quote"></a>Revidiranje ponude

Ako morate promijeniti aktiviranu ponudu, odaberite **Revidiraj ponudu**. Ponuda je zatvorena te se koristi šifra razloga **revidirano**. Zatim se izrađuje nova ponuda koja ima isti ID i uvećani broj revizije. Sve pojedinosti iz originalne ponude kopiraju se u novu ponudu. Nova ponuda je u statusu nacrta i može se uređivati po potrebi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
