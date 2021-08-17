---
title: Sinkronizacija kategorija izdataka za projekt između aplikacija Finance and Operations i Project Service Automation
description: U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju kategorija izdataka za projekt između sustava Microsoft Dynamics 365 Finance i aplikacije Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 52c79f8b641d4b2df3b30964331633f2487402f8f8d229b540f9544c0f848557
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001107"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sinkronizacija kategorija izdataka za projekt između aplikacija Finance and Operations i Project Service Automation

[!include[banner](../includes/banner.md)]

U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju kategorija izdataka za projekt između sustava Dynamics 365 Finance i aplikacije Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.
> - Ako upotrebljavate Enterprise Edition 7.3.0, nakon što instalirate zakrpe KB 4132657 i KB 4132660 moći ćete upotrebljavati predloške za integraciju projektnih zadataka, kategorija transakcija izdataka, procjena sati rada, procjena izdataka i stvarnih podataka te za konfiguraciju funkcije zaključavanja. Ako morate vratiti zadane računovodstvene distribucije, preporučujemo da instalirate i zakrpu KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Tijek podataka za aplikacije Project Service Automation i Financije

Rješenje za integraciju aplikacija Project Service Automation i Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije. Predlošci integracije koji su dostupni uz značajku Integracija podataka omogućuju tijek podataka o kategorijama transakcija izdataka za projekt između aplikacija Financije i Project Service Automation.

Ako se kategorije izdataka za projekt obrade u Financijama, tijek integracije ide od Financija do aplikacije Project Service Automation. ID-ovi integracije kategorija izdataka za projekt potom se ažuriraju sinkronizacijom iz aplikacije Project Service Automation u Financije.

Ako se kategorije izdataka za projekt obrade u aplikaciji Project Service Automation, tijek integracije ide od aplikacije Project Service Automation do Financija. Prije sinkronizacije iz aplikacije Project Service Automation kategorije projekata već moraju biti konfigurirane u aplikaciji Financije. Zatim sinkronizirajte iz Financija natrag u aplikaciju Project Service Automation, pa ponovno iz aplikacije Project Service Automation u Financije. Na taj način zajamčena je povezanosti kategorija i nemogućnost stvaranja duplikata.

> [!NOTE]
> Kategorije izdataka za projekt obično se obrađuju u Financijama. Međutim, ako to nije slučaj ili ako su kategorije izdataka već stvorene u aplikaciji Project Service Automation, prvo morate sinkronizirati s pomoću predloška kategorija transakcija izdataka za projekt (PSA u Fin i Ops). Zatim sinkronizirajte s pomoću predloška kategorija transakcija izdataka za projekt (Fin i Ops u PSA). Tada biste trebali još jednom pokrenuti sinkronizaciju od aplikacije Project Service Automation do Financija.
>
> Ako prvo sinkronizirate iz aplikacije Project Service Automation, u aplikaciji Financije prije pokretanja sinkronizacije moraju biti ispunjeni sljedeći zahtjevi:
>
> - Dijeljena kategorija podudarna s kategorijom projekta koja je postavljena u aplikaciju Project Service Automation mora postojati i mora biti omogućena kako za **Projekt** tako i za **Izdatak**.
> - Za svaku pravnu osobu u Financijama s kojom se mora integrirati moraju postojati sljedeće kategorije projekata:
>
>     - Postoji stavka **Kategorija projekta**. 
>     - Omogućena je stavka **Upotrijebi u izdatku**.
>     - Omogućena je stavka **Aktivan u dnevniku**.
>     - **Vrsta transakcije** postavljena je na **Izdatak**.

Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.

[![Tijek podataka za integraciju usluge Project Service Automation s Financijama.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sinkronizacija kategorije izdataka za projekt iz aplikacije Financije u aplikaciju Project Service Automation

### <a name="template-and-task"></a>Predložak i zadatak

Kako biste pristupili predlošku, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti**, a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.

Predložak u nastavku i temeljni zadatak upotrebljavaju se za sinkronizaciju kategorija izdataka za izdataka za projekt iz Financija u aplikaciju Project Service Automation:

- **Naziv predloška u Integraciji podataka:** Kategorije transakcije izdataka za projekt (Fin i Ops u PSA)
- **Naziv zadatka u projektu:** Sinkronizacija kategorija s PSA

### <a name="entity-set"></a>Postavljanje entiteta

| Financije                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entitet integracije za kategorije | Kategorije transakcija     |

### <a name="entity-flow"></a>Tijek entiteta

Kategorijama izdataka za projekt upravlja se u usluzi Financije, a sinkroniziraju se s aplikacijom Project Service Automation kao kategorije transakcija.

### <a name="power-query"></a>Power Query

Kada se sinkronizirate s aplikacijom Project Service Automation, morate upotrebljavati aplikaciju Microsoft Power Query za Excel kako biste postavili vrstu naplate za kategoriju transakcije. Predložak kategorija transakcija izdataka za projekt (Fin i Ops u PSA) omogućuje zadani stupac i mapiranje. Ako stvorite vlastiti predložak, ovaj uvjetni stupac morate dodati modulu Power Query. Slijedite ove korake.

1. Kliknite strelicu kako biste otvorili mapiranje zadatka kategorija izdataka za projekt u predlošku kategorija transakcija izdataka za projekt (Fin i Ops u PSA).
2. Kliknite vezu **Napredni upit i filtriranje** kako biste otvorili modul Power Query.
2. Odaberite **Dodaj uvjetni stupac**.
3. Unesite naziv novog stupca, kao što je **Vrsta naplate**.
4. Unesite sljedeći uvjet: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Kliknite **U redu** na stupcu.
6. Uvjerite se kako ste ovaj novi stupac mapirali na stranicu za mapiranje.

Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz Financija u aplikaciju Project Service Automation.

[![Mapiranje predloška Kategorije izdataka za projekt u aplikaciju Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sinkronizacija kategorije izdataka za projekt iz aplikacije Project Service Automation u Financije

### <a name="template-and-task"></a>Predložak i zadatak

Predložak u nastavku i temeljni zadatak upotrebljavaju se za sinkronizaciju kategorija izdataka za izdataka za projekt iz aplikacije Project Service Automation u Financije:

- **Naziv predloška u Integraciji podataka:** Kategorije transakcije izdataka za projekt (PSA u Fin i Ops)
- **Naziv zadatka u projektu:** Sinkronizacija kategorija s Fin Ops

### <a name="entity-set"></a>Postavljanje entiteta

| Project Service Automation | Financije                           |
|----------------------------|-----------------------------------|
| Kategorije transakcija     | Entitet integracije za kategorije |

### <a name="entity-flow"></a>Tijek entiteta

Kategorijama izdataka za projekt upravlja se u usluzi Financije, a sinkroniziraju se s aplikacijom Project Service Automation kao kategorije transakcija. Sinkronizacija natrag na Financije ažurira kategoriju projekta u Financijama s pomoću ID-a integracije iz aplikacije Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka.

> [!NOTE]
> Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.

[![Mapiranje predloška iz aplikacije Project Service Automation u aplikaciju Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]