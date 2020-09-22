---
title: Praćenje statusa projekta
description: Praćenje statusa projekta u programu Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750196"
---
# <a name="track-a-projects-status-project-service"></a>Praćenje statusa projekta (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Koristite [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] da biste pratili tijek klijentovog projekta.  

Kako aktivnost napreduje tako se faze projekta ažuriraju kako bi odražavale fazu aktivnosti:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Novo**    | Kada stvorite projekt, faza je postavljena na **Novo**. Ako ste projekt stvorili iz predloška, u ovoj fazi projekt možda ima raspored, procjene i podatke o timu. U suprotnom, imat ćete strukturu projekta i morat ćete ručno unijeti ostale komponente projekta. |
|  **Ponuda**   |      Kada projekt pridružujete ponudi ili ga stvarate iz ponude, faza projekta postavljena je na **Ponuda** i procijenjeni datumi početka i završetka također se ažuriraju. Kada je projekt u fazi ponude, detalji o ponudi prikazuju se na kartici **Prodaja** na stranici **Projekt**.      |
|   **Plan**   |                                     Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze ugovora, faza projekta ažurira se na **Plan**. Detalji o ugovoru prikazuju se na kartici **Prodaja** na stranici **Projekt**.                                      |
| **Dovrši** |                    Nakon dovršetka projekta možete prebaciti fazu na **Dovršeno**. Kada je faza projekta postavljena na dovršeno, podrazumijeva se da je posao 100% dovršen, ali je projekt još uvijek otvoren za vrijeme na čekanju ili stavke troškova koje treba zabilježiti.                     |
|  **Zatvori**   |           Kada zabilježite sve transakcije na projektu i ne očekujete daljnje transakcije, možete fazu ručno postaviti na **Zatvoreno**. Kada je projekt postavljen na **Zatvoreno**, više ne možete bilježiti transakcije na projektu i projekt će biti samo za čitanje.           |

## <a name="to-track-a-projects-status"></a>Za praćenje statusa projekta  

1.  Idite na **Project Service > Projekti**.  

2.  Kliknite projekt na kojem radite.  

3.  Na traci na vrhu ekrana odaberite strelicu prema dolje pokraj naziva projekta, a zatim kliknite **Praćenje projekta**.  

4.  Odaberite **Praćenje truda** ili **Praćenje troška** na padajućem popisu iznad popisa zadataka.  

5.  Dvokliknite bilo koji zadatak da biste ga uredili. Također možete premjestiti ili promijeniti veličinu traka u Ganttovom grafikonu da biste promijenili vrijeme i tijek za zadatak.  

### <a name="see-also"></a>Pogledajte također  
 [Vodič voditelja projekta](../project-service/project-manager-guide.md)
