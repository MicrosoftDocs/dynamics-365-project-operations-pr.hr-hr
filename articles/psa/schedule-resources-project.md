---
title: Zakažite resurse za projekt
description: Zakazivanje resursa za projekt u programu Project Service
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
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132119"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Zakazivanje resursa za projekt (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Moguća je provjera raspoloživosti resursa da biste dobili opći pregled o tome koliko su rezervirani resursi ili možete filtrirati prikaze po vještinama, timu, lokacijama i drugim mogućnostima.  
  
Ploča s rasporedom prikazuje popis resursa i njihovu raspoloživost. Odaberite način prikaza za prikaz raspoloživosti po **Satima**, **Danu**, **Tjednu**, ili **Mjesecu**.  
  
Prije nego što koristite raspored, važno je da ga postavite. Dodatne informacije potražite u članku [Konfiguriranje ploče rasporeda (Field Service, Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Ako koristite stariju verziju, za dostupnost resursa pogledajte članak [Prikaz dostupnosti resursa](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Da biste upotrebljavali funkcije rezervacija ploče s rasporedom, geokodiranje i usluge lokacije, trebate uključiti karte.  
> 
> 1. Na glavnom izborniku odaberite mogućnost **Zakazivanje resursa** > **Administracija**.  
> 2. Kliknite **Parametri zakazivanja**.  
> 3. Otvorite zapis i pomaknite se prema dolje do odjeljka **Resource Scheduling Optimization**.  
> 4. U polju **Povezivanje s kartama** odaberite **Da**.  
> 5. Prihvatite uvjete i spremite zapis.  
> 6. Na glavnom izborniku odaberite mogućnost **Project Service** > **Ploča s rasporedom**. Postoji nekoliko različitih načina da biste ručno zakazali zahtjev za rezervaciju. Odaberite metodu koja radi za vas.
  
## <a name="find-available-resources"></a>Traženje dostupnih resursa

1.  Na popisu **Rezervacija zahtjeva** desnom tipkom miša kliknite nezakazanu rezervaciju i odaberite nešto od sljedećeg:  
  
- Odaberite **Pronađi dostupnost – trenutačni resursi** da biste pronašli dostupan resurs na popisu resursa na ploči s rasporedom.  
- Odaberite **Pronađi dostupnost – Svi resursi** da biste pronašli dostupan resurs među resursima u sustavu.  
   > [!NOTE]
   >  Kada to učinite, filtri će prikazati mogućnosti odabranog zahtjeva rezervacije.  
  
2. Kada se pojavi dostupan termin, desnom tipkom miša kliknite vremensko razdoblje na ploči s rasporedom, a zatim odaberite mogućnost **Rezerviraj ovdje**. Možete i povući i ispustiti rezervaciju u dostupan termin.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervirajte resurs pomoću dnevnog prikaza i saznajte tko je nedovoljno rezerviran
  
1.  Na ploči rasporeda odaberite mogućnost **Način prikaza** i odaberite stavku **Dani**.  
  
    Prikazuje prikaz rešetke s brojem radnih sati koliko je resurs rezerviran po danu i koji dani su slobodni.  
  
2.  Kliknite naziv resursa koji želite rezervirati, a zatim odaberite mogućnost **Rezerviraj**.  
  
3.  Na dijaloškom okviru **Rezervacija resursa (stvori)** odaberite projekt za koji želite rezervirati resurs i način rezervacije i termine početka i kraja.  
  
4.  Kada završite, odaberite **Rezerviraj**.  
  
## <a name="view-to-the-schedule-board"></a>Pogled na ploču s rasporedom
  
1.  Odaberite nezakazani zahtjev za rezervaciju s popisa na dnu.  
  
2.  Povucite preduvjet za rezervaciju na dostupni resurs/termin za raspored na ploču s rasporedom.  
  
3.  Kada završite, odaberite mogućnost **Rezerviraj**.  
  
### <a name="additional-resources"></a>Dodatni resursi  
 [Vodič za upravitelje resursa](../psa/resource-manager-guide.md)
