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
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949805"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="b7fcb-103">Razvoj predložaka projekata s pomoću mogućnosti Kopiranja projekta</span><span class="sxs-lookup"><span data-stu-id="b7fcb-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="b7fcb-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b7fcb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b7fcb-105">Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja svih zadataka natrag generičkim resursima koji predstavljaju ulogu.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="b7fcb-106">Klijenti mogu upotrebljavati ovu funkcionalnost za izradu osnovnih predložaka projekta.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="b7fcb-107">Kad odaberete **Kopiraj projekt**, ažurira se status ciljnog projekta.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="b7fcb-108">Upotrijebite **Razlog statusa** kako biste odredili kada je radnja kopiranja dovršena.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="b7fcb-109">Odabir **Kopiraj projekt** također ažurira datum početka projekta na trenutačni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="b7fcb-110">Prilagođena radnja značajke Kopiraj projekt</span><span class="sxs-lookup"><span data-stu-id="b7fcb-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="b7fcb-111">Ime</span><span class="sxs-lookup"><span data-stu-id="b7fcb-111">Name</span></span> 

<span data-ttu-id="b7fcb-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="b7fcb-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="b7fcb-113">Ulazni parametri</span><span class="sxs-lookup"><span data-stu-id="b7fcb-113">Input parameters</span></span>
<span data-ttu-id="b7fcb-114">Postoje tri ulazna parametra:</span><span class="sxs-lookup"><span data-stu-id="b7fcb-114">There are three input parameters:</span></span>

| <span data-ttu-id="b7fcb-115">Parametar</span><span class="sxs-lookup"><span data-stu-id="b7fcb-115">Parameter</span></span>          | <span data-ttu-id="b7fcb-116">Tip</span><span class="sxs-lookup"><span data-stu-id="b7fcb-116">Type</span></span>   | <span data-ttu-id="b7fcb-117">Vrijednosti</span><span class="sxs-lookup"><span data-stu-id="b7fcb-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="b7fcb-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="b7fcb-118">ProjectCopyOption</span></span>  | <span data-ttu-id="b7fcb-119">String</span><span class="sxs-lookup"><span data-stu-id="b7fcb-119">String</span></span> | <span data-ttu-id="b7fcb-120">**{"removeNamedResources":true}** ili **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="b7fcb-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="b7fcb-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="b7fcb-121">SourceProject</span></span>      | <span data-ttu-id="b7fcb-122">Referenca entiteta</span><span class="sxs-lookup"><span data-stu-id="b7fcb-122">Entity Reference</span></span> | <span data-ttu-id="b7fcb-123">SourceProject</span><span class="sxs-lookup"><span data-stu-id="b7fcb-123">Source Project</span></span> |
| <span data-ttu-id="b7fcb-124">Cilj</span><span class="sxs-lookup"><span data-stu-id="b7fcb-124">Target</span></span>             | <span data-ttu-id="b7fcb-125">Referenca entiteta</span><span class="sxs-lookup"><span data-stu-id="b7fcb-125">Entity Reference</span></span> | <span data-ttu-id="b7fcb-126">Ciljani projekt</span><span class="sxs-lookup"><span data-stu-id="b7fcb-126">Target Project</span></span> |


- <span data-ttu-id="b7fcb-127">**{"clearTeamsAndAssignments":true}** : Tri zadana ponašanja za aplikaciju Project for the Web i uklonit će sve zadatke i članove tima.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="b7fcb-128">**{"removeNamedResources":true}** Zadano ponašanje za aplikaciju Project Operations i vratit će dodjele na generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="b7fcb-129">Dodatne informacije o radnjama potražite u članku [Uporaba Web API radnji](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="b7fcb-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="b7fcb-130">Navedite polja za kopiranje</span><span class="sxs-lookup"><span data-stu-id="b7fcb-130">Specify fields to copy</span></span> 
<span data-ttu-id="b7fcb-131">Kada je akcija pozvana, značajka **Kopiraj projekt** pogledat će u projektu prikaz **Kopiranje stupaca projekta** kako bi se utvrdilo koja polja kopirati kada se projekt kopira.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="b7fcb-132">Primjer</span><span class="sxs-lookup"><span data-stu-id="b7fcb-132">Example</span></span>
<span data-ttu-id="b7fcb-133">Sljedeći primjer prikazuje način pozivanja prilagođene radnje **CopyProject** s pomoću skupa parametara **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="b7fcb-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]