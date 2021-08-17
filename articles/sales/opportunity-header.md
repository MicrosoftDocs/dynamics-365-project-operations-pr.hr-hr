---
title: Zaglavlje/sažetak prilike
description: U ovoj temi nalaze se informacije o poslovima koji se temelje na projektu i redcima prilike koji se temelje na projektu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 83a47502112a4862fa7b99a7821c82730e0de0938cabe65b0dd4fc382bdd5515
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996382"
---
# <a name="header-details-for-project-based-opportunities"></a>Pojedinosti zaglavlja za prilike koje se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


Zaglavlje Prilike, ili sažetak, dohvaća ukupne podatke o poslu koji se temelji na projektu i primjenjuje se na sve retke prilike koja se temelji na projektu.

Prilike koje se temelje na projektu u aplikaciji Dynamics 365 Project Operations proširenja su mogućnosti u aplikaciji Dynamics 365 Sales. Ova proširenja pružaju dodatnu funkcionalnost koja je specifična i potrebna za prilike koje se temelje na projektu. Ta proširenja mogu uključivati nova polja i radnje vrpce dostupne u prilikama koje se temelje na projektu. Možda ćete pronaći neka polja, funkcionalnost i zadanu logiku koja je dostupna u aplikaciji Sales, ali ne i u aplikaciji Project Operations.

Sljedeća tablica uključuje polja u prilici koji se temelji na projektu koja su jedinstvena za aplikaciju Project Operations ili imaju neke bitne promjene u ponašanju iz Prilika u aplikaciji Sales.

| **Polje** | **Mjesto** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- | --- |
| Tip | Kartica općenito (skrivena) | Ovo polje skupa mogućnosti ima sljedeće mogućnosti:</br>- Na temelju rada (dostupno samo s aplikacijom Project Operations)</br>- na temelju stavke (dostupno samo kada su instalirane aplikacije Project Operations i Sales)</br>- Temeljeno na servisnom održavanju (dostupno kada se instalira aplikacija Field Service) | Kada upotrebljavate aplikaciju Project Operations, vrijednost ovog polja automatski se postavlja na vrijednost **Na temelju rada** što Priliku klasificira kao priliku koji se temelji na projektu. Za ovaj posao potrebna je prilika koji se temelji na projektu, koja će omogućiti sva proširenja specifična za projekt i funkcionalnost u procesu prodaje prema nižim razinama. |
| Tvrtka vlasnik | Kartica Općenito | Ovo je tvrtka ili pravna osoba koja će klijentu isporučiti projekt. | Podaci o ovom polju kopirat će se u odgovarajuće polje na ponudi projekta koja je stvorena iz ove Prilike. |
| Kontakt | Kartica Općenito | Upućivanje na primarni kontakt klijenta za ovaj posao. | |
| Poslovni subjekt | Kartica Općenito | Upućivanje na zapis tvrtke ili računa klijenta. | |
| Voditelj računa | Kartica Općenito | Ime upravitelja računa za ovu priliku koji se temelji na projektu. | Voditelj računa odgovoran je za upravljanje odnosom s klijentom kroz dovršetak ovog projekta. Na temelju zapisa resursa koji se može rezervirati vezanog za upravitelja računa, ugovorna je jedinica zadana. |
| Ugovorena jedinica | Kartica Općenito | Organizacijska jedinica koja je odgovorna za isporuku projekta ili projekata povezanih s ovim poslom. | Ugovorna jedinica odjel je tvrtke koji će dovršiti projekt(e) nakon sklapanja posla. Svaka ugovorna jedinica ima valutu i ta se valuta upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom izvršenja projekta. |

Za sva ostala polja i odjeljke na kartici **Sažetak** prilike, pogledajte članak [Stvaranje ili uređivanje prilika (Prodaja i Središte prodaje)](/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
