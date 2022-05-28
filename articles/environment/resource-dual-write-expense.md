---
title: Integracija upravljanja troškovima
description: U ovoj temi nalaze se informacije o integraciji izvješća o trošku u aplikaciji Project Operations s pomoću dvostrukog pisanja.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b41be519dbfa89668712bc28ccb1888cd08c38a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585783"
---
# <a name="expense-management-integration"></a>Integracija upravljanja troškovima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o integraciji izvješća o trošku u aplikaciji Project Operations [s punom implementacijom troška](../expense/expense-overview.md) s pomoću dvostrukog pisanja.

## <a name="expense-categories"></a>Kategorije troška

U potpunom uvođenju troškova stvaraju se i održavaju kategorije troškova u aplikacijama za financije i operacije. Kako biste stvorili novu kategoriju troška, poduzmite sljedeće korake:

1. U aplikaciji Microsoft Dataverse stvorite kategoriju **Transakcije**. Integracija s dvostrukim pisanjem sinkronizirat će ovu kategoriju transakcije s aplikacijama Financije i operacije. Dodatne informacije potražite u člancima [Konfiguriranje kategorija projekata](/dynamics365/project-operations/project-accounting/configure-project-categories) i [Postavljanje aplikacije Project Operations i integracija konfiguracijskih podataka](resource-dual-write-setup-integration.md). Kao rezultat ove integracije, sustav stvara četiri zajednička zapisa kategorija u aplikacijama Financije i operacije.
2. U aplikaciji Financije, idite na **Upravljanje troškom** > **Postavke** > **Dijeljene kategorije** i odaberite dijeljenu kategoriju transakcijske klase **Trošak**. Parametar **Može se upotrijebiti u troškovima** postavite na **Točno** i definirajte vrstu troška koju ćete upotrijebiti.
3. S pomoću ovog zapisa dijeljene kategorije stvorite novu kategoriju troška tako da odete na **Upravljanje troškovima** > **Postavke** > **Kategorije troška** i odaberete **Nova**. Kada je zapis spremljen, dvostruko pisanje upotrebljava kartu tablice **Entitet izvoza kategorije troška projekta integracije aplikacije Project Operations (msdyn\_expensecategories)** za sinkronizaciju ovog zapisa s platformom Dataverse.

  ![Integracija kategorija troška.](./media/DW6ExpenseCategories.png)

Kategorije troškova u aplikacijama za financije i operacije specifične su za tvrtku ili pravnu osobu. To su odvojeni, odgovarajući zapisi specifični za pravne osobe na platformi Dataverse. Kada voditelj projekta procjenjuje troškove, ne može odabrati kategorije troška stvorene za projekt koji je u vlasništvu tvrtke koja je različita od tvrtke koja je vlasnik projekta na kojem radi. 

## <a name="expense-reports"></a>Izvješća o troškovima

Izvješća o troškovima kreiraju se i odobravaju u aplikacijama za financije i operacije. Dodatne informacije potražite u članku [Stvaranje i obrada izvješća o troškovima u aplikaciji Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Nakon što voditelj projekta odobri izvješće o troškovima, ono se knjiži u glavnu knjigu. Redci izvješća o troškovima u aplikaciji Project Operations, koji se odnose na projekt, knjiže se s pomoću posebnih pravila knjiženja:

  - Troškovi povezani s projektom (uključujući bespovratni porez) ne knjiže se odmah na račun troškova projekta u glavnoj knjizi, već se knjiže na račun integracije troškova. Taj se račun konfigurira na kartici **Upravljanje projektima i računovodstvo** > **Postavke** > **Upravljanje projektom i računovodstveni parametri**, **Project Operations u aplikaciji Dynamics 365 Customer Engagement**.
  - Dvostruko pisanje sinkronizira se s platformom Dataverse s pomoću karte tablice **Entitet izvoza troškova projekta integracije aplikacije Project Operations (msdyn\_expenses)**.
  - Sporedne računovodstvene knjige za porez, dobavljača i ostala financijska knjiženja evidentiraju se prema potrebi u vrijeme knjiženja izvješća o troškovima.

  ![Integracija izvješća o troškovima.](./media/DW6ExpenseReports.png)

Kad se zapis upiše u entitet **Trošak** platforme Dataverse, sustav pokreće postupak automatskog odobravanja zapisa. Ako je potrebno, stanje postupka automatskog odobrenja može se pregledati na platformi Dataverse tako da se ode na **Napredne postavke** > **Sustav** > **Poslovi sustava**. Nakon dovršetka postupka odobravanja, stvaraju se zapisi klase transakcija troškova u entitetu **Stvarni podaci**.

Stvarni podaci povezani s troškovima zatim se obrađuju s pomoću karte tablice s dvostrukim pisanjem **Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)**. Dodatne informacije potražite u članku [Procjene i stvarni podaci o projektu](resource-dual-write-estimates-actuals.md).

Povremeni postupak **Uvoz iz pripreme** stvara retke dnevnika koji se odnose na izvješće o troškovima u dnevniku integracije aplikacije Project Operations. Transakcijski je račun zadan za račun integracije troškova. Dnevnik knjiženja integracije briše saldo računa za transakciju troškova i iznos troškova premješta na račun troškova za projekt. Sustav također stvara transakcije sporedne knjige projekta u svrhe nizvodnog fakturiranja i priznavanja prihoda.
