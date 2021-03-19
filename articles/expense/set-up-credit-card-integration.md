---
title: Postavljanje integracije kreditne kartice
description: U ovoj se temi objašnjava način uvoza i održavanja transakcija kreditne kartice povezane s troškovima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276159"
---
# <a name="set-up-credit-card-integration"></a>Postavljanje integracije kreditne kartice

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Transakcije kreditne kartice povezane s troškovima mogu se postaviti tako da se automatski uvoze ponavljajućim rasporedom. Alternativno, transakcije se prema potrebi mogu ručno uvesti. Transakcije kreditnom karticom uvoze se putem entiteta s podacima o transakcijama kreditnim karticama.

## <a name="import-credit-card-transactions"></a>Uvoz transakcija kreditnom karticom

1. Na stranici **Transakcije kreditnom karticom** odaberite **Uvoz transakcija**. Ako prvi put otvarate mogućnost upravljanja podacima, sustav mora ažurirati popis podatkovnih entiteta prije nego što nastavite.
2. U polje **Naziv** unesite jedinstveni opis posla koji se uvozi.
3. U polju **Oblik izvornih podataka** odaberite oblik datoteke koja sadrži transakcije kreditnom karticom za uvoz.
4. Odaberite **Prenesi**, a zatim pronađite i odaberite datoteku za uvoz.
5. Nakon što je datoteka prenesena, provjerite valjanost mapiranja datoteke s transakcijama kreditne kartice i stupaca entiteta podataka o transakcijama kreditnom karticom odabirom veze **Prikaz karte** na pločici. Ako postoje pogreške mapiranja ili ako morate promijeniti mapiranje, napravite promjene mapiranja ili iz kartice **Vizualizacija mapiranja** ili iz kartice **Pojedinosti mapiranja**.
6. Kako biste automatizirali transakcije kreditnom karticom, odaberite mogućnost **Stvori posao ponavljajućih podataka**. Tada možete postaviti ponavljanje koje definira učestalost uvoza transakcija kreditnom karticom. Kada dovršite, odaberite **U redu**.
7. Kako biste odmah uvezli odabranu datoteku, odaberite **Uvoz**.
8. Ako se tijekom uvoza pojave pogreške, možete pregledati zapis izvršavanja ili podatke o fazama kako biste vidjeli pogreške koje morate ispraviti kako biste zajamčili uspješan uvoz.

> [!NOTE]
> Ako morate uvesti više oblika datoteke, morate stvoriti zasebne poslove uvoza za svaku vrstu oblika.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponovna dodjela transakcije kreditnom karticom otkazanim zaposlenicima

Nakon prekidanja zapisa o zaposleniku, onemogućen je račun usluge domene Active Directory (AD DS, Active Directory Domain Services) zaposlenika. Međutim, možda postoje aktivne transakcije kreditnom karticom koje se i dalje moraju trošiti i nadoknaditi. Sa stranice **Transakcije kreditnom karticom** možete ponovno dodijeliti zaposlenika za svaku transakciju kreditnom karticom u kojoj je pridruženi zaposlenik otkazan.

Odaberite jednu ili više transakcija kreditnom karticom, a zatim odaberite **Ponovno dodijeli transakcije**. Zatim možete odabrati drugog zaposlenika kojem ćete dodijeliti transakcije kreditnom karticom. Nakon što se transakcije kreditnom karticom ponovno dodijele, mogu se odabrati za izvješće o troškovima i platiti uobičajenim postupkom za nadoknadu prema izvješću o troškovima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]