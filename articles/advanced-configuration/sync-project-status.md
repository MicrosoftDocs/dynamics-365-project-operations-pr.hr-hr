---
title: Sinkronizacija stanja projekta radi sprječavanja ulaska u zatvorene projekte
description: U ovom se članku objašnjava kako sinkronizirati stanje projekta da biste spriječili ulazak u odnosu na neaktivne ili zatvorene projekte.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinkronizacija stanja projekta radi sprječavanja ulaska u zatvorene projekte

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

## <a name="scenario"></a>Scenarij

Contoso uživo s Microsoftom Dynamics 365 Project Operations za scenarije resursa/nenaseljenih resursa. Kao dio uobičajenih poslovnih aktivnosti, projekti se mogu dovršiti ili staviti na čekanje. Projekt možete inaktivirati kako biste osigurali da se ne generiraju troškovi ili fakture.

## <a name="solution"></a>Rješenje

### <a name="prerequisites"></a>Preduvjeti

-   Microsoft Dynamics 365 Financije 10.0.29 ili novije moraju biti instalirane.
-   Karta dvostrukog pisanja 1.0.0.3 za projekte V2 (msdyn\_ projekti) moraju biti instalirana ili ručno konfigurirana kako je opisano u nastavku.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Stvaranje ažurirane verzije karte dvostrukog pisanja Projekati integracije projektnih operacija V2

Da biste ažurirali kartu dvostrukog pisanja projekata projektnih operacija V2:

1. Otvorite **radni prostor za upravljanje** podacima i odaberite **Dvostruko pisanje**.
2. Odaberite pločicu **s dvostrukim pisanjem**.
3. Iz stupca karta T **tablice pronađite i odaberite** Project V2 (msdyn **projekti),\_ a zatim odaberite** Zaustavi.
4. Odaberite naziv karte da biste otvorili kartu, a zatim odaberite **[Ništa]**.
5. U dijaloškom okviru Odabir stupca odaberite **stanje\[ projekta kodiranja \]** stanja stanja, a zatim odaberite U redu. Da biste suzili popis, možete upisati **stanje** u vrijednost filtra.
6.  Odaberite **Dodaj ili uredi pretvorbu** u stupcu **vrste** karte da biste uredili pretvorbu.
7.  U odjeljku **Vrsta** pretvorbe odaberite **ValueMap**.
8.  Odaberite **Dodaj mapiranje** vrijednosti, a zatim dodajte sljedeće **tipke** i **vrijednosti**:

   Tipka       | Vrijednost 
   ----------|-------
   InProcesi | 0     
   Dovršeno | 1     

![Snimka zaslona s prikazom preslikavanja dvostrukog pisanja](media/projectstage-dw-mapping.png)

9. Odaberite **Spremi**.
10. Na vrhu stranice > projekata **s dvostrukim pisanjem V2 (msdyn_projects)** odaberite **Spremi kao**.
11. U odjeljku **Dodavanje tablice** **u polje Publisher** odaberite **ZADANI izdavač CDS-a**.
12. **Postavite polje Verzija** na 1.0.0.3.
13. **Upišite Opis**, a zatim odaberite **Spremi**.
14. Na vrhu **stranice Dual-write > Projects V2 (msdyn_projects)** odaberite **Pokreni** da biste pokrenuli kartu, a zatim sekirajte **Da** ako se od vas zatraži potvrda prije pokretanja. 

### <a name="close-a-newly-completed-project"></a>Zatvaranje novodovršenog projekta

Dynamics 365 Finance koristi **polje faze** projekta za razlikovanje projekata **koji su u tijeku** ili **dovršeni**. **Dovršeni** projekti ne mogu snositi troškove ili se fakturirati kupcima.

1. Otvorite projekt da biste ga deaktivirali.
2. Na vrpci odaberite **Deaktiviraj**.

> [!NOTE]
> Možete deaktivirati ili zatvoriti projekt jer će se oboje ponašati isto u kontekstu financija.

3. U odjeljku Financije otvorite **stranicu popisa** Svi projekti.
4. Potvrdite da se deaktivirani projekt ne pojavljuje na popisu.
5. U filtru dijaprojekcija **projekata** iznad popisa promijenite vrijednost iz **Aktivno** u **Sve**.
6. Sada ćete vidjeti deaktivirani projekt.

Ako pokušate zabilježiti vrijeme ili trošak u odnosu na ovaj projekt u financijama, ne biste trebali vidjeti projekt za odabir. Ako ručno unesete broj projekta na trošak, prikazat će se poruka poput "Završena faza projekta ne dopušta snimanje u projektu". Fakturiranje i druge funkcije naplate trebale bi biti onemogućene jer će biti u kontekstu zatvorenog projekta.

