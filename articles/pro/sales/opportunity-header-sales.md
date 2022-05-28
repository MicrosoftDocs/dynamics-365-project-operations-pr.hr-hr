---
title: Postavke prilike – jednostavno
description: U ovoj temi nalaze se informacije o poslovima i redcima prilike koji se temelje na projektu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f40154fed5790083e3a4d3264cc9f8cc23ae18bc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596823"
---
# <a name="header-details-for-project-opportunities"></a>Pojedinosti zaglavlja za prilike za projekt

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Zaglavlje Prilike dohvaća ukupne podatke o poslu koji se temelji na projektu i primjenjuje se na sve retke prilike koji se temelji na projektu.

Prilike koje se temelje na projektu u aplikaciji Dynamics 365 Project Operations proširenja su mogućnosti u aplikaciji Dynamics 365 Sales. Ova proširenja pružaju dodatnu funkcionalnost koja je specifična i potrebna za prilike koje se temelje na projektu. Ta proširenja mogu uključivati nova polja i radnje vrpce dostupne u prilikama koje se temelje na projektu. Možda ćete pronaći neka polja, funkcionalnost i zadanu logiku koja je dostupna u aplikaciji Sales, ali ne i u aplikaciji Project Operations.

Sljedeća tablica uključuje polja u prilici koji se temelji na projektu koja su jedinstvena za aplikaciju Project Operations ili imaju neke bitne promjene u ponašanju iz Prilika u aplikaciji Sales.

| **Polje** | **Mjesto** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- | --- |
| Tip | Kartica općenito (skrivena) | Ovo polje skupa mogućnosti ima sljedeće mogućnosti:</br>- Na temelju rada (dostupno samo s aplikacijom Project Operations)</br>- na temelju stavke (dostupno samo kada su instalirane aplikacije Project Operations i Sales)</br>- Temeljeno na servisnom održavanju (dostupno kada se instalira aplikacija Field Service) | Kada upotrebljavate aplikaciju Project Operations, vrijednost ovog polja automatski se postavlja na vrijednost **Na temelju rada** što Priliku klasificira kao priliku koji se temelji na projektu. Za ovaj posao potrebna je prilika koji se temelji na projektu, koja će omogućiti sva proširenja specifična za projekt i funkcionalnost u procesu prodaje prema nižim razinama. |
| Kontakt | Kartica Općenito | Upućivanje na primarni kontakt klijenta za ovaj posao. | |
| Poslovni subjekt | Kartica Općenito | Upućivanje na zapis tvrtke ili računa klijenta. | |
| Voditelj računa | Kartica Općenito | Ime upravitelja računa za ovu priliku koji se temelji na projektu. | Voditelj računa odgovoran je za upravljanje odnosom s klijentom kroz dovršetak ovog projekta. Na temelju zapisa resursa koji se može rezervirati vezanog za upravitelja računa, ugovorna je jedinica zadana. |
| Ugovorena jedinica | Kartica Općenito | Organizacijska jedinica koja je odgovorna za isporuku projekta ili projekata povezanih s ovim poslom. | Ugovorna jedinica odjel je tvrtke koji će dovršiti projekt(e) nakon sklapanja posla. Svaka ugovorna jedinica ima valutu i ta se valuta upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom izvršenja projekta. |

Za sva ostala polja i odjeljke na kartici **Sažetak** prilike, pogledajte članak [Stvaranje ili uređivanje prilika (Prodaja i Središte prodaje)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
