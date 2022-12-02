---
title: Vrste razdoblja
description: U ovom članku nalaze se informacije o načinu postavljanja vrsta razdoblja za procjenu prihoda.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bbf2dcb4758611aa9d0591ddfec42869f4438c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930953"
---
# <a name="period-types"></a>Vrste razdoblja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Vrsta razdoblja definira koliko se često procjenjuje prihod od projekta. U ovom članku nalaze se informacije o načinu postavljanja vrsta razdoblja za procjenu prihoda. 

## <a name="create-and-work-with-period-types"></a>Stvaranje vrsta razdoblja i rad s njima
Kako biste stvorili vrste razdoblja i radili s njima, poduzmite sljedeće korake:

1. U svom okruženju aplikacije Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Procjene** > **Vrste razdoblja**.
2. Kako biste stvorili novu vrstu razdoblja, odaberite **Novo**. Unesite naziv i opis.
3. U polje **Učestalost** unesite vrijednost:

    - Ako odaberete **Tjedan**, **Dvotjedno**, **Polumjesečno**, **Mjesec**, **Dan**, **Kvartal** ili **Godina**, za generiranje razdoblja upotrebljavat će se kalendar. 
    - Ako odaberete **Računovodstveno razdoblje**, računovodstvena razdoblja iz konfiguracije Glavne knjige upotrijebit će se za generiranje razdoblja.
    - Ako odaberete **Neograničeno**, možete odrediti prilagođena razdoblja.
4. Odaberite zapis vrste razdoblja, a zatim **Generiraj razdoblja** kako biste stvorili razdoblja za vrstu razdoblja. Na temelju učestalosti razdoblja koje ste odabrali, možda ćete moći odrediti datum početka ili broj razdoblja koja treba generirati.
5. Za pregled generiranih razdoblja odaberite **Razdoblja**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]