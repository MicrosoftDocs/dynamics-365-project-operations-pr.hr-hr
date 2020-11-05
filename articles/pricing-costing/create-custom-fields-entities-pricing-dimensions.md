---
title: Stvaranje prilagođenih polja i entitete kao cjenovnih veličina
description: U ovoj se temi nalaze informacije o načinu stvaranja prilagođenih skupova mogućnosti ili entiteta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073426"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Stvaranje prilagođenih polja i entitete kao cjenovnih veličina

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Dovršite sljedeće korake u bilo kojem trenutku kada želite stvoriti prilagođeni skup mogućnosti ili entitet.

> [!IMPORTANT]
> Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu. Nakon što ste izvršili sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Izradi prilagođeno rješenje za dimenzije određivanja cijena
1. Idite na **Postavke** > **Rješenja** , a zatim odaberite **Novo** kako biste stvorili novo rješenje. 
2. Rješenju dodijelite naziv **\<your organization name> dimenzije za određivanje cijena** , unesite preostale potrebne podatke, a zatim odaberite **Spremi**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena

Dimenzija određivanja cijena može biti skup mogućnosti ili entitet. Oboje se moraju izraditi u vašem rješenju za određivanje cijena. Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.

### <a name="entity-based-dimensions"></a>Dimenzije koje se temelje na entitetu

1. Idite na **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti**.
3. Odaberite **Novo** kako biste stvorili novi entitet pod nazivom **Standardni naslov**. 
4. Unesite preostale potrebne informacije, a zatim odaberite **Spremi**.


### <a name="option-set-based-dimensions"></a>Dimenzije koje se temelje na skupu mogućnosti 
Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti. Koristite **Mjesto rada resursa** da biste pratili cijenu rada **Od kuće** i rada **Na radnom mjestu** i koristite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Prekovremeno** da biste primijenili maržu kada se dovrši rad.


1. Idite na **Postavke** > **Rješenja** i dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite  **Skupovi mogućnosti**. 
3. Odaberite **Novo** kako biste stvorili novi skup mogućnosti, unesite preostale potrebne podatke, a zatim odaberite **Spremi**.

## <a name="create-data-for-entity-based-dimensions"></a>Izradi podatake za dimenzije koje se temeljene na entitetu

Podatke za dimenzije koje se temeljene na entitetu možete izraditi ručno ili s pomoću Microsoft Excel poziva za uvoz ili servisiranje. Koristite korake u ovom postupku za izradu dvaju standardnih naslova, **Inženjer sustava** i **Viši inženjer sustava** iz dimenzije koja se temelji na entitetu, **Standardni naslov**. Ako su podaci koje želite izraditi mali, kao u sljedećem primjeru, možete koristiti standardni obrazac.

1. Odaberite **Napredno pretraživanje** , odaberite entitet **Standardni naslov** , a zatim odaberite **Rezultati**. Prikazat će se svi redovi u entitetu **Standardni naslov**.
2. Odaberite **Novo** i upolju **Naziv** unesite „Inženjer sustava”, a zatim odaberite **Spremi**.
3. Zatvori obrazac. 
4. Ponovite korake 1 - 3 za izradu drugog standardnog naslova za "Viši inženjer sustava".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodavanje svih potrebnih entiteta i povezanih komponenti u rješenje dimenzije za određivanje cijena
Morat ćete dodati sljedeće entitete svojem rješenju za određivanje cijena. Koristite ove korake u tom postupku da biste izvršili neke važne promjene sheme u rješenju određivanja cijena da bi entiteti prepoznali nove dimenzije određivanja cijena.

1. Odaberite **Postavke** > **Rješenja** i dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.
3. U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:

  - Stvarna vrijednost
  - Resurs koji se može rezervirati
  - Redak procjene
  - Pojedinost retka fakture
  - Redak u dnevniku
  - Pojedinost retka ugovora projekta
  - Članov projektnog tima
  - Pojedinost retka ponude
  - Provizija cijene uloge
  - Cijena uloge 
  - Vremenski unos 


> [!NOTE]
> Obavezno uključite sve obrasce i prikaze za svaki odabrani entitet.

4. Kada se od vas zatraži da uključite ovisne entitete za odabrane entitete, odaberite **Ne**.

