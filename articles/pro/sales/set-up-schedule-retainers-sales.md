---
title: Postavljanje rasporeda akontacija
description: U ovoj temi nalaze se informacije o načinu postavljanja rasporeda akontacija u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596363"
---
# <a name="set-up-a-retainer-schedule"></a>Postavljanje rasporeda akontacija

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Rasporedi akontacija postavljeni su na stranici **Ugovor o projektu** u aplikaciji Dynamics 365 Project Operations.

1. Na stranici **Ugovor o projektu**, na kartici **Predujmovi i akontacije** odaberite **Postavi raspored akontacija**.
2. Na dijaloškoj stranici koja se otvori prikazana su polja navedena u sljedećoj tablici. Tablica daje predodžbu o tome kako unesene vrijednosti utječu ili djeluju na raspored akontacija koji će se stvoriti.

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| Klijent ugovora projekta | Klijent na ugovoru kojem će se fakturirati za ovu akontaciju ili predujam. | Ako imate više klijenata na ugovoru i ako trebate fakturirati svakom od njih za određeni iznos akontacije ili predujma, ručno stvorite po jednu fakturu za svakog klijenta. |
| Početak rasporeda akontacija | Unesite datum početka rasporeda akontacija. | Ovaj datum ne mora biti datum kada je stvorena prva akontacija ili predujam. Na datum stvaranja prve akontacije ili predujma utječe i učestalost faktura. |
| Završetak rasporeda akontacija | Unesite datum završetka rasporeda akontacija. | Ovaj datum ne mora biti datum kada je stvorena posljednja akontacija ili predujam. Na datum stvaranja posljednje akontacije ili predujma utječe i učestalost faktura. |
| Broj akontacija koje treba stvoriti | Kada unesete broj akontacija koje treba stvoriti, za stvaranje broja u ovom polju sustav upotrebljava datum početka i učestalost. | Kada se ovo polje ručno ažurira, sustav zanemaruje vrijednost u polju **Kraj rasporeda akontacija** i umjesto toga stvara određeni broj akontacija ili predujmova. |
| Učestalost fakturiranja | Koliko će često aplikacija stvoriti akontacije i predujmove? | Ova vrijednost izravno utječe na broj akontacija i predujmova te na stvorene datume. |
| Ukupni iznos | Ukupni iznos je iznos koji se dijeli na plaćanja pojedine akontacije ili predujma koji će se stvoriti. | Ovo polje ne utječe na niže razine. |
