---
title: Izradi prilagođena polja i entitete
description: U ovoj se temi pojašnjava način izrade skupova mogućnosti i entiteta u vlastitom rješenju na platformi Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073457"
---
# <a name="create-custom-fields-and-entities"></a>Izradi prilagođena polja i entitete 

Izvršite sljedeće korake u bilo kojem trenutku kada želite izraditi prilagođeni skup mogućnosti ili entitet na platformi Power Apps.  
Postupci u ovoj temi trebaju se izvršiti s pomoću web-sučelja sustava Project Service Automation (PSA).

> [!IMPORTANT]
> Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu. Nakon što ste izvršili sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena

Dimenzija određivanja cijena može biti skup mogućnosti ili entitet. Oboje se moraju izraditi u vašem rješenju za određivanje cijena. Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.

### <a name="entity-based-dimensions"></a>Dimenzije koje se temelje na entitetu

1. U PSA-u kliknite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti**.
3. Kliknite **Novo** da biste izradili novi entitet pod nazivom **Standardni naslov**. Unesite preostale potrebne informacije, a zatim kliknite **Spremi**.

> ![Definicija entiteta Standardni naslov](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimenzije koje se temelje na skupu mogućnosti 
Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti. Koristite **Mjesto rada resursa** da biste pratili cijenu rada **Od kuće** i rada **Na radnom mjestu** i koristite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Prekovremeno** da biste primijenili maržu kada se dovrši rad.


1. U PSA-u kliknite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite  **Skupovi mogućnosti**. 
3. Kliknite **Novo** da biste izradili novi skup mogućnosti, unesite preostale potrebne informacije, a zatim kliknite **Spremi.**

> ![Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Lokacija rada resursa ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Radno vrijeme resursa ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Izradi podatake za dimenzije koje se temeljene na entitetu

Podatke za dimenzije koje se temeljene na entitetu možete izraditi ručno ili s pomoću Microsoft Excel poziva za uvoz ili servisiranje. Koristite korake u ovom postupku za izradu dvaju standardnih naslova, **Inženjer sustava** i **Viši inženjer sustava** iz dimenzije koja se temelji na entitetu, **Standardni naslov**. Ako su podaci koje želite izraditi mali, kao u sljedećem primjeru, možete koristiti standardni obrazac.

1. U sustavu PSA, Kliknite **Napredno pretraživanje**. Odaberite entitet **Standardni naslov** i zatim kliknite **Rezultati** . Prikazat će se svi redovi u entitetu **Standardni naslov**.
2. Kliknite **Novo**. U polje **Naziv** unesite "Inženjer sustava", a zatim kliknite **Spremi**.
3. Zatvorite obrazac. 
4. Ponovite korake 1 - 3 za izradu drugog standardnog naslova za "Viši inženjer sustava".

> ![Ogledni podaci za entitet Standardni naslov ](media/ST-data.png)

