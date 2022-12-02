---
title: Zapošljavanje ugovornih radnika i podugovornih kapaciteta na projektu
description: Ovaj članak objašnjava kako se zahtjevi projekta mogu popuniti osobljem korištenjem ugovornih radnika ili podugovorenim kapacitetima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522426"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Zapošljavanje ugovornih radnika i podugovornih kapaciteta na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Generičkim članovima projektnog tima mogu se kao osoblje dodijeliti zaposlenici ili ugovorni radnici. Kada projektu kao osoblje dodjeljujete ugovorne radnike, možete ograničiti svoje mogućnosti dodjeljivanja osoblja na određene ugovorne radnike koji su dodijeljeni retku podugovora. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Traženje zahtjeva za resurse osoblja s ugovornim radnicima koji pripadaju određenom retku podugovora

Za traženje zahtjeva za resurse osoblja s ugovornim radnicima koji pripadaju određenom retku podugovora slijedite ove korake:

1. Stvorite generičkog člana projektnog tima koji se poziva na podugovor i redak podugovora.
2. Generirajte zahtjev za resurs za ovog generičkog člana projektnog tima pomoću gumba **Generiraj zahtjev** na podrešetci članova projektnog tima.
3. Odaberite redak člana tima, a zatim odaberite gumb **Rezerviraj** na podrešetci. 
4. Time se otvara Ploča rasporeda s kontekstom zahtjeva. Zajedno s drugim atributima kao što su polja datumi, uloga i organizacijska jedinica, filtri Ploče rasporeda također se automatski popunjavaju poljima dobavljač, podugovor i redak podugovora iz zahtjeva za resursima.
5. Sustav traži resurse koji zadovoljavaju kriterije filtera i navodi ih. 
6. Odaberite jedan od filtriranih resursa i rezervirajte resurs za zahtjev. 
7. Stvara se član projektnog tima i ažurira se pozivanjima na podugovor i redak podugovora. Otvorite **Procjene projekta** i odaberite **Ažuriraj cijene** da biste vidjeli ažurirani trošak dodjele resursa. 

> [!NOTE]
> Ažuriranje člana projektnog tima pozivanjima na podugovor i redak podugovora i možda neće uvijek biti moguće tijekom rezervacije ako je resurs dodijeljen višestrukim redcima podugovora. Ako sustav ne može ažurirati člana projektnog tima podugovorom i retkom podugovora, otvorite zapis člana projektnog tima i ručno ažurirajte ova polja tako da procjena financijskog troška točno odražava trošak podizvođača.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Traženje i dodjela osoblja zahtjevima za resursima iz redova svih ugovornih radnika

Za traženje i dodjelu osoblja zahtjevima za resursima iz redova svih ugovornih radnika slijedite ove korake:

1. Stvorite generičkog člana projektnog tima.
2. Generirajte zahtjev za resurs za ovog generičkog člana projektnog tima pomoću gumba **Generiraj zahtjev** na podrešetci članova projektnog tima.
3. Odaberite redak člana tima, a zatim odaberite gumb **Rezerviraj** na podrešetci. 
4. Time se otvara Ploča rasporeda s kontekstom zahtjeva. Zajedno s drugim atributima kao što su polja datumi, uloga i organizacijska jedinica, filtri Ploče rasporeda također se automatski popunjavaju poljima dobavljač, podugovor i redak podugovora iz zahtjeva za resursima. Budući da zahtjev nije imao ispunjene vrijednosti podugovora ili retka podugovora, ti će atributi biti prazni u oknu filtra.
5. Sustav traži resurse koji zadovoljavaju kriterije filtera i navodi ih.
6. Ažurirajte polje **Vrsta radnika** u oknu filtra na vrijednost **Ugovorni radnik** radi ograničenja pretrage na ugovorne radnike. Ažurirajte polje **Dobavljač** u oknu filtra za odabir dobavljača kako biste ograničili pretragu na prikaz samo ugovornih radnika koji pripadaju određenoj tvrtki dobavljača.
7. Odaberite ugovornog radnika s popisa i rezervirajte resurs za zahtjev.
8. Stvara se član projektnog tima. Međutim, član projektnog tima nije ažuriran nikakvim podugovorom ili retkom podugovora i stoga dodjela resursa neće biti obračunata korištenjem cijena podugovora. Ručno ažurirajte člana projektnog tima retkom podugovora i otvorite **Procjene projekta** i odaberite **Ažuriraj cijene** da vidite ažurirani trošak dodjele resursa.

> [!NOTE]
> Članovi projektnog tima za koje je stavka **Vrsta radnika** postavljena na **Ugovorni radnik**, no koji nemaju referencu podugovora, nose oznaku **Nevažeće** na rešetki **Članovi projektnog tima**. Ako ima članova projektnog tima s tim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja podugovor i redak podugovora tako da procjena financijskog troška točno odražava trošak podizvođača na kartici **Procjene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
