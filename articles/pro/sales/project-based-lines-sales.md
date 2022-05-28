---
title: Redci prilike koji se temelje na projektu – jednostavno
description: U ovoj temi nalaze se informacije o redcima prilike koji se temelje na projektu. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c0c868aa6c54209c31429278fda19bf925267bce
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596731"
---
# <a name="project-based-opportunity-lines---lite"></a>Redci prilike koji se temelje na projektu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Redci prilike koji se temelje na projektu dostupni su samo u prilikama koje se temelje na projektu. Zapisi prilike koja se temelji na projektu imaju vrijednost polja **Vrsta** postavljenu na **Na temelju rada**.

Redci prilike koji se temelje na projektu stavke su redaka koje će se isporučiti klijentu s pomoću projekta. Međutim, projekt se ne može vezati uz redak prilike koja se temelji na projektu. Projekti se mogu vezati uz stavke retka iz faze **Ponuda** i prema naprijed, jer prilika je obično u ranoj fazi životnog ciklusa posla. Odluka o tome koliko će se projekata upotrijebiti za isporuku posla klijentu odluka je koja se donosi kasnije, u fazi prodaje. Fazu prilike možete upotrijebiti za identificiranje diskretnih komponenti isporuke klijentu. Odluke u vezi sa stvarnim brojem projekata upotrijebljenih za isporuku ovih komponenti mogu se izbaciti dok se ne sazna više informacija o samom radu.

Ispod su polja na retku prilike koji se temelji na projektu:

| **Polje** | **Mjesto** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- | --- |
| Vrsta proizvoda | Kartica općenito (skrivena) | Možete odabrati jednu od sljedećih mogućnosti:</br>- Usluga koja se temelji na projektu (dostupna samo kada se instalira aplikacija Dynamics 365 Project Operations)</br>- Proizvod (dostupno samo kada su instalirane aplikacije Project Operations i Dynamics 365 Sales) | Vrijednost ovog polja postavljena je na **Usluga koja se temelji na projektu** kada se redak prilike koji se temelji na projektu stvara iz rešetke redaka koji se temelje na projektu na prilici. <br> Ako promijenite ili poništite ovu vrijednost, funkcionalnost projekta neće biti omogućena na stavkama retka koji se temelji na projektu. |
| Prilika | Kartica Općenito | Ovo je polje samo za čitanje i odnosi se na zapis nadređene Prilike kojem pripada ova stavka retka. | Iz ovog polja nema utjecaja na niže razine. |
| Ime | Kartica Općenito | Ovo tekstno polje koje se može uređivati može se upotrebljavati za davanje kratkog identiteta stavci retka. | Ova se vrijednost prenosi na redak ponude kada iz ove prilike stvarate ponudu. |
| Proračun klijenta | Kartica Općenito | Ovo polje valute koje se može uređivati može se upotrebljavati za praćenje iznosa kojeg je klijent spreman potrošiti za ovu stavku retka. | Ova se vrijednost prenosi na odgovarajuće polje na retku ponude kada iz ove prilike stvarate ponudu. |
| Način naplate | Kartica Općenito | To polje koje se može uređivati ima sljedeće vrijednosti:</br>- Vrijeme i materijal</br>- Fiksnu cijenu | Ova se vrijednost prenosi na odgovarajuće polje na retku ponude kada iz ove prilike stvarate ponudu. Nakon stvaranja retka ponude, polje se zaključa i ne može se mijenjati. Dodijelite vrijednost ovom polju što je moguće točnije. Ako trebate promijeniti vrijednost ovog polja na retku ponude, izbrišite i ponovno stvorite redak ponude. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]