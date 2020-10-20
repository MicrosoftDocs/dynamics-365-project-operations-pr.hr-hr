---
title: Zaglavlje prilike
description: U ovoj temi nalaze se informacije o ukupnim podacima o poslovima koji se temelje na projektu i redcima prilike koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906103"
---
# <a name="opportunity-header"></a>Zaglavlje prilike

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Zaglavlje Prilike dohvaća ukupne podatke o poslu koji se temelji na projektu i primjenjuje se na sve retke prilike koji se temelji na projektu.

Prilike koje se temelje na projektu u aplikaciji Dynamics 365 Project Operations proširenja su prilika aplikacije Dynamics 365 Sales. Ova proširenja pružaju dodatnu funkcionalnost koja je specifična i potrebna za prilike koje se temelje na projektu. Ta proširenja mogu uključivati nova polja i radnje vrpce dostupne u prilikama koje se temelje na projektu. Možda ćete pronaći neka polja, funkcionalnost i zadanu logiku koja je dostupna u aplikaciji Sales, ali ne i u aplikaciji Project Operations.

Sljedeća tablica uključuje polja u prilici koji se temelji na projektu koja su jedinstvena za aplikaciju Project Operations ili imaju neke bitne promjene u ponašanju iz Prilika u aplikaciji Sales.

| **Polje** | **Mjesto** | **Relevantnost, svrha i smjernice** | **Utjecaj na niže razine** |
| --- | --- | --- | --- |
| Tip | Kartica općenito (skrivena) | Ovo polje skupa mogućnosti ima sljedeće mogućnosti:</br>- Na temelju rada (dostupno samo s aplikacijom Project Operations)</br>- na temelju stavke (dostupno samo kada su instalirane aplikacije Project Operations i Sales)</br>- Temeljeno na servisnom održavanju (dostupno kada se instalira aplikacija Field Service) | Kada upotrebljavate aplikaciju Project Operations, vrijednost ovog polja automatski se postavlja na vrijednost **Na temelju rada** što Priliku klasificira kao priliku koji se temelji na projektu. Za ovaj posao potrebna je prilika koji se temelji na projektu, koja će omogućiti sva proširenja specifična za projekt i funkcionalnost u procesu prodaje prema nižim razinama. |
| Kontakt | Kartica Općenito | Upućivanje na primarni kontakt klijenta za ovaj posao. | |
| Poslovni subjekt | Kartica Općenito | Upućivanje na zapis tvrtke ili računa klijenta. | |
| Voditelj kupaca | Kartica Općenito | Ime upravitelja računa za ovu priliku koji se temelji na projektu. | Voditelj računa odgovoran je za upravljanje odnosom s klijentom kroz dovršetak ovog projekta. Na temelju zapisa resursa koji se može rezervirati vezanog za upravitelja računa, ugovorna je jedinica zadana. |
| Ugovorena jedinica | Kartica Općenito | Organizacijska jedinica koja je odgovorna za isporuku projekta ili projekata povezanih s ovim poslom. | Ugovorna jedinica odjel je tvrtke koji će dovršiti projekt(e) nakon sklapanja posla. Svaka ugovorna jedinica ima valutu i ta se valuta upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom izvršenja projekta. |

Za sva ostala polja i odjeljke na kartici **Sažetak** prilike, pogledajte članak [Stvaranje ili uređivanje prilika (Prodaja i Središte prodaje)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
