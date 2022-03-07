---
title: Bilješke razvojnog inženjera za odobrenja
description: U ovoj temi nalaze se dodatne informacije za razvojne inženjere o radu s odobrenjima.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991657"
---
# <a name="developer-notes-for-approvals"></a>Bilješke razvojnog inženjera za odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje logiku provjere valjanosti koja osigurava ispravan prijelaz zapisa kroz faze odobrenja. Ispravni prijelazi zapisa osiguravaju sljedeće: 

  - Svi potporni redci stvaraju se u povezanim tablicama, poput dnevnika i stvarnih podataka.
  - Prije nego što nastavite, odobravatelj se u projektu označava kao **Odobravtelj projekta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]