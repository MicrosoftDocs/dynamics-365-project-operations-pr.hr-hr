---
title: Omogući značajke aplikacije Project Finder Mobile
description: Kako omogućiti značajke aplikacije Project Finder Mobile za Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144539"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="bcdba-103">Omogući značajke aplikacije Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="bcdba-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bcdba-104">Vaši resursi mogu upotrebljavati aplikaciju Project Finder Mobile na svom telefonu s pomoću sustava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kako bi pronašli nove projekte za rad i ažurirali svoje skupove vještina.</span><span class="sxs-lookup"><span data-stu-id="bcdba-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skillsets.</span></span>  
  
 <span data-ttu-id="bcdba-105">Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="bcdba-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
    
 <span data-ttu-id="bcdba-106">Kako biste dopustili korisnicima da pregledavaju preduvjete resursa za projekt i ažuriraju svoje vještine, u postavkama parametara vaše organizacijske jedinice morate odabrati mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="bcdba-106">To allow users to view project resource requirements and update skills, options must be selected in the parameter settings for your organizational unit.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="bcdba-107">Aplikacija Project Finder Mobile radi samo sa sustavom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ne s lokalnim instalacijama.</span><span class="sxs-lookup"><span data-stu-id="bcdba-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="bcdba-108">Idite na **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="bcdba-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="bcdba-109">Kliknite postavku parametara koju želite koristiti za dopuštanje značajki aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="bcdba-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="bcdba-110">U dijelu **Općenito**, postavite **Zahtjevi resursa vidljivi resursima** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="bcdba-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="bcdba-111">Postavite **Dopusti ažuriranje vještine od strane resursa** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="bcdba-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="bcdba-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="bcdba-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="bcdba-113">Ovo je globalna postavka.</span><span class="sxs-lookup"><span data-stu-id="bcdba-113">This is a global setting.</span></span> <span data-ttu-id="bcdba-114">Upravitelji projekta imaju mogućnost postavljanja vidljivosti pojedinačnog projekta na stranici **Tim projekta** tog projekta.</span><span class="sxs-lookup"><span data-stu-id="bcdba-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="bcdba-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="bcdba-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="bcdba-116">Obavijesti e-poštom</span><span class="sxs-lookup"><span data-stu-id="bcdba-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="bcdba-117">šalje poruke e-pošte vezane za zahtjeve resursa sljedećim primateljima u sljedeće vrijeme:</span><span class="sxs-lookup"><span data-stu-id="bcdba-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="bcdba-118">Primatelj</span><span class="sxs-lookup"><span data-stu-id="bcdba-118">Recipient</span></span>|<span data-ttu-id="bcdba-119">Događaj</span><span class="sxs-lookup"><span data-stu-id="bcdba-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="bcdba-120">Upravitelj projekta</span><span class="sxs-lookup"><span data-stu-id="bcdba-120">Project manager</span></span>|<span data-ttu-id="bcdba-121">- Kada se resurs prijavi za projekt s pomoću aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="bcdba-121">- A resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="bcdba-122">Resurs</span><span class="sxs-lookup"><span data-stu-id="bcdba-122">Resource</span></span>|<span data-ttu-id="bcdba-123">- Kada je posao projekta za koji se resurs prijavio već izvršio neki drugi resurs.</span><span class="sxs-lookup"><span data-stu-id="bcdba-123">- The project work that the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="bcdba-124">- Kada je njihov zahtjev za odobrenjem vještine odobren ili odbijen.</span><span class="sxs-lookup"><span data-stu-id="bcdba-124">- The skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="bcdba-125">- Kada je njihov zahtjev za prijavom na projekt odobren ili odbijen.</span><span class="sxs-lookup"><span data-stu-id="bcdba-125">- The project sign-up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="bcdba-126">Obavijest o zaštiti privatnosti</span><span class="sxs-lookup"><span data-stu-id="bcdba-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="bcdba-127">Pogledajte također</span><span class="sxs-lookup"><span data-stu-id="bcdba-127">See Also</span></span>  
 [<span data-ttu-id="bcdba-128">Postavljanje resursa</span><span class="sxs-lookup"><span data-stu-id="bcdba-128">Set up resources</span></span>](../psa/set-up-resources.md)
