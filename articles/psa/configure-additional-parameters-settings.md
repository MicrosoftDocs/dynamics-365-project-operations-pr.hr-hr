---
title: Konfiguriraj dodatne postavke parametara
description: Koko konfigurirati postavke dodatnih parametara u programu Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290755"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="0fa0e-103">Konfiguriraj postavke dodatnih parametara (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0fa0e-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0fa0e-104">Nakon konfiguriranja stavki u prethodnoj temi, morate postaviti dodatne parametre projekta za korištenje na projektima.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="0fa0e-105">Prilikom prve instalacije [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] izradili ste postavku parametara da biste najprije izradili sve zapise koji su potrebni za rad [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="0fa0e-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="0fa0e-106">Sada je vrijeme da se vratite i konfigurirate dodatna polja za ove postavke.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="0fa0e-107">Morat ćete konfigurirati sljedeće postavke:</span><span class="sxs-lookup"><span data-stu-id="0fa0e-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="0fa0e-108">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="0fa0e-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="0fa0e-109">Učestalost faktura</span><span class="sxs-lookup"><span data-stu-id="0fa0e-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="0fa0e-110">Predložak radnog vremena</span><span class="sxs-lookup"><span data-stu-id="0fa0e-110">Work hours template</span></span>  
  
-   <span data-ttu-id="0fa0e-111">Cjenik</span><span class="sxs-lookup"><span data-stu-id="0fa0e-111">Price list</span></span>  
 
<span data-ttu-id="0fa0e-112">U ovom koraku također ćete navesti koju vrstu dodjele resursa želite:</span><span class="sxs-lookup"><span data-stu-id="0fa0e-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="0fa0e-113">**Centralna**.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-113">**Central**.</span></span> <span data-ttu-id="0fa0e-114">Samo upravitelji resursa mogu dodijeliti resurse projektima.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="0fa0e-115">**Hibridna**.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-115">**Hybrid**.</span></span> <span data-ttu-id="0fa0e-116">Upravitelji resursa, upravitelji projekata i upravitelji računa mogu dodijeliti resurse projektima.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="0fa0e-117">Za postavljanje parametara projekta:</span><span class="sxs-lookup"><span data-stu-id="0fa0e-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="0fa0e-118">Idite na **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="0fa0e-119">Kliknite postavku parametara koju želite konfigurirati (onu koje ste izradili tijekom prve instalacije [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), ili kliknite **Novo** da biste izradili novi zapis.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="0fa0e-120">U dijelu **Općenito**, postavite sve mogućnosti za parametre projekta.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="0fa0e-121">U dijelu **Cjenik** kliknite **+** da biste dodali cjenik, odaberite cjenik na padajućem popisu **Cjenik parametara projekta**, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="0fa0e-122">Kliknite gumb **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="0fa0e-123">Za pravilno funkcioniranje Projektne usluge mora se voditi zapis parametra projekta.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="0fa0e-124">Taj se zapis ne smije izbrisati.</span><span class="sxs-lookup"><span data-stu-id="0fa0e-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="0fa0e-125">Pogledajte također</span><span class="sxs-lookup"><span data-stu-id="0fa0e-125">See Also</span></span>  
 [<span data-ttu-id="0fa0e-126">Postavljanje resursa</span><span class="sxs-lookup"><span data-stu-id="0fa0e-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]