---
title: Bilješke razvojnog inženjera za odobrenja
description: U ovom se članku navode dodatne informacije za razvojne inženjere o radu s odobrenjima.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924743"
---
# <a name="developer-notes-for-approvals"></a>Bilješke razvojnog inženjera za odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje logiku provjere valjanosti koja osigurava ispravan prijelaz zapisa kroz faze odobrenja. Ispravni prijelazi zapisa osiguravaju sljedeće: 

  - Svi potporni redci stvaraju se u povezanim tablicama, poput dnevnika i stvarnih podataka.
  - Prije nego što nastavite, odobravatelj se u projektu označava kao **Odobravtelj projekta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]