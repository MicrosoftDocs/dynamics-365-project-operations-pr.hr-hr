---
title: Izmijenjena izvješća o troškovima
description: U ovoj temi nalaze se informacije o izmijenjenom i ponovno osmišljenom iskustvu za unos izvješća o troškovima u aplikaciji Microsoft Dynamics 365 Finance. Novo iskustvo pojednostavljuje postupak popunjavanja izvješća o troškovima i smanjuje potrebno vrijeme.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ec8737d848ae5ad25219a43c68306d19b1c1fbce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073431"
---
# <a name="redesigned-expense-reports"></a>Izmijenjena izvješća o troškovima
[!include[banner](../includes/banner.md)]

Unos izvješća o troškovima izmijenjen je kako bi se pojednostavio postupak popunjavanja izvješća o troškovima i smanjilo vrijeme potrebno za to. Evo glavnih komponenti novog iskustva s troškovima:

- Novi radni prostor za upravljanje troškovima koji vam omogućuje pristup troškovima vašeg delegata.
- Novo iskustvo podudaranja iskustva kako bi se bolje prikazali računi na razini zaglavlja i pojednostavio postupak vezivanja računa za retke troškova.
- Nova rešetka samo je za čitanje i omogućuje vam pregled mnogo više redaka troškova i dodatnih stupaca s podacima. Sada možete vidjeti sve specificirane i podijeljene retke, zajedno s nadređenim troškovima.
- Pojednostavljeno okno za troškove uređivanja.
- Izmijenjene poruke o pogreškama, upozorenjima i pravilima kako bi se zajamčilo da imate točan kontekst radi razumijevanja problema i načina za njegovo rješavanje. Microsoft je uklonio mnoge poruke koje su se prikazivale prije nego što su korisnici imali priliku dovršiti svoje zadatke i riješiti probleme, poput nepotpune poruke o pojedinostima.
- Nova stranica na kojoj se navodi koja polja su nužna za vašu tvrtku ili ustanovu, koja su neobvezna i koja se polja ne trebaju dohvaćati. Ta će stranica pomoći pri smanjivanju broj polja koja korisnici moraju postaviti.
- Novi izgled i dojam izvješća o troškovima, tako da izvješća više ne izgledaju kao da su dizajnirana za računovodstveno osoblje.

Kako biste uključili novo iskustvo, upotrijebite radni prostor **Upravljanje značajkama** za uključivanje značajke **Ponovno osmišljena izvješća o troškovima**. Kada uključite ovu značajku, događaju se sljedeće radnje:

- Postojeći radni prostor troška zamjenjuje se novim radnim prostorom.
- Dodana je nova stavka izbornika za vidljivost polja troška.
- Ne uklanjaju se postojeće stavke izbornika za izvješća o troškovima (postojeća stranica) ili polja izvješća o troškovima.
- Tijekovi rada i sva odobrenja i dalje vas vode na postojeću stranicu izvješća o troškovima.

## <a name="getting-started-video-for-new-users"></a>Videozapis za početnike za nove korisnike

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Iskustvo troškova u videozapisu Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (prikazan gore) uključen je u [popis za reprodukciju aplikacija Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostupno na platformi YouTube.

## <a name="new-features"></a>Nove značajke

| Nova značajka | Opis |
|---|----|
| Vidljivost polja troška | Nova stranica za postavljanje omogućuje vam određivanje polja koja treba onemogućiti za tvrtku ili ustanovu, koja trebaju biti obvezna i koja se preporučuju. |
| Obvezna polja | Nova jednostavna konfiguracija omogućuje vam da napravite neka polja obvezna bez uporabe okvirnih pravila. |
| Neobvezna polja | Dodana je druga stranica za neobvezna polja. Na taj način zaposlenici neće imati dojam kao da moraju postaviti polja, ali su polja i dalje lako dostupna. |
| Dodavanje nepovezanih računa | Mogućnost dodavanja nepovezanih računa u izvješće o troškovima vidljivija je iz radnog prostora i u izvješću o troškovima. |
| Poboljšana razmjena poruka | Bolja je vidljivost redaka troškova koji imaju upozorenja ili pogreške. |
| Smanjivanje broja poruka na traci s porukama| Smanjen je broj poruka informativnog dnevnika, a u mnogim se slučajevima nastojalo spriječiti prikazivanje dupliciranih poruka. |
| Grupirane uobičajenih radnji | Sučelje je očišćeno dodavanjem novog gumba za radnje za većinu uobičajenih radnji na razini retka i dodavanjem gumba s tri točke (...) za zaglavlje i druge rjeđe radnje. |
| Novi radni prostor za povećanje vidljivosti | Novi radni prostor objedinjuje značajke i veze koje korisnicima omogućuju kretanje različitim područjima. |
| Dodavanje postojećih troškova i računa tijekom stvaranja troškova | Kada izrađujete izvješća o troškovima, možete dodati sve ili odabrane troškove i račune. |
| Kalkulator tečaja | Dodan je kalkulator tečaja koji vam omogućuje izračun deviznog tečaja za viševalutne transakcije neposrednih troškova. |
| Spremanje i dodavanje novih redaka troškova | Gumbi **Spremi** i **Novo** dostupni su kada se unose novi troškovi, što vam pomaže pri brzom unosu redaka troškova. |
| Bolja vidljivost unutar razdvojenih i specificiranih redaka | Specificirani i razdvojeni redci dodaju se izravno na popis troškova kako bi se povećala vidljivost i olakšalo utvrđivanje bilo postojanja pogrešaka u pravilima bilo drugih pogrešaka. |
| Prikaz računa tijekom specificiranja | Tijekom specificiranja mogu se prikazati računi. |

Početno izdanje usredotočeno je na scenarije unosa troškova. Svaki scenarij pregleda ili odobrenja izvješća o troškovima i dalje će upotrebljavati postojeću stranicu unosa troškova.

Sljedeće značajke postoje na postojećoj stranici, ali ih još nema na novoj. Te će se značajke ponovno uvesti tijekom sljedećih nekoliko izdanja:

- Odobrenja
- Odobrenja dugovanja i mogućnost uređivanja računovodstva
- Više točki unosa
- Integracija putnog naloga
- Entitet podataka za vidljivost polja troškova
- Ulaz za troškove dnevnice
- Tijek rada na razini retka
- Privremena podrška odobravatelja
- Napredno specificiranje