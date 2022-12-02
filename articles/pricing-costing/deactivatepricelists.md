---
title: Deaktiviranje cjenika
description: U ovom se članku objašnjava kako deaktivirati ili ukloniti neupotrijebljene ili stare cjenike.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56bd498d2cb892bdf0c7514d0918e3873098b8d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924375"
---
# <a name="deactivate-price-lists"></a>Deaktiviranje cjenika 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Za uklanjanje starih ili neupotrijebljenih cjenika iz aplikacije Dynamics 365 Project Operations, morate poduzeti dva koraka. 

1. Uklonite ili izbrišite cjenik s određenih stranica.
2. Deaktivirajte ili izbrišite cjenik iz Aktivnih cjenika na stranici **Cjenici**.

>[!IMPORTANT]
> Morate izvršiti oba koraka kako biste u potpunosti uklonili cjenik. Nije dovoljno samo izvođenje 2. koraka tj. izravnog brisanja ili deaktiviranja cjenika iz prikaza Aktivni cjenici. Morate izbrisati i povezanost ovog cjenika sa svim mjestima spomenutim u 1. koraku.

## <a name="delete-the-price-list-from-specific-pages"></a>Brisanje cjenika s određenih stranica
1. Kako biste izbrisali cjenik iz aplikacije Project Operations, idite na sljedeće stranice:  

      - Stranica **Parametri projekta** > kartica **Cjenici**
      - Stranica **Organizacijska jedinica** > rešetka **Cjenici**
      - Stranica **Račun** > rešetka **Cjenici projekta**
      - Stranica **Ponude projekta** > rešetka **Cjenici projekta**: Ovo se primjenjuje na sve aktivne ponude projekta.
      - Stranica **Ugovori o projektu** > rešetka **Cjenici projekta**: Ovo se primjenjuje na sve aktivne ugovore o projektu.

 2. Za svaku stranicu morate odabrati cjenik koji želite izbrisati, a zatim odaberite **Briši**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Brisanje ili deaktiviranje cjenika sa stranice Cjenici
 
1. Kako biste izbrisali cjenik iz aktivnih cjenika, idite na **Prodajni** > **Klijenti** > **Cjenici**. 
2. Odaberite cjenik koji želite izbrisati i zatim odaberite **Briši**. Ako se cjenik navodi na nekoj postojećoj transakciji, nećete ga moći izbrisati. Ako se to dogodi, možete deaktivirati cjenik tako da se ne prikazuje ni u jednom prikazu. 
3. Kako biste deaktivirali cjenik, ponovno odaberite cjenik, a zatim odaberite **Deaktiviraj**.   
