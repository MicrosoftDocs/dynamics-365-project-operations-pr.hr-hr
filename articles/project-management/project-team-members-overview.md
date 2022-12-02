---
title: Članovi projektnog tima
description: U ovom članku nalaze se informacije o načinu rada s podacima o članu projektnog tima, atributima i planiranju.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3465688fb267f3ab785fcb0d252e8616ac1aa1c8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929297"
---
# <a name="project-team-members"></a>Članovi projektnog tima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Članovi projektnog tima sudionici su projekta koji rade na projektu. Cilj je rešetke članova tima omogućiti popis imenovanih resursa koji su predani angažmanu i generičkih članova tima koji su resursi rezerviranog mjesta i koji će biti zaposleni kasnije.

Voditelj projekta i ostali sudionici projekta iz rešetke članova tima mogu vidjeti tko je posvećen projektu. Mogu i pregledati sažetak svojih rezervacija, planirani rad i pojedinačne dodjele resursa. Rešetka članova tima omogućuje voditeljima projekata definiranje preduvjeta resursa za generičke članove tima i upravljanje rezervacijama postojećih članova tima.

Tablica u nastavku navodi ključne atribute člana projektnog tima.

| Naziv polja          | Opis                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Način dodjele        | Metoda raspodjele koja se upotrebljava za rezerviranje resursa na projektu.                                                                         |
| Vrsta naplate             | Odaberite je li član tima klasificiran kao naplativ.                                                                                                                                       |
| Resurs koji je moguće rezervirati        | Resursi koje je moguće rezervirati odabrani za zamjenu generičkog resursa.                                                                                                                   |
| Status brisanja            | Status brisanja člana tima kako bi se pratilo postoji li zahtjev za brisanje poslan PSS-u i hoće li PSS odgovor poslati uspješno i unutar očekivanog vremenskog okvira. |
| Ukupan rad (sati)     | Ukupan rad člana tima na zadacima.                                                                                                                         |
| Dovršeni rad (sati) | Praćenje rada koji je član tima izvršio na svojim zadacima.                                                                                           |
| Preostali rad (sati) | Praćenje rada koji član tima još nije izvršio na svojim zadacima.                                                                                    |
| Završi                   | Datum završetka članstva resursa u timu.                                                                                                                                            |
| Fiksno rezervirani sati        | Fiksno rezervirani sati člana tima.                                                                                                                                                                |
| Naziv položaja            | Naziv koji se koristi za identificiranje generičkog resursa.                                                                                                                                   |
| Jedinica za resurse          | Organizacijska jedinica resursa koji obavlja posao.                                                                                                                      |
| Odobravatelj projekta         | Odaberite smije li član tima naplativ odobriti vrijeme i troškove.                                                                                                                     |
| Potrebni sati           | Obvezni sati koje za člana tima zahtijevaju preduvjeti člana tima.                                                                                                                       |
| Uloga                     | Uloga koju član tima ispunjava u ovom timu.                                                                                                                                |
| Opis položaja     | Unesite opis uloge ovog člana tima.                                                                                                                             |
| Promjenjivo rezervirani sati        | Sati člana tima koji nisu fiksno rezervirani.                                                                                                                                                                 |
| Početak                    | Datum početka članstva resursa u timu.                                                                                                                                          |

Iz rešetke člana tima mogu se poduzeti sljedeće radnje:

- **Rezervacija**: Za tvrtke ili ustanove koje izvršavaju iskorištavanje metodologije hibridnih rezervacija, radnja rezervacije omogućit će korisnicima rezerviranje imenovanih resursa na temelju zahtjeva za preduvjetima koji se generiraju od generičkog člana tima
- **Generiraj zahtjev**: Ova radnja generira zahtjev.
- **Navedi obrazac**: Omogućuje voditeljima projekata prilagodbu kontura preduvjeta resursa na razini pojedinosti. Voditelji projekata mogu se prilagoditi specifičnim potrebama projekta u slučajevima kada zadana raspodjela ne pristaje.
- **Pošalji zahtjev**: Za tvrtke ili ustanove koje upotrebljavaju metodologiju središnjeg rezerviranja.
- **Uredi**: Atributi člana tima mogu se uređivati, uključujući organizacijsku jedinicu, ulogu i naziv radnog mjesta.
- **Održavaj rezervacije**: Kada je potrebno ažurirati rezervacije resursa, održavanje rezervacija omogućite voditelju projekta da prilagodi:

    - Početak
    - Završetak
    - Raspodjelu ukupnog rada

- **Novi**: Osim dodavanja resursa izravno iz rasporeda, voditelji projekata mogu dodati nove imenovane ili generičke članove tima iz rešetke članova tima.
- **Izbriši**: Odabirom jednog ili više članova tima, voditelj projekta može izbrisati resurse koji više neće sudjelovati u projektu. Brisanje člana tima također će izbrisati sve pridružene dodjele resursa i otkazati sve postojeće rezervacije.


[!INCLUDE[footer-include](../includes/footer-banner.md)]