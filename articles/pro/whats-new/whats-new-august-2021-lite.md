---
title: Što je novo u kolovozu 2021. – implementacija osnovne aplikacije Project Operations
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju implementacije osnovne aplikacije Project Operations u kolovozu 2021. godine.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3cb6f92bfb28dc64f0f689e0070b0506644c2320
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586427"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Što je novo u kolovozu 2021. – implementacija osnovne aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations u verziji 4.13.0.152 okruženja platforme Dataverse

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- **Skupovi odobrenja**: Skupovi odobrenja grupiraju zahtjeve za vrijeme, trošak ili uporabu materijala u manje podskupove operacija. Ovo grupiranje omogućuje da se odobrenja obrađuju određenim redoslijedom po projektu i omogućuje ponovni pokušaj i sekvencioniranje. Grupiranje zahtjeva poboljšava pouzdanost i sljedivost obrade odobrenja za velike količine odobrenja. Dodatne informacije potražite u članku [Skupovi odobrenja](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2295625 | Naziv kontrolne točke mora se kopirati iz rasporeda računa u pojedinost retka fakture. |
| Naplata i određivanje cijene | 2316323 | Popust se ne smije uređivati na predračunu u aplikaciji Project Operations za scenarije koji se temelje na resursima. |
|   Upravljanje prilikama | 2338619 | Poslovna pravila **Prilika** i **Ponuda** moraju se pozivati samo na stranicama. |
| Upravljanje resursima | 2316523 | Uporaba mogućnosti **Pošalji zahtjev** iz zahtjeva za resurs koji ima pridruženu ulogu ne bi trebao prikazati pogrešku. |
| Upravljanje resursima | 2326885 | Stvaranje zahtjeva za resurs kroz projekt ne bi trebalo prikazivati pogrešku. |
| Vrijeme i trošak | 2335584 | Zastarjeli zadatak teče u vremenskom unosu. |
| Vrijeme i trošak | 2336884 | Gumb za vremenski unos **Kopiraj tjedan** mora raditi ne samo za trenutačnog korisnika. |
