---
title: Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations
description: U ovom članku navedene su informacije o postavljanju i konfiguraciji karata s dvostrukim pisanjem u aplikaciji Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029143"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovom članku navedene su informacije o integraciji s dvostrukim pisanjem u aplikaciji Project Operations za postavljanje i konfiguriranje entiteta.

## <a name="project-contracts-contract-lines-and-projects"></a>Ugovor o projektu, redci ugovora i projekti

Ugovori o projektima, redci ugovora i projekti stvaraju se na platformi Dataverse i sinkroniziraju s aplikacijama za financije i operacije radi dodatnog računovodstva. Zapisi u tim entitetima mogu se stvarati i brisati samo na platformi Dataverse. Međutim, računovodstveni atributi kao što su zadane vrijednosti grupe poreza na promet i financijske veličine mogu se dodati tim evidencijama u aplikacijama za financije i operacije.

  ![Koncepti integracije ugovora o projektu.](./media/1ProjectContract.jpg)

Prati se aktivnost prodaje za potencijalne kupce, prilike i ponude na platformi Dataverse, ali se ne sinkronizira s aplikacijama za financije i operacije, jer uz ovu aktivnost nije povezano nizvodno računovodstvo.

Funkcionalnost ugovora o projektu na platformi Dataverse stvara zapis ugovora o projektu u aplikacijama za financije i operacije s pomoću karte tablice **Zaglavlja ugovora o projektu (prodajni nalozi)**. Spremanje ugovora o projektu na platformi Dataverse također počinje stvarati zapis entiteta klijenta ugovora o projektu. Ovaj se zapis sinkronizira s aplikacijama za financije i operacije s pomoću karte tablice **Izvor financiranja projekata (msdyn\_projectcontractssplitbillingrules)**. Ova karta također sinkronizira dodavanja, ažuriranja i brisanja klijenata u ugovoru o projektu. Postocima podijeljene naplate između klijenata ugovora o projektu upravlja se samo na platformi Dataverse, a bez sinkronizacije s aplikacijama za financije i operacije.

Nakon stvaranja ugovora o projektu na platformi Dataverse, računovođa projekta može za taj ugovor o projektu ažurirati računovodstvene atribute u aplikacijama za financije i operacije tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o projektu** > **Postavke** > **Prikaži zadano računovodstvo**. Računovođa može pregledati operativne atribute ugovora o projektu, kao što su traženi datum isporuke i iznos ugovora, tako da odabere ID ugovora o projektu u aplikacijama za financije i računovodstvo, čime otvara povezani zapis ugovora o projektu na platformi Dataverse.

Entitet projekta sinkronizira se s aplikacijama za financije i operacije s pomoću karte tablice **Projekti V2 (msdyn\_projects)**. Računovođa projekta može:

  - Pregledati projekte u aplikacijama za financije i operacije tako da ode na **Upravljanje projektima i računovodstvo** > **Svi projekti**. 
  - Ažurirati računovodstvene atribute za projekt u aplikacijama za financije i operacije tako da ode na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Postavke** > **Prikaži zadano računovodstvo**.  
  - Pregledati operativne atribute projekta, kao što su procijenjeni datumi početka i završetka, tako da odabere ID projekta u aplikacijama za financije i operacije, čime se otvara povezani zapis o projektu na platformi Dataverse.

Projekt je povezan s ugovorom o projektu putem entiteta **Redak ugovora o projektu**.

Redci ugovora o projektu na platformi Dataverse stvaraju pravilo naplate za ugovor o projektu u aplikacijama za financije i operacije s pomoću karte tablice **Redci ugovora o projektu (salesorderdetails)**. Metoda fakturiranja definira vrstu pravila fakturiranja ugovora o projektu u aplikacijama za financije i operacije:

  - Redci ugovora o projektu s načinom naplate vremena i materijala stvaraju pravilo naplate vrste vremena i materijala.
  - Redci ugovora s načinom naplate uz nepromjenjivu cijenu stvaraju pravilo naplate putem kontrolne točke.

Retke ugovora o projektu može pregledati knjigovođa projekta u aplikacijama za financije i operacije tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o projektu** > **Postavke** > **Prikaži zadano računovodstvo** i pregleda pojedinosti na kartici **Redci ugovora**. Računovođa na ovoj kartici također može postaviti zadane financijske veličine za način naplate redaka ugovora s nepromjenjivom cijenom.

## <a name="billing-milestones"></a>Kontrolne točke naplate

Redci ugovora o projektu koji upotrebljavaju način naplate s nepromjenjivom cijenom fakturiraju se putem kontrolnih točaka za naplatu. Kontrolne točke za naplatu sinkroniziraju se s djelomično plaćenim transakcijama projekta u aplikacijama za financije i operacije s pomoću karte tablice **Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integracija kontrolnih točaka naplate.](./media/2Milestones.jpg)

Računovođa može pregledati djelomično plaćene transakcije i prilagoditi računovodstvene atribute tim transakcijama tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o projektu** > **Održavanje** > **Transakcije djelomičnog plaćanja** ili **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Održavanje** > **Transakcije djelomičnog plaćanja**.

Kada prvi put stvorite kontrolnu točku za naplatu za određeni redak ugovora o projektu, sustav automatski stvara projekt procjene prihoda s nepromjenjivom cijenom za projekt povezan s ovim retkom ugovora. Projekti procjene prihoda s nepromjenjivom cijenom mogu se pregledati tako da se ode na **Upravljanje projektima i računovodstvo** > **Projekti procjene prihoda s nepromjenjivom cijenom**.

### <a name="project-tasks"></a>Projektni zadaci

Projektni zadaci sinkroniziraju se s aplikacijama za financije i operacije putem karte tablice **Projektni zadaci (msdyn\_projecttasks)** samo za referencu. Operacije stvaranja, ažuriranja i brisanja nisu podržane putem aplikacija za financije i operacije.

  ![Integracija projektnih zadataka.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektni resursi

Entitet **Uloge projektnih resursa** sinkronizira se s aplikacijama za financije i operacije s pomoću karte tablice **Uloge projektnih resursa za sve tvrtke (bookableresourcecategories)** samo za referencu. Budući da uloge resursa na platformi Dataverse nisu specifične za tvrtku, sustav automatski stvara odgovarajuće zapise o ulogama resursa specifične za tvrtku u aplikacijama za financije i operacije te to automatski za sve pravne osobe uključene u raspon integracije s dvostrukim pisanjem.

![Integracija uloga resursa.](./media/5Resources.jpg)

Projektni resursi u aplikaciji Project Operations održavaju se na platformi Dataverse i ne sinkroniziraju se s aplikacijama za financije i operacije.

### <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija održavaju se na platformi Dataverse i sinkroniziraju s aplikacijama za financije i operacije s pomoću karte tablice **Kategorije projektnih transakcija (msdyn\_transactioncategories)**. Nakon sinkronizacije zapisa kategorije transakcije, sustav automatski stvara četiri dijeljena zapisa kategorije. Svaki se zapis podudara s vrstom transakcije u aplikacijama za financije i operacije te ih povezuje sa zapisom kategorije transakcije.

![Integracija kategorija transakcije.](./media/4TransactionCategories.jpg)

Uporaba kategorija transakcija za procjene i stvarne podatke zahtijeva od knjigovođe projekta ili administratora sustava da stvori odgovarajuće kategorije projekata u svakoj pravnoj osobi. Dodatne informacije potražite u članku [Konfiguracija kategorija projekata](../project-accounting/configure-project-categories.md).
