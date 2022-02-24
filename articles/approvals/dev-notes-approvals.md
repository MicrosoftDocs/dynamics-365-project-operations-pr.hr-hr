---
title: Bilješke razvojnog inženjera za odobrenja
description: U ovoj temi nalaze se dodatne informacije za razvojne inženjere o radu s odobrenjima.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483939"
---
# <a name="developer-notes-for-approvals"></a>Bilješke razvojnog inženjera za odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje logiku provjere valjanosti koja osigurava ispravan prijelaz zapisa kroz faze odobrenja. Ispravni prijelazi zapisa osiguravaju sljedeće: 

  - Svi potporni redci stvaraju se u povezanim tablicama, poput dnevnika i stvarnih podataka.
  - Prije nego što nastavite, odobravatelj se u projektu označava kao **Odobravtelj projekta**.
