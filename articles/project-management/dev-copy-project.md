---
title: Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta
description: U ovoj temi nalaze se informacije o načinu stvaranja predložaka projekta s pomoću prilagođene radnje Kopiraj projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073328"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja svih zadataka natrag u generičke resurse koji predstavljaju ulogu. Klijenti mogu upotrebljavati ovu funkcionalnost za izradu osnovnih predložaka projekta.

Kad odaberete **Kopiraj projekt** , ažurira se status ciljnog projekta. Upotrijebite **Razlog statusa** kako biste odredili kada je radnja kopiranja dovršena. Odabir **Kopiraj projekt** također ažurira datum početka projekta na trenutačni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.

## <a name="copy-project-custom-action"></a>Prilagođena radnja značajke Kopiraj projekt 

### <a name="name"></a>Ime 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Ulazni parametri
Postoje tri ulazna parametra:

| Parametar          | Tip   | Vrijednosti                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** ili **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referenca entiteta | SourceProject |
| Cilj             | Referenca entiteta | Ciljani projekt |


- **{"clearTeamsAndAssignments":true}** : Tri zadana ponašanja za Projekt za Web i uklonit će sve zadatke i članove tima.
- **{"removeNamedResources":true}** Zadano ponašanje za aplikaciju Project Operations i vratit će dodjele na generičke resurse.

Dodatne informacije o radnjama potražite u članku [Uporaba Web API radnji](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Navedite polja za kopiranje 
Kada je akcija pozvana, značajka **Kopiraj projekt** pogledat će u projektu prikaz **Kopiranje stupaca projekta** kako bi se utvrdilo koja polja kopirati kada se projekt kopira.
