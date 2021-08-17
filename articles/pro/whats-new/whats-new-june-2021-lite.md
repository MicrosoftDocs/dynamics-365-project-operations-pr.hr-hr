---
title: Što je novo u lipnju 2021. – implementacija osnovne aplikacije Project Operations
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju implementacije osnovne aplikacije Project Operations u lipnju 2021. godine.
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e418057e695d4a7686c278bb8ca865bddbdacfb19da88860bb35dd39ab852091
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009162"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>Što je novo u lipnju 2021. – implementacija osnovne aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations u okruženju platforme Dataverse verzije 4.11.0.156 ili 4.11.0.164.

## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2281417 | Ispravljen je problem u vezi s neuspjehom radnje automatskog stvaranja fakture putem rasporeda faktura. |
| Naplata i određivanje cijene | 2287835 |   Poboljšana je učinkovitost potvrde računa. |
| Upravljanje prilikama | 2222555 | Naplativost procjena materijala mora se ispravno kopirati u pojedinosti retka ponude pri uporabi mogućnosti **Uvoz iz procjene projekta**. |
| Upravljanje prilikama | 2223427 | Prilagodbe su sada dozvoljene za radnju **GenerateRetainersFromRetainerScheduleOptions**. |
| Upravljanje prilikama | 2277528 | Popravljen je izračun vrijednosti kontrolne točke za naplatu za retke ugovora o projektu s više klijenata. |
| Planiranje i praćenje projekta | 2226110 | Popravljen je problem s prekidima funkcije **Generiraj zahtjev** u rešetki **Projektni tim**. |
| Planiranje i praćenje projekta | 2208109 | Korisnici ne mogu stvoriti projekt u jednoj valuti s povezanim zadacima u drugoj valuti. |
| Planiranje i praćenje projekta | 2258228 | Ažuriran je popis polja kojima je dozvoljeno mijenjati entitete **Zakazivanje** koji upotrebljavaju API rasporeda. |
| Planiranje i praćenje projekta | 2293989 | Ispravni jezik i regionalne postavke moraju se proslijediti rešetki **Projektni zadaci**.|
| Upravljanje resursima | 2220493 | Popravljeno je korisničko iskustvo u rešetki **Zadatak** kada se zahtjev za resursom brzo označavao kao završen. |
| Upravljanje resursima | 2330496 | Popravljen je problem s učitavanjem **Ploče s rasporedom**. (Ažuriranje kvalitete dostupno je u verziji 4.11.0.164) |
| Vrijeme i trošak | 2194431 | Rešetka **Vremenski unos** mora poštivati početak tjedna kako je postavljeno u stavci **Postavke sustava**. |
| Vrijeme i trošak | 2277311 | Nakon što izbrišete vrijednost u ćeliji u rešetki **Vremenski unos**, pokazivač ostaje u rešetki. |
