---
title: Pregled usluge Project Service Automation
description: U ovoj se temi nalaze informacije o rješenju za integraciju usluge Dynamics 365 Project Service Automation u aplikaciju Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073529"
---
# <a name="project-service-automation-overview"></a>Pregled usluge Project Service Automation

[!include[banner](../includes/banner.md)]

Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Dynamics 365 Finance i Dynamics 365 Project Service Automation preko platforme Common Data Service. Predlošci integracije koji su dostupni uz značajku Integracija podataka omogućuju tijek projekata, ugovore o projektu, retke ugovora o projektu, prekretnice u retku ugovora o projektu, projektne zadatke, kategorije transakcija izdataka, procjene sati i izdataka od usluge Project Service Automation do Financija.

> [!NOTE]
> - Ako upotrebljavate verziju 7.3.0, morate instalirati zakrpu KB 4074835. Tada ćete moći integrirati projekte s fiksnom cijenom.
> - Ako upotrebljavate verziju 7.3.0 i transakcije naknada prenosite iz usluge Project Service Automation, morate instalirati zakrpu KB 4345320 kako biste te naknade uključili u fakturu projekta.
> - Ako upotrebljavate verziju 8.0, moći ćete upotrebljavati integraciju projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti.
> - Ako upotrebljavate verziju 8.0.1 ili noviju, moći ćete sinkronizirati stvarne podatke.

Kako biste mogli integrirati Financije usluge Project Service Automation, morate konfigurirati parametre integracije usluge Project Service Automation. Dodatne informacije potražite u odjeljku [Parametri integracije usluge Project Service Automation](PSA-parameters.md).

Ovo rješenje integracije omogućuje izravnu sinkronizaciju u sljedećim scenarijima:

- Održavajte ugovore o projektu u usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.
- Stvarajte projekte na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.
- Održavajte retke ugovora o projektu na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.
- Održavajte prekretnice redaka ugovora o projektu na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.
- Održavajte projektne zadatke na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.
- Održavajte kategorije transakcija izdatka u Financijama i sinkronizirajte ih izravno s Financija na uslugu Project Service Automation.
- Stvarajte procjene sati za projekt na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.
- Stvarajte procjene izdataka za projekt na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.
- Stvorite vrijeme za projekt, izdatke i stvarne naknade na usluzi Project Service Automation i stvorite projektne transakcije u dnevniku o integraciji usluge Project Service Automation tako da se mogu objaviti u Financijama.

## <a name="data-synchronization"></a>Sinkronizacija podataka

Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju kao dio integracije između usluge Project Service Automation i Financija.

> [!NOTE]
> Trenutačno nisu dostupni svi predlošci. Predlošci će se objaviti čim budu dovršeni.

[![Integracija usluge Project Service Automation s Financijama](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Preduvjeti sustava za financije

Kako biste upotrebljavali rješenje za integraciju usluge Project Service Automation s Financijama, morate instalirati verziju Enterprise Edition 7.3 s ažuriranjem platforme 12 ili novijim.

## <a name="system-requirements-for-project-service-automation"></a>Preduvjeti sustava za uslugu Project Service Automation

Kako biste upotrebljavali rješenje za integraciju usluge Project Service Automation s Financijama, morate instalirati sljedeće komponente:

- Dynamics 365 Project Service Automation, verzija 9.0.0.0 ili noviji
- Mogućnost gotovinskog rješenja za aplikaciju Dynamics 365 Sales, verzija 1.14.0.0 (v14) ili novija
- Rješenje Project Service Automation u Financije za aplikaciju Dynamics 365 Project Service Automation verzija 1.0.0.0 ili novija

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instalirajte rješenje za integraciju usluge Project Service Automation u Financije u svojoj instanci Project Service Automation

Preuzmite rješenje za integraciju usluge Project Service Automation u Financije u [Microsoftovu centru za preuzimanje](https://www.microsoft.com/download/details.aspx?id=57016) i slijedite upute koje ste dobili uz rješenje.
