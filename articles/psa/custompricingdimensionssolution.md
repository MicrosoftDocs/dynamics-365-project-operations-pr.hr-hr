---
title: Stvaranje prilagođenih rješenja za dimenzije određivanja cijena
description: U ovoj se temi objašnjava način stvaranja prilagođenog rješenja tijekom stvaranja dimenzija za prilagođeno određivanje cijena.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995257"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Stvaranje prilagođenih rješenja za dimenzije određivanja cijena

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Sve promjene dimenzija za određivanje prilagođenih cijena tebale bi biti u zasebnom rješenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu. Nakon što izvršite sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.

1. Odaberite **Postavke** > **Rješenja**, a zatim odaberite **Novo**. 
2. Rješenju dodijelite naziv **\<your organization name> dimenzije za određivanje cijena**, unesite preostale potrebne podatke, a zatim odaberite **Spremi**.

> ![Izrada prilagođenog rješenja za veličine određivanja cijena.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodavanje svih potrebnih entiteta i povezanih komponenti u rješenje dimenzije za određivanje cijena
Morat ćete dodati sljedeće entitete programa Project Service u svoje rješenje za određivanje cijena. Dovršite ove korake u tom postupku kako biste izvršili neke važne promjene sheme u rješenju određivanja cijena kako bi entiteti prepoznali nove dimenzije određivanja cijena.

1. Odaberite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.
3. U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:

- Stvarno
- Resurs koji je moguće rezervirati
- Redak procjene
- Projektni zadatak
- Pojedinost retka fakture
- Redak u dnevniku
- Pojedinost retka ugovora projekta
- Član projektnog tima
- Pojedinost retka ponude
- Provizija cijene uloge
- Cijena uloge 
- Vremenski unos 

> ![Dodajte postojeće entitete u rješenje veličina za određivanja cijena.](media/Existing-entities-to-PD-solution.png)

> ![Uklanjanje komponenata rješenja u tijeku.](media/Dimension-Components.png)

> [!NOTE]
> Obavezno uključite sve obrasce i prikaze za svaki odabrani entitet.

4. Kada se od vas zatraži da uključite sve ovisne entitete za odabrane entitete, odaberite **Ne**.

> ![Nemojte uključivati sve povezane komponente.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]