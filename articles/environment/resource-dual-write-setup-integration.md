---
title: Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations
description: U ovoj temi nalaze se informacije o postavljanju i konfiguraciji karata s dvostrukim pisanjem u aplikaciji Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586887"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o integraciji s dvostrukim pisanjem u aplikaciji Project Operations za postavljanje i konfiguriranje entiteta.

## <a name="project-contracts-contract-lines-and-projects"></a>Ugovor o projektu, redci ugovora i projekti

Ugovori o projektu, reci ugovora i projekti kreiraju se u Dataverse aplikacijama Financije i operacije i sinkroniziraju ih s njima radi dodatnog računovodstva. Zapisi u tim entitetima mogu se stvarati i brisati samo na platformi Dataverse. Međutim, računovodstveni atributi kao što su neispunjavanja obveza porezne grupe za promet i financijske dimenzije mogu se dodati tim zapisima u aplikacijama Financije i operacije.

  ![Koncepti integracije ugovora o projektu.](./media/1ProjectContract.jpg)

Potencijalni klijenti, prilike i ponude prodajnih aktivnosti prate se i Dataverse ne sinkroniziraju se s aplikacijama Financije i operacije jer s tom aktivnošću nije povezano daljnje računovodstvo.

Funkcija ugovora o projektu u programu Dataverse kreira zapis o ugovoru o projektu u aplikacijama Financije i operacije pomoću **karte tablice Zaglavlja ugovora o projektu (prodaje).** Spremanje ugovora o projektu na platformi Dataverse također počinje stvarati zapis entiteta klijenta ugovora o projektu. Taj se zapis sinkronizira s aplikacijama za financije i operacije pomoću **karte tablice Izvor financiranja projekta (msdyn\_ projectcontractssplitbillingrules).** Ova karta također sinkronizira dodavanja, ažuriranja i brisanja klijenata u ugovoru o projektu. Podijeljeni postoci naplate između korisnika ugovora o projektu ovladavaju se samo u Dataverse aplikacijama Financije i operacije i ne sinkroniziraju se s njima.

Nakon kreiranja ugovora o projektu u Dataverse programu, računovođa projekta može ažurirati računovodstvene atribute za ovaj ugovor o projektu u aplikacijama Financije i operacije tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o** > **projektu Postavljanje** > **prikaži zadano računovodstvo**. Računovođa može pregledati atribute ugovora o operativnom projektu, kao što su zatraženi datum isporuke i iznos ugovora odabirom ID-a ugovora o projektu u aplikacijama Financije i operacije koja otvara povezani zapis ugovora o projektu u Dataverse sustavu.

Projektni entitet sinkronizira se s aplikacijama Za financije i operacije pomoću **karte tablice Projekti V2 (msdyn\_ projekti).** Računovođa projekta može:

  - Pregledajte projekte u aplikacijama za financije i operacije odlaskom na **Upravljanje projektima i računovodstvo** > **Svi projekti**. 
  - Ažurirajte računovodstvene atribute za projekt u aplikacijama Financije i Operacije tako da **otvorite Upravljanje projektima i računovodstvo** > **Svi projekti** > **Postavljeni Prikaži zadano** > **računovodstvo**.  
  - Pregledajte atribute operativnog projekta, kao što su procijenjeni datumi početka i završetka, odabirom ID-a projekta u aplikacijama Financije i operacije koji otvara povezani zapis projekta u Dataverse sustavu.

Projekt je povezan s ugovorom o projektu putem entiteta **Redak ugovora o projektu**.

Reci ugovora o projektu u programu Dataverse kreira pravilo naplate ugovora o projektu u aplikacijama Financije i operacije pomoću **karte tablice Reci ugovora o projektu (salesorderdetails**). Način naplate definira vrstu pravila naplate ugovora o projektu u aplikacijama Financije i operacije:

  - Redci ugovora o projektu s načinom naplate vremena i materijala stvaraju pravilo naplate vrste vremena i materijala.
  - Redci ugovora s načinom naplate uz nepromjenjivu cijenu stvaraju pravilo naplate putem kontrolne točke.

Retke ugovora o projektu računovođa projekta može pregledati u aplikacijama Financije i operacije tako da odete na **Ugovor o upravljanju projektima i računovodstvu** > **Ugovori o** > **projektu Postavite** > **Prikaži zadano računovodstvo** i pregledate detalje na **kartici Reci** ugovora. Računovođa također može postaviti zadane financijske dimenzije za retke ugovora o načinu naplate fiksne cijene na ovoj kartici.

## <a name="billing-milestones"></a>Kontrolne točke naplate

Redci ugovora o projektu koji upotrebljavaju način naplate s nepromjenjivom cijenom fakturiraju se putem kontrolnih točaka za naplatu. Ključne etape za naplatu sinkroniziraju se s projiciranjem transakcija na računu u aplikacijama za financije i operacije pomoću **karte tablice između ključnih etapa retka ugovora o integraciji projekata (msdyn\_ contractlinescheduleofvalues).**

  ![Integracija kontrolnih točaka naplate.](./media/2Milestones.jpg)

Računovođa može pregledati djelomično plaćene transakcije i prilagoditi računovodstvene atribute tim transakcijama tako da ode na **Upravljanje projektima i računovodstvo** > **Ugovori o projektu** > **Održavanje** > **Transakcije djelomičnog plaćanja** ili **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Održavanje** > **Transakcije djelomičnog plaćanja**.

Kada prvi put stvorite kontrolnu točku za naplatu za određeni redak ugovora o projektu, sustav automatski stvara projekt procjene prihoda s nepromjenjivom cijenom za projekt povezan s ovim retkom ugovora. Projekti procjene prihoda s nepromjenjivom cijenom mogu se pregledati tako da se ode na **Upravljanje projektima i računovodstvo** > **Projekti procjene prihoda s nepromjenjivom cijenom**.

### <a name="project-tasks"></a>Projektni zadaci

Projektni zadaci sinkroniziraju se s aplikacijama Financije i Operacije putem **karte tablice Projektni zadaci (msdyn\_ projecttasks)** samo u referentne svrhe. Stvaranje, ažuriranje i brisanje operacija nije podržano putem aplikacija Za financije i operacije.

  ![Integracija projektnih zadataka.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektni resursi

Entitet **uloga** resursa projekta sinkronizira se s aplikacijama Financije i operacije pomoću **karte resursa projekta za sva poduzeća (kategorije izvora za rezervacije)** samo u referentne svrhe. Budući da uloge resursa u sustavu nisu specifične za tvrtku Dataverse, sustav automatski stvara odgovarajuće zapise uloga resursa specifične za tvrtku u aplikacijama Financije i operacije za sve pravne osobe uključene u opseg integracije s dvostrukim pisanjem.

![Integracija uloga resursa.](./media/5Resources.jpg)

Projektni resursi u projektnim operacijama održavaju se u Dataverse aplikaciji Za financije i operacije i ne sinkroniziraju se s njima.

### <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija održavaju se i Dataverse sinkroniziraju s aplikacijama Financije i operacije pomoću **karte tablice Kategorije transakcija projekta (msdyn\_ kategorije transakcija).** Nakon sinkronizacije zapisa kategorije transakcije, sustav automatski stvara četiri dijeljena zapisa kategorije. Svaki zapis odgovara vrsti transakcije u aplikacijama Financije i operacije i povezuje ih sa zapisom kategorije transakcije.

![Integracija kategorija transakcije.](./media/4TransactionCategories.jpg)

Uporaba kategorija transakcija za procjene i stvarne podatke zahtijeva od knjigovođe projekta ili administratora sustava da stvori odgovarajuće kategorije projekata u svakoj pravnoj osobi. Dodatne informacije potražite u članku [Konfiguracija kategorija projekata](../project-accounting/configure-project-categories.md).
