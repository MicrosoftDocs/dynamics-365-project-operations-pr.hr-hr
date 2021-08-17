---
title: Integracija upravljanja troškovima
description: U ovoj temi nalaze se informacije o integraciji izvješća o trošku u aplikaciji Project Operations s pomoću dvostrukog pisanja.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986572"
---
# <a name="expense-management-integration"></a>Integracija upravljanja troškovima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o integraciji izvješća o trošku u aplikaciji Project Operations [s punom implementacijom troška](../expense/expense-overview.md) s pomoću dvostrukog pisanja.

## <a name="expense-categories"></a>Kategorije troška

U punoj implementaciji troška, kategorije troška stvaraju se i održavaju u aplikacijama Finance and Operations. Kako biste stvorili novu kategoriju troška, poduzmite sljedeće korake:

1. U aplikaciji Microsoft Dataverse stvorite kategoriju **Transakcije**. Integracija dvostrukog pisanja sinkronizirat će ovu kategoriju transakcija s aplikacijama Finance and Operations. Dodatne informacije potražite u člancima [Konfiguriranje kategorija projekata](/dynamics365/project-operations/project-accounting/configure-project-categories) i [Postavljanje aplikacije Project Operations i integracija konfiguracijskih podataka](resource-dual-write-setup-integration.md). Kao rezultat ove integracije, sustav stvara četiri zapisa dijeljene kategorije u aplikacijama Finance and Operations.
2. U aplikaciji Financije, idite na **Upravljanje troškom** > **Postavke** > **Dijeljene kategorije** i odaberite dijeljenu kategoriju transakcijske klase **Trošak**. Parametar **Može se upotrijebiti u troškovima** postavite na **Točno** i definirajte vrstu troška koju ćete upotrijebiti.
3. S pomoću ovog zapisa dijeljene kategorije stvorite novu kategoriju troška tako da odete na **Upravljanje troškovima** > **Postavke** > **Kategorije troška** i odaberete **Nova**. Kada je zapis spremljen, dvostruko pisanje upotrebljava kartu tablice **Entitet izvoza kategorije troška projekta integracije aplikacije Project Operations (msdyn\_expensecategories)** za sinkronizaciju ovog zapisa s platformom Dataverse.

  ![Integracija kategorija troška.](./media/DW6ExpenseCategories.png)

Kategorije troška u aplikacijama Finance and Operations specifične su za tvrtku ili pravnu osobu. To su odvojeni, odgovarajući zapisi specifični za pravne osobe na platformi Dataverse. Kada voditelj projekta procjenjuje troškove, ne može odabrati kategorije troška stvorene za projekt koji je u vlasništvu tvrtke koja je različita od tvrtke koja je vlasnik projekta na kojem radi. 

## <a name="expense-reports"></a>Izvješća o troškovima

Izvješća o troškovima stvaraju se i odobravaju u aplikacijama Finance and Operations. Dodatne informacije potražite u članku [Stvaranje i obrada izvješća o troškovima u aplikaciji Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Nakon što voditelj projekta odobri izvješće o troškovima, ono se knjiži u glavnu knjigu. Redci izvješća o troškovima u aplikaciji Project Operations, koji se odnose na projekt, knjiže se s pomoću posebnih pravila knjiženja:

  - Troškovi povezani s projektom (uključujući bespovratni porez) ne knjiže se odmah na račun troškova projekta u glavnoj knjizi, već se knjiže na račun integracije troškova. Taj se račun konfigurira na kartici **Upravljanje projektima i računovodstvo** > **Postavke** > **Upravljanje projektom i računovodstveni parametri**, **Project Operations u aplikaciji Dynamics 365 Customer Engagement**.
  - Dvostruko pisanje sinkronizira se s platformom Dataverse s pomoću karte tablice **Entitet izvoza troškova projekta integracije aplikacije Project Operations (msdyn\_expenses)**.
  - Sporedne računovodstvene knjige za porez, dobavljača i ostala financijska knjiženja evidentiraju se prema potrebi u vrijeme knjiženja izvješća o troškovima.

  ![Integracija izvješća o troškovima.](./media/DW6ExpenseReports.png)

Kad se zapis upiše u entitet **Trošak** platforme Dataverse, sustav pokreće postupak automatskog odobravanja zapisa. Ako je potrebno, stanje postupka automatskog odobrenja može se pregledati na platformi Dataverse tako da se ode na **Napredne postavke** > **Sustav** > **Poslovi sustava**. Nakon dovršetka postupka odobravanja, stvaraju se zapisi klase transakcija troškova u entitetu **Stvarni podaci**.

Stvarni podaci povezani s troškovima zatim se obrađuju s pomoću karte tablice s dvostrukim pisanjem **Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)**. Dodatne informacije potražite u članku [Procjene i stvarni podaci o projektu](resource-dual-write-estimates-actuals.md).

Povremeni postupak **Uvoz iz pripreme** stvara retke dnevnika koji se odnose na izvješće o troškovima u dnevniku integracije aplikacije Project Operations. Transakcijski je račun zadan za račun integracije troškova. Dnevnik knjiženja integracije briše saldo računa za transakciju troškova i iznos troškova premješta na račun troškova za projekt. Sustav također stvara transakcije sporedne knjige projekta u svrhe nizvodnog fakturiranja i priznavanja prihoda.
