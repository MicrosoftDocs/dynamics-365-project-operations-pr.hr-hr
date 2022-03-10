---
title: Zadane postavke financijske dimenzije
description: U ovoj temi nalaze se informacije o načinu postavljanja zadanih financijskih veličina.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922929"
---
# <a name="financial-dimension-defaults"></a>Zadane postavke financijske dimenzije

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations upotrebljava okvir [Financijske veličine](/dynamics365/finance/general-ledger/financial-dimensions) u aplikaciji Dynamics 365 Finance za pružanje dodatnih uvida u transakcije sporednih i glavne knjige.

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

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Zatvaranje financijskih dimenzija za stavke vremena projekta
Da biste primijenili financijske dimenzije za stavke vremena projekta, imajte na umu da se zadana vrijednost dimenzije temelji na sljedećem redoslijedu:

1. Resurs
2. Project
3. Izvor financiranja

Na primjer, ako je zadana dimenzija navedena na resursu, primijenit će se na zadanu vrijednost navedenu u projektu. Slično tome, zadana dimenzija projekta primijenit će se na zadanu vrijednost navedenu u izvoru financiranja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
