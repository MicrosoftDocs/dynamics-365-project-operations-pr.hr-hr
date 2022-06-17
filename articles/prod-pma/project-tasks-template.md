---
title: Sinkronizacija projektnih zadataka izravno s automatizacije projektnih usluga na financije i operacije
description: U ovom se članku opisuju predložak i temeljni zadatak koji se koriste za sinkronizaciju projektnih zadataka izravno iz Microsoft Dynamics 365 Project Service Automation Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7b8ba77bbb08052952a8a557bb71300652dca3b2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931137"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sinkronizacija projektnih zadataka izravno s automatizacije projektnih usluga na financije i operacije

[!include[banner](../includes/banner.md)]

U ovom se članku opisuju predložak i temeljni zadatak koji se koriste za sinkronizaciju projektnih zadataka izravno iz Dynamics 365 Project Service Automation Dynamics 365 Finance.

> [!NOTE]
> - Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Ako upotrebljavate Enterprise Edition 7.3.0, nakon što instalirate zakrpe KB 4132657 i KB 4132660 moći ćete upotrebljavati predloške za integraciju projektnih zadataka, kategorija transakcija izdataka, procjena sati rada, procjena izdataka i stvarnih podataka te za konfiguraciju funkcije zaključavanja. Ako morate vratiti zadane računovodstvene distribucije, preporučujemo da instalirate i zakrpu KB 4131710.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tijek podataka s usluge Project Service Automation na Financije

Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije. Predložak integracije koji je dostupan sa značajkom Integracija podataka omogućuje protok podataka o projektnim zadacima s usluge Project Service Automation u Financije.

Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.

[![Tijek podataka za integraciju usluge Project Service Automation s aplikacijom Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

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

Ako je ovaj uvjet zadovoljen, morate koristiti Microsoft Power Query za Excel za filtriranje podataka:

- U projektnom zadatku imate zapise specifične za resurse.

Ako morate koristiti Power Query, slijedite ove smjernice:

- Predložak projektnih zadataka (PSA u Fin i Ops) ima zadani filtar koji isključuje zapise specifične za resurse iz projektnog zadatka postavljanjem filtra na stavki **IsLineTask** na **Netočno**. Ako stvorite vlastiti predložak, morate dodati ovaj filtar.

## <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.

[![Mapiranje predloška.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]