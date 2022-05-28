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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7a15c5fc45ada4394dcb8e3dc2b477cb2a0bb8c6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592269"
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
