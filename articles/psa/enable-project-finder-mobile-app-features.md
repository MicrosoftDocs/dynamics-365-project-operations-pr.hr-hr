---
title: Omogući značajke aplikacije Project Finder Mobile
description: Kako omogućiti značajke aplikacije Project Finder Mobile za Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073395"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Omogući značajke aplikacije Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaši resursi mogu koristiti aplikaciju Project Finder Mobile na svom telefonu s pomoću sustava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da bi pronašli nove projekte za rad i ažurirali svoje skupove vještina.  
  
 Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Morate postaviti nekoliko mogućnosti u postavci parametara za organizacijsku jedinicu da biste dopustili korisnicima da pregledavaju zahtjeve resursa projekta i ažuriraju svoje vještine.  
  
> [!NOTE]
>  Aplikacija Project Finder Mobile radi samo sa sustavom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ne s lokalnim instalacijama.  
  
1. Idite na **Project Service > Parametri**.  
  
2. Kliknite postavku parametara koju želite koristiti za dopuštanje značajki aplikacije Project Finder Mobile.  
  
3. U dijelu **Općenito** , postavite **Zahtjevi resursa vidljivi resursima** na **Da**.  
  
4. Postavite **Dopusti ažuriranje vještine od strane resursa** na **Da**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ovo je globalna postavka. Upravitelji projekta imaju mogućnost postavljanja vidljivosti pojedinačnog projekta na stranici **Tim projekta** tog projekta.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Obavijesti e-poštom  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] šalje poruke e-pošte vezane za zahtjeve resursa sljedećim primateljima u sljedeće vrijeme:  
  
|Primatelj|Događaj|  
|---------------|-----------|  
|Upravitelj projekta|-   Kada se resurs prijavi za projekt pomoću aplikacije Project Finder Mobile.|  
|Resurs|-   Kada je zadatak projekta za koji se resurs prijavio već izvršio neki drugi resurs.<br />-   Kada je zahtjev za odobrenjem vještine odobren ili odbijen.<br />-   Kada je zahtjev za prijavom na projekt odobren ili odbijen.|  
  
## <a name="privacy-notice"></a>Napomena o zaštiti privatnosti  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Pogledajte također  
 [Postavljanje resursa](../psa/set-up-resources.md)
