---
title: Kopiranje ugovora temeljenih na projektu
description: U ovom se članku nalaze informacije o kopiranju projektnih ugovora u microsoftu Dynamics 365 Project Operations.
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
# <a name="copy-project-based-contracts"></a>Kopiranje ugovora temeljenih na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Nove projektne ugovore možete jednostavno stvoriti kopiranjem postojećih ugovora na jedan od dva načina:

- **Na stranici popisa Ugovori o** projektu odaberite ugovor o projektu, a zatim **Kopiraj**.
- Na stranici s pojedinostima **Ugovor o projektu** odaberite **Kopiraj**.

U oba slučaja pojavit će se dijaloški okvir u kojem možete postaviti parametre kopiranog ugovora. Dijaloški okvir sadrži sljedeća polja. Ovisno o vrijednostima koje odaberete, postupak kopiranja može se promijeniti.

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| Tema | Unesite naziv ciljanog ugovora. Kada se dijaloški okvir otvori, sustav postavlja polje na naziv izvornog ugovora, ali mu se dodaje riječ "kopija". | Ovo polje ne utječe na niže razine. |
| klijente | Upućivanje na zapis tvrtke ili računa klijenta. Kada se otvori dijaloški okvir, sustav postavlja polje na račun na izvornom ugovoru. | Ovo polje primarni je klijent u ugovoru. |
| Tvrtka vlasnik | Tvrtka koja je odgovorna za isporuku projekata koji su povezani s ovim poslom. Kada se otvori dijaloški okvir, sustav postavlja polje na poduzeće vlasnika izvornog ugovora. | Vlastita tvrtka je pravna osoba koja će izvršiti projekt nakon zaključenja posla. Valuta vlasnika mora odgovarati valuti ugovorne jedinice. |
| Ugovorna jedinica | Organizacijska jedinica koja je odgovorna za isporuku projekata koji su povezani s ovim poslom. Kada se otvori dijaloški okvir, sustav postavlja polje na jedinicu ugovaranja izvornog ugovora. | Ugovorna jedinica odjel je tvrtke koji će izvršiti projekte nakon zaključenja posla. Svaka ugovorna jedinica ima valutu. Ova se valuta koristi za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom projekta. |
| Valuta | Valuta u kojoj se transakcija posla obavlja. Kada se otvori dijaloški okvir, sustav postavlja polje na valutu izvornog ugovora. Valuta se može promijeniti. Ako jest, **polje Kopiraj cijene** uvijek je postavljeno na **Ne** jer cjenici na izvornom ugovoru više nisu relevantni. | Ova valuta koristi se za zadane cjenike, za generiranje financijskih procjena na ugovoru i za fakturiranje kupcu prilikom dobivanja posla. |
| Zatraženi datum isporuke | Datum isporuke koji je kupac zatražio. | Taj se datum koristi kao završni datum kada stvarate datume fakturiranja na određenoj frekvenciji. |
| Kopiranje cijena | Vrijednost koja pokazuje treba li cijene na ugovoru kopirati iz izvornog ugovora. | Ako je polje postavljeno na **Da**, reference cjenika projekta i proizvoda kopiraju se iz izvornog ugovora u ciljni ugovor. Ako je postavljen na **Ne**, koriste se zadani cjenici na temelju najnovijih cjenika na računu ili parametrima projekta. |

Kada u dijaloškom okviru odaberete **U redu**, sustav stvara kopiju ugovora na temelju vrijednosti parametara koje ste postavili. Tada se otvara novi ugovor.

Sljedeće informacije ne **kopiraju se** iz izvornog ugovora u ciljni ugovor jer su specifične za svaki ugovor:

- Rasporedi fakturiranja
- Klijenti ugovora i retka ugovora
- Referenca projekta na redcima ugovora koji se temelje na projektu
- Podaci o proračunu klijenta

Kopiraju se reci ugovora za projekte i proizvode, procjene u detaljima retka ugovora i vrijednosti koje ne prelaze na razini ugovora. Unos zadanih cijena i cijena troškova ovisi o odabiru u **polju Kopiranje cijena** u dijaloškom okviru Kopiranje **parametara**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
