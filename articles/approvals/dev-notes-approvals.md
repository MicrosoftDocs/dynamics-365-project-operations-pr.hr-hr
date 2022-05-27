---
title: Bilješke razvojnog inženjera za odobrenja
description: U ovoj temi nalaze se dodatne informacije za razvojne inženjere o radu s odobrenjima.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579711"
---
# <a name="developer-notes-for-approvals"></a>Bilješke razvojnog inženjera za odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje logiku provjere valjanosti koja osigurava ispravan prijelaz zapisa kroz faze odobrenja. Ispravni prijelazi zapisa osiguravaju sljedeće: 

  - Svi potporni redci stvaraju se u povezanim tablicama, poput dnevnika i stvarnih podataka.
  - Prije nego što nastavite, odobravatelj se u projektu označava kao **Odobravtelj projekta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]