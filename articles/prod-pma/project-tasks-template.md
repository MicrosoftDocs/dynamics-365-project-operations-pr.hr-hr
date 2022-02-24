---
title: Sinkronizirajte projektne zadatke izravno iz usluge Project Service Automation na uslugu Finance and Operations
description: U ovoj se temi opisuju predložak i temeljni zadatak koji se upotrebljavaju za sinkronizaciju projektnih zadataka izravno iz sustava Microsoft Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.
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
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073370"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sinkronizirajte projektne zadatke izravno iz usluge Project Service Automation na uslugu Finance and Operations

[!include[banner](../includes/banner.md)]

U ovoj se temi opisuju predložak i temeljni zadatak koji se upotrebljavaju za sinkronizaciju projektnih zadataka izravno iz sustava Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.

> [!NOTE]
> - Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Ako upotrebljavate Enterprise Edition 7.3.0, nakon što instalirate zakrpe KB 4132657 i KB 4132660 moći ćete upotrebljavati predloške za integraciju projektnih zadataka, kategorija transakcija izdataka, procjena sati rada, procjena izdataka i stvarnih podataka te za konfiguraciju funkcije zaključavanja. Ako morate vratiti zadane računovodstvene distribucije, preporučujemo da instalirate i zakrpu KB 4131710.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tijek podataka s usluge Project Service Automation na Financije

Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije. Predložak integracije koji je dostupan sa značajkom Integracija podataka omogućuje protok podataka o projektnim zadacima s usluge Project Service Automation u Financije.

Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.

[![Tijek podataka za integraciju usluge Project Service Automation s Financijama](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Predložak i zadatak

Kako biste pristupili predlošku, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti**, a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.

Predložak u nastavku i temeljni zadatak upotrebljavaju se za sinkronizaciju projektnih zadataka iz usluge Project Service Automation u Financije:

- **Naziv predloška u Integraciji podataka:** Projektni zadaci (PSA u Fin i Ops)
- **Naziv zadatka u projektu:** Projektni zadaci

Prije nego što dođe do sinkronizacije projektnih zadataka, morate sinkronizirati ugovore o projektima i projekte.

## <a name="entity-set"></a>Postavljanje entiteta

| Project Service Automation | Financije                             |
|----------------------------|-------------------------------------|
| Zadaci projekta              | Entitet integracije za projektni zadatak |

## <a name="entity-flow"></a>Tijek entiteta

Projektnim zadacima upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao projektne aktivnostima.

## <a name="prerequisites-and-mapping-setup"></a>Preduvjeti i postavljanje mapiranja

Prije nego što dođe do sinkronizacije projektnih zadataka, morate sinkronizirati ugovore o projektima i projekte.

## <a name="power-query"></a>Power Query

Morate upotrijebiti uslugu Microsoft Power Query za Excel kako biste filtrirali podatke ako je ispunjen ovaj uvjet:

- U projektnom zadatku imate zapise specifične za resurse.

Ako morate upotrijebiti modul Power Query, slijedite ovu smjernicu:

- Predložak projektnih zadataka (PSA u Fin i Ops) ima zadani filtar koji isključuje zapise specifične za resurse iz projektnog zadatka postavljanjem filtra na stavki **IsLineTask** na **Netočno**. Ako stvorite vlastiti predložak, morate dodati ovaj filtar.

## <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.

[![Mapiranje predloška](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
