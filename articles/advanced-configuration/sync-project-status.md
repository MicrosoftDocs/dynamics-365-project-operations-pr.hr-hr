---
title: Sinkronizacija statusa projekta radi sprječavanja unosa u zatvorene projekte
description: Ovaj članak objašnjava kako sinkronizirati Status projekta kako biste spriječili unose za neaktivne ili zatvorene projekte.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348099"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinkronizacija statusa projekta radi sprječavanja unosa u zatvorene projekte

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

## <a name="scenario"></a>Scenarij

Contoso aktivira Microsoft Dynamics 365 Project Operations za scenarije temeljene na resursima / bez zaliha. Kao dio uobičajenih poslovnih aktivnosti projekti se mogu dovršiti ili staviti na čekanje. Možete deaktivirati projekt kako biste osigurali da se ne generiraju troškovi ili fakture.

## <a name="solution"></a>Rješenje

### <a name="prerequisites"></a>Preduvjeti

-   Mora biti instalirana platforma Microsoft Dynamics 365 Finance 10.0.29 ili novija.
-   Karta dvostrukog zapisivanja 1.0.0.3 za Projects V2 (msdyn\_projects) mora se instalirati ili ručno konfigurirati kako je opisano u nastavku.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Stvaranje ažurirane verziju karte dvostrukog zapisivanja za integraciju Projects V2 u Project Operations

Za ažuriranja karte dvostrukog zapisivanja Projects V2 u aplikaciji Project Operations:

1. Idite u radni prostor **Upravljanje podacima** i odaberite **Dvostruko pisanje**.
2. Odaberite pločicu **Dvostruko pisanje**.
3. U stupcu T **Stolna karta** pronađite i odaberite **Project V2 (msdyn\_projects)**, a zatim odaberite Zaustavi.
4. Odaberite naziv karte da biste otvorili kartu, a zatim odaberite **[Ništa]**.
5. U dijaloškom okviru Odabir stupca odaberite **statecode \[Status projekta\]**, a zatim odaberite U redu. Možete utipkati **state** u vrijednost filtra da suzite popis.
6.  Odaberite **Dodaj ili uredi transformaciju** u stupcu **vrsta karte** za uređivanje transformacije.
7.  U odjeljku **Vrsta transformacije** odaberite **ValueMap**.
8.  Odaberite **Dodaj mapiranje vrijednosti**, a zatim dodajte sljedeće **Ključeve** i **Vrijednosti**:

   Tipka       | Vrijednost 
   ----------|-------
   InProcess | 0     
   Dovršeno | 1     

![Snimka zaslona koja prikazuje mapiranje dvostrukog pisanja](media/projectstage-dw-mapping.png)

9. Odaberite **Spremi**.
10. S vrha stranice **Dvostruko pisanje > Projects V2 (msdyn_projects)** odaberite **Spremi kao**.
11. Iz odjeljka **Dodaj tablicu** u polju **Izdavač** odaberite **Zadani izdavač CDS-a**.
12. Postavite polje **Verzija** na 1.0.0.3.
13. Utipkajte **Opis**, a zatim odaberite **Spremi**.
14. S vrha stranice **Dvostruko pisanje > Projects V2 (msdyn_projects)** odaberite **Pokreni** za pokretanje karte, a zatim odaberite **Da** ako se zatraži potvrda prije pokretanja. 

### <a name="close-a-newly-completed-project"></a>Zatvaranje tek završenog projekta

Dynamics 365 Finance upotrebljava polje **faza projekta** za razlikovanje projekata koji su **u tijeku** ili **dovršeni**. **Dovršeni** projekti ne mogu stvarati troškove niti se mogu fakturirati kupcima.

1. Otvorite projekt za deaktivaciju.
2. Na vrpci odaberite mogućnost **Deaktivacija**.

> [!NOTE]
> Možete ili deaktivirati ili zatvoriti projekt jer će se obje mogućnosti ponašati isto u kontekstu aplikacije Finance.

3. U aplikaciji Finance otvorite stranicu **Popis svih projekata**.
4. Potvrdite da se deaktivirani projekt ne pojavljuje na popisu.
5. U filtru **prikaz projekata** iznad popisa promijenite vrijednost iz **Aktivni** u **Svi**.
6. Sada ćete vidjeti deaktivirani projekt.

Ako pokušate zabilježiti vrijeme ili troškove za ovaj projekt u aplikaciji Finance, ne biste trebali vidjeti projekt za odabir. Ako ručno unesete broj projekta na trošku, vidjet ćete poruku poput „Faza projekta Dovršeno ne dopušta zapisivanje u projektu”. Fakturiranje i druge funkcije naplate trebale bi biti onemogućene jer će biti u kontekstu zatvorenog projekta.

