---
title: Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations
description: U ovoj temi nalaze se informacije o postavljanju i konfiguraciji karata s dvostrukim pisanjem u aplikaciji Project Operations.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938961"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o integraciji s dvostrukim pisanjem u aplikaciji Project Operations za postavljanje i konfiguriranje entiteta.

## <a name="project-contracts-contract-lines-and-projects"></a>Ugovor o projektu, redci ugovora i projekti

Ugovori o projektima, redci ugovora i projekti stvaraju se na platformi Dataverse i sinkroniziraju s aplikacijama Finance and Operations za dodatno računovodstvo. Zapisi u tim entitetima mogu se stvarati i brisati samo na platformi Dataverse. Međutim, računovodstveni atributi kao što su zadane vrijednosti grupe poreza na promet i financijske veličine mogu se dodati tim evidencijama u aplikacijama Finance and Operations.

  ![Koncepti integracije ugovora o projektu](./media/1ProjectContract.jpg)

Prati se aktivnost prodaje za potencijalne kupce, prilike i ponude na platformi Dataverse, ali se ne sinkronizira s aplikacijama Finance and Operations, jer uz ovu aktivnost nije povezano nizvodno računovodstvo.

Funkcionalnost ugovora o projektu na platformi Dataverse stvara zapis ugovora o projektu u aplikacijama Finance and Operations s pomoću karte tablice **Zaglavlja ugovora o projektu (prodajni nalozi)**. Spremanje ugovora o projektu na platformi Dataverse također počinje stvarati zapis entiteta klijenta ugovora o projektu. Ovaj se zapis sinkronizira s aplikacijama Finance and Operations s pomoću karte tablice **Izvor financiranja projekata (msdyn\_projectcontractssplitbillingrules)**. Ova karta također sinkronizira dodavanja, ažuriranja i brisanja klijenata u ugovoru o projektu. Postocima podijeljene naplate između klijenata ugovora o projektu upravlja se samo na platformi Dataverse, a bez sinkronizacije s aplikacijama Finance and Operations.

Nakon stvaranja ugovora o projektu na platformi Dataverse, računovođa projekta može za taj ugovor o projektu ažurirati računovodstvene atribute u aplikacijama Finance and Operations tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o projektu** > **Postavke** > **Prikaži zadano računovodstvo**. Računovođa može pregledati operativne atribute ugovora o projektu, kao što su traženi datum isporuke i iznos ugovora, tako da odabere ID ugovora o projektu u aplikacijama Finance and Operations, čime otvara povezani zapis ugovora o projektu na platformi Dataverse.

Entitet projekta sinkronizira se s aplikacijama Finance and Operations s pomoću karte tablice **Projekti V2 (msdyn\_projects)**. Računovođa projekta može:

  - Pregledati projekte u aplikacijama Finance and Operations tako da ode na **Upravljanje projektima i računovodstvo** > **Svi projekti**. 
  - Ažurirati računovodstvene atribute za projekt u aplikacijama Finance and Operations tako da ode na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Postavke** > **Prikaži zadano računovodstvo**.  
  - Pregledati operativne atribute projekta, kao što su procijenjeni datumi početka i završetka, tako da odabere ID projekta u aplikacijama Finance and Operations, čime se otvara povezani zapis o projektu na platformi Dataverse.

Projekt je povezan s ugovorom o projektu putem entiteta **Redak ugovora o projektu**.

Redci ugovora o projektu na platformi Dataverse stvaraju pravilo naplate za ugovor o projektu u aplikacijama Finance and Operations s pomoću karte tablice **Redci ugovora o projektu (pojedinosti prodajnog naloga)**. Način naplate definira vrstu pravila naplate za ugovor o projektu u aplikacijama Finance and Operations:

  - Redci ugovora o projektu s načinom naplate vremena i materijala stvaraju pravilo naplate vrste vremena i materijala.
  - Redci ugovora s načinom naplate uz nepromjenjivu cijenu stvaraju pravilo naplate putem kontrolne točke.

Retke ugovora o projektu može pregledati knjigovođa projekta u aplikacijama Finance and Operations tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o projektu** > **Postavke** > **Prikaži zadano računovodstvo** i pregleda pojedinosti na kartici **Redci ugovora**. Računovođa na ovoj kartici također može postaviti zadane financijske veličine za način naplate redaka ugovora s nepromjenjivom cijenom.

## <a name="billing-milestones"></a>Kontrolne točke naplate

Redci ugovora o projektu koji upotrebljavaju način naplate s nepromjenjivom cijenom fakturiraju se putem kontrolnih točaka za naplatu. Kontrolne točke za naplatu sinkroniziraju se s djelomično plaćenim transakcijama projekta u aplikacijama Finance and Operations s pomoću karte tablice **Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integracija kontrolnih točaka naplate](./media/2Milestones.jpg)

Računovođa može pregledati djelomično plaćene transakcije i prilagoditi računovodstvene atribute tim transakcijama tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o projektu** > **Održavanje** > **Transakcije djelomičnog plaćanja** ili **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Održavanje** > **Transakcije djelomičnog plaćanja**.

Kada prvi put stvorite kontrolnu točku za naplatu za određeni redak ugovora o projektu, sustav automatski stvara projekt procjene prihoda s nepromjenjivom cijenom za projekt povezan s ovim retkom ugovora. Projekti procjene prihoda s nepromjenjivom cijenom mogu se pregledati tako da se ode na **Upravljanje projektima i računovodstvo** > **Projekti procjene prihoda s nepromjenjivom cijenom**.

### <a name="project-tasks"></a>Projektni zadaci

Projektni zadaci sinkroniziraju se s aplikacijama Finance and Operations putem karte tablice **Projektni zadaci (msdyn\_projecttasks)** samo za referencu. Operacije stvaranja, ažuriranja i brisanja nisu podržane putem aplikacija Finance and Operations.

  ![Integracija projektnih zadataka](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektni resursi

Entitet **Uloge projektnih resursa** sinkronizira se s aplikacijama Finance and Operations s pomoću karte tablice **Uloge projektnih resursa za sve tvrtke (kategorije koje se mogu rezervirati)** samo za referencu. Budući da uloge resursa na platformi Dataverse nisu specifične za tvrtku, sustav automatski stvara odgovarajuće zapise o ulogama resursa specifične za tvrtku u aplikacijama Finance and Operations i to automatski za sve pravne osobe uključene u raspon integracije s dvostrukim pisanjem.

![Integracija uloga resursa](./media/5Resources.jpg)

Projektni resursi u aplikaciji Project Operations održavaju se na platformi Dataverse i ne sinkroniziraju se s aplikacijama Finance and Operations.

### <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija održavaju se na platformi Dataverse i sinkroniziraju s aplikacijama Finance and Operations s pomoću karte tablice **Kategorije projektnih transakcija (msdyn\_transactioncategories)**. Nakon sinkronizacije zapisa kategorije transakcije, sustav automatski stvara četiri dijeljena zapisa kategorije. Svaki se zapis podudara s vrstom transakcije u aplikacijama Finance and Operations i povezuje ih sa zapisom kategorije transakcije.

![Integracija kategorija transakcije](./media/4TransactionCategories.jpg)

Uporaba kategorija transakcija za procjene i stvarne podatke zahtijeva od knjigovođe projekta ili administratora sustava da stvori odgovarajuće kategorije projekata u svakoj pravnoj osobi. Dodatne informacije potražite u članku [Konfiguracija kategorija projekata](../project-accounting/configure-project-categories.md).
