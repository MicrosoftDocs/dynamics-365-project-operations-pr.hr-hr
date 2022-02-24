---
title: Narudžbenice za projekte
description: U ovom se članku opisuju različite metode koje možete upotrebljavati za stvaranje narudžbenica za projekt. Način koji upotrebljavate ovisi o svrsi narudžbenice i vremenu kada su kupljene stavke utrošene u projektu i naplaćene.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073376"
---
# <a name="purchase-orders-for-a-project"></a>Narudžbenice za projekte

[!include [banner](../includes/banner.md)]

U ovom se članku opisuju različite metode koje možete upotrebljavati za stvaranje narudžbenica za projekt. Način koji upotrebljavate ovisi o svrsi narudžbenice i vremenu kada su kupljene stavke utrošene u projektu i naplaćene.

### <a name="methods-for-creating-a-purchase-order"></a>Načini stvaranja narudžbenice

Za stvaranje narudžbenice u Upravljanju projektima i računovodstvu možete upotrijebiti jednu od sljedećih metoda. Svrha narudžbenice određuje kada se narudžbenica troši i, prema tome, kada se stavke naplaćuju projektu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Način</th>
<th>Svrha</th>
<th>Potrošnja stavki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stvorite narudžbenicu izravno iz projekta.</td>
<td>Ovaj način upotrebljavajte kako biste stavke koje se troše na projektu kupili od vanjskog dobavljača. Narudžbenicu možete stvoriti na dva načina:
<ul>
<li>Iz samog projekta. U tom je slučaju projekt već definiran za narudžbenicu.</li>
<li>Pomicanjem do narudžbenice za projekt. Morate odabrati dobavljača i projekt za koji ćete stvoriti narudžbenicu.</li>
</ul></td>
<td>Stavke se troše kada se ažurira faktura dobavljača.</td>
</tr>
<tr class="even">
<td>Stvorite narudžbenicu izravno iz prodajnog naloga.</td>
<td>Ovaj način upotrijebite kako biste stavke kupili kada iz projekta stvorite prodajni nalog.</td>
<td>Stavke se troše kad se klijentu fakturira prodajni nalog.</td>
</tr>
<tr class="odd">
<td>Stvorite narudžbenicu iz zahtjeva za stavkom.</td>
<td>Ovaj način upotrijebite kako biste stavke kupili kada iz projekta stvorite zahtjev za stavkom.</td>
<td>Stavke se troše kada se ažurira otpremnica zahtjeva za stavkom.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Kada ažurirate fakturu dobavljača ili otpremnicu, od vas će se zatražiti da ažurirate otpremnicu na zahtjevu za stavku.

Dodatne informacija potražite u odjeljku [Primanje stavki na narudžbenicu iz zahtjeva za stavkom](tasks/receive-items-purchase-order-item-requirement.md).

