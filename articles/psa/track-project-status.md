---
title: Praćenje statusa projekta
description: Praćenje statusa projekta u programu Project Service
author: ruhercul
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
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593373"
---
# <a name="track-a-projects-status-project-service"></a>Praćenje statusa projekta (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Koristite [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] da biste pratili tijek klijentovog projekta.  

Kako aktivnost napreduje tako se faze projekta ažuriraju kako bi odražavale fazu aktivnosti:  

| Zadatak | Opis | 
|------------|----------|
| **New** | Kada stvorite projekt, faza je postavljena na **Novo**. Ako ste projekt stvorili iz predloška, u ovoj fazi projekt možda ima raspored, procjene i podatke o timu. U suprotnom, imat ćete strukturu projekta i morat ćete ručno unijeti ostale komponente projekta. |
| **Ponuda** |  Kada projekt pridružujete ponudi ili ga stvarate iz ponude, faza projekta postavljena je na **Ponuda**, a procijenjeni datumi početka i završetka također se ažuriraju. Kada je projekt u fazi ponude, detalji o ponudi prikazuju se na kartici **Prodaja** na stranici **Projekt**. |
| **Plan** |  Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze ugovora, faza projekta ažurira se na **Plan**. Detalji o ugovoru prikazuju se na kartici **Prodaja** na stranici **Projekt**. |
| **Dovrši** | Nakon dovršetka projekta možete prebaciti fazu na **Dovršeno**. Kada je faza projekta postavljena na dovršeno, podrazumijeva se da je posao 100% dovršen, ali je projekt još uvijek otvoren za vrijeme na čekanju ili stavke troškova koje treba zabilježiti. |
| **Zatvori** | Kada zabilježite sve transakcije na projektu i ne očekujete daljnje transakcije, možete fazu ručno postaviti na **Zatvoreno**. Kada je projekt postavljen na **Zatvoreno**, više ne možete bilježiti transakcije na projektu i projekt će biti samo za čitanje. |

## <a name="to-track-a-projects-status"></a>Za praćenje statusa projekta  

1.  Idite na **Project Service > Projekti**.  

2.  Kliknite projekt na kojem radite.  

3.  Na traci na vrhu ekrana odaberite strelicu prema dolje pokraj naziva projekta, a zatim kliknite **Praćenje projekta**.  

4.  Odaberite **Praćenje truda** ili **Praćenje troška** na padajućem popisu iznad popisa zadataka.  

5.  Dvokliknite bilo koji zadatak da biste ga uredili. Također možete premjestiti ili promijeniti veličinu traka u Ganttovom grafikonu da biste promijenili vrijeme i tijek za zadatak.  

### <a name="see-also"></a>Pogledajte također  
 [Vodič voditelja projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
