---
title: Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta
description: U ovoj temi nalaze se informacije o načinu stvaranja predložaka projekta s pomoću prilagođene radnje Kopiraj projekt.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045000"
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


### <a name="example"></a>Primjer
Sljedeći primjer prikazuje način pozivanja prilagođene radnje **CopyProject** s pomoću skupa parametara **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
