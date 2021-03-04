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
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="f73c6-103">Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta</span><span class="sxs-lookup"><span data-stu-id="f73c6-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="f73c6-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="f73c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f73c6-105">Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja svih zadataka natrag generičkim resursima koji predstavljaju ulogu.</span><span class="sxs-lookup"><span data-stu-id="f73c6-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="f73c6-106">Klijenti mogu upotrebljavati ovu funkcionalnost za izradu osnovnih predložaka projekta.</span><span class="sxs-lookup"><span data-stu-id="f73c6-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="f73c6-107">Kad odaberete **Kopiraj projekt**, ažurira se status ciljnog projekta.</span><span class="sxs-lookup"><span data-stu-id="f73c6-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="f73c6-108">Upotrijebite **Razlog statusa** kako biste odredili kada je radnja kopiranja dovršena.</span><span class="sxs-lookup"><span data-stu-id="f73c6-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="f73c6-109">Odabir **Kopiraj projekt** također ažurira datum početka projekta na trenutačni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.</span><span class="sxs-lookup"><span data-stu-id="f73c6-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="f73c6-110">Prilagođena radnja značajke Kopiraj projekt</span><span class="sxs-lookup"><span data-stu-id="f73c6-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="f73c6-111">Ime</span><span class="sxs-lookup"><span data-stu-id="f73c6-111">Name</span></span> 

<span data-ttu-id="f73c6-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="f73c6-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="f73c6-113">Ulazni parametri</span><span class="sxs-lookup"><span data-stu-id="f73c6-113">Input parameters</span></span>
<span data-ttu-id="f73c6-114">Postoje tri ulazna parametra:</span><span class="sxs-lookup"><span data-stu-id="f73c6-114">There are three input parameters:</span></span>

| <span data-ttu-id="f73c6-115">Parametar</span><span class="sxs-lookup"><span data-stu-id="f73c6-115">Parameter</span></span>          | <span data-ttu-id="f73c6-116">Tip</span><span class="sxs-lookup"><span data-stu-id="f73c6-116">Type</span></span>   | <span data-ttu-id="f73c6-117">Vrijednosti</span><span class="sxs-lookup"><span data-stu-id="f73c6-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="f73c6-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="f73c6-118">ProjectCopyOption</span></span>  | <span data-ttu-id="f73c6-119">String</span><span class="sxs-lookup"><span data-stu-id="f73c6-119">String</span></span> | <span data-ttu-id="f73c6-120">**{"removeNamedResources":true}** ili **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="f73c6-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="f73c6-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="f73c6-121">SourceProject</span></span>      | <span data-ttu-id="f73c6-122">Referenca entiteta</span><span class="sxs-lookup"><span data-stu-id="f73c6-122">Entity Reference</span></span> | <span data-ttu-id="f73c6-123">SourceProject</span><span class="sxs-lookup"><span data-stu-id="f73c6-123">Source Project</span></span> |
| <span data-ttu-id="f73c6-124">Cilj</span><span class="sxs-lookup"><span data-stu-id="f73c6-124">Target</span></span>             | <span data-ttu-id="f73c6-125">Referenca entiteta</span><span class="sxs-lookup"><span data-stu-id="f73c6-125">Entity Reference</span></span> | <span data-ttu-id="f73c6-126">Ciljani projekt</span><span class="sxs-lookup"><span data-stu-id="f73c6-126">Target Project</span></span> |


- <span data-ttu-id="f73c6-127">**{"clearTeamsAndAssignments":true}** : Tri zadana ponašanja za Projekt za Web i uklonit će sve zadatke i članove tima.</span><span class="sxs-lookup"><span data-stu-id="f73c6-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="f73c6-128">**{"removeNamedResources":true}** Zadano ponašanje za aplikaciju Project Operations i vratit će dodjele na generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="f73c6-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="f73c6-129">Dodatne informacije o radnjama potražite u članku [Uporaba Web API radnji](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="f73c6-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="f73c6-130">Navedite polja za kopiranje</span><span class="sxs-lookup"><span data-stu-id="f73c6-130">Specify fields to copy</span></span> 
<span data-ttu-id="f73c6-131">Kada je akcija pozvana, značajka **Kopiraj projekt** pogledat će u projektu prikaz **Kopiranje stupaca projekta** kako bi se utvrdilo koja polja kopirati kada se projekt kopira.</span><span class="sxs-lookup"><span data-stu-id="f73c6-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="f73c6-132">Primjer</span><span class="sxs-lookup"><span data-stu-id="f73c6-132">Example</span></span>
<span data-ttu-id="f73c6-133">Sljedeći primjer prikazuje način pozivanja prilagođene radnje **CopyProject** s pomoću skupa parametara **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="f73c6-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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
