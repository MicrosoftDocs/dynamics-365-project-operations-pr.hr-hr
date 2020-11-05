---
title: Integracija programa Microsoft Project Client
description: Planiranje i održavanje rasporeda projekata može biti složeno, pa voditelji projekata trebaju upotrebljavati alate koji im pomažu pri upravljanju tim zadatkom. Integracija s programom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturnom analizom rada na projektu.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073449"
---
# <a name="microsoft-project-client-integration"></a>Integracija programa Microsoft Project Client

[!include [banner](../includes/banner.md)]

Planiranje i održavanje rasporeda projekata može biti složeno, pa voditelji projekata trebaju upotrebljavati alate koji im pomažu pri upravljanju tim zadatkom. Integracija s programom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturnom analizom rada na projektu. Voditelj projekta može objaviti sve promjene natrag na strukturnu analizu rada projekta aplikacije Dynamics 365 Finance.

> [!NOTE]
> Ako koristite srpanjsko ažuriranje (verzija 10.0.4), morate instalirati zakrpe KB 4054797 i 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfiguriranje dodatka programu Microsoft Project Client
Kako biste omogućili integraciju s programom Microsoft Project Client, potrebno je instalirati dodatak sustava Microsoft Dynamics 365 na korisnikov klijent aplikacije Microsoft Project. To se postiže otvaranjem mogućnosti **Radni prostor za upravljanje projektima**.

•   Kliknite **Konfiguriraj dodatak za klijenta** iz odjeljka radnog prostora **Veze** > **Postavljanje**.

•   Kliknite **Otvori** , a zatim, kad se od vas to zatraži, kliknite **Pokreni**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Otvaranje i uređivanje postojećeg nacrta strukturne analize rada u programu Microsoft Project Client
Ako projekt u aplikaciji Dynamics 365 Finance već ima stvorenu strukturnu analizu rada, ona se može otvoriti u programu Microsoft Project Client ako je strukturna analiza rada u stanju skice. Za otvaranje sa stranice **Projekt** , kliknite vezu **Otvori u aplikaciji Microsoft Project** na kartici **Plan**. Ova se stranica također može otvoriti iz programa Microsoft Project Client klikom mogućnosti **Otvori** na kartici **Microsoft Dynamics 365**. S popisa odaberite **Pravna osoba** i **Projekt**.

> [!NOTE]
> Ako upotrebljavate preglednik Internet Explorer, morat ćete kliknuti **Spremi** za ručno otvaranje s mjesta na kojem se nalazi preuzeta datoteka. Ili kliknite **Spremi i otvori** kako biste datoteku otvorili u programu Microsoft Project Client. Nemojte preimenovati naziv datoteke tijekom spremanja.

Prije bilo kakvog uređivanja datoteke s pomoću programa Microsoft Project Client, morate je provjeriti. Kliknite **Provjeri** na kartici **Microsoft Dynamics 365**. To će spriječiti druge korisnike da istodobno uređuju strukturnu analizu rada iz Financija. Kako biste objavili strukturnu analizu rada nakon dovršetka uređivanja, kliknite **Prijava** na kartici **Microsoft Dynamics 365**.

Ako je projektni tim već dodan projektu u aplikaciji Financije, popis resursa popunit će se članovima tima. Ako projektni tim još nije dodan projektu, možete odabrati resurse i izgraditi tim unutar programa Microsoft Project Client tako da kliknete gumb **Resursi** na kartici **Microsoft Dynamics 365**. 

Sljedeći će se podaci sinkronizirati natrag u aplikaciju Financije kao dio postupka prijave:

•   Naziv zadatka

•   Datum početka

•   Datum završetka

•   Prethodnici

•   Nazivi resursa

•   Kategorija

•   Kategorija resursa

•   Radno vrijeme

•   Bilješke

•   Prioritet

> [!NOTE]
> Ako u datoteku programa Microsoft Project Client dodate neki drugi stupac, neće se spremiti u datoteku i neće se prikazati kad se datoteka ponovno otvori.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Stvaranje strukturne analize rada za postojeći projekt s pomoću programa Microsoft Project Client
Za stvaranje nove strukturne analize rada s pomoću programa Microsoft Project Client slijedite ove korake:


1.  Otvorite program Microsoft Project Client.

2.  Na kartici **Microsoft Dynamics 365** kliknite **Otvori**.

3.  Odaberite mogućnost **Pravna osoba** za projekt.

4.  Odaberite **Projekt**.

5.  Kliknite **Pregledaj** na kartici **Microsoft Dynamics 365**.

6.  Kada ste spremni za objavljivanje u Financijama, kliknite **Prijava** na kartici **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Zamjena postojeće strukturne analize rada za postojeći projekt s pomoću programa Microsoft Project Client
Kako biste stvorili novu strukturnu analizu rada s pomoću programa Microsoft Project Client i zamijenili postojeću strukturnu analizu rada za postojeći projekt, slijedite ove korake:

1.  Otvorite program Microsoft Project Client.

2.  Stvorite raspored u programu Microsoft Project Client.

3.  Na kartici **Microsoft Dynamics 365** kliknite **Spremi promjene** > **Zamijeni postojeći projekt**.

4.  Odaberite mogućnost **Pravna osoba** za projekt.

5.  Odaberite **Projekt**.

6.  Kliknite **U redu**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Stvaranje novog projekta iz programa Microsoft Project Client


1.  Otvorite program Microsoft Project Client.

2.  Stvorite raspored u programu Microsoft Project Client.

3.  Na kartici **Microsoft Dynamics 365** kliknite **Spremi promjene** > **Spremi u novi projekt**.

4.  Odaberite mogućnost **Pravna osoba** za projekt.

5.  Unesite **ID projekta** , ako je potrebno.

6.  Unesite **Naziv proizvoda**.

7.  Odaberite mogućnost **Vrsta projekta** , **Grupa projekta** i **ID ugovora o projektu**. Alternativno, klikom mogućnosti **Novo** možete stvoriti novi ugovor o projektu.

8.  Odaberite **Kalendar** koji će se upotrebljavati za raspodjelu resursa.

11. Kliknite **U redu**.
