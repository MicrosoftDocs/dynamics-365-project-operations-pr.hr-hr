---
title: Postavljanje rasporeda akontacija
description: U ovoj temi nalaze se informacije o načinu postavljanja rasporeda akontacija u aplikaciji Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1c48f04aa47d50c9f3ab46031ef0d6cd68619d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574743"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]