---
title: Što je novo u lipnju 2022. – implementacija osnovne aplikacije Project Operations
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju osnovne implementacije aplikacije Microsoft Dynamics 365 Project Operations iz lipnja 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031184"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Što je novo u lipnju 2022. – implementacija osnovne aplikacije Project Operations

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.43.0.77 ili 4.43.0.119

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Podugovaranje | 2708885 | Ispravljena je poruka o pogrešci koja se pojavljuje kada korisnik kreira zapis zaglavlja rezervacije resursa koji se može rezervirati gdje nije popunjen nijedan resurs koji se može rezervirati. |
| Planiranje i praćenje projekta | 2629441 | Ispravljena je logika pokretanja tijeka rada kako bi se spriječila beskonačna petlja kada se projektni zadaci ažuriraju. |
| Vrijeme i trošak | 2641209 | Uvozi vremenskih unosa iz dodjela/rezervacija moraju zadržati referencu resursa koji se može rezervirati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti zaštićeno.|
| Planiranje i praćenje projekta | 2653145 | Dodane su provjere valjanosti kako bi se osiguralo da se ne može stvoriti zapis projekta koji u nazivu ima nevažeće znakove. |
| Vrijeme i trošak | 2654710 | Ispravljeno je filtriranje na stranici **Odobrenja**. |
| Naplata i određivanje cijene | 2667805 | Dodane su provjere valjanosti kako bi se spriječilo stvaranje stvarnih vrijednosti naplaćene prodaje ako ne postoje pozadinske stvarne vrijednosti nenaplaćene prodaje. |
| Naplata i određivanje cijene | 2668378 | Dodane su provjere valjanosti kako bi se spriječilo dodavanje prilagođene dimenzije cijena osim ako su popunjeni naziv logike i naziv polja. |
| Vrijeme i trošak | 2700428 | Poboljšana je logika odobrenja kako bi se osiguralo da se drugi skupovi odobrenja za projekt mogu obraditi čak i ako je jedan od skupova odobrenja zapeo u poslovima sustava. |
