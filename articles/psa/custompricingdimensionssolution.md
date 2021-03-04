---
title: Stvaranje prilagođenih rješenja za dimenzije određivanja cijena
description: U ovoj se temi objašnjava način stvaranja prilagođenog rješenja tijekom stvaranja dimenzija za prilagođeno određivanje cijena.
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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144629"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Stvaranje prilagođenih rješenja za dimenzije određivanja cijena

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Sve promjene dimenzija za određivanje prilagođenih cijena tebale bi biti u zasebnom rješenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu. Nakon što izvršite sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.

1. Odaberite **Postavke** > **Rješenja**, a zatim odaberite **Novo**. 
2. Rješenju dodijelite naziv **\<your organization name> dimenzije za određivanje cijena**, unesite preostale potrebne podatke, a zatim odaberite **Spremi**.

> ![Izrada prilagođenog rješenja za dimenzije određivanja cijena](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
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
- Unos vremena 

> ![Dodaj postojeće entitete u rješenje dimenzija određivanja cijena](media/Existing-entities-to-PD-solution.png)

> ![Odaberi komponente rješenja](media/Dimension-Components.png)

> [!NOTE]
> Obavezno uključite sve obrasce i prikaze za svaki odabrani entitet.

4. Kada se od vas zatraži da uključite sve ovisne entitete za odabrane entitete, odaberite **Ne**.

> ![Ne, ne želim dodati sve povezane komponente.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]