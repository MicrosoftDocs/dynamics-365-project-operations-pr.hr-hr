---
title: Redci prilike koji se temelje na projektu (Pro)
description: U ovoj temi nalaze se informacije o redcima prilike koji se temelje na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073313"
---
# <a name="project-based-opportunity-lines-pro"></a>Redci prilike koji se temelje na projektu (Pro)

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Redci prilike koji se temelje na projektu dostupni su samo u prilikama koje se temelje na projektu. Zapisi prilike koja se temelji na projektu imaju vrijednost polja **Vrsta** postavljenu na **Na temelju rada**.

Redci prilike koji se temelje na projektu stavke su redaka koje će se isporučiti klijentu s pomoću projekta. Međutim, projekt se ne može vezati uz redak prilike koja se temelji na projektu. Projekti se mogu vezati uz stavke retka iz faze **Ponuda** i prema naprijed, jer prilika je obično u ranoj fazi životnog ciklusa posla. Odluka o tome koliko će se projekata upotrijebiti za isporuku posla klijentu odluka je koja se donosi kasnije, u fazi prodaje. Fazu prilike možete upotrijebiti za identificiranje diskretnih komponenti isporuke klijentu. Odluke u vezi sa stvarnim brojem projekata upotrijebljenih za isporuku ovih komponenti mogu se izbaciti dok se ne sazna više informacija o samom radu.

Ispod su polja na retku prilike koji se temelji na projektu:

| **Polje** | **Mjesto** | **Relevantnost, svrha i smjernice** | **Utjecaj na niže razine** |
| --- | --- | --- | --- |
| Vrsta proizvoda | Kartica općenito (skrivena) | Možete odabrati jednu od sljedećih mogućnosti:</br>– Usluga koja se temelji na projektu (dostupno samo kada je instalirana aplikacija Dynamics 365 Project Operations)</br>– Proizvod (dostupno samo kada su instalirane aplikacije Project Operations i Dynamics 365 Sales) | Vrijednost ovog polja postavljena je na **Usluga koja se temelji na projektu** kada se redak prilike koji se temelji na projektu stvara iz rešetke redaka koji se temelje na projektu na prilici. <br> Ako promijenite ili poništite ovu vrijednost, funkcionalnost projekta neće biti omogućena na stavkama retka koji se temelji na projektu. |
| Prilika | Kartica Općenito | Ovo je polje samo za čitanje i odnosi se na zapis nadređene Prilike kojem pripada ova stavka retka. | Iz ovog polja nema utjecaja na niže razine. |
| Ime | Kartica Općenito | Ovo tekstno polje koje se može uređivati može se upotrebljavati za davanje kratkog identiteta stavci retka. | Ova se vrijednost prenosi na redak ponude kada iz ove prilike stvarate ponudu. |
| Proračun klijenta | Kartica Općenito | Ovo polje valute koje se može uređivati može se upotrebljavati za praćenje iznosa kojeg je kupac spreman potrošiti za ovu stavku retka. | Ova se vrijednost prenosi na odgovarajuće polje na retku ponude kada iz ove prilike stvarate ponudu. |
| Način naplate | Kartica Općenito | To polje koje se može uređivati ima sljedeće vrijednosti:</br>– Vrijeme i materijal</br>– Fiksnu cijenu | Ova se vrijednost prenosi na odgovarajuće polje na retku ponude kada iz ove prilike stvarate ponudu. Nakon stvaranja retka ponude, polje se zaključa i ne može se mijenjati. Dodijelite vrijednost ovom polju što je moguće točnije. Ako trebate promijeniti vrijednost ovog polja na retku ponude, izbrišite i ponovno stvorite redak ponude. |
