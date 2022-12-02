---
title: Zahtjevi za stavke za ugovore o projektu s više izvora financiranja
description: U ovom se članku navode informacije o tome kako konfigurirati i upotrebljavati zahtjeve za stavke s višestrukim izvorima financiranja.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028464"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Zahtjevi za stavke za ugovore o projektu s više izvora financiranja

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

Neki ugovorni sporazumi za predmete isporuke temeljene na projektu mogu zahtijevati više izvora financiranja. U ovom se članku objašnjava kako odabrati i konfigurirati željene izvore financiranja kada je za projekt ili ugovor za projekt potrebno više izvora.

## <a name="terminology"></a>Terminologija

- **Izvor financiranja** – entitet koji financira ugovoreni rad na projektu. Taj entitet može biti interna organizacija ili vanjski račun za fakturu (klijent ili potpora).
- **Klijent projekta** – entitet kojem se isporučuje rad na projektu.
- **Račun fakture** – vanjski entitet koji plaća rad na projektu.

## <a name="example"></a>Primjer

Tvrtki Contoso dodijeljen je ugovor za obnovu opreme za dva klijenta: Adatum US i Adatum Corporate. Ugovor uključuje isporuku hardvera i usluge ugradnje za tvrtku Adatum US (klijent projekta). Hardver će financirati Adatum Corporate (račun za fakturu 1), a radove na ugradnji Adatum US (račun za fakturu 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Postavljanje pravila za zadane vrijednosti za račun za fakturu za zahtjeve za stavkom

### <a name="prerequisites"></a>Preduvjeti

- Verzija sustava Microsoft Dynamics 365 Finance **10.0.27 ili novija** potrebna je za korištenje zahtjevima za stavkom koji imaju više računa za fakture.
- Vaš administrator sustava mora omogućiti značajku **Dopusti zahtjeve za stavkom s višestrukim izvorima financiranja za scenarije koji se temelje na zalihama/proizvodnji aplikacije Project Operations** u radnom prostoru **Upravljanje značajkama**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Postavljanje pravila za zadane vrijednosti računa za fakturu

Da biste postavili zadana pravila za račun za fakture, slijedite ove korake.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Parametri upravljanja projektom i računovodstva**.
1. Na kartici **Općenito**, u odjeljku **Prodajni nalozi i zahtjevi za stavke**, mogućnost **Omogući za projekte s više izvora financiranja** postavite na **Da**.
1. U polju **Zadani kupac** odredite odakle klijent isporuke projekta na zahtjevu za stavku dolazi prema zadanim postavkama:

    - **Iz izvora financiranja** – zadani klijent isporuke projekta dolazi iz izvora financiranja. Ako je s ugovorom o projektu povezano više izvora financiranja, koristit će se prvi izvor financiranja na popisu.
    - **Iz projekta** – zadani korisnik isporuke projekta dolazi od klijenta koji je odabran u polju **Račun zapisa projekta**.

1. Izborno: postavite ili promijenite zadani račun za fakture u zapisima projekta:

    1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i otvorite pojedinosti zapisa projekta.
    2. Na kartici **Općenito** postavite ili ažurirajte polje **Zadani račun za fakturu**. Račun koji navedete koristit će se kao zadani račun za fakturu za nove zahtjeve za stavke koje se izrade za projekt. Ako polje ostavite praznim, račun za fakturu prvog izvora financiranja ugovora o projektu koristit će se prema zadanim postavkama. Međutim, korisnici će moći promijeniti račun kada spreme zapis.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Biranje računa za fakturu koji će se koristiti kada izradite zahtjev za stavku

Slijedite ove korake da biste odabrali račun za fakturu koji će se koristiti kada izradite zahtjev za stavku.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i odaberite zapis projekta.
1. Na kartici **Plan** odaberite **Zahtjevi za stavkom**.
1. Izradite novi zapis zahtjeva za stavkom.

    - Prema zadanim postavkama, polje **Račun za fakturu** u zapisu postavljeno je na račun za fakturu koji je postavljen za projekt. Možete promijeniti vrijednost polja **Račun za fakturu** i zatim spremite zapis. Nakon što je zapis spremljen, više ne možete ažurirati vrijednost **Račun za fakturu**. Ako morate ažurirati vrijednost **Račun za fakturu** za zahtjev za stavkom, izbrišite postojeći zahtjev za stavkom, a zatim izradite novi koji ima željenu vrijednost.
    - Prema zadanim postavkama, polje **Klijent** za zahtjev za stavkom postavlja se na temelju vrijednosti **Zadani kupac** koja je postavljena na stranici **Upravljanje projektima i računovodstveni parametri**.

    Kada se zapis zahtjeva za stavkom spremi, sustav ga povezuje sa zapisom zaglavlja **Prodajni nalog zahtjeva za stavkom**. Ako nijedno otvoreno zaglavlje prodajnog naloga nema odabrani račun za fakturu, sustav će ga izraditi i pridružiti mu redak zahtjeva za stavkom.

> [!NOTE]
> Zahtjevi za stavkom uvijek se u potpunosti fakturiraju na račun za fakturu koji je postavljen u zapisu. Sustav trenutačno ne podržava pravila za dodjelu sredstava koja imaju zahtjeve za stavkom i neće podijeliti knjiženje na temelju postavki pravila za dodjelu sredstava.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Izrada zahtjeva za stavkom iz zapisa predviđanja o stavci

Slijedite ove korake da biste izradali zahtjev za stavkom iz zapisa predviđanja o stavci.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i odaberite zapis projekta.
1. Na kartici **Plan** odaberite **Predviđanja o stavci**.
1. Izradite novi zapis predviđanja o stavci.
1. Izborno: na kartici **Projekt**, u polju **Izvor financiranja**, odaberite željeni račun za fakturu.
1. Odaberite **Izradi zahtjev za stavkom** i potvrdite poruku koju primite.

    > [!NOTE]
    > Sustav kopira vrijednost **Izvor financiranja** iz zapisa predviđanja o stavci u novoizrađeni zapis zahtjeva za stavkom.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Zadani račun za fakturu kada sustav automatski izradi zahtjev za stavkom iz retka narudžbenice

Ako je mogućnost **Izradi zahtjev za stavkom** postavljena na **Da** na stranici **Upravljanje projektom i računovodstveni parametri**, sustav automatski izrađuje zahtjev za stavkom kada se novi redak narudžbenice projekta spremi. Prema zadanim postavkama, polja **Račun za fakturu** i **Zahtjev za stavkom** postavljena su na vrijednost polja **Zadani račun za fakturu** u zapisu projekta. Sustav trenutačno ne podržava ažuriranje ili promjenu računa za fakturu za zapise ove vrste.
