---
title: Evidentiranje vremena, troškova i uporabe materijala za podugovorne komponente
description: U ovom se članku objašnjava kako Microsoft prati vrijeme, troškove i korištenje materijala zabilježeno na projektima iz kooperantskih komponenti Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522504"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Vrijeme bilježenja, troškovi i upotreba materijala na projektima za komponente kooperanta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U ovom se članku objašnjava kako Microsoft prati vrijeme, troškove i korištenje materijala zabilježeno na projektima iz kooperantskih komponenti Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Trošak vremena podizvođača na projektima
U projektnim operacijama ugovorni radnici mogu zabilježiti vrijeme na projektima na sličan način kao i zaposlenici. Prilikom unosa vremena na projekte i/ili projektne zadatke, ugovorni radnik može odabrati određeni redak kooperanata i kooperacije.

Kada je vrijeme koje su dostavili ugovorni radnici odobreno, trošak projekta bilježi se pomoću stope jediničnog troška koja je postavljena za taj resurs ugovornog radnika u **odjeljku Cijene** uloga u nabavnom cjeniku na podugovaranju.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Trošak troškova podugovaranja projekata
Prilikom unosa troškova nastalih na projektima možete odabrati redak podugovaratelja i kooperacije u stavci troškova. 

Kada se ova stavka troškova podnese i odobri, trošak troška bilježi se na projektu na temelju jediničnog troška postavljenog za tu kategoriju transakcije u **odjeljku Cijene** kategorija nabavnog cjenika na podugovaranju.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Troškovi materijala kooperanta na projektima
Prilikom unosa upotrebe materijala na projekte možete odabrati redak kooperanta i kooperacije u zapisniku korištenja materijala. Kada se zapisnik korištenja materijala pošalje i odobri, trošak materijala bilježi se na projektu na temelju jediničnog troška postavljenog za taj proizvod u **odjeljku Stavke cjenika** cjenika kooperanta.

Upotreba materijala može se zabilježiti i za upisne proizvode na projektima. Ova vrsta upotrebe materijala također se može povezati s kooperantskom i podugovarateljskom linijom. Prilikom bilježenja upotrebe materijala za dopisane proizvode potrebno je unijeti po jediničnom trošku dopisanog proizvoda. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
