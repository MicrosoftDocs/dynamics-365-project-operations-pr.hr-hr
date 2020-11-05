---
title: Procjene prodaje i projekti
description: Ova tema pruža informacije o tome kako iskoristiti prednosti rasporeda i procjena u postupku prodaje.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073406"
---
# <a name="sales-estimates-and-projects"></a>Procjene prodaje i projekti

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tijekom prodajnog postupka možete stvoriti procjenu prodaje povezivanjem projekta s prodajnom ponudom. Na taj način moguća je deterministička procjena tijekom prodajnog postupka kako biste iskoristili prednosti mogućnosti zakazivanja i procjene projekta. Ako se ostvari prodaja, raspored koji je korišten za svrhe procjene prodaje može se koristiti kao temelj za daljnje preciziranje plana projekta.

## <a name="linking-a-project-to-a-quote-line"></a>Povezivanje projekta s retkom ponude

Kada stvorite redak ponude temeljen na projektu, možete stvoriti novi projekt ili povezati postojeći projekt na stranici **Redak ponude**. 

> ![Obrazac retka ponude](media/project-8.png)
 
Kada stvorite novi projekt na temelju pojedinosti retka ponude, možete iskoristiti prednosti predložaka projekta. Predlošci projekata modeli su projekata koji predstavljaju standardne projektne planove i financijske procjene koje su uobičajene u tvrtki li ustanovi. Također mogu predstavljati kopije projektnih planova i procjena iz prethodnih projekata.

> ![Detalji retka ponude](media/project-9.png)
  
Kada stvorite projekt na temelju ponude, projekt se automatski povezuje s retkom ponude.

## <a name="components-of-estimates-in-a-project"></a>Komponente procjena u projektu

Raspored omogućuje dijeljenje posla u zadatke, održavanje hijerarhije zadataka, određivanje resursa potrebnih za dovršetak zadatka i dodjelu procjene rada potrebnog za dovršetak zadatka.

Procjene rada i rasporeda možete definirati pomoću polja na kartici **Raspored** na stranici **Projekt**. Budući da je cjenik povezan s projektom, financijske procjene izračunavaju se pomoću cijena troškova i prodajnih cijena definiranih u cjeniku.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Uvoz procjena iz projekta u ponudu

Nakon što definirate procjene projekta, možete ih uvesti u redak ponude. Na stranici **Pojedinosti retka ponude** odaberite **Uvezi iz procjene** na vrpci da biste saželi procjene projekta po vrsti transakcije, ulozi ili razini zadatka.
