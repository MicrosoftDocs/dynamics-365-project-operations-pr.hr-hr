---
title: Zadane postavke financijske dimenzije
description: U ovoj temi nalaze se informacije o načinu postavljanja zadanih financijskih veličina.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131874"
---
# <a name="financial-dimension-defaults"></a>Zadane postavke financijske dimenzije

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Dynamics 365 Project Operations upotrebljava okvir [Financijske veličine](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) u aplikaciji Dynamics 365 Finance za pružanje dodatnih uvida o transakcijama sporednih knjiga i glavne knjige.

Zadane financijske dimenzije mogu se postaviti na kupca, izvor financiranja projekta, kontrolnu točku, redak ugovora o projektu ili projekt.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definiranje zadanih financijskih veličina za klijenta

Zadane postavke veličine kupca navedene su u aplikaciji Finance. Kako biste postavili zadane postavke veličine, poduzmite sljedeće korake.

1. Idite na **Potraživanja** > **Klijenti** > **Svi klijenti**.
2. Na stranici **Klijenti**, na kartici **Financijske veličine**, postavite vrijednosti financijske veličine za određenog kupca.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definiranje zadanih financijskih veličina za ugovore o projektu

Projektni ugovori stvaraju se i održavaju na platformi Common Data Service (CDS). Atributi računovodstva za ugovore o projektu postavljeni su u modulu **Upravljanje projektom i računovodstvo** u aplikaciji Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Postavljanje financijskih veličina za izvor financiranja projekta

1. Idite na **Upravljanje projektom i računovodstvo** > **Projekti** > **Ugovori o projektu**.
2. Odaberite zapis koji želite ažurirati, a zatim na kartici **Ugovor o projektu** odaberite **Prikaži zadano računovodstvo**.
3. Proširite mogućnost **Povezane informacije** i odaberite karticu **Izvori financiranja**.
4. Postavite zadane postavke financijske veličine. Primjećujete kako se financijske veličine zadaju iz korisničkog računa.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Postavljanje financijskih veličina za redak ugovora o projektu

1. Idite na **Upravljanje projektom i računovodstvo** > **Projekti** > **Ugovori o projektu**.
2. Odaberite zapis koji želite ažurirati, a zatim na kartici **Ugovor o projektu** odaberite **Prikaži zadano računovodstvo**.
3. Proširite mogućnost **Povezane informacije** i odaberite karticu **Redci ugovora**.
4. Postavite zadane postavke financijske veličine. Zadane postavke financijske veličine primjenjive su i mogu se upotrebljavati samo s redcima ugovora s fiksnom cijenom (kontrolna točka).

Te zadane vrijednosti upotrebljavaju se za transakcije po računu i retke fakture.

## <a name="define-default-financial-dimensions-for-projects"></a>Definiranje zadanih financijskih veličina za projekte

Projekti se stvaraju i održavaju na platformi CDS. Atributi računovodstva za projekte postavljeni su u modulu **Upravljanje projektom i računovodstvo** u aplikaciji Finance.

1. Idite na mogućnost **Upravljanje projektom i računovodstvo** > **Projekti** > **Svi projekti**.
2. Odaberite zapis koji želite ažurirati, a zatim na kartici **Projekt** odaberite **Prikaži zadano računovodstvo**.
3. Proširite mogućnost **Povezane informacije** i odaberite karticu **Postavke**.
4. Postavite zadane postavke financijske veličine. Primjećujete kako se financijske veličine zadaju iz korisničkog računa. Ako je projekt povezan s retkom ugovora koji ima više klijenata ugovora o projektu, za zadane financijske veličine upotrebljava se primarni klijent.

Zadane financijske veličine projekta upotrebljavaju se za postavljanje zadanih vrijednosti retka dnevnika za vrijeme, troškove i transakcije naknada u **Dnevniku integracije aplikacije Project Operations** i na povezanim redcima fakture za projekt.