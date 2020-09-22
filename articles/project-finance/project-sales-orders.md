---
title: Projektni prodajni nalozi za vremenske i materijalne projekte
description: U ovoj se temi objašnjava način stvaranja prodajnih naloga na temelju projekata za vremenske i materijalne projekte.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750079"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektni prodajni nalozi za vremenske i materijalne projekte

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

U ovoj temi opisuje se način stvaranja prodajnog naloga za projekt. Prodajni nalozi mogu se stvarati samo za projekte vrste **vrijeme i materijal**.

Ako projekt za vrijeme i materijal ima više izvora financiranja na ugovoru o projektu, morate omogućiti parametar **Omogući prodajne naloge za projekte s više izvora financiranja** na stranici **Parametri upravljanja projektom i računovodstveni parametri**. 

> [!NOTE]
> - Podrška za projektne prodajne naloge s više izvora financiranja dostupna je počevši od izdanja aplikacije 10.0.2 i novijeg.
> - Parametar za omogućivanje podrške za projektne prodajne naloge s više izvora financiranja uklonit će se u valu izdanja za travanj 2020., nakon čega će funkcionalnost uvijek biti omogućena.

Prodajne naloge na temelju projekta možete stvoriti na dva načina:

- Idite na sam projekt. U Oknu radnji odaberite **Upravljanje > Zadaci stavke > Prodajni nalog**. Podaci o projektu zadavat će se prodajnom nalogu iz projekta. Ako ugovor o projektu ima više izvora financiranja, morat ćete odabrati izvor financiranja kako biste postavili klijenta za prodajni nalog. Ako postoji samo jedan izvor financiranja projekta, klijent će se automatski postaviti.
- Idite na stranicu s popisom **Svi prodajni nalozi** i stvorite novi prodajni nalog. Morat ćete odabrati projekt za prodajni nalog. Nakon odabira projekta postavit će se klijent iz izvora financiranja ili, ako ugovor o projektu ima više izvora financiranja, morat ćete odabrati izvor financiranja.

