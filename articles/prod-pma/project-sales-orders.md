---
title: Projektni prodajni nalozi za vremenske i materijalne projekte
description: U ovoj se temi objašnjava način stvaranja prodajnih naloga na temelju projekata za vremenske i materijalne projekte.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289045"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektni prodajni nalozi za vremenske i materijalne projekte

[!include[banner](../includes/banner.md)]

U ovoj temi opisuje se način stvaranja prodajnog naloga za projekt. Prodajni nalozi mogu se stvarati samo za projekte vrste **vrijeme i materijal**.

Ako projekt za vrijeme i materijal ima više izvora financiranja na ugovoru o projektu, morate omogućiti parametar **Omogući prodajne naloge za projekte s više izvora financiranja** na stranici **Parametri upravljanja projektom i računovodstveni parametri**. 

> [!NOTE]
> - Podrška za projektne prodajne naloge s više izvora financiranja dostupna je počevši od izdanja aplikacije 10.0.2 i novijeg.
> - Parametar za omogućivanje podrške za projektne prodajne naloge s više izvora financiranja uklonit će se u valu izdanja za travanj 2020., nakon čega će funkcionalnost uvijek biti omogućena.

Prodajne naloge na temelju projekta možete stvoriti na dva načina:

- Idite na sam projekt. U Oknu radnji odaberite **Upravljanje > Zadaci stavke > Prodajni nalog**. Podaci o projektu zadavat će se prodajnom nalogu iz projekta. Ako ugovor o projektu ima više izvora financiranja, morat ćete odabrati izvor financiranja kako biste postavili klijenta za prodajni nalog. Ako postoji samo jedan izvor financiranja projekta, klijent će se automatski postaviti.
- Idite na stranicu s popisom **Svi prodajni nalozi** i stvorite novi prodajni nalog. Morat ćete odabrati projekt za prodajni nalog. Nakon odabira projekta postavit će se klijent iz izvora financiranja ili, ako ugovor o projektu ima više izvora financiranja, morat ćete odabrati izvor financiranja.



[!INCLUDE[footer-include](../includes/footer-banner.md)]