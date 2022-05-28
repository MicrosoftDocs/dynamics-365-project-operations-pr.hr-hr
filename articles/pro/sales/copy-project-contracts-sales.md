---
title: Kopiranje ugovora o projektu – jednostavno
description: U ovoj temi nalaze se informacije o kopiranju ugovora o projektima u aplikaciji Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 082cd6597a066f6dac8a7583a377d8e34bc74e2e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594063"
---
# <a name="copy-project-contracts---lite"></a>Kopiranje ugovora o projektu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Možete jednostavno stvoriti nove ugovore o projektu kopiranjem postojećih ugovora na jedan od dva načina: 

  - Na stranici s popisom **Ugovori o projektima** odaberite ugovor o projektu i odaberite **Kopiraj**.
  - Na stranici s pojedinostima **Ugovor o projektu** odaberite **Kopiraj**.

Otvorit će se dijaloška stranica na kojoj možete odabrati parametre za kopiranje ugovora. Dijaloški okvir obuhvaća sljedeća polja. Ovisno vrijednostima odabranim u tom dijaloškom okviru, postupak kopiranja može se promijeniti.

| **Polje** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- |
| Tema | Unesite naziv ciljanog ugovora. Kad se otvori dijaloška stranica, sustav će to polje postaviti na naziv izvornog ugovora sa stavkom **–kopija** dodanom uz njega. | Ovo polje ne utječe na niže razine. |
| Klijent | Upućivanje na zapis tvrtke ili računa klijenta. Kada se otvori dijaloški okvir, sustav će ovo polje postaviti na račun na izvornom ugovoru. | Ovo polje primarni je klijent u ugovoru. |
| Ugovorena jedinica | Organizacijska jedinica koja je odgovorna za isporuku projekata povezanih s ovim poslom. Kad se otvori dijaloška stranica, sustav će ga postaviti na ugovornu jedinicu izvornog ugovora. | Ugovorna jedinica odjel je tvrtke koji će izvršiti projekte nakon zaključenja posla. Svaka ugovorna jedinica ima valutu. Ta valuta upotrebljava se za izvješćivanje o procijenjenim i stvarnim troškovima koji su nastali tijekom projekta. |
| Valuta | Valuta u kojoj se transakcija posla obavlja. Kad se otvori dijaloška stranica, sustav će polje postaviti na valutu izvornog ugovora. Valuta se može promijeniti. Ako jest, polje **Kopiraj cijenu** uvijek je postavljeno na **Ne** jer cjenici na izvornom ugovoru više nisu relevantni. | Valuta se upotrebljava za zadane cjenike, za izradu financijskih procjena za ugovor i za fakturiranje klijentu kada se posao dobije. |
| Zatraženi datum dostave | Datum isporuke koji je tražio klijent. | Taj datum upotrebljava se kao datum završetka tijekom stvaranja datuma za fakturiranje uz određenu učestalost. |
| Kopiranje cijena | Označava treba li cijenu na ugovoru kopirati iz izvornog ugovora. | Ako je polje postavljeno na **Da**, referentni cjenik projekta i proizvoda kopiraju se iz izvornog u ciljani ugovor. Ako se odabere **Ne**, zadani cjenici temelje se na posljednjim cjenicima parametara računa ili projekta. |

Kad na dijaloškoj stranici odaberete **U redu**, sustav stvara kopiju ugovora na temelju odabranih parametara. Otvorit će se novi ugovor.

Sljedeće se informacije ne kopiraju iz **Izvora** u **Ciljani ugovor**:

  - Rasporedi fakturiranja
  - Klijenti ugovora i retka ugovora
  - Referenca projekta na redcima ugovora koji se temelje na projektu
  - Podaci o proračunu klijenta

Budući da su ovi podaci vrlo specifični za svaki ugovor, ta se polja i zapisi ne kopiraju. Kopiraju se redci ugovora za projekte i proizvode, procjene za pojedinosti redaka ugovora i vrijednosti koje ne smiju premašiti na razini ugovora. Zadavanje cijene i koštanja troška ovise o odabiru u polju **Kopiraj cijene** na dijaloškoj stranici **Kopiraj parametre**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]