---
title: Vrijeme bilježenja, troškovi i upotreba materijala za podugovarale komponente
description: Ovaj tema objašnjava kako Microsoft prati vrijeme, trošak i upotrebu materijala zabilježene na projektima iz kooperiranih komponenti Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903634"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Bilježenje vremena, troškova i upotrebe materijala na projektima za kooperantske komponente

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj tema objašnjava kako Microsoft prati vrijeme, trošak i upotrebu materijala zabilježene na projektima iz kooperiranih komponenti Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Troškovi za vrijeme podizvođača na projektima
U projektnim operacijama ugovorni radnici mogu bilježiti vrijeme na projektima na sličan način kao i zaposlenici. Prilikom unosa vremena na projekte i/ili projektne zadatke ugovorni radnik može odabrati određeni redak kooperanta i kooperanta.

Kada je vrijeme koje su poslali ugovorni radnici odobreno, trošak projekta bilježi se pomoću jedinične stope troška koja je postavljena za taj resurs **ugovornog radnika u odjeljku Cijene uloga** cjenika nabave na podugovaljku.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Troškovi kooperantskih troškova na projektima
Prilikom unosa troškova nastalih na projektima možete odabrati redak kooperanta i kooperanta u stavci troška. 

Kada se ova stavka troška podnese i odobri, trošak se bilježi na projektu na temelju jediničnog troška postavljenog za tu kategoriju transakcije u **odjeljku Cijene** kategorije cjenika nabave na podugovaranom listu.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Troškovi kooperantnih materijala na projektima
Prilikom unosa upotrebe materijala na projekte možete odabrati redak kooperanta i kooperanta u zapisniku korištenja materijala. Kada se evidencija korištenja materijala pošalje i odobri, trošak materijala bilježi se na projektu na temelju jediničnog troška postavljenog za taj proizvod u **odjeljku Stavke** cjenika cjenika.

Upotreba materijala može se zabilježiti i za dopisne proizvode na projektima. Ova vrsta korištenja materijala također se može povezati s retkom kooperanta i kooperanta. Prilikom bilježenja upotrebe materijala za dopisne proizvode potrebno je unijeti jedinični trošak proizvoda za upis. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
