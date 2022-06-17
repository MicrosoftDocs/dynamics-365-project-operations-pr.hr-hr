---
title: Opoziv fakture dobavljača projekta
description: U ovom se članku objašnjava kako otkazati fakturu dobavljača projekta u Microsoftu Dynamics 365 Project Operations i financijski učinak otkazivanja fakture dobavljača projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911541"
---
# <a name="cancel-a-project-vendor-invoice"></a>Opoziv fakture dobavljača projekta

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Nakon potvrde fakture dobavljača ne može se uređivati ni brisati. Ako je došlo do pogreške na fakturi dobavljača koja je potvrđena, akcijom Storniraj možete stornirati utjecaj fakture dobavljača i kreirati novu fakturu dobavljača.

Kada na fakturi dobavljača odaberete **Odustani**, događa se sljedeće ponašanje:

1. Stanje fakture dobavljača obnavlja se u **Otkazano**.
2. Otkazana faktura dobavljača i povezani zapisi postaju samo za čitanje i ne mogu se uređivati ili brisati.
3. Storniraju se sve stvarne količine troškova kreirane na temelju redaka fakture dobavljača kao dio potvrde fakture dobavljača.
4. Ako su stvarni troškovi povezani s recima fakture dobavljača kao dio postupka podudaranja, izvorna potvrda fakture dobavljača ih je stornirala. Tijekom otkazivanja fakture dobavljača te se stvarne troškove ponovno kreiraju. Podrijetlo upućuje na vrijeme, trošak ili stavke upotrebe materijala.
5. Nakon storniranja fakture dobavljača možete još jednom kreirati temeljnice ispravaka, obrađivati opozive stavki vremena i stornirati odobravanje izvornog vremena, troškova ili stvarnog materijala.

> [!NOTE]
> Moguće je otkazati samo potvrđene fakture dobavljača projekta. Fakture dobavljača u drugim državama ne mogu se otkazati.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
