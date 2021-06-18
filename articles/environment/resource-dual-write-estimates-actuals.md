---
title: Procjene projekata i integracija stvarnih podataka
description: U ovoj temi nalaze se informacije o integraciji dvostrukog pisanja u aplikaciji Project Operations za procjene i stvarne podatke projekata.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d8aa1541a3560db175acead1d000895312b299db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000022"
---
# <a name="project-estimates-and-actuals-integration"></a>Procjene projekata i integracija stvarnih podataka

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o integraciji dvostrukog pisanja u aplikaciji Project Operations za procjene i stvarne podatke projekata.

## <a name="project-estimates"></a>Procjene projekta

Procjene rada, troška i materijala za projekt stvaraju se i održavaju u sustavu Microsoft Dataverse i sinkroniziraju s aplikacijama Finance and Operations u računovodstvene svrhe. Operacije stvaranja, ažuriranja i brisanja nisu podržane putem aplikacija Finance and Operations.

Stvaranje procjena zahtijeva valjanu računovodstvenu konfiguraciju za projekt. Projekti koji su povezani s redcima ugovora moraju imati valjani profil troškova i prihoda projekta definiran u pravilima profila za trošak i prihod projekta. Dodatne informacija potražite u članku [Konfiguriranje računovodstva za naplative projekte](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Procjene rada

Procjenu rada stvara voditelj projekta ili voditelj resursa koji projektnom zadatku također dodjeljuje generički ili imenovani resurs. Zapisi o dodjeli resursa mogu se pregledati na kartici **Dodjele resursa** na stranici **Pojedinosti projekta** platforme Dataverse. Zapisi o dodjeli resursa na platformi Dataverse stvaraju zapise predviđanja sati rada u aplikacijama Finance and Operations s pomoću stavke **Entitet integracije aplikacije Project Operations za procjene sati rada (msdyn\_resourceassignments)**.

   ![Integracija procjena rada](./Media/DW4LaborEstimates.png)

Dvostruko upisivanje sinkronizira zapise o dodjeli resursa s pripremnom tablicom (**ProjCDSEstimateHoursImport**), a zatim upotrebljava poslovnu logiku za stvaranje i ažuriranje zapisa o predviđanju sati rada (**ProjForecastEmpl**).

Računovođa projekta pregledava predviđanja o satima rada stvorena u aplikacijama Finance and Operations tako da ode na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Planiranje** > **Predviđanja sati rada**.

## <a name="expense-estimates"></a>Procjena troška

Procjene troškova stvara voditelj projekta na kartici **Procjene troškova** stranice **Pojedinosti projekta** na platformi Dataverse. Zapisi o procjeni troškova pohranjuju se u entitetu **Redak procjene** na platformi Dataverse. Ovi zapisi procjene imaju klasu transakcije **Trošak** i sinkroniziraju se sa zapisima predviđanja troškova u aplikacijama Finance and Operations s pomoću značajke **Entitet integracije aplikacije Project Operations za procjene troška (msdyn\_estimatelines)**.

   ![Integracija procjena troška](./Media/DW4ExpenseEstimates.png)

Dvostruko upisivanje sinkronizira zapise o procjeni troška s pripremnom tablicom (**ProjCDSEstimateExpenseImport**), a zatim upotrebljava poslovnu logiku za stvaranje i ažuriranje zapisa o predviđanju troška (**ProjForecastCost**). Redci procjene odvojeno pohranjuju zapise o procjeni prodaje od zapisa o procjeni troškova. Poslovna logika u aplikacijama Finance and Operations popunjavaju jedan zapis predviđanja troškova s pomoću ove pojedinosti u pripremnoj tablici.

Računovođa projekta može pregledati predviđanja o trošku u aplikacijama Finance and Operations tako da ode na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Planiranje** > **Predviđanja troška**.

## <a name="material-estimates"></a>Procijene materijala

Procjene materijala stvara voditelj projekta na kartici **Procjene materijala** stranice **Pojedinosti projekta** na platformi Dataverse. Zapisi o procjeni materijala pohranjuju se u entitetu **Redak procjene** na platformi Dataverse. Ovi zapisi procjene imaju klasu transakcije **Materijal** i sinkroniziraju se sa zapisima predviđanja stavke u aplikacijama Finance and Operations s pomoću značajke **Tablica integracije projekta za procjene materijala (msdyn\_estimatelines)**.

   ![Integracija procjena materijala](./Media/DW4MaterialEstimates.png)

Dvostruko upisivanje sinkronizira zapise o procjeni materijala s pripremnom tablicom **ProjForecastSalesImpor**, a zatim upotrebljava poslovnu logiku za stvaranje i ažuriranje zapisa o predviđanju stavke (**ForecastSales**). Redci procjene odvojeno pohranjuju zapise o procjeni prodaje od zapisa o procjeni troškova. Poslovna logika u aplikacijama Finance and Operations popunjavaju jedan zapis predviđanja stavke s pomoću ove pojedinosti u pripremnoj tablici.

Računovođa projekta može pregledati predviđanja o stavci u aplikacijama Finance and Operations tako da ode na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Planiranje** > **Predviđanja stavke**.

## <a name="project-actuals"></a>Stvarni podaci o projektu

Stvarni podaci o projektu stvaraju se na platformi Dataverse na temelju radnog vremena, troškova, materijala i aktivnosti naplate. Svi operativni atributi ovih transakcija, uključujući količinu, cijenu koštanja, prodajnu cijenu i projekt, obuhvaćeni su u tom entitetu platforme Dataverse. Dodatne informacije potražite u odjeljku [Stvarni podaci](../actuals/actuals-overview.md). Zapisi o stvarnim podacima sinkronizirani su s aplikacijama Finance and Operations s pomoću karte tablice s dvostrukim ispisom **Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)** za nizvodno računovodstvo.

   ![Integracija stvarnih podataka](./Media/DW4Actuals.png)

Karta tablice **Stvarni podaci integracije aplikacije Project Operations** sinkronizira sve zapise iz entiteta **Stvarni podaci** na platformi Dataverse s atributom **Preskoči sinkronizaciju (samo za internu uporabu)** postavljenim na **Netočno**. Ova se vrijednost atributa automatski postavlja na platformi Dataverse kada se stvori zapis. Sljedeći su primjeri gdje je ovaj atribut postavljen na **Točno**:

  - Stvarni podaci o trošku projekta za transakcije među poduzećima unutar tvrtke. Dodatne informacije potražite u članku [Stvaranje transakcija među poduzećima unutar tvrtke](../project-accounting/create-intercompany-transactions.md). Ti se zapisi preskaču jer sustav ponovno stvara stvarne podatke o trošku projekta u aplikacijama Finance and Operations kada se knjiži račun dobavljača među poduzećima unutar tvrtke.
  - Negativni nenaplaćeni zapisi o prodaji stvoreni kada se potvrdi predračun. Ti se zapisi preskaču jer se u sporednoj knjizi projekta pri fakturiranju u aplikacijama Finance and Operations ne poništava zapis o nenaplaćenoj prodaji, ali mijenja status u potpuno fakturiran.

Karta tablice s dvostrukim zapisom sinkronizira zapise sa stvarnim podacima s pripremnom tablicom **ProjCDSActualsImport**. Ti se zapisi obrađuju povremenim postupkom **Uvoz iz pripremne tablice** pri stvaranju redaka dnevnika integracije aplikacije Project Operations i redaka prijedloga fakture za projekt. Dodatne informacije potražite u članku [Dnevnik integracije u aplikaciji Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse također dohvaća veze između stvarnih projektnih transakcija u entitetu **Veza transakcije**. Dodatne informacije potražite u članku [Povezivanje stvarnih podataka s izvornim zapisima](../actuals/linkingactuals.md). Veze između stvarnih transakcija također se sinkroniziraju s aplikacijama Finance and Operations s pomoću karte tablice s dvostrukim upisom, **Entitet integracije za odnose projektnih transakcija (msdyn\_transactionconnections)**. Te zapise upotrebljava povremeni postupak **Uvoz iz pripremne tablice** pri stvaranju redaka dnevnika integracije aplikacije Project Operations i redaka prijedloga fakture za projekt.

Knjiženje dnevnika integracije aplikacije Project Operations i prijedloga fakture za projekt pokreće ažuriranje u odgovarajućim zapisima pripremne tablice, **ProjCDSActualsImport**. Sustav dohvaća i bilježi sljedeće računovodstvene atribute za stvarne transakcije:

- Iznos računovodstvene valute
- Tečaj
- Broj vaučera
- Iznos poreza na promet

Karta tablice **Stvarni podaci o integraciji aplikacije Project Operations** ažurira odgovarajuće zapise stvarnih podataka na platformi Dataverse s tim podacima.
