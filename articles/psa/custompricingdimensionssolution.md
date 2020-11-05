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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073397"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Stvaranje prilagođenih rješenja za dimenzije određivanja cijena

> [!IMPORTANT]
> Sve promjene dimenzija za određivanje prilagođenih cijena tebale bi biti u zasebnom rješenju. Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu. Nakon što izvršite sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.

1. Odaberite **Postavke** > **Rješenja** , a zatim odaberite **Novo**. 
2. Rješenju dodijelite naziv **\<your organization name> dimenzije za određivanje cijena** , unesite preostale potrebne podatke, a zatim odaberite **Spremi**.

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


