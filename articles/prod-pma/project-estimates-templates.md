---
title: Sinkronizacija procjena projekta izravno iz usluge Project Service Automation na uslugu Finance and Operations
description: U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju procjena radnih sati na projektu i izdataka za projekt izravno iz sustava Microsofta Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073516"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sinkronizacija procjena projekta izravno iz usluge Project Service Automation na uslugu Finance and Operations

[!include[banner](../includes/banner.md)]

U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju procjena radnih sati na projektu i procjena izdataka za projekt izravno iz sustava Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.

> [!NOTE]
> - Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tijek podataka s usluge Project Service Automation na Financije

Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije. Predlošci integracije koji su dostupni uz značajku Integracija podataka omogućuju tijek podataka o procjeni sati rada na projektu i procjeni izdataka za projekt iz usluge Project Service Automation u Financije.

Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.

[![Tijek podataka za integraciju usluge Project Service Automation s Financijama](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Procjene sati rada na projektu

### <a name="template-and-tasks"></a>Predlošci i zadaci

Kako biste pristupili dostupnim predlošcima, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti** , a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.

Predložak u nastavku i temeljni zadaci upotrebljavaju se za sinkronizaciju procjena radnih sati za projekt iz usluge Project Service Automation u Financije:

- **Naziv predloška u Integraciji podataka:** Procjene radnih sati za projekt (PSA u Fin i Ops)
- **Naziv zadataka u projektu:**

    - Odnosi transakcija
    - Procjena troška

### <a name="entity-set"></a>Postavljanje entiteta

| Project Service Automation | Financije                                       |
|----------------------------|-----------------------------------------------|
| Projektni zadaci              | Entitet integracije za procjenu sati rada na projektu |

### <a name="entity-flow"></a>Tijek entiteta

Procjenama radnih sati za projekt upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao predviđanja radnih sati za projekt.

### <a name="prerequisites"></a>Preduvjeti

Prije nego što se dogodi sinkronizacija procjena sati rada na projektu, morate sinkronizirati projekte, projektne zadatke i kategorije transakcija izdataka za projekt.

### <a name="power-query"></a>Power Query

U predlošku procjene radnih sati za projekt morate upotrijebiti uslugu Microsoft Power Query za Excel kako biste izvršili ove zadatke:

- Postavite zadani ID modela predviđanja koji će se upotrebljavati kada integracija stvara nova predviđanja radnih sati.
- U zadatku filtrirajte sve zapise specifične za resurse koji se neće uspjeti integrirati u predviđanja radnih sati.
- Filtrirajte sve prazne retke kategorija transakcija. Neispunjavanje ovog zadatka može dovesti do pogrešnih predviđanja radnih sati.

#### <a name="set-the-default-forecast-model-id"></a>Postavljanje zadanog ID-a modela predviđanja

Kako biste u predlošku ažurirali zadani ID modela predviđanja, kliknite strelicu **Mapiraj** kako biste otvorili mapiranje. Zatim odaberite vezu **Napredni upit i filtriranje**.

- Ako upotrebljavate zadani predložak Procjene radnih sati za projekt (PSA u Fin i Ops), odaberite **Umetnuti uvjet** na popisu **Primijenjeni koraci**. U unosu **Funkcija** zamijenite **O\_forecast** nazivom ID-a modela predviđanja koji bi se trebao upotrijebiti s integracijom. Zadani predložak ima ID modela predviđanja iz pokaznih podataka.
- Ako stvarate novi predložak, morate dodati ovaj stupac. U modulu Power Query odaberite **Dodaj uvjetni stupac** i unesite naziv novog stupca, kao što je **ModelID**. Unesite uvjet za stupac, gdje, ako Projektni zadatak ima vrijednost nula , onda \<enter the forecast model ID\>; inače ima vrijednost nula.

#### <a name="filter-out-resource-specific-records"></a>Filtriranje zapisa specifičnih za resurse

Predložak procjena sati rada na projektu (PSA u Fin i Ops) ima zadani filtar koji uklanja sve zapise specifične za resurs. Ako stvorite vlastiti predložak, morate dodati ovaj filtar. Odaberite vezu **Napredni upit i filtriranje** kako biste filtrirali stupac **msdyn\_islinetask** tako da su uključeni samo zapisi **Netočno**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtriranje praznih redaka kategorija transakcija

Morate dodati filtar kako biste uklonili sve retke koji imaju prazne kategorije transakcija. Ovaj je zadatak potreban, bez obzira upotrebljavate li zadani predložak ili stvarate vlastiti. Ovaj filtar uklanja sve retke sažetka iz usluge Project Service Automation koji mogu uzrokovati netočna predviđanja radnih sati u Financijama. Odaberite vezu **Napredni upit i filtriranje** kako biste filtrirali prazne zapise u stupcu **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.

[![Mapiranje zadatka predloška u integraciji podataka](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Procjene izdataka za projekt

### <a name="template-and-tasks"></a>Predlošci i zadaci

Predložak u nastavku i temeljni zadaci upotrebljavaju se za sinkronizaciju procjena izdataka za projekt iz usluge Project Service Automation u Financije:

- **Naziv predloška u Integraciji podataka:** Procjene izdataka za projekt (PSA u Fin i Ops)
- **Naziv zadataka u projektu:**

    - Odnosi transakcija 
    - Procjena troška

### <a name="entity-set"></a>Postavljanje entiteta

| Project Service Automation | Financije                                                  |
|----------------------------|----------------------------------------------------------|
| Veze transakcija    | Entitet integracije za odnose transakcije projekta |
| Reci procjene             | Entitet integracije za procjenu izdataka za projekt         |

### <a name="entity-flow"></a>Tijek entiteta

Procjenama izdataka za projekt upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao predviđanja izdataka za projekt.

### <a name="prerequisites"></a>Preduvjeti

Prije nego što se dogodi sinkronizacija procjena izdataka na projektu, morate sinkronizirati projekte, projektne zadatke i kategorije transakcija izdataka za projekt.

### <a name="power-query"></a>Power Query

U predlošku procjene izdataka za projekt morate upotrijebiti modul Power Query kako biste izvršili sljedeće zadatke:

- Filtrirajte kako biste uključili samo zapise redaka procjene izdataka.
- Postavite zadani ID modela predviđanja koji će se upotrebljavati kada integracija stvara nova predviđanja radnih sati.
- Pretvorite vrste naplata.
- Pretvorite vrste transakcija.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtriranje kako bi se uključili samo redci procjene izdataka

Predložak procjena izdataka za projekt (PSA u Fin i Ops) ima zadani filtar koji pri integraciji uključuje samo retke izdataka. Ako stvorite vlastiti predložak, morate dodati ovaj filtar. Odaberite zadatak **Odnosi transakcije** , a zatim kliknite strelicu **Mapiraj** kako biste otvorili mapiranje. Odaberite vezu **Napredni upit i filtriranje**. Filtrirajte stupac **msdyn\_transactiontype1** tako da uključuje samo **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Postavljanje zadanog ID-a modela predviđanja

Kako biste u predlošku ažurirali zadani ID modela predviđanja, odaberite zadatak **Procjene izdataka** i zatim kliknite strelicu **Mapiraj** kako biste otvorili mapiranje. Odaberite vezu **Napredni upit i filtriranje**.

- Ako upotrebljavate zadani predložak Procjene izdataka za projekt (PSA u Fin i Ops), u modulu Power Query odaberite prvi **Umetnuti uvjet** iz odjeljka **Primijenjeni koraci**. U unosu **Funkcija** zamijenite **O\_forecast** nazivom ID-a modela predviđanja koji bi se trebao upotrijebiti s integracijom. Zadani predložak ima ID modela predviđanja iz pokaznih podataka.
- Ako stvarate novi predložak, morate dodati ovaj stupac. U modulu Power Query odaberite **Dodaj uvjetni stupac** i unesite naziv novog stupca, kao što je **ModelID**. Unesite uvjet za stupac, gdje, ako vrijednost ID retka Procjene nije nula , onda \<enter the forecast model ID\>; inače ima vrijednost nula.

#### <a name="transform-the-billing-types"></a>Pretvaranje vrsta naplata

Predložak procjene izdataka za projekt (PSA u Fin i Ops) uključuje uvjetni stupac koji se upotrebljava za pretvaranje vrsta naplate primljenih iz usluge Project Service Automation tijekom integracije. Ako stvorite vlastiti predložak, morate dodati ovaj uvjetni stupac. Odaberite vezu **Napredni upit i filtriranje** , a zatim odaberite **Dodaj uvjetni stupac**. Unesite naziv novog stupca, kao što je **Vrsta naplate**. Zatim unesite sljedeći uvjet:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Pretvaranje vrsta transakcija

Predložak procjene izdataka za projekt (PSA u Fin i Ops) uključuje uvjetni stupac koji se upotrebljava za pretvaranje vrsta transakcija primljenih iz usluge Project Service Automation tijekom integracije. Ako stvorite vlastiti predložak, morate dodati ovaj uvjetni stupac. Odaberite vezu **Napredni upit i filtriranje** , a zatim odaberite **Dodaj uvjetni stupac**. Unesite naziv novog stupca, kao što je **Vrsta transakcije**. Zatim unesite sljedeći uvjet:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

Sljedeće slike prikazuju primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.

[![Mapiranje predloška transakcija procjene troškova](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapiranje predloška procjene troškova](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]