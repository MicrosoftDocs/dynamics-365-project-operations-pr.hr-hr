---
title: Stvaranje ponuda projekta iz prilika
description: U ovoj temi nalaze se informacije o stvaranju ponude projekta iz prilike.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073300"
---
# <a name="create-project-quotes-from-opportunities"></a>Stvaranje ponuda projekta iz prilika

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Ponude se mogu stvoriti iz prilika za projekt na sljedeće načine:

- Iz kartice **Ponude** na stranici **Prilika za projekt**
- Iz tijeka rada postupka prodaje prilike.
- Ažuriranjem reference prilike na postojeću ponudu

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Iz kartice Ponuda na stranici Prilika za projekt

Kako biste stvorili ponudu projekta iz prilike, poduzmite sljedeće korake.

1. Otvorite stranicu **Prilika za ponudu** i odaberite karticu **Ponude**. 
2. Na podrešetki **Ponude** odaberite **+** kako biste stvorili novu ponudu projekta na temelju prilike. Svi redci prilike i povezani cjenici za projekt, kopiraju se iz prilike u novu ponudu.

## <a name="from-the-opportunity-sales-process-flow"></a>Iz tijeka rada postupka prodaje prilike.

Kako biste stvorili ponudu iz tijeka rada postupka prodaje prilike, poduzmite sljedeće korake.

1. U tijeku postupka prodaje prilike otvorite Priliku.
2. Odaberite fazu **Kvalificiran**. 
3. Odaberite mogućnost **Sljedeći** , a zatim odaberite **+ Stvori** kako biste stvorili novu ponudu. Većina podataka na kartici **Sažetak** za ovu novu ponudu zadani su iz prilike. 
4. Unesite sve potrebne podatke koji nedostaju ili, ako je nužno, ažurirajte zadane vrijednosti na kartici **Sažetak**.
5. Odaberite **Spremi**. Nova je ponuda stvorena i povezana s prilikom. Sada možete vidjeti podatke o ponudi na kartici **Ponude** stranice **Prilika**. 

   Postupak prodaje prilike prelazi u sljedeću fazu, **Predloži**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Ažuriranjem reference prilike na postojeću ponudu

Postojeća ponuda može se povezati s prilikom. Poduzmite sljedeće korake za ažuriranje podataka o prilici na postojećoj ponudi.

1. Otvorite stranicu **Ponuda** i odaberite karticu **Sažetak**.
2. U polju **Prilika** odaberite priliku koju želite povezati s ponudom. Ponudu možete vidjeti u rešetki **Ponude** od Prilike. 
3. S pomoću postupka prodaje prilike, prilika se može premjestiti u sljedeću fazu, **Predloži**. 

   Kada premjestite priliku u ovu fazu, možete odabrati ovu ponudu s popisa ponuda povezanih s tom prilikom. Odabir ove ponude označava da s njom napredujete.

   Sve ostale ponude povezane s prilikom i dalje će biti dostupne i aktivne dok se jedna od njih ne prihvati. Postupak prodaje možete vratiti u prethodnu fazu **Kvalificiraj** i odabrati još jednu ponudu s kojom ćete krenuti dalje.
