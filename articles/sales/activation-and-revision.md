---
title: Aktiviranje i revidiranje ponude projekta
description: U ovom se članku nalaze informacije o aktivaciji i reviziji ponuda u microsoftu Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Aktiviranje i revidiranje ponude projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Mogućnosti aktivacije i revizije pomažu vam da pratite određivanje verzija za ponude temeljene na projektima tijekom faza procjene i pregovora. Kada se aktivira skica ponude, ona postaje samo za čitanje.

Mogućnosti aktivacije i revizije omogućuju vam izvršavanje sljedećih zadataka:

- Osvojite ili izgubite ponude tek nakon aktivacije.
- Revidirajte ponudu da biste promijenili postojeću ponudu ili stvorili novu verziju.

> [!NOTE]
> Nakon što je značajka za aktivaciju i reviziju ponuda omogućena, ona se ne može onemogućiti.

Da biste uključili mogućnost aktiviranja i revizije ponuda temeljenih na projektu, slijedite ove korake.

1. Otvorite **Parametri postavki** \> **·**.
1. **Otvorite zapis Parametri**.
1. U oknu akcije na **kartici Kontrola** značajki odaberite **Omogući aktivaciju i reviziju ponuda**.
1. U potvrdnom dijaloškom okviru kliknite **U redu**.
1. Nakon nekoliko trenutaka osvježite preglednik. Mogućnosti aktivacije i revizije sada bi trebale biti dostupne. Znat ćete da su te mogućnosti omogućene **ako se gumb Omogući aktivaciju** i reviziju ponuda više ne pojavljuje u oknu akcije.

## <a name="activating-a-quote"></a>Aktiviranje ponude

Nakon što je omogućena značajka za aktivaciju i reviziju ponuda, **gumbi Zatvori ponudu kao osvojenu** i **Zatvori ponudu kao izgubljenu** u oknu akcije nisu dostupni za skice ponuda projekta. Dostupni su tek nakon aktivacije ponude.

Aktivacija predstavlja fazu u procesu citiranja kada želite spriječiti nove promjene ponude. U ovoj fazi ponuda se šalje na interni pregled ili kupcu.

Gumbi **Zatvori ponudu kao osvojenu** i **Zatvori ponudu kao izgubljenu** u oknu akcije dostupni su za aktivirane navodnike. Ovisno o ishodu interne recenzije ili recenzije kupca, možete koristiti jedan od ovih gumba za zatvaranje aktivirane ponude. Pregovore i promjene na aktiviranim ponudama možete izvršiti tako da odaberete **Revidiraj ponudu**.

## <a name="revising-a-quote"></a>Revizija ponude

Ako morate izmijeniti aktiviranu ponudu, odaberite **Revidiraj ponudu**. Ponuda je zatvorena i koristi se **revidirana** šifra razloga. Zatim se stvara nova ponuda koja ima isti ID i povećani broj revizije. Svi detalji iz izvorne ponude kopiraju se u novu ponudu. Nova ponuda je u statusu skice i može se uređivati prema potrebi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
