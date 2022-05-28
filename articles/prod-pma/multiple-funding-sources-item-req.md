---
title: Zahtjevi za stavke za projektne ugovore s više izvora financiranja
description: Ova tema pruža informacije o konfiguriranju i korištenju zahtjeva za artiklima s više izvora financiranja.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d4af03e02d3c2eb0d442e6213ff5b9cf583d54b3
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728082"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Zahtjevi za stavke za projektne ugovore s više izvora financiranja

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

Neki ugovorni sporazumi za rezultate koji se temelje na projektima mogu zahtijevati više izvora financiranja. Ova tema objašnjava kako odabrati i konfigurirati željene izvore financiranja kada je za projekt ili projektni ugovor potrebno više izvora.

## <a name="terminology"></a>Terminologija

- **Izvor** financiranja – Subjekt koji financira projektni ugovor radi. Taj entitet može biti interna organizacija ili vanjski račun fakture (kupac ili bespovratna sredstva).
- **Korisnik** projekta – entitet kojem se projekt isporučuje.
- **Račun** fakture – vanjski subjekt koji plaća projektni rad.

## <a name="example"></a>Primjer

Contoso je dobio ugovor o obnovi opreme s dva svoja kupca: Adatum US i Adatum Corporate. Ugovor uključuje hardverske i instalacijske usluge koje će biti isporučene Adatumu SAD (kupcu projekta). Hardver će financirati tvrtka Adatum Corporate (račun računa 1), a instalacijske radove financirat će Adatum US (račun računa 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Postavljanje zadanih pravila računa fakture za zahtjeve artikla

### <a name="prerequisites"></a>Preduvjeti

- Microsoft Dynamics 365 Verzija financija i operacija **10.0.27 ili novija** potrebna je za korištenje zahtjeva za artiklima koji imaju više računa računa.
- Administrator sustava mora omogućiti zahtjeve dopusti stavku **s više izvora financiranja za značajku projektnih operacija opskrbljenih/proizvodnih scenarija** u **radnom prostoru za upravljanje** značajkama.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Postavljanje zadanih pravila računa fakture

Da biste postavili zadana pravila za račun fakture, slijedite ove korake.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Parametri upravljanja projektom i računovodstva**.
1. Na kartici **Općenito** u **odjeljku Nalozi za prodaju i zahtjevi za artiklom** postavite **mogućnost Dopusti projekte s više izvora financiranja** na **Da**.
1. **U polju Zadani kupac** navedite odakle kupac isporuke projekta prema zahtjevu artikla po zadanom dolazi:

    - **Iz izvora** financiranja - Zadani kupac isporuke projekta dolazi iz izvora financiranja. Ako je s ugovorom o projektu povezano više izvora financiranja, koristit će se prvi izvor financiranja na popisu.
    - **Iz projekta** – zadani kupac isporuke projekta dolazi od kupca odabranog **u polju Račun** zapisa projekta.

1. Neobavezno: Postavite ili promijenite zadani račun fakture u zapisima projekta:

    1. Idite na **Projekti upravljanja i računovodstva** \> **Projekti** \> **Svi projekti** i otvorite detalje o zapisu projekta.
    2. Na kartici **Općenito** postavite ili ažurirajte polje Zadani **račun fakture**. Račun koji navedete koristit će se kao zadani račun fakture za nove zahtjeve artikla kreirane za projekt. Ako polje ostavite prazno, račun fakture prvog izvora financiranja ugovora o projektu koristit će se prema zadanim postavkama. Međutim, korisnici će moći promijeniti račun kada zaspreme zapis.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Odaberite račun fakture koji će se koristiti prilikom stvaranja zahtjeva za artiklom

Da biste odabrali račun fakture koji će se koristiti prilikom kreiranja zahtjeva za artiklom, slijedite ove korake.

1. Idite na **Projekti upravljanja i računovodstva** \> **Projekti** \> **Svi projekti** i odaberite zapis projekta.
1. Na kartici **Planiranje** odaberite **Preduvjeti za stavku**.
1. Stvorite novi zapis zahtjeva za artiklom.

    - Po zadanome **, polje Račun** fakture u zapisu postavljeno je na račun fakture koji je postavljen za projekt. Možete promijeniti vrijednost polja Račun **fakture**, a zatim spremiti zapis. Nakon spremanja zapisa više ne možete ažurirati vrijednost računa **fakture**. Ako morate obnoviti **vrijednost računa** fakture za zahtjev artikla, izbrišite postojeći zahtjev za artiklom, a zatim stvorite novi koji ima željenu vrijednost.
    - Polje Kupac za zahtjev artikla po zadanom **se postavlja na temelju zadane vrijednosti kupca** postavljene **na** stranici Upravljanje projektom i računovodstveni parametri **.**

    Kada se spremi zapis o zahtjevu za artiklom, sustav ga povezuje sa zapisom **zaglavlja naloga za prodaju** zahtjeva za artiklom. Ako nijedno otvoreno zaglavlje naloga za prodaju nema odabrani račun fakture, sustav će ga kreirati i njime povezati redak zahtjeva za artiklom.

> [!NOTE]
> Zahtjevi za artiklom uvijek se u potpunosti fakturiraju računu fakture postavljenom u zapisu. Sustav trenutno ne podržava pravila dodjele financijskih sredstava koja imaju zahtjeve za artiklima i neće podijeliti knjiženje na temelju postavljanja pravila o dodjeli financiranja.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Stvaranje zahtjeva za artiklom iz zapisa predviđanja artikla

Da biste kreirali zahtjev za artiklom iz zapisa predviđanja artikla, slijedite ove korake.

1. Idite na **Projekti upravljanja i računovodstva** \> **Projekti** \> **Svi projekti** i odaberite zapis projekta.
1. Na kartici **Plan** odaberite **Predviđanja artikla**.
1. Stvorite novi zapis predviđanja artikla.
1. Neobavezno: na **kartici Projekt** u **polju Izvor** financiranja odaberite željeni račun fakture.
1. Odaberite **Kreiraj zahtjev za** stavku i potvrdite poruku koju primite.

    > [!NOTE]
    > Sustav kopira vrijednost izvora **financiranja** iz zapisa predviđanja artikla u novostvoreni zapis zahtjeva za artiklom.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Zadani račun fakture kada sustav automatski kreira zahtjev za artiklom iz retka narudžbenice

**Ako je mogućnost Kreiranje zahtjeva za** artiklom postavljena na **Da** na **stranici Parametri upravljanja projektom i računovodstvenih parametara**, sustav automatski kreira zahtjev za artiklom prilikom spremanja novog retka narudžbenice za projekt. Prema zadanim postavkama polja **Račun** fakture i **Zahtjev** za artiklom postavljena **su na vrijednost polja Zadani račun** fakture u zapisu projekta. Sustav trenutno ne podržava ažuriranje ili promjenu računa fakture za zapise ove vrste.
