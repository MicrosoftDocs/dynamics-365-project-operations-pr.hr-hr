---
title: Osoblje projekta s ugovornim radnicima i kooperantskim kapacitetom
description: Ovaj tema objašnjava kako se zahtjevi projekta mogu koristiti pomoću ugovornih radnika ili kooperantskih kapaciteta u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903007"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Osoblje projekta s ugovornim radnicima i kooperantskim kapacitetom

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Generički članovi projektnog tima mogu biti zaposleni sa zaposlenicima ili ugovornim radnicima. Prilikom osoblja projekta s ugovornim radnicima možete ograničiti mogućnosti osoblja na određene ugovorne radnike koji su dodijeljeni retku kooperanta. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Traženje zahtjeva za resursima osoblja s ugovornim radnicima koji pripadaju određenoj liniji kooperanta

Da biste potražili zahtjeve i zahtjeve resursa osoblja s ugovornim radnicima koji pripadaju određenoj liniji kooperanta, slijedite ove korake:

1. Stvorite generičkog člana projektnog tima koji upućuje na redak kooperanta i kooperanta.
2. Generirajte potrebu za resursom za ovog generičkog člana projektnog tima pomoću **gumba Generiraj** zahtjeve na podrešetki članova projektnog tima.
3. Odaberite redak člana tima, a zatim **gumb Knjiga** na podrešetki. 
4. Time se otvara ploča rasporeda s kontekstom zahtjeva. Zajedno s drugim atributima kao što su datumi, uloga i polja organizacijske jedinice, filtri ploče rasporeda automatski se popunjavaju i poljima retka dobavljača, kooperanta i kooperanta iz zahtjeva resursa.
5. Sustav traži resurse koji zadovoljavaju kriterije filtriranja i popisuje ih. 
6. Odaberite jedan od filtriranih resursa i rezervirajte resurs za zahtjev. 
7. Član projektnog tima stvara se i ažurira referencama podugovarača i podizvođača. Idite na **Procjene projekata** i odaberite **Ažuriraj cijene da biste vidjeli** ažurirani trošak dodjele resursa. 

> [!NOTE]
> Ažuriranje člana projektnog tima referencom podugovora i retka kooperanta možda neće uvijek biti moguće tijekom rezervacije ako je resurs dodijeljen više redaka kooperanta. Ako sustav ne može ažurirati člana projektnog tima linijom kooperanta i kooperanta, otvorite zapis člana projektnog tima i ručno ažurirajte ta polja tako da procjena financijskih troškova točno odražava trošak kooperanta.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Traženje i zahtjevi u pogledu resursa osoblja s bilo kojim ugovornim radnikom

Da biste potražili zahtjeve za resurse i resurse osoblja s bilo kojim ugovornim radnikom, slijedite ove korake:

1. Stvorite generičkog člana projektnog tima.
2. Generirajte potrebu za resursom za ovog generičkog člana projektnog tima pomoću **gumba Generiraj** zahtjeve na podrešetki članova projektnog tima.
3. Odaberite redak člana tima, a zatim **gumb Knjiga** na podrešetki. 
4. Time se otvara ploča rasporeda s kontekstom zahtjeva. Zajedno s drugim atributima kao što su datumi, uloga i polja organizacijske jedinice, filtri ploče rasporeda automatski se popunjavaju i poljima retka dobavljača, kooperanta i kooperanta iz zahtjeva resursa. Budući da zahtjev nije imao ispunjene vrijednosti redaka kooperanta ili kooperanta, ti će atributi biti prazni u oknu filtra.
5. Sustav traži resurse koji zadovoljavaju kriterije filtriranja i popisuje ih.
6. Ažurirajte **polje Vrsta** radnika u oknu filtra **ugovornom** radniku da biste ograničili pretraživanje na ugovorne radnike. Ažurirajte **dobavljača** u oknu filtra da biste odabrali dobavljača da biste ograničili pretraživanje tako da prikazuje samo ugovorne radnike koji pripadaju određenom poduzeću dobavljača.
7. Odaberite ugovornog radnika s popisa i rezervirajte resurs za zahtjev.
8. Stvara se član projektnog tima. Međutim, član projektnog tima ne ažurira se nijednom linijom kooperanta ili kooperanta te stoga dodjela resursa neće biti skupa pomoću cijena kooperanta. Ručno ažurirajte člana projektnog tima retkom kooperanta i idite na **Procjene projekta** i odaberite **Ažuriraj cijene da biste** vidjeli ažurirani trošak dodjele resursa.

> [!NOTE]
> Članovi projektnog tima koji imaju **vrstu Radnik** kao **ugovorni radnik,** ali nemaju referencu podugovora, označeni su kao **nevažeći u** **rešetki članova projektnog** tima. Ako postoje članovi projektnog tima s tim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja retka kooperanta i kooperanta tako da procjena financijskih troškova točno odražava trošak kooperanta na **kartici** Procjene. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
