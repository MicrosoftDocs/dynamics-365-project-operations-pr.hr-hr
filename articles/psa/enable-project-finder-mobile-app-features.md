---
title: Omogući značajke aplikacije Project Finder Mobile
description: Kako omogućiti značajke aplikacije Project Finder Mobile za Project Service
author: JohnPBurrows
ms.prod: ''
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 3f8f23c1f32d94a514de9ae40bd07b3d8063824c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593676"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Omogući značajke aplikacije Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaši resursi mogu upotrebljavati aplikaciju Project Finder Mobile na svom telefonu s pomoću sustava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kako bi pronašli nove projekte za rad i ažurirali svoje skupove vještina.  
  
 Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Kako biste dopustili korisnicima da pregledavaju preduvjete resursa za projekt i ažuriraju svoje vještine, u postavkama parametara vaše organizacijske jedinice morate odabrati mogućnosti.
  
> [!NOTE]
>  Aplikacija Project Finder Mobile radi samo sa sustavom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ne s lokalnim instalacijama.  
  
1. Idite na **Project Service > Parametri**.  
  
2. Kliknite postavku parametara koju želite koristiti za dopuštanje značajki aplikacije Project Finder Mobile.  
  
3. U dijelu **Općenito**, postavite **Zahtjevi resursa vidljivi resursima** na **Da**.  
  
4. Postavite **Dopusti ažuriranje vještine od strane resursa** na **Da**.  
  
   ![ProjectService&#95; ProjectFinderEnable.](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ovo je globalna postavka. Upravitelji projekta imaju mogućnost postavljanja vidljivosti pojedinačnog projekta na stranici **Tim projekta** tog projekta.  
  
   ![ProjectService&#95; ProjectTeamVisible.](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Obavijesti e-poštom  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] šalje poruke e-pošte vezane za zahtjeve resursa sljedećim primateljima u sljedeće vrijeme:  
  
|Primatelj|Događaj|  
|---------------|-----------|  
|Upravitelj projekta|- Kada se resurs prijavi za projekt s pomoću aplikacije Project Finder Mobile.|  
|Resurs|- Kada je posao projekta za koji se resurs prijavio već izvršio neki drugi resurs.<br />- Kada je njihov zahtjev za odobrenjem vještine odobren ili odbijen.<br />- Kada je njihov zahtjev za prijavom na projekt odobren ili odbijen.|  
  
## <a name="privacy-notice"></a>Obavijest o zaštiti privatnosti  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Pogledajte također  
 [Postavljanje resursa](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
