---
title: Zapošljavanje ugovornih radnika i podugovornih kapaciteta na projektu
description: Ovaj tema objašnjava kako se zahtjevi projekta mogu zapošljavati pomoću ugovornih radnika ili podugovaratelja u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574633"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Zapošljavanje ugovornih radnika i podugovornih kapaciteta na projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Članovi generičkog projektnog tima mogu raditi sa zaposlenicima ili ugovornim radnicima. Kada zapošljavate projekt s ugovornim radnicima, možete ograničiti mogućnosti zapošljavanja na određene ugovorne radnike koji su dodijeljeni liniji podugovaranja. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Traženje zahtjeva za resursima osoblja s ugovornim radnicima koji pripadaju određenoj liniji kooperanta

Da biste tražili zahtjeve i zahtjeve resursa osoblja s ugovornim radnicima koji pripadaju određenoj liniji podugovaranja, slijedite ove korake:

1. Stvorite generičkog člana projektnog tima koji upućuje na liniju podugovaratelja i kooperacije.
2. Generirajte zahtjev za resursom za ovog generičkog člana projektnog tima pomoću gumba **Generiraj zahtjev** u podrešetci članova projektnog tima.
3. Odaberite redak člana tima, a zatim odaberite **gumb Knjiga** u podrešetki. 
4. Time se ploča za raspored otvara kontekstom zahtjeva. Zajedno s drugim atributima kao što su polja datuma, uloge i organizacijske jedinice, filtri Rasporedna ploča također se automatski popunjavaju poljima retka dobavljača, podugovaratelja i kooperacije iz zahtjeva resursa.
5. Sustav traži resurse koji zadovoljavaju kriterije filtriranja i navodi ih. 
6. Odaberite jedan od filtriranih resursa i rezervirajte resurs za zahtjev. 
7. Član projektnog tima stvara se i ažurira referencama kooperanta i redaka podugovaranja. Otvorite **Procjene** projekta i odaberite **Ažuriraj cijene** da biste vidjeli ažurirani trošak dodjele resursa. 

> [!NOTE]
> Ažuriranje člana projektnog tima referencom na redak podugovaratelja i podugovaratelja možda neće uvijek biti moguće tijekom rezervacije ako je resurs dodijeljen više redaka podugovaranja. Ako sustav ne može ažurirati člana projektnog tima kooperantskom i podizvođačkom linijom, otvorite zapis člana projektnog tima i ručno ažurirajte ta polja tako da procjena financijskog troška točno odražava trošak kooperanta.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Traženje i zahtjevi resursa osoblja s bilo kojim ugovornim radnikom

Da biste tražili i zahtjeve resursa osoblja s bilo kojim ugovornim radnikom, slijedite ove korake:

1. Stvorite generičkog člana projektnog tima.
2. Generirajte zahtjev za resursom za ovog generičkog člana projektnog tima pomoću gumba **Generiraj zahtjev** u podrešetci članova projektnog tima.
3. Odaberite redak člana tima, a zatim odaberite **gumb Knjiga** u podrešetki. 
4. Time se ploča za raspored otvara kontekstom zahtjeva. Zajedno s drugim atributima kao što su polja datuma, uloge i organizacijske jedinice, filtri Rasporedna ploča također se automatski popunjavaju poljima retka dobavljača, podugovaratelja i kooperacije iz zahtjeva resursa. Budući da zahtjev nije imao ispunjene vrijednosti retka kooperanta ili kooperanta, ti će atributi biti prazni u oknu filtra.
5. Sustav traži resurse koji zadovoljavaju kriterije filtriranja i navodi ih.
6. **Ažurirajte polje Vrsta** radnika u oknu filtra u Ugovorni radnik **da biste** ograničili pretraživanje na ugovorne radnike. Ažurirajte **dobavljača** u oknu filtra da biste odabrali dobavljača da biste ograničili pretraživanje tako da prikazuje samo ugovorne radnike koji pripadaju određenom poduzeću dobavljača.
7. Odaberite ugovornog radnika s popisa i rezervirajte resurs za zahtjev.
8. Stvara se član projektnog tima. Međutim, član projektnog tima nije ažuriran nijednom linijom podugovaratelja ili podugovaratelja te se stoga dodjela resursa neće koštati pomoću cijena podugovaratelja. Ručno ažurirajte člana projektnog tima retkom kooperanta i idite na **Procjene** projekta i odaberite **Ažuriraj cijene** da biste vidjeli ažurirani trošak dodjele resursa.

> [!NOTE]
> Članovi projektnog tima koji imaju vrstu Radnika kao **ugovorni radnik**, ali nemaju referencu kooperanta, označeni su kao **Nevažeći** u rešetki članova **projektnog** **tima.** Ako postoje članovi projektnog tima s tim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja retka podugovaratelja i podugovaranja tako da procjena financijskog troška točno odražava trošak kooperanta na **kartici Procjene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
