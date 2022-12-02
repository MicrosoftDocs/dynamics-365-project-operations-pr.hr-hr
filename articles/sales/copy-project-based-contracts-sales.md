---
title: Kopiranje ugovora koji se temelje na projektima
description: U ovom se članku navode informacije o kopiranju ugovora o projektima u sustavu Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410362"
---
# <a name="copy-project-based-contracts"></a>Kopiranje ugovora koji se temelje na projektima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Možete jednostavno izraditi nove ugovore o projektima kopiranjem postojećih ugovora na jedan od dva načina:

- Na stranici s popisom **Ugovori o projektima** odaberite ugovor o projektu, a zatim **Kopiraj**.
- Na stranici s pojedinostima **Ugovor o projektu** odaberite **Kopiraj**.

U oba će se slučaja otvoriti dijaloški okvir u kojem možete odrediti parametre kopiranog ugovora. Dijaloški okvir obuhvaća sljedeća polja. Ovisno o vrijednostima koje odaberete, postupak kopiranja može se promijeniti.

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| Tema | Unesite naziv ciljanog ugovora. Kad se otvori dijaloški okvir, sustav određuje polje prema nazivu izvornog ugovora s time da mu dodaje riječ "kopija". | Ovo polje ne utječe na niže razine. |
| klijente | Upućivanje na zapis tvrtke ili računa klijenta. Kada se otvori dijaloški okvir, sustav će ovo polje odrediti prema računu na izvornom ugovoru. | Ovo polje primarni je klijent u ugovoru. |
| Tvrtka vlasnik | Tvrtka koja je odgovorna za isporuku projekata povezanih s ovim poslom. Kada se otvori dijaloški okvir, sustav će ovo polje odrediti prema tvrtki vlasnici na izvornom ugovoru. | Tvrtka vlasnica je pravna osoba koja će izvršiti projekte nakon zaključenja posla. Valuta tvrtke vlasnice mora se podudarati s valutom ugovorne jedinice. |
| Ugovorna jedinica | Organizacijska jedinica koja je odgovorna za isporuku projekata povezanih s ovim poslom. Kada se otvori dijaloški okvir, sustav će polje odrediti prema ugovornoj jedinici na izvornom ugovoru. | Ugovorna jedinica odjel je tvrtke koji će izvršiti projekte nakon zaključenja posla. Svaka ugovorna jedinica ima valutu. Ta valuta upotrebljava se za izvješćivanje o procijenjenim i stvarnim troškovima koji nastanu tijekom projekta. |
| Valuta | Valuta u kojoj se transakcija posla obavlja. Kad se otvori dijaloški okvir, sustav će polje odrediti prema valuti izvornog ugovora. Valuta se može promijeniti. Ako jest, polje **Kopiraj cijenu** uvijek je postavljeno na **Ne** jer cjenici na izvornom ugovoru više nisu relevantni. | Ova se valuta upotrebljava za zadane cjenike, za izradu financijskih procjena za ugovor i za fakturiranje klijentu kada se posao dobije. |
| Zatraženi datum isporuke | Datum isporuke koji je klijent tražio. | Taj datum upotrebljava se kao datum završetka tijekom izrade datuma za fakturiranje pri određenoj učestalosti. |
| Kopiranje cijena | Vrijednost koja označava treba li cijenu na ugovoru kopirati iz izvornog ugovora. | Ako je polje postavljeno na **Da**, referentni cjenik projekta i proizvoda kopiraju se iz izvornog ugovora u ciljani ugovor. Ako je postavljeno na **Ne**, upotrebljavaju se zadani cjenici temeljeni na najnovijim cjenicima u parametrima računa ili projekta. |

Kad u dijaloškom okviru odaberete **U redu**, sustav izrađuje kopiju ugovora na temelju vrijednosti parametara koje ste odredili. Potom se otvara novi ugovor.

Sljedeći podaci se **ne** kopiraju iz izvornog ugovora u ciljni ugovor jer su specifični za svaki ugovor:

- Rasporedi fakturiranja
- Klijenti ugovora i retka ugovora
- Referenca projekta na redcima ugovora koji se temelje na projektu
- Podaci o proračunu klijenta

Kopiraju se redci ugovora za projekte i proizvode, procjene u pojedinostima redaka ugovora i vrijednosti koje ne smiju premašiti na razini ugovora. Unos zadanih cijena i stopa troškova ovisi o odabiru u polju **Kopiraj cijene** u dijaloškom okviru **Kopiraj parametre**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
