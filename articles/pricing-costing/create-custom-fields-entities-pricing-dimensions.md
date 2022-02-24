---
title: Stvaranje prilagođenih polja i entitete kao cjenovnih veličina
description: U ovoj se temi nalaze informacije o načinu stvaranja prilagođenih skupova mogućnosti ili entiteta.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642804"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Stvaranje prilagođenih polja i entitete kao cjenovnih veličina

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Poduzmite sljedeće korake kada želite izraditi prilagođeni skup mogućnosti ili entitet koji biste upotrebljavali kao veličinu za određivane cijene. Dodatne informacije potražite u odjeljku [Pregled veličina za određivanje cijene](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju. Ova značajna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi. To će pomoći i pri ponovnoj uporabi vašeg posla i olakšat će prijenos ovih promjena na drugu instancu. Nakon što izvršite sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance za ponovnu uporabu postavki cijena.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena

Dimenzija određivanja cijena može biti skup mogućnosti ili entitet. Oboje se moraju izraditi u vašem rješenju za određivanje cijena. Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.

### <a name="entity-based-dimensions"></a>Dimenzije koje se temelje na entitetu
Kako biste stvorili veličine koje se temelje na entitetu, slijedite ove korake:

1. Idite na **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.
2. U pregledniku rješenja, u lijevom navigacijskom oknu, odaberite mogućnost **Entiteti**.
3. Odaberite **Novo** kako biste stvorili novi entitet pod nazivom **Standardni naslov**. 
4. Unesite preostale potrebne informacije, a zatim odaberite **Spremi**.

> ![Definicija entiteta Standardni naslov](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimenzije koje se temelje na skupu mogućnosti 
Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti. 

- S pomoću stavke **Mjesto rada resursa** pratite cijene rada na mjestu **Početno** i rada **Na lokaciji**. 
- Upotrijebite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Tijekom vremena** kako biste primjenili proviziju kad se posao završi.

Sljedeći grafika daje prikaz veličine **Mjesto rada resursa**. 

> ![Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Lokacija rada resursa](media/Option-set-PD-called-Resource-Work-Location.png)

Sljedeći grafika daje prikaz veličine **Radno vrijeme resursa**. 

> ![Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Radno vrijeme resursa](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Idite na **Postavke** > **Rješenja** i dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U pregledniku rješenja, u lijevom navigacijskom oknu, odaberite stavku **Skupovi mogućnosti**. 
3. Odaberite **Novo** kako biste stvorili novi skup mogućnosti, unesite preostale potrebne podatke, a zatim odaberite **Spremi**.

## <a name="create-data-for-entity-based-dimensions"></a>Izradi podatake za dimenzije koje se temeljene na entitetu

Podatke za dimenzije koje se temeljene na entitetu možete izraditi ručno ili s pomoću Microsoft Excel poziva za uvoz ili servisiranje. Koristite korake u ovom postupku za izradu dvaju standardnih naslova, **Inženjer sustava** i **Viši inženjer sustava** iz dimenzije koja se temelji na entitetu, **Standardni naslov**. Ako su podaci koje želite izraditi mali, kao u sljedećem primjeru, možete koristiti standardni obrazac.

1. Odaberite **Napredno traženje**.
2. Odaberite entitet **Standardni naslov** i zatim **Rezultati** . Prikazat će se svi redci u entitetu **Standardni naslov**.
3. Odaberite **Novo** i upolju **Naziv** unesite „Inženjer sustava”, a zatim odaberite **Spremi**.
4. Zatvorite stranicu. 
5. Ponovite korake 1 - 3 za izradu drugog standardnog naslova za "Viši inženjer sustava".

> ![Uzorak podataka za entitet Standardni naslov](media/ST-data.png)
