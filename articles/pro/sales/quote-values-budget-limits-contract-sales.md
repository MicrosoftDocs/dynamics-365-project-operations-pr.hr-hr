---
title: Sažeti podaci i ponuda projekta (prodaja)
description: U ovoj temi nalaze se informacije o podacima i postavkama koje se primjenjuju na ponude projekata i utječu na njih. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d050258ae457bb4392d5fa761442cfc7a444feb0
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966749"
---
# <a name="summary-information-on-a-project-quote-sales"></a>Sažeti podaci i ponuda projekta (prodaja)

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Ovaj članak pojašnjava informacije koje se primjenjuju na ponudu projekta. To uključuje postavke koje utječu na sve retke ponude i informacije o ponudi koje su sažete u svim stavkama retka za pokretanje KPI-jeva ponude projekta.

Sljedeća tablica navodi sažeta informacijska polja na ponudi projekta koja su jedinstvena za aplikaciju Dynamics 365 Project Operations ili imaju neke važne promjene u ponašanju iz ponuda u aplikaciji Dynamics 365 Sales.

| **Polje** | **Mjesto** | **Relevantnost, svrha i smjernice** | **Utjecaj na niže razine** |
| --- | --- | --- | --- |
| Tip | Kartica sažetka (skrivena) | Ovo polje skupa mogućnosti ima sljedeće mogućnosti:</br>- na temelju rada (dostupno samo kada je instalirana aplikacija Project Operations)</br>- na temelju stavke (dostupno samo kada su instalirane aplikacije Project Operations i Sales)</br>- Temeljeno na servisnom održavanju (dostupno kada se instalira aplikacija Dynamics 365 Field Service) | Kada upotrebljavate aplikaciju Project Operations, vrijednost ovog polja automatski se postavlja na vrijednost **Na temelju rada**. Ovo klasificira ponudu kao ponudu koji se temelji na projektu. Ponuda bi se trebala temeljiti na projektu kako bi se omogućila sva proširenja i funkcionalnosti specifične za projekt. |
| Potencijalni klijent | Kartica sažetka | Upućivanje na zapis tvrtke ili računa klijenta. Kada je ponuda stvorena iz prilike, ovo se polje kopira iz odgovarajućeg polja u prilici. | Valuta na ponudi projekta zadana je na temelju valute klijenta. No, to se može promijeniti prije nego što se ponuda spremi. |
| Voditelj kupaca | Kartica sažetka | Naziv upravitelja računa za ovaj posao. Kada je ponuda stvorena iz prilike, ovo se polje kopira iz odgovarajućeg polja u prilici. | Voditelj računa odgovoran je za upravljanje odnosom s klijentom kroz dovršetak ovog projekta. Na temelju zapisa resursa koji se može rezervirati vezanog za upravitelja računa, ugovorna jedinica zadana je u ponudi projekta. |
| Ugovorena jedinica | Kartica sažetka | Organizacijska jedinica koja je odgovorna za isporuku projekta ili projekata povezanih s ovom ponudom. Kada je ponuda stvorena iz prilike, ovo se polje kopira iz odgovarajućeg polja u prilici. | Ugovorna jedinica odjel je tvrtke koji će izvršiti projekte nakon zaključenja posla. Svaka ugovorna jedinica ima valutu i ta se valuta upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom izvršenja projekta. |
| Cjenik proizvoda | Kartica sažetka | Ovo je cjenik koji se upotrebljava za zadavanje cijena na redcima ponude koji se temelje na proizvodu. Popis mogućnosti za ovo polje prikazuje popis cjenika na kojima se valuta cjenika podudara s valutom ponude. Kada je ponuda stvorena iz prilike, ovo se polje kopira iz odgovarajućeg polja u prilici. Ovo polje na prilici zadano je iz zapisa računa, ali se može promijeniti. | Kada se ponuda prihvati, vrijednost polja kopira se u redak stvorenog ugovora o projektu. |
| Valuta | Kartica sažetka | Ovo ukazuje na valutu koja će se upotrebljavati za izvješćivanje o vrijednosti ovog posla. To je također valuta u kojoj će se klijentu fakturirati ako se posao dobije. Kada je ponuda stvorena iz prilike, ovo se polje kopira iz odgovarajućeg polja u prilici. Ovo polje na prilici zadano je iz zapisa računa, ali ga korisnik može promijeniti. | Nakon spremanja ponude, ovo se polje više ne može uređivati. To se upotrebljava za zadavanje cjenika proizvoda i projekata u ponudi. Valuta na ponudi upotrebljava se za podudaranje s valutom na cjeniku. |
| Ograničenje koje se ne smije prekoračiti | Kartica sažetka | To ukazuje na ugovoreno ograničenje konačne vrijednosti na koje kupac pristaje za ovaj posao. | Ovo se ograničenje procjenjuje tijekom izvršenja i primjenjivo je na sve stavke i projekte povezane s ovom poslom. |
| Traženi datum isporuke | Kartica sažetka | Kada je ponuda stvorena iz prilike, ovo se polje kopira iz odgovarajućeg polja u prilici. | Taj datum upotrebljava se kao datum završetka za generiranje rasporeda računa. |

Ispod su kartice i KPI-ji dostupni na ponudi projekta koji su jedinstveni za aplikaciju Project Operations ili imaju neke važne promjene u ponašanju iz ponuda u aplikaciji Sales:

| **Polje** | **Mjesto** | **Relevantnost, svrha i smjernice** |
| --- | --- | --- |
| Analiza profitabilnosti | Kartica na ponudi | Kartica prikazuje sljedeće mjerne podatke:</br>- Ukupan naplativi trošak</br></br>- Ukupan nenaplativi trošak</br>- Ukupni prihod</br>- Ukupan prihod (osnovni)</br>- Bruto maržu</br>- Prilagođenu bruto maržu|
| Usporedba s očekivanjima klijenta | Kartica na ponudi | Ova kartica prikazuje sljedeće mjerne podatke:</br>- Očekivani rok završetka</br>- Traženi rok završetka</br>- Proračun klijenta</br>- Vrijednost ponude |
| Analiza ponude | Kartica na ponudi | Ova kartica sažima sljedeće najvažnije KPI-je za ponudu projekta</br>- Usporedba s očekivanjima klijenta za proračun i raspored</br>- Bruto maržu</br>- Prilagođenu bruto maržu |
