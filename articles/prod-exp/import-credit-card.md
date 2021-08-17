---
title: Uvoz i održavanje transakcija kreditnim karticama
description: U ovoj se temi objašnjava način uvoza i održavanja transakcija kreditne kartice povezane s troškovima. Te se transakcije mogu postaviti tako da se automatski uvoze po ponavljajućem rasporedu ili se prema potrebi mogu ručno uvesti.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995842"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Uvoz i održavanje transakcija kreditnim karticama

Transakcije kreditne kartice povezane s troškovima mogu se postaviti tako da se automatski uvoze ponavljajućim rasporedom. Alternativno, transakcije se prema potrebi mogu ručno uvesti. Transakcije kreditnom karticom uvoze se putem entiteta s podacima o transakcijama kreditnim karticama.

Dodatne informacije o entitetima podataka potražite u članku [Entiteti podataka](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Uvoz transakcija kreditnom karticom

1. Na stranici **Transakcije kreditnom karticom** odaberite **Uvoz transakcija**. Ako prvi put otvarate mogućnost upravljanja podacima, sustav mora ažurirati popis podatkovnih entiteta prije nego što nastavite.
2. U polje **Naziv** unesite jedinstveni opis posla koji se uvozi.
3. U polju **Oblik izvornih podataka** odaberite oblik datoteke koja sadrži transakcije kreditnom karticom za uvoz.
4. Odaberite **Prenesi**, a zatim pronađite i odaberite datoteku za uvoz.
5. Nakon što je datoteka prenesena, provjerite valjanost mapiranja datoteke s transakcijama kreditne kartice i stupaca entiteta podataka o transakcijama kreditnom karticom odabirom veze **Prikaz karte** na pločici. Ako postoje pogreške mapiranja ili ako morate promijeniti mapiranje, napravite promjene mapiranja ili iz kartice **Vizualizacija mapiranja** ili iz kartice **Pojedinosti mapiranja**.
6. Kako biste automatizirali transakcije kreditnom karticom, odaberite mogućnost **Stvori posao ponavljajućih podataka**. Tada možete postaviti ponavljanje koje definira učestalost uvoza transakcija kreditnom karticom. Kada dovršite, odaberite **U redu**.
7. Kako biste odmah uvezli odabranu datoteku, odaberite **Uvoz**.
8. Ako se tijekom uvoza pojave pogreške, možete pregledati zapis izvršavanja ili pripremne podatke kako biste vidjeli pogreške koje morate ispraviti kako biste zajamčili uspješan uvoz.

> [!NOTE]
> Ako morate uvesti više oblika datoteke, morate stvoriti zasebne poslove uvoza za svaku vrstu oblika.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponovna dodjela transakcije kreditnom karticom otkazanim zaposlenicima

Nakon prekidanja zapisa o zaposleniku, onemogućen je račun usluge domene Active Directory (AD DS, Active Directory Domain Services) zaposlenika. Međutim, možda postoje aktivne transakcije kreditnom karticom koje se i dalje moraju trošiti i nadoknaditi. Sa stranice **Transakcije kreditnom karticom** možete ponovno dodijeliti zaposlenika za svaku transakciju kreditnom karticom u kojoj je pridruženi zaposlenik otkazan.

Odaberite jednu ili više transakcija kreditnom karticom, a zatim odaberite **Ponovno dodijeli transakcije**. Zatim možete odabrati drugog zaposlenika kojem ćete dodijeliti transakcije kreditnom karticom. Nakon što se transakcije kreditnom karticom ponovno dodijele, mogu se odabrati za izvješće o troškovima i platiti uobičajenim postupkom za nadoknadu prema izvješću o troškovima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]