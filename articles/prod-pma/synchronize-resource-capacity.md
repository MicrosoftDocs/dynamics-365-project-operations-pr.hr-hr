---
title: Sinkroniziranje kapaciteta resursa
description: U ovoj temi nalaze se informacije o načinu sinkronizacije kapaciteta resursa u kalendarima i projektima.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073366"
---
# <a name="synchronize-resource-capacity"></a>Sinkroniziranje kapaciteta resursa

[!include [banner](../includes/banner.md)]

Postupci sinkronizacije resursa pomažu kako bi se zajamčilo da se informacije za kalendar i osnovni kalendar slijevaju u planiranje resursa projekta. Ako se kalendar promijeni, postupci izvršavaju potrebna ažuriranja u planiranju projektnih resursa. Postupci također pomažu pri poboljšanju izvedbe jer se podaci o resursima kalendara unaprijed sinkroniziraju. Stoga se ažuriranja podataka o rasporedu resursa događaju brže. Preporučujemo da postupke planirate kao skupne, umjesto jednog po jednog. U suprotnom postoji opasnost da će netko zaboraviti uključene datume nakon posljednjeg sinkroniziranja podataka. Ako se ne upotrebljavaju uključeni datumi, može doći do praznina tijekom sinkronizacije datuma.

![Sinkronizacijski kalendara](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sinkronizacija skupnih vrijednosti kapaciteta resursa

Postupak sinkronizacije osmišljen je za sinkronizaciju svih podataka kalendara resursa. Te informacije uključuju osnovne podatke kalendara o svim promjenama u tablici kapaciteta kalendara resursa projekta. Ako se u projekt dodaju novi resursi, sinkronizacija pomaže zajamčiti dostupnost ažuriranih podataka kalendara. Ova se sinkronizacija može izvršiti u bilo kojem trenutku.

Preporučujemo da upotrijebite skupinu. Tijekom sinkronizacije rezervacija kapaciteta dostupne su mogućnosti.

1. Odaberite **Upravljanje projektima i računovodstvo** &gt; **Povremeno** &gt; **Sinkronizacija kapaciteta** &gt; **Sinkroniziraj skupnih vrijednosti kapaciteta resursa**.
2. Postavite mogućnosti u sljedeću tablicu.

    | Mogućnost      | Opis |
    |-------------|-------------|
    | Šifra razdoblja | Po želji odaberite šifru intervala datuma glavne knjige kako biste postavili datume početka i završetka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa. |
    | Datum početka  | Unesite datum početka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa. |
    | Datum završetka    | Unesite datum završetka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa. |

[![Postupak sinkronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)