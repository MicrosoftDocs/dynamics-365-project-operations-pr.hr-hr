---
title: Izradi predložak projekta
description: Kako izraditi predložak projekta u programu Project Service
author: ruhercul
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149354"
---
# <a name="create-a-project-template-project-service"></a>Izradi predložak projekta (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Predlošci projekta štede vrijeme ako se vaše poduzeće redovito prijavljuje na slične vrste projekata. Nude standardni skup uloga i procijenjenih sati za vrstu projekta. Upravitelji računa i projekta mogu izrađivati projekte koji se temelje na predlošku projekta ili mogu kopirati predložak i izraditi vlastiti.  
  
## <a name="components-of-project-template"></a>Komponente predloška projekta
 Predložak projekta sastoji se od tri komponente:  
  
- **Strukturna analiza rada**: strukturna analiza rada u predlošku projekta ima isti skup elemenata kao projekt. Možete izraditi hijerarhiju zadataka, povezati uloge sa zadacima, odrediti atribute rasporeda, postaviti ovisnosti i prikazati sve podatake u Ganttovom dijagramu. Strukturna analiza rada u predlošcima projekta podržava načine zadatka za svaki zadatak. Nema razlike između predloška projekta i projekta prilikom izrade radnog rasporeda.  
  
- **Procjene projekta**: procjene projekta u predlošcima funkcioniraju na isti način kao i u projektima, osim što su cjenici za zadane cijene i troškove uvijek zadani cjenici troškova i prodaje definirani u parametrima sustava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Ostale funkcije iste su kao u projektu.  
  
- **Formiranje tima projekta**: prilikom formiranja tima projekta za predložak projekta, nije moguće rezervirati imenovani resurs u predlošku. Možete koristiti **Generiraj tim projekta** u strukturnoj analizi rada za generiranje skupa generičkih resursa. Također možete navesti potrebne vještine i stručnosti za generičke resurse. Generički resurs ne možete zamijeniti s resursom koji je moguće rezervirati u predlošku projekta.  
  
## <a name="create-a-project-from-a-template"></a>Izradi projekt iz predloška  
 Projekt iz predloška možete izraditi na sljedeće načine:  
  
-   Kada izrađujete projekt iz ponude, možete odabrati predložak projekta u obrascu za brzu izradu projekta.  
  
-   Prilikom izrade projekta klikom na **Novi projekt**, obrazac projekta prikazuje se prije nego što spremite zapis. Ovdje možete kliknuti polje **Odaberi predložak** da biste odabrali s popisa unaprijed definiranih predložaka projekta u vašoj organizaciji.  
  
-   Kliknite **Izradi projekt iz predloška** na stranici **Predložak projekta** da biste izradili projekt iz predloška.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopiranje komponenti predloška u projekt:  
 Kada kopirate komponente predloška u projekt, postoji nekoliko stvari o kojima biste trebali znati više.  
  
 **Kopiranje strukturne analize rada**: kada kopirate strukturnu analizu rada iz predloška projekta, ako projekt ima kalendar projekta različit od predloška, radno vrijeme iz kalendara projekta primijenit će se na raspored zadataka. To će prilagoditi raspored kalendaru projekta. Isto tako, prvi zadatak strukturne analize rada preuzima datum početka projekta, tako da se ostatak rasporeda hijerarhije zadataka ažurira na temelju trajanja i ovisnosti navedenih u strukturnoj analizi rada predloška.  
  
 **Kopiranje procjene projekta**: prilikom kopiranja redaka procjene projekta, cjenici se ažuriraju na temelju jedinice s vlasništvom projekta za cjenik troškova i klijenta za cjenik prodaje. Jedinična cijena i prodajne cijene određuju se na temelju ovih cjenika na projektima koji su povezani s entitetom prodaje.  
  
 **Kopiranje tima projekta**: kada kopirate tim projekta iz predloška u projekt, generički resursi kopiraju se zajedno s vještinama i stručnostima definiranima u predlošku. Dodjele generičkih resursa također se zadržavaju kao predložak projekta.  
  
### <a name="see-also"></a>Također pogledajte  
 [Vodič za voditelja projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]