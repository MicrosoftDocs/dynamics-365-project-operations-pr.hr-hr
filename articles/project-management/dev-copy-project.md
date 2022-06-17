---
title: Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta
description: U ovom se članku nalaze informacije o stvaranju predložaka projekata pomoću prilagođene akcije Kopiraj projekt.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923823"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja svih zadataka natrag generičkim resursima koji predstavljaju ulogu. Klijenti mogu upotrebljavati ovu funkcionalnost za izradu osnovnih predložaka projekta.

Kad odaberete **Kopiraj projekt**, ažurira se status ciljnog projekta. Upotrijebite **Razlog statusa** kako biste odredili kada je radnja kopiranja dovršena. Odabir **Kopiraj projekt** također ažurira datum početka projekta na trenutačni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.

## <a name="copy-project-custom-action"></a>Prilagođena radnja značajke Kopiraj projekt

### <a name="name"></a>Ime/naziv 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Ulazni parametri

Postoje tri ulazna parametra:

- **ReplaceNamedResources** ili **ClearTeamsAndAssignments** – Postavite samo jednu od mogućnosti. Ne postavljajte oboje.

    - **\{"ReplaceNamedResources":true\}** – zadano ponašanje za projektne operacije. Svi imenovani resursi zamjenjuju se generičkim resursima.
    - **\{"ClearTeamsAndAssignments":true\}** – zadano ponašanje za Project for the Web. Svi zadaci i članovi tima su uklonjeni.

- **SourceProject** – referenca entiteta izvornog projekta iz kojeg se kopira. Ovaj parametar ne može imati vrijednost null.
- **Cilj** – referenca entiteta ciljnog projekta u koji se kopira. Ovaj parametar ne može imati vrijednost null.

Sljedeća tablica sadrži sažetak tri parametra.

| Parametar                | Tip             | Vrijednost                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Booleov          | **Istinito** ili **netočno** |
| ClearTeamsAndAssignments | Booleov          | **Istinito** ili **netočno** |
| SourceProject            | Referenca entiteta | Izvorni projekt    |
| Cilj                   | Referenca entiteta | Ciljni projekt    |

Dodatne zadane postavke za akcije potražite u članku [Korištenje akcija web-API-ja](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Provjere valjanosti

Izvršene su sljedeće provjere valjanosti.

1. Null provjerava i dohvaća izvorne i ciljne projekte kako bi potvrdio postojanje oba projekta u organizaciji.
2. Sustav provjerava je li ciljni projekt valjan za kopiranje provjerom sljedećih uvjeta:

    - Na projektu nema prethodne aktivnosti (uključujući odabir kartice **Zadaci**), a projekt je novostvoren.
    - Nema prethodne kopije, za ovaj projekt nije zatražen uvoz, a projekt nema status **Neuspjeli**.

3. Operacija se ne poziva korištenjem HTTP-a.

## <a name="specify-fields-to-copy"></a>Navedite polja za kopiranje

Kada je akcija pozvana, značajka **Kopiraj projekt** pogledat će u projektu prikaz **Kopiranje stupaca projekta** kako bi se utvrdilo koja polja kopirati kada se projekt kopira.

### <a name="example"></a>Primjer

Sljedeći primjer pokazuje kako nazvati prilagođenu akciju **CopyProjectV3** sa skupom parametara **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
