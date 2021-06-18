---
title: Bilješke razvojnog inženjera za odobrenja
description: U ovoj temi nalaze se dodatne informacije za razvojne inženjere o radu s odobrenjima.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996782"
---
# <a name="developer-notes-for-approvals"></a>Bilješke razvojnog inženjera za odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje logiku provjere valjanosti koja osigurava ispravan prijelaz zapisa kroz faze odobrenja. Ispravni prijelazi zapisa osiguravaju sljedeće: 

  - Svi potporni redci stvaraju se u povezanim tablicama, poput dnevnika i stvarnih podataka.
  - Prije nego što nastavite, odobravatelj se u projektu označava kao **Odobravtelj projekta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]