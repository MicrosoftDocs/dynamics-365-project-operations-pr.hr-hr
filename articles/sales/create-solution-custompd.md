---
title: Stvaranje rješenja za prilagođene veličine za određivanje cijena
description: U ovoj temi nalaze se informacije o načinu stvaranja rješenja prilagođenih veličina za određivanje cijena.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513967"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Stvaranje rješenja za prilagođene veličine za određivanje cijena

 _**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_ 

>[!IMPORTANT]
>Sve promjene dimenzija za određivanje prilagođenih cijena tebale bi biti u zasebnom rješenju. Ova značajna najbolja praksa omogućuje fleksibilnost za ažuriranje ili uklanjanje promjena po potrebi, pomaže u ponovnoj uporabi vašeg rada i olakšava prijenos tih promjena na drugu instancu. Nakon što napravite potrebne promjene, izvezite ovo rješenje kao **Upravljano** rješenje i zatim ga uvezite u druge instance radi ponovne uporabe.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Stvaranje rješenja za prilagođene veličine za određivanje cijena

1.  Odaberite **Postavke** > **Rješenja**, a zatim odaberite **Novo**.
2.  Imenujte rješenje, *<your organization name> veličine za određivanje cijene*.
3. Unesite preostale potrebne informacije, a zatim odaberite **Spremi**.

  ![Stvaranje rješenja za prilagođene veličine za određivanje cijena](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodavanje svih potrebnih entiteta i povezanih komponenti u rješenje dimenzije za određivanje cijena

Dodajte sljedeće entitete aplikacije Project Service u svoje rješenje za određivanje cijene kako biste napravili bitne promjene sheme u rješenju za određivanje cijene. Nakon što dovršite ovaj postupak, entiteti će prepoznati nove veličine za određivanje cijene.

1.  Odaberite **Postavke** > **Rješenja** i zatim dvaput kliknite **<*naziv svoje tvrtke ili ustanove*> veličine za određivanje cijene**.
2.  U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.
3.  U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:
 
   - **Stvarno**
   - **Resurs koji je moguće rezervirati**
   - **Redak procjene**
   - **Projektni zadatak**
   - **Pojedinost retka fakture**
   - **Redak u dnevniku**
   - **Pojedinost retka ugovora projekta**
   - **Član projektnog tima**
   - **Pojedinost retka ponude**
   - **Provizija cijene uloge**
   - **Cijena uloge**
   - **Unos vremena**
 
   ![Dodavanje postojećih entiteta s rješenjem prilagođene veličine za određivanje cijene](./media/Existing-entities-to-PD-solution.png)
 
 4. Pregledajte komponente koje se dodaju i konačni popis sredstava entiteta za svaki entitet. 

   >[!NOTE]
   > Uključite sve obrasce i prikaze za svaki odabrani entitet.

  ![Dodani entiteti](./media/solution-component-selection.png)


5.  Kada se od vas zatraži da uključite bilo koji ovisni entitet za odabrane entitete, odaberite **Nemoj uključivati potrebne komponente.**

    ![Uključivanje ovisnih entiteta](./media/Do-not-include-required.png)