---
title: Procjene projekata i integracija stvarnih podataka
description: U ovom se članku nalaze informacije o integraciji dvostrukog pisanja operacija projekta za procjene i stvarne vrijednosti projekata.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029071"
---
# <a name="project-estimates-and-actuals-integration"></a>Procjene projekata i integracija stvarnih podataka

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovom se članku nalaze informacije o integraciji dvostrukog pisanja operacija projekta za procjene i stvarne vrijednosti projekata.

## <a name="project-estimates"></a>Procjene projekta

Procjene rada, troškova i materijala projekta stvaraju se i održavaju i sinkroniziraju s financijskim i operativnim aplikacijama u Microsoft Dataverse računovodstvene svrhe. Operacije stvaranja, ažuriranja i brisanja nisu podržane putem aplikacija za financije i operacije.

Stvaranje procjena zahtijeva valjanu računovodstvenu konfiguraciju za projekt. Projekti koji su povezani s redcima ugovora moraju imati valjani profil troškova i prihoda projekta definiran u pravilima profila za trošak i prihod projekta. Dodatne informacija potražite u članku [Konfiguriranje računovodstva za naplative projekte](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Procjene rada

Procjenu rada stvara voditelj projekta ili voditelj resursa koji projektnom zadatku također dodjeljuje generički ili imenovani resurs. Zapisi o dodjeli resursa mogu se pregledati na kartici **Dodjele resursa** na stranici **Pojedinosti projekta** platforme Dataverse. Zapisi o dodjeli resursa u Dataverse kreiranju zapisa predviđanja sata u aplikacijama za financije i operacije pomoću **entiteta integracije operacija projekta za procjene sata (msdyn\_ resourceassignments)**.

   ![Integracija procjena rada.](./Media/DW4LaborEstimates.png)

Dvostruko upisivanje sinkronizira zapise o dodjeli resursa s pripremnom tablicom (**ProjCDSEstimateHoursImport**), a zatim upotrebljava poslovnu logiku za stvaranje i ažuriranje zapisa o predviđanju sati rada (**ProjForecastEmpl**).

Računovođa projekta pregledava zapise o satu predviđanja stvorene u aplikacijama za financije i operacije odlaskom na **projekte upravljanja i računovodstva** > **Svih projekata** > **·** > **predviđanja sata plana**.

## <a name="expense-estimates"></a>Procjena troška

Procjene troškova stvara voditelj projekta na kartici **Procjene troškova** stranice **Pojedinosti projekta** na platformi Dataverse. Zapisi o procjeni troškova pohranjuju se u entitetu **Redak procjene** na platformi Dataverse. Ti zapisi procjene imaju klasu transakcija, **trošak** i sinkroniziraju se sa zapisima predviđanja troškova u aplikacijama za financije i operacije pomoću **entiteta integracije operacija projekta za procjene troškova (msdyn\_ procjene)**.

   ![Integracija procjena troška.](./Media/DW4ExpenseEstimates.png)

Dvostruko upisivanje sinkronizira zapise o procjeni troška s pripremnom tablicom (**ProjCDSEstimateExpenseImport**), a zatim upotrebljava poslovnu logiku za stvaranje i ažuriranje zapisa o predviđanju troška (**ProjForecastCost**). Redci procjene odvojeno pohranjuju zapise o procjeni prodaje od zapisa o procjeni troškova. Poslovna logika u aplikacijama za financije i operacije popunjava jedan zapis predviđanja troškova pomoću tog detalja u tablici postavljanja.

Računovođa projekta može pregledati zapise predviđanja troškova u aplikacijama za financije i operacije tako da ode na **Projektiranje i računovodstvo** > **Svi projekti** > **planiraju** > **predviđanja troškova**.

## <a name="material-estimates"></a>Procijene materijala

Procjene materijala stvara voditelj projekta na kartici **Procjene materijala** stranice **Pojedinosti projekta** na platformi Dataverse. Zapisi o procjeni materijala pohranjuju se u entitetu **Redak procjene** na platformi Dataverse. Ti zapisi procjene imaju klasu transakcija, **Materijal** i sinkroniziraju se sa zapisima predviđanja artikla u aplikacijama za financije i operacije pomoću **tablice Integracija projekta za procjene materijala (msdyn\_ procjene)**.

   ![Integracija procjena materijala.](./Media/DW4MaterialEstimates.png)

Dvostruko upisivanje sinkronizira zapise o procjeni materijala s pripremnom tablicom **ProjForecastSalesImpor**, a zatim upotrebljava poslovnu logiku za stvaranje i ažuriranje zapisa o predviđanju stavke (**ForecastSales**). Redci procjene odvojeno pohranjuju zapise o procjeni prodaje od zapisa o procjeni troškova. Poslovna logika u aplikacijama za financije i operacije popunjava jedan zapis predviđanja stavke pomoću tog detalja u pripremnoj tablici.

Računovođa projekta može pregledati zapise predviđanja artikla u aplikacijama za financije i operacije tako da ode na **upravljanje projektima i računovodstvo** > **Svih projekata** > **·** > **Planiraju predviđanja artikla**.

## <a name="project-actuals"></a>Stvarni podaci o projektu

Stvarni podaci o projektu stvaraju se na platformi Dataverse na temelju radnog vremena, troškova, materijala i aktivnosti naplate. Svi operativni atributi ovih transakcija, uključujući količinu, cijenu koštanja, prodajnu cijenu i projekt, obuhvaćeni su u tom entitetu platforme Dataverse. Dodatne informacije potražite u odjeljku [Stvarni podaci](../actuals/actuals-overview.md). Stvarni zapisi sinkroniziraju se s financijskim i operativnim aplikacijama pomoću tablice s dva zapisa mapa **Project Operations integracije stvar (msdyn\_ actuals)** za računovodstvo na kraju proizvodnog lanca.

   ![Integracija stvarnih podataka.](./Media/DW4Actuals.png)

Karta tablice **Stvarni podaci integracije aplikacije Project Operations** sinkronizira sve zapise iz entiteta **Stvarni podaci** na platformi Dataverse s atributom **Preskoči sinkronizaciju (samo za internu uporabu)** postavljenim na **Netočno**. Ova se vrijednost atributa automatski postavlja na platformi Dataverse kada se stvori zapis. Sljedeći su primjeri gdje je ovaj atribut postavljen na **Točno**:

  - Stvarni podaci o trošku projekta za transakcije među poduzećima unutar tvrtke. Dodatne informacije potražite u članku [Stvaranje transakcija među poduzećima unutar tvrtke](../project-accounting/create-intercompany-transactions.md). Ti se zapisi preskaču jer sustav ponovno stvara stvarni trošak projekta u aplikacijama za financije i operacije prilikom knjiženja međukompanijske fakture dobavljača.
  - Negativni nenaplaćeni zapisi o prodaji stvoreni kada se potvrdi predračun. Ti se zapisi preskaču jer podstanar projekta u aplikacijama za financije i operacije ne poništava neplaćeni zapis prodaje prilikom fakturiranja, već mijenja status u potpuno fakturirano.

Karta tablice s dvostrukim zapisom sinkronizira zapise sa stvarnim podacima s pripremnom tablicom **ProjCDSActualsImport**. Ti se zapisi obrađuju povremenim postupkom **Uvoz iz pripremne tablice** pri stvaranju redaka dnevnika integracije aplikacije Project Operations i redaka prijedloga fakture za projekt. Dodatne informacije potražite u članku [Dnevnik integracije u aplikaciji Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse također dohvaća veze između stvarnih projektnih transakcija u entitetu **Veza transakcije**. Dodatne informacije potražite u članku [Povezivanje stvarnih podataka s izvornim zapisima](../actuals/linkingactuals.md). Veze između stvarnih transakcija sinkroniziraju se i s aplikacijama za financije i operacije pomoću karte tablice s dvostrukim pisanjem, **entiteta Integracija za Odnosi projektnih transakcija (spajanja transakcija msdyn\_)**. Te zapise upotrebljava povremeni postupak **Uvoz iz pripremne tablice** pri stvaranju redaka dnevnika integracije aplikacije Project Operations i redaka prijedloga fakture za projekt.

Knjiženje dnevnika integracije aplikacije Project Operations i prijedloga fakture za projekt pokreće ažuriranje u odgovarajućim zapisima pripremne tablice, **ProjCDSActualsImport**. Sustav dohvaća i bilježi sljedeće računovodstvene atribute za stvarne transakcije:

- Iznos računovodstvene valute
- Tečaj
- Broj vaučera
- Iznos poreza na promet

Karta tablice **Stvarni podaci o integraciji aplikacije Project Operations** ažurira odgovarajuće zapise stvarnih podataka na platformi Dataverse s tim podacima.
