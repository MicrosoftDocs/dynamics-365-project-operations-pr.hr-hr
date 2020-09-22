---
title: Izradi prilagođena polja i entitete
description: U ovoj se temi pojašnjava način izrade skupova mogućnosti i entiteta u vlastitom rješenju na platformi Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750190"
---
# <a name="create-custom-fields-and-entities"></a>Izradi prilagođena polja i entitete 

Izvršite sljedeće korake u bilo kojem trenutku kada želite izraditi prilagođeni skup mogućnosti ili entitet na platformi Power Apps.  
Postupci u ovoj temi trebaju se izvršiti s pomoću web-sučelja sustava Project Service Automation (PSA).

> [!IMPORTANT]
> Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu. Nakon što ste izvršili sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Izradi prilagođeno rješenje za dimenzije određivanja cijena
1. U sustavu PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite **Novo** da biste izradili novo rješenje. 
2. Rješenju dodijelite naziv **\<, naziv tvrtke ili ustanove >dimenzije određivanja cijena**, unesite preostale potrebne informacije, a zatim kliknite **Spremi**.

> ![Izrada prilagođenog rješenja za dimenzije određivanja cijena](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena

Dimenzija određivanja cijena može biti skup mogućnosti ili entitet. Oboje se moraju izraditi u vašem rješenju za određivanje cijena. Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.

### <a name="entity-based-dimensions"></a>Dimenzije koje se temelje na entitetu

1. U PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite dvaput **\<naziv organizacije> dimenzije određivanja cijena**.
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti**.
3. Kliknite **Novo** da biste izradili novi entitet pod nazivom **Standardni naslov**. Unesite preostale potrebne informacije, a zatim kliknite **Spremi**.

> ![Definicija entiteta Standardni naslov](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimenzije koje se temelje na skupu mogućnosti 
Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti. Koristite **Mjesto rada resursa** da biste pratili cijenu rada **Od kuće** i rada **Na radnom mjestu** i koristite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Prekovremeno** da biste primijenili maržu kada se dovrši rad.


1. U sustavu PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite dvaput  **\<naziv organizacije> dimenzije određivanja cijena**. 
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

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodaj sve potrebne entiteta sustava PSA i srodne komponente u rješenje dimenzije određivanja cijena
Morat ćete dodati sljedeće entitete programa Project Service u svoje rješenje za određivanje cijena. Koristite ove korake u tom postupku da biste izvršili neke važne promjene sheme u rješenju određivanja cijena da bi entiteti prepoznali nove dimenzije određivanja cijena.

1. U PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite dvaput **\<naziv organizacije> dimenzije određivanja cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.
3. U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:

- Stvarna vrijednost
- Resurs koji se može rezervirati
- Redak procjene
- Pojedinost retka fakture
- Redak u dnevniku
- Pojedinost retka ugovora projekta
- Član projektnog tima
- Pojedinost retka ponude
- Provizija cijene uloge
- Cijena uloge 
- Unos vremena 

> ![Dodaj postojeće entitete u rješenje dimenzija određivanja cijena](media/Existing-entities-to-PD-solution.png)

> ![Odaberi komponente rješenja](media/Dimension-Components.png)

> [!NOTE]
> Obavezno uključite sve obrasce i prikaze za svaki odabrani entitet.

4. Kada se od vas zatraži da uključite ovisne entitete za odabrane entitete, kliknite **Ne**.

> ![Ne, ne želim dodati sve povezane komponente.](media/Do-not-include-required.png)


