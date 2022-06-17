---
title: Stvaranje rješenja za prilagođene veličine za određivanje cijena
description: U ovom se članku nalaze informacije o stvaranju rješenja za prilagođene dimenzije određivanja cijena.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cd7fedaa7bece16e99131bcc0faff3ce547580e8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915129"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Stvaranje rješenja za prilagođene veličine za određivanje cijena

 _**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_ 

>[!IMPORTANT]
>Sve promjene dimenzija za određivanje prilagođenih cijena tebale bi biti u zasebnom rješenju. Ova značajna najbolja praksa omogućuje fleksibilnost za ažuriranje ili uklanjanje promjena po potrebi, pomaže u ponovnoj uporabi vašeg rada i olakšava prijenos tih promjena na drugu instancu. Nakon što napravite potrebne promjene, izvezite ovo rješenje kao **Upravljano** rješenje i zatim ga uvezite u druge instance radi ponovne uporabe.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Stvaranje rješenja za prilagođene veličine za određivanje cijena

1.  Odaberite **Postavke** > **Rješenja**, a zatim odaberite **Novo**.
2.  Imenujte rješenje, *\<your organization name\> veličine za određivanje cijene*.
3. Unesite preostale potrebne informacije, a zatim odaberite **Spremi**.

  ![Stvaranje rješenja za prilagođene veličine za određivanje cijena.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
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
   - **Vremenski unos**
 
   ![Dodavanje postojećih entiteta s rješenjem prilagođene veličine za određivanje cijene.](./media/Existing-entities-to-PD-solution.png)
 
 4. Pregledajte komponente koje se dodaju i konačni popis sredstava entiteta za svaki entitet. 

   >[!NOTE]
   > Uključite sve obrasce i prikaze za svaki odabrani entitet.

  ![Dodani entiteti.](./media/solution-component-selection.png)


5.  Kada se od vas zatraži da uključite bilo koji ovisni entitet za odabrane entitete, odaberite **Nemoj uključivati potrebne komponente.**

    ![Uključivanje ovisnih entiteta.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]