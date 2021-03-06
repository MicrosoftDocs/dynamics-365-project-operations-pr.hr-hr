---
title: Redci prilike utemeljeni na projektu
description: U ovoj temi nalaze se informacije o načinu rada s redcima prilike koji se temelje na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898387"
---
# <a name="project-based-opportunity-lines"></a>Redci prilike utemeljeni na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


Redci prilike koji se temelje na projektu dostupni su samo u prilikama koje se temelje na projektu. Zapisi prilike koja se temelji na projektu imaju vrijednost polja **Vrsta** postavljenu na **Na temelju rada**.

Redci prilike koji se temelje na projektu stavke su redaka koje će se isporučiti klijentu s pomoću projekta. Međutim, projekt se ne može vezati uz redak prilike koja se temelji na projektu. Projekti se mogu vezati uz stavke retka iz faze **Ponuda** i dalje, jer se prilika obično pojavi u ranoj fazi životnog ciklusa posla. Odluka o tome koliko će se projekata upotrijebiti za isporuku posla klijentu odluka je koja se donosi kasnije, u fazi prodaje. Fazu prilike upotrijebite za identificiranje diskretnih komponenti isporuke klijentu. Odluke u vezi sa stvarnim brojem projekata upotrijebljenih za isporuku ovih komponenti mogu se izbaciti dok se ne sazna više informacija o samom radu.

Ispod su polja na retku prilike koji se temelji na projektu:

| **Polje** | **Mjesto** | **Relevantnost, svrha i smjernice** | **Utjecaj na niže razine** |
| --- | --- | --- | --- |
| Vrsta proizvoda | Kartica općenito (skrivena) | Ovo je polje skupa mogućnosti Ako imate instaliranu aplikaciju Dynamics 365 Operations, **Usluga koja se temelji na projektu** jedna je od dostupnih mogućnosti.  | Vrijednost ovog polja postavljena je na **Usluga koja se temelji na projektu** kada se redak prilike koji se temelji na projektu stvara iz rešetke redaka koji se temelje na projektu na prilici. <br> Ako promijenite ili poništite ovu vrijednost, funkcionalnost projekta neće biti omogućena na stavkama retka koji se temelji na projektu. |
| Prilika | Kartica Općenito | Ovo je polje samo za čitanje i odnosi se na zapis nadređene Prilike kojem pripada ova stavka retka. | Nema utjecaja ovog polja na niže razine. |
| Ime | Kartica Općenito | Ovo je tekstno polje koje se može uređivati i može se upotrebljavati za davanje kratkog identiteta toj stavci retka | Ova se vrijednost prenosi na redak ponude kada iz ove prilike stvarate ponudu |
| Proračun klijenta | Kartica Općenito | Ovo polje valute koje se može uređivati može se upotrebljavati za praćenje iznosa kojeg je kupac spreman potrošiti za ovu stavku retka. | Ova se vrijednost prenosi na odgovarajuće polje na retku ponude kada iz ove prilike stvarate ponudu |
| Način naplate | Kartica Općenito | To polje koje se može uređivati ima sljedeće vrijednosti:</br>- Vrijeme i materijal</br>- Fiksnu cijenu | Ova se vrijednost prenosi na odgovarajuće polje na retku ponude kada iz ove prilike stvarate ponudu. Nakon stvaranja retka ponude, polje se zaključa i ne može se mijenjati. Dodijelite vrijednost ovom polju što je moguće točnije. Ako trebate promijeniti vrijednost ovog polja na retku ponude, izbrišite i ponovno stvorite redak ponude. |
