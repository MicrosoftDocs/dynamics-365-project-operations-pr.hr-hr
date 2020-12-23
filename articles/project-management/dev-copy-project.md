---
title: Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta
description: U ovoj temi nalaze se informacije o načinu stvaranja predložaka projekta s pomoću prilagođene radnje Kopiraj projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642399"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja svih zadataka natrag generičkim resursima koji predstavljaju ulogu. Klijenti mogu upotrebljavati ovu funkcionalnost za izradu osnovnih predložaka projekta.

Kad odaberete **Kopiraj projekt**, ažurira se status ciljnog projekta. Upotrijebite **Razlog statusa** kako biste odredili kada je radnja kopiranja dovršena. Odabir **Kopiraj projekt** također ažurira datum početka projekta na trenutačni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.

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
