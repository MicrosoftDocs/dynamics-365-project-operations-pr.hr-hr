---
title: Novosti u prosincu 2020. – Osnovna implementacija aplikacije Project Operations – od sklapanja posla do predračuna
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju osnovne implementacije aplikacije Project Operations za prosinac 2020. – od sklapanja posla do predračuna.
author: sigitac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 81a5556e98d333fa86d73b1c7f03245a23a454372168f8bd7c79fc4425387734
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009342"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novosti u prosincu 2020. – Osnovna implementacija aplikacije Project Operations – od sklapanja posla do predračuna

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations na verziji 4.5.0.134 okruženja platforme Dataverse 

U sljedećoj tablici navode se ažuriranja za aplikaciju Project Operations u verziji 4.5.0.134. okruženja platforme Dataverse.

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 1986009 | Ručno stvoreni redci dnevnika imaju nedosljedne performanse kada se potvrde prije nego što se projekt poveže s retkom ugovora ili s njime prekine vezu. |
| Naplata i određivanje cijene | 2014153 | Proizvodi se ne fakturiraju ako se izvršavaju iz rasporeda faktura. |
| Naplata i određivanje cijene | 2014159 | Proizvodi se ne povlače kada se račun osvježi za transakcije. |
| Naplata i određivanje cijene | 2028174 | Ažuriranja pojedinosti retka fakture trebala bi slijediti logiku dnevnika ispravaka. |
| Naplata i određivanje cijene | 2028315 | Popravci ponašanja ugniježđene rešetke koja se može uređivati. |
| Naplata i određivanje cijene | 2031070 | Prilagođavanje pojedinosti retka korektivne fakture mora slijediti logiku dnevnika ispravaka. |
| Naplata i određivanje cijene | 2034186 | Mora biti moguće ažurirati projekt na retku ugovora. |
| Naplata i određivanje cijene | 2034206 | Status prilagodbe mora se postaviti tijekom stvarnog storniranja za vrijeme dok se prekida veza projekta iz retka ugovora. |
| Naplata i određivanje cijene | 2040871 | Ažuriranja ćelija Omogući jedinicu i Grupa jedinica na rešetki Procjene troškova. |
| Naplata i određivanje cijene | 2053754 | Stvarne vrijednosti stvorene iz uređivanja faktura nisu označene statusom prilagodbe i naplate. |
| Naplata i određivanje cijene | 2057874 | Ispravljena veza transakcije stvorena tijekom uređivanja pojedinosti retka fakture. |
| Naplata i određivanje cijene | 2057875 | Ispravni izvori transakcije stvoreni tijekom uređivanja pojedinosti retka fakture. |
| Naplata i određivanje cijene | 2057944 | Stanje koje se ne smije prekoračiti postavljeno je kao Namjensko za stvarne vrijednosti koje nisu spremne za fakturiranje iz ispravka fakture. |
| Naplata i određivanje cijene | 2057963 | Stvaranje podjele\_Proizvodne ovlasti iz Stvaranja\_Ovlast ProjectContract. |
| Naplata i određivanje cijene | 2067622 | Ikona obrade trebala bi se prikazati tijekom stvaranja kontrolnih točaka. |
| Naplata i određivanje cijene | 2067624 | Ugovoreni iznos treba biti označen kao Poslovna preporuka pri stvaranju kontrolnih točaka. |
| Naplata i određivanje cijene | 2086880 | Skrivanje gumba **Prijedlog** na vrpci za retke ponude koji se na temelje na projektu. |
| Implementacija i konfiguracija | 2101152 | Novo okruženje stvoreno s pomoću predloška aplikacije Project Operations iz Centra za administratore aplikacije Power Platform mora izvršiti sve operacije nakon instalacije. |
|   Upravljanje prilikama | 2022204 | Rešetka za naplatu koja se temelji na projektu na kartici **Naplata zadatka**, na stranici **Projekt** treba sakriti rešetku koja se temelji na projektu ako ne postoji redak ponude/ugovora s mogućnošću **Svi zadaci** i obrnuto. |
|   Upravljanje prilikama | 2086601 | Uloge i kategorije koje se deaktiviraju ne smiju se kopirati na popise naplatnih uloga i naplatnih kategorija na redcima ponude i redcima ugovora. |
| Planiranje i praćenje projekta | 1949065 | Vidljivost podataka ispravno radi pri zumiranju od 200 % |
| Planiranje i praćenje projekta | 2046317 | Mogućnost preimenovanja entiteta projekta u aplikaciji Project Operations |
| Planiranje i praćenje projekta | 2057171 | Ažurirana poruka o pogrešci kada je polje **Datum početka projekta** na stranici **Projekt** prazno. |
| Planiranje i praćenje projekta | 2057197 | Procjena kopije retka s referencom zadatka nije podržana. |
| Planiranje i praćenje projekta | 2060687 | Upozorenje o vremenskoj zoni sada nestaje nakon određenog trajanja. |
| Upravljanje resursima | 1832887 | Zadani ID kategorije resursa mora biti statičan kako bi se osiguralo ponavljajuće učitavanje podataka za okruženja aplikacija Dataverse i Finance. |
| Vrijeme i trošak | 2034882 | Gumb **Novo** prikazuje se dvaput na naredbenoj traci za vremenske unose nakon instalacije aplikacije Dynamics 365 Field Service. |
| Vrijeme i trošak | 2056028 | Ažuriranje stranice **Uređivanje vremena** kako bi uključila vremensku traku. |
| Vrijeme i trošak | 1983747 | Grafikon vremenskog unosa prikazuje dodatne podatke. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]