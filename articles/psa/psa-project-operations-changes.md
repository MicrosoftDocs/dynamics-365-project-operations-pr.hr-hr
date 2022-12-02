---
title: Izmjene značajki s aplikacije Project Service Automation na aplikaciju Project Operations
description: U ovom članku nalazi se pregled promjena značajki za nadogradnju iz servisa Project Service Automation na servis Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459917"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Izmjene značajki s aplikacije Project Service Automation na aplikaciju Project Operations

Nadogradnja iz servisa Dynamics 365 Project Service Automation na servis Dynamics 365 Project Operations Lite isporučivat će se u tri faze. Ovaj članak pruža informacije o glavnim promjenama koje možete očekivati kada nadogradnja bude dovršena.

| Isporuka nadogradnje | Faza 1 <br>(siječanj 2022.) | Faza 2 <br>(studeni 2022.) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nema ovisnosti o strukturnoj analizi rada (SAR) za projekte. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| SAR je uključena u trenutačno podržana ograničenja aplikacije Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| SAR izvan trenutačno podržanih ograničenja aplikacije Project Operations, uključujući podršku za Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Upravljanje projektima

Najznačajnije promjene u korisničkom iskustvu bit će u području planiranja projekta. Project Operations usvaja novo moderno iskustvo za upravljanje strukturnom analizom rada (SAR) iskorištavanjem mogućnosti zakazivanja koje pruža [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Razlike u iskustvu zakazivanja

Sljedeća tablica sažima razlike u zakazivanju između servisa Project Service Automation i servisa Project Operations.

|  Planiranje     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Predlošci projekta - Mogućnost definiranja i primjene predložaka projekata kada se projekt stvara  |  &nbsp;    | :heavy_check_mark: |
| Integracija strukturne analize rada (SAR) projekta sa servisom Desktop Client   |    &nbsp;  | :heavy_check_mark: |
| Ograničenja - nemoj početi ranije, nemojte završiti kasnije  | :heavy_check_mark: |   &nbsp;  |
| Kontrolne točke - Zadaci s nultim trajanjem   | :heavy_check_mark:  |  &nbsp;  |
| Zadaci na temelju resursa poštivat će dostupnost dodijeljenih resursa   | :heavy_check_mark: |  &nbsp;    |
| Uređivanje prema vremenskim fazama - Uredite planove i radite na dnevnoj osnovi   |   &nbsp;  | :heavy_check_mark: |
| Automatsko/ručno zakazivanje - Koristite modul za zakazivanje projekta za automatsko ili ručno zakazivanje zadataka |  &nbsp; | :heavy_check_mark:  |
| Uredite velike projekte izravno u korisničkom sučelju: nema ograničenja u veličini planova koji se mogu uređivati  | Ograničenje od 500 zadataka  | :heavy_check_mark:       |
| Postotak dovršenosti - Označite napredak zadatka   | :heavy_check_mark:  |  &nbsp;  |
| [Načini zakazivanja projekta](../project-management/scheduling-modes.md) - Definirajte projekt kao fiksne jedinice, fiksni napor ili fiksno trajanje | :heavy_check_mark: | &nbsp; |
| Vremenska crta - Izgradite i prilagodite prikaz vremenske crte za vizualizaciju detalja zakazivanja i komunikaciju sa zainteresiranim stranama. | :heavy_check_mark:  | &nbsp; |
| Zadaci na temelju napora - Podrška modula za zakazivanje za zakazivanje zadatka na temelju napora  | :heavy_check_mark:  | &nbsp; |
| Dijaloški okvir **Informacije o zadatku** - Spremite detalje zadatka pomoću dijaloškog okvira | :heavy_check_mark:  |  &nbsp;  |
| Povuci i ispusti - višestruko odaberite zadatke i promijenite njihov položaj na SAR-u | :heavy_check_mark: | &nbsp;  |
| Fleksibilni postojani prikazi - Definirajte preciznije prikaze atributa zadatka   | :heavy_check_mark:  | &nbsp; |
| Sortiranje i filtriranje SAR-a  | :heavy_check_mark:  | &nbsp; |
| Prikaz ploča za isporuku nekaskadnog projekta  | :heavy_check_mark:   | &nbsp; |
| Prikaz vremenske crte - Interaktivni Ganttov grafikon koji se koristi za vizualizaciju i uređivanje SAR-a   | :heavy_check_mark:  | &nbsp; |
| Tipkovni prečaci - koristite tipkovne prečace za uobičajene operacije, kao što su uvlačenje ili umetanje  | :heavy_check_mark:  |  &nbsp; |
| Višerazinsko poništavanje - Izvršite analizu što ako da biste u potpunosti razumjeli utjecaj promjena poništavanjem i ponovnom primjenom čitavog skupa operacija | :heavy_check_mark: | &nbsp; |
| Izreži/Kopiraj/Zalijepi - Surađujte na razvoju rasporeda kopiranjem i lijepljenjem detalja rasporeda između aplikacija  | :heavy_check_mark: | &nbsp; |
| Kontrolni popisi zadatka - Dodajte do 20 stavki kontrolnog popisa zadatku   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planiranje projekta

Stranica **Projekt** u servisu Project Operations ima značajan broj razlika u usporedbi sa stranicom **Projekt** u servisu Project Service Automation.

Sljedeće su radnje uklonjene sa stranice **Projekti** kao dio nadogradnje faze 1:

  - **Otvaranje u programu MS Project**
  - **Stvori predložak**
  - **Poništi vezu s programom MS Project**

Stranica **Projekt** u servisu Project Operations uključuje sljedeće nove kartice.

- **Procijene materijala**
- **Postavljanje zadatka za naplatu**

Kartica **Status** uklonjena je i polje **Status** sada je na kartici **Sažetak** s načinom zakazivanja projekta.

   ![Ažuriranja na stranici Projekt.](media/projectform.png)

Kartica **Raspored** preimenovana je u karticu **Zadatak** i sadrži novo iskustvo planiranja projekta uz servis Project for the Web.

   ![Nova kartica Projektni zadaci.](media/tasktab.png)

## <a name="scheduling-modes"></a>Načini planiranja

Servis Project Operations uveo je novu značajku, [Načini zakazivanja](../project-management/scheduling-modes.md). Svi postojeći projekti servisa Project Service Automation bit će zadani na **Fiksno trajanje** u servisu Project Operations. Međutim, zadanim postavkama za nove projekte može se upravljati odlaskom u **Postavke** > **Parametri** > **Parametar** > **Način zakazivanja**.

   ![Postavke parametara projekta za način zakazivanja.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Ograničenja planiranja projekta

Project Operations oslanja se na Project for the Web za sve operacije zakazivanja projekta. Project for the Web upravlja strukturnom analizom rada pomoću ograničenja u sljedećoj tablici.

| **Polje**                                          | **Ograničenje**             |
|----------------------------------------------------|-----------------------|
| Maksimalan ukupan broj zadataka projekta                  | 500                   |
| Maksimalno ukupno trajanje projekta               | 3650 dana (10 godina)  |
| Maksimalni ukupni resursi projekta              | 300                   |
| Maksimalan broj veza (samo slijednik) za projekt | 600                   |
| Maksimalna ukupna prilagođena polja za projekt          | 1,0                    |
| Maksimalna razina hijerarhije                            | 10 razina             |
| Maksimalan broj veza (slijednik + prednik)            | 20                    |
| Maksimalno trajanje zadatka lista                      | 1250 dana             |
| Maksimalno trajanje sažetog zadatka                 | 3650 dana (10 godina)  |
| Maksimalni resursi dodijeljeni zadatku               | 20 resursa          |
| Podržani datumski raspon za zadatak                    | 01. 01. 2000. – 31. 12. 2149. |
| Stavke popisa za provjeru                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Proširivost i razvoj planiranja projekta

Nakon nadogradnje na Project Operations, morate koristiti API-je zakazivanja projekta za izvršavanje operacija stvaranja, ažuriranja i brisanja na sljedećim entitetima:

|   Naziv entiteta           |   Logički naziv entiteta       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Zadatak projekta            | msdyn_projecttask           |
| Ovisnost projektnog zadatka | msdyn_projecttaskdependency |
| Dodjela resursa     | msdyn_resourceassignment    |
| Grupa projekta          | msdyn_projectbucket         |
| Članov projektnog tima     | msdyn_projectteam           |

Ako trenutno imate prilagodbe koje uključuju te entitete, pogledajte [Koristite API-je zakazivanja projekta za izvršavanje operacija s entitetima zakazivanja](../project-management/schedule-api-preview.md) za smjernice za implementaciju.

## <a name="data-model-changes"></a>Promjene podatkovnog modela

Kao dio 1. faze nadogradnje, postoje promjene u podatkovnom modelu. Ove promjene prvenstveno su izmjene polja postojećih entiteta. U 1. fazi, entiteti, **msydn_project** i **msdyn_projectteam** su refaktoriranje prilagodbi. 

> [!IMPORTANT]
> Ovaj odjeljak ažurirat će se dodatnim entitetima kako buduće faze nadogradnje budu dovršene.

Sljedeća polja zamijenjena su novim poljima.

|   Entity          |   Stari logički naziv   |   Novi logički naziv    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Dodana su sljedeća polja.

|   Entity          |   Logički naziv                               |   Opis |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Prikazuje zbroj vrijednosti stvarne prodaje s naknadom u projektu. Samo za upotrebu u servisu Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Prikazuje zbroj stvarnih materijalnih troškova projekta. Samo za upotrebu u servisu Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Prikazuje zbroj stvarnih prodajnih materijala u projektu. Samo za upotrebu u servisu Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Redak ugovora povezan s ovim projektom. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ovo je polje internog sustava koje se koristi za **kopiranje projekta** povezanog s identifikatorom korelacije. Samo za upotrebu u servisu Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ovo je polje internog sustava koje se koristi za **kopiranje projekta** povezanog s identifikatorom sesije. Samo za upotrebu u servisu Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Posljednja sinkronizacija xRM globalne revizije tokena iz usluge zakazivanja projekta. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokument Microsoft Project koji pripada projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Zbroj planiranih materijalnih troškova projekta. Samo za upotrebu u servisu Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Zbroj planiranih prodaja materijala projekta. Samo za upotrebu u servisu Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program s kojim je ovaj projekt povezan. |
| msdyn_project     | msdyn_quotelineproject                       | Redak ponude povezan s ovim projektom. |
| msdyn_project     | msdyn_replaylogheader                        | Zaglavlje za zapisnike ponovne reprodukcije. |
| msdyn_project     | msdyn_schedulemode                           | Zadani način zakazivanja koji se koristi za sve zadatke u projektu.  |
| msdyn_project     | msdyn_taskearlieststart                      | Najraniji datum početka bilo kojeg zadatka u projektu.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Prikazuje člana projektnog tima iz kojeg je kopiran taj član projektnog tima. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Navodi treba li stvoriti zahtjev za resurs za novoosnovanog člana generičkog tima.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status brisanja člana tima kako bi se pratilo postoji li zahtjev za brisanje poslan usluzi zakazivanja projekta i hoće li odgovor poslati uspješno i unutar očekivanog vremenskog okvira. |
| msdyn_projectteam | msdyn_effortcompleted                        | Praćenje rada koji je član tima izvršio na svojim zadacima. |
| msdyn_projectteam | msdyn_effortremaining                        | Praćenje rada koji član tima još nije izvršio na svojim zadacima. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Razdoblje čekanja od trenutka kada član tima pošalje zahtjev za brisanje u uslugu zakazivanja projekta do stvarnog brisanja člana tima u servisu Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Podaci vremenske oznake za zapis vremena slanja zahtjeva za brisanje člana tima u uslugu zakazivanja projekta. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Prikazuje člana projektnog tima iz kojeg je kopiran taj član projektnog tima.  |

## <a name="project-templates"></a>Predlošci projekta

Project Operations ne pruža podršku za predloške projekta. Međutim, možete replicirati velik dio temeljne funkcionalnosti upotrebom [API-ja kopiranja projekta](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Podrška za dodatke za stolna računala

Podrška za dodatke za stolna računala Microsoft Project neće biti dostupna u prve 2 faze nadogradnje. U 3. fazi, korisnici koji imaju projekte veće od trenutno podržanih ograničenja servisa Project for the Web moći će koristiti dodatak za stolna računala.

## <a name="editing-resource-assignment-contours"></a>Uređivanje kontura za dodjelu resursa

Mogućnost uređivanja kontura dodjele resursa bit će dostupna kada bude dostupna 2. faza nadogradnje.

## <a name="billing-and-pricing"></a>Naplata i određivanje cijene

Sljedeće nove značajke dodane su u Project Operations. Ove su značajke aditivne prirode i ne utječu na podatkovni model servisa Project Service Automation.

- [Zapis utrošenog materijala na projektima i projektnim zadacima](../material/material-usage-log.md)
- [Upravljanje podugovorima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Predujmovi i ugovori koji e temelje na povremenim plaćanjima](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Ugovor sa statusom koji se ne smije premašiti i provjerama valjanosti](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Naplata na temelju zadataka](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Zastarjele komponente

Sljedeće tablice dokumentiraju sva zastarjela polja koja su premještena u rješenje za zastarjele komponente nakon nadogradnje. Za dodatne informacije i vezu na rješenje pogledajte [Dynamics 365 Project Service Automation 3x u servisu Project Operations 4x zastarjele komponente](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

