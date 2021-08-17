---
title: Postavljanje resursa projekta
description: U ovoj temi nalaze se informacije o načinu postavljanja ili zahtijevanja resursa za projekt.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c8e4373da50999a0cc57f4eab672a98e7cf21edcfa5a5589d87691603a777de
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995707"
---
# <a name="set-up-project-resources"></a>Postavljanje resursa projekta

[!include [banner](../includes/banner.md)]

Morate postaviti kalendar i povezati ga sa zaposlenikom ili radnikom. Kalendar se upotrebljava za planiranje projekta i radnog vremena resursa rezerviranih za projekt. Tijekom postavljanja kalendara, voditelji projekata mogu izvršiti ujednačavanje resursa kao dio optimizacije resursa. Na temelju kalendarskog rasporeda na resurse se mogu staviti ograničenja. Kalendar možete postaviti na stranicu **Kalendari**.

Kada radnika postavite kao resurs projekta, možete birati između radnika koji rade u tvrtki za koju postavljate resurse. Možete odabrati i radnike iz drugih tvrtki unutar svoje tvrtke ili ustanove. Ti su radnici poznati kao resursi unutar tvrtke.

U slijedećim se postupcima objašnjava način za postavljanje radnika kao resursa projekta u vašoj tvrtki i način za postavljanje resursa unutar tvrtke za projekt.

## <a name="set-up-a-worker-as-a-project-resource"></a>Postavljanje radnika kao resursa projekta

1. Na stranici **Radnici**, na popisu **Radnici**, odaberite radnika kojeg dodajete kao resurs projekta i otvorite zapis za radnika.
2. U oknu radnji odaberite **Projekt** &gt; **Postavljanje** &gt; **Postavljanje projekta**.
3. Odaberite kalendar, a zatim zatvorite stranicu.

Također možete odrediti zadane projekte za resurs kao vrstu prethodne dodjele. Prethodne dodjele mogu se upotrebljavati kada voditelj resursa ili voditelj projekata unaprijed zna na kojim će projektima resurs raditi. Prethodne dodjele također se mogu temeljiti na zahtjevu sponzora projekta ili klijenta. Kako biste unaprijed dodijelili projekt, odaberite odgovarajući projekt na stranici **Dodijeli projekte**, na kartici **Projekti** s popisa **Preostali projekti**.

## <a name="set-up-an-intercompany-resource"></a>Postavljanje resursa unutar tvrtke

Kada radnika postavite kao resurs unutar tvrtke, morate dovršiti postavljanje i u tvrtki davateljici posudbe i u tvrtki primateljici posudbe.

### <a name="in-the-lending-company"></a>U tvrtki davateljici posudbe

1. U Financijama provjerite je li odabrana tvrtka davateljica posudbe, a zatim dovršite postupak iz prethodnog odjeljka „Postavljanje radnika kao resursa projekta”.
2. Na stranici **Računovodstvo unutar tvrtke** odaberite mogućnost **Novo**.
3. U polju **ID pravne osobe**, odaberite tvrtku davateljicu posudbe. Prema potrebi popunite preostala polja, a zatim odaberite **Spremi**.
4. Na stranici **Cijena prijenosa** odaberite **Novo**.
5. U polju **Pravna osoba koja prima posudbu** odaberite odgovarajuću tvrtku.
6. Kako biste posudili tvrtki primateljici posudbe samo one resurse koje ste stvorili na početku ovog odjeljka u polju **Resurs**, odaberite naziv resursa koji ste stvorili. Kako biste tvrtki primateljici posudbe omogućili sve resurse tvrtke davateljice posudbe, polje **Resurs** ostavite prazno.
7. Na stranici **Parametri upravljanja projektom i računovodstveni parametri**, na kartici **Unutar tvrtke**, postavite mogućnost **Omogući raspoređivanje resursa i evidencija radnog vremena unutar tvrtke** na **Da**.

### <a name="in-the-borrowing-company"></a>U tvrtki primateljici posudbe

- U filtar za pretraživanje na stranici **Popis resursa** unesite naziv resursa koji ste stvorili za tvrtku primateljicu posudbe kako biste provjerili je li ime uključeno u popis resursa za tvrtku primateljicu posudbe.

## <a name="request-project-resources"></a>Zahtjevi za resurse za projekt
Funkcionalnost za planiranje resursa projekata omogućuju voditeljima resursa samo da raspoređuju resurse osoblja na angažmanima ili projektima. Kako biste omogućili ovu funkciju, dovršite sljedeće zadatke ili provjerite jesu li dovršeni:

- Postavite nizove brojeva.
- Postavite tijekove upravljanja projektima i računovodstva.
- Omogućite tijekove zahtjeva za resursima.

Nakon dovršenja prethodnih zadataka, prema potrebi možete izvršiti sljedeće zadatke:

- Izraditi zahtjev za resursom iz uvjetnog resursa osoblja.
- Nadzirati zahtjeve za resursom.
- Ispuniti zahtjev za resurse.
- Zatražiti resurs osoblja iz WBS-a.
- Rezervirajte resurse za projekt bez zahtjeva za resursom osoblja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]