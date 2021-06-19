---
title: Postavljanje integracije kreditne kartice
description: U ovoj se temi objašnjava način rada s transakcijama kreditnih kartica povezanih s troškovima.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001798"
---
# <a name="set-up-credit-card-integration"></a>Postavljanje integracije kreditne kartice

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Transakcije kreditne kartice povezane s troškovima mogu se postaviti tako da se automatski uvoze ponavljajućim rasporedom. Alternativno, transakcije se prema potrebi mogu ručno uvesti. Transakcije kreditnom karticom uvoze se putem entiteta s podacima o transakcijama kreditnim karticama.

## <a name="import-credit-card-transactions"></a>Uvoz transakcija kreditnom karticom

Kako biste uvezli transakcije kreditnom karticom, slijedite ove korake:

1. Na stranici **Transakcije kreditnom karticom** odaberite **Uvoz transakcija**. Ako prvi put otvarate mogućnost upravljanja podacima, sustav mora ažurirati popis podatkovnih entiteta prije nego što nastavite.
2. U polje **Naziv** unesite jedinstveni opis posla uvoza.
3. U polju **Oblik izvornih podataka** odaberite oblik datoteke koja sadrži transakcije kreditnom karticom za uvoz.
4. Odaberite **Prenesi**, a zatim pronađite i odaberite datoteku za uvoz.
5. Nakon što je datoteka prenesena, provjerite valjanost mapiranja datoteke s transakcijama kreditne kartice i stupaca entiteta podataka o transakcijama kreditnom karticom odabirom veze **Prikaz karte** na pločici. Ako postoje pogreške mapiranja ili ako morate promijeniti mapiranje, napravite promjene mapiranja ili iz kartice **Vizualizacija mapiranja** ili iz kartice **Pojedinosti mapiranja**.
6. Kako biste automatizirali transakcije kreditnom karticom, odaberite mogućnost **Stvori posao ponavljajućih podataka**. Tada možete postaviti ponavljanje koje definira učestalost uvoza transakcija kreditnom karticom. Kada dovršite, odaberite **U redu**.
7. Kako biste odmah uvezli odabranu datoteku, odaberite **Uvoz**.
8. Ako se tijekom uvoza prikažu pogreške, možete pregledati zapisnik izvršenja ili prikazati podatke kako biste vidjeli pogreške koje morate ispraviti kako biste osigurali uspješan uvoz.

> [!NOTE]
> Ako trebate uvesti više datotečnih oblika, morate stvoriti zasebne poslove uvoza za svaku vrstu oblika.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponovna dodjela transakcije kreditnom karticom otkazanim zaposlenicima

Nakon prekidanja zapisa o zaposleniku, onemogućen je račun usluge domene Active Directory (AD DS, Active Directory Domain Services) zaposlenika. Međutim, možda postoje aktivne transakcije kreditnom karticom koje se i dalje moraju trošiti i nadoknaditi. Na stranici **Transakcije kreditnim karticama** možete ponovno dodijeliti zaposlenika za bilo koju transakciju kreditnom karticom s koje je povezani zaposlenik izbrisan.

Odaberite jednu ili više transakcija kreditnom karticom, a zatim odaberite **Ponovno dodijeli transakcije**. Zatim možete odabrati drugog zaposlenika kojem ćete dodijeliti transakcije kreditnom karticom. Nakon što se transakcije kreditnom karticom ponovno dodijele, mogu se odabrati za izvješće o troškovima i platiti uobičajenim postupkom za nadoknadu prema izvješću o troškovima.

## <a name="delete-credit-card-transactions"></a>Brisanje transakcija kreditnom karticom 

Ponekad, nakon uvoza transakcija kreditnom karticom, određene transakcije možda će trebati izbrisati. To će možda trebati učiniti zato što su transakcije duplikati ili što podaci možda nisu točni. Administratori mogu upotrebljavati značajku **„Brisanje transakcija kreditnom karticom”** za odabir i brisanje transakcija kreditnom karticom koje **nisu priložene** izvješću o troškovima. 

1. Idite na **Povremeni zadaci** > **Izbriši transakcije kreditnom karticom**.
2. Odaberite **Filtar** i osigurajte podatke za identifikaciju zapisa koje treba uključiti.
3. Za brisanje zapisa odaberite **U redu**. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
