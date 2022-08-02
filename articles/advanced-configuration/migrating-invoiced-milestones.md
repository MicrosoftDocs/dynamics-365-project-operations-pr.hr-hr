---
title: Migrirajte potpuno fakturirane ključne etape za naplatu pri smanjenju
description: U ovom se članku objašnjava kako migrirati ključne etape za naplatu s fiksnom cijenom koje su fakturirane kupcu za otvorene projektne ugovore prije datuma pokretanja uživo.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028693"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrirajte potpuno fakturirane ključne etape za naplatu pri smanjenju

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

## <a name="scenario"></a>Scenarij

Contoso će s Microsoftom Dynamics 365 Project Operations živjeti za scenarije resursa/nenaseljenih resursa. Kao dio prijelaznih aktivnosti, provedbeni tim mora migrirati otvorene projektne ugovore iz starog sustava. Neki od ugovora o projektu obuhvaćaju retke ugovora koji koriste način naplate s fiksnom cijenom i već su djelomično fakturirani krajnjem kupcu. Tim za implementaciju mora migrirati te prekretnice za naplatu kao **proknjiženu** fakturu kupca jer moraju biti obuhvaćene ukupnom vrijednošću ugovora za potrebe priznavanja prihoda. Međutim, to ne smije utjecati na salda kupaca u potraživanjima i glavnoj knjizi.

## <a name="solution"></a>Rješenje

### <a name="prerequisites"></a>Preduvjeti

- Dynamics 365 Finance 10.0.24 ili noviji moraju biti instalirani.
- Okruženje u kojem će se dovršiti koraci migracije mora biti u načinu održavanja. Tijekom migracije ključnih etapa ne bi se smjele obavljati druge aktivnosti.
- Koraci migracije moraju se slijediti točno onako kako je ovdje opisano i mogu se koristiti samo za prijelaznu aktivnost. Microsoft ne podržava nikakvo drugo korištenje ove mogućnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Stvaranje prijelazne verzije prekretnica linije ugovora o integraciji projektnih operacija 

1. Provjerite je li mapiranje cilja za **entitet ključnih etapa retka ugovora o integraciji** projektnih operacija ažurno. 

    1. U odjeljku Financije otvorite **entitete** podataka o upravljanju \>**podacima** i odaberite **entitet ključnih etapa retka ugovora o integraciji projektnih** operacija. 
    2. Odaberite **Izmijeni ciljna mapiranja**. 
    3. **Na stranici Postavljanje karte do cilja** odaberite **Generiraj mapiranje**, a zatim potvrdite da želite generirati mapiranje.

2. Zaustavite i osvježite **prekretnice u liniji ugovora o integraciji projektnih** operacija (**msdyn\_ contractlinescheduleofvalues**) karte s dvostrukim pisanjem. 

    1. Idite na **Upravljanje** \> **podacima Dual-write**, odaberite kartu i otvorite njezine detalje. 
    2. Odaberite **Zaustavi** i pričekajte dok sustav ne zaustavi kartu. 
    3. Odaberite **Osvježi tablice**.

3. Dodajte mapiranje za status transakcije.

    1. Odaberite **Dodaj mapiranje**.
    2. U novom retku u stupcu **Aplikacije** za financije i operacije odaberite **polje TRANSSTATUS \[TRANSSTATUS\]**.
    3. U stupcu odaberite **Microsoft Dataverse** **status\_ msdyn\[invoicestatus \]** Invoice.
    4. U stupcu **Vrsta** karte odaberite strelicu desno (**\>**).
    5. U dijaloškom okviru koji će se pojaviti u polju Smjer **sinkronizacije** odaberite **Dataverse aplikacije** Financije i operacije.
    6. Odaberite **Dodaj pretvorbu**.
    7. **U polju Vrsta pretvorbe** odaberite **Visina vrijednosti**.
    8. Odaberite **Dodaj mapiranje** vrijednosti.
    9. U lijevo polje unesite **4**. U desno polje unesite **192350001**. 
    10. Odaberite **Spremi**, a zatim zatvorite dijaloški okvir.

4. Odaberite **Spremi kao** da biste spremili verziju karte s dvostrukim pisanjem. 
5. **U oknu Dodavanje tablice** **u polju Publisher** odaberite **Zadani izdavač**.
6. **U polje Verzija** unesite verziju.
7. **U polje Opis** unesite bilješku o ovoj prijelaznoj verziji karte. 
8. Odaberite **Spremi**.
9. Pokrenite kartu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migracija fakturiranih ključnih etapa u Dataverse okoliš

1. U okruženju Projektne operacije Dataverse stvorite ključne etape koje imaju status fakture Spremno **za fakturiranje**. U ovom trenutku nemojte migrirati prekretnice koje nisu fakturirane.

    > [!NOTE]
    > Prije migracije ključnih etapa za naplatu provjerite jesu li financijske dimenzije povezane s retkom ugovora o projektu postavljene prema očekivanjima. Financijske dimenzije ne mogu se uređivati nakon dovršetka migracije.

2. Nakon migracije svih ključnih etapa zaustavite sljedeće karte dvostrukog pisanja:

    - Ključne etape za integraciju ugovornih linija projektnih operacija (msdyn\_ contractlinescheduleofvalues)
    - Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)
    - Prijedlog fakture za projekt V2 (fakture)

    Da biste zaustavili karte, slijedite ove korake:

    1. U odjeljku Financije idite na **Upravljanje** \> **podacima Dual-write**, odaberite kartu i otvorite njezine detalje.
    2. Odaberite **Zaustavi** i pričekajte da sustav zaustavi kartu.

3. U okruženju Projektne operacije Dataverse izradite i potvrdite pro-forma fakture za ključne etape za naplatu. 

    1. Na karti web-mjesta idite na ugovore o projektu, odaberite ugovore, a zatim odaberite **Kreiraj fakture**.
    2. Nakon kreiranja faktura otvorite ih s izbornika Fakture na **karti web-mjesta, a zatim odaberite** Potvrdi **.**

    Ovaj korak stvara potrebne zapise u Dataverse okruženju. Međutim, to ne utječe na financije i potraživanja, jer su prethodno navedene karte s dvostrukim pisanjem zaustavljene.

4. Nakon što se potvrde svi pro-forma računi, vratite sve karte dvostrukog pisanja u početno stanje.

    1. Ažurirajte verziju ključnih etapa **linije ugovora o integraciji projektnih** operacija (**msdyn\_ contractlinescheduleofvalues) karte dvostrukog pisanja** natrag na izvornik. 
    2. Odaberite kartu dvostrukog pisanja na popisu karata, odaberite **Verzija** karte tablice, a zatim odaberite izvornu verziju karte tablice.
    3. Odaberite **Spremi**.
    4. Ponovno pokrenite sljedeće karte s dvostrukim pisanjem:

        - Ključne etape za integraciju ugovornih linija projektnih operacija (msdyn\_ contractlinescheduleofvalues)
        - Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)
        - Prijedlog fakture za projekt V2 (fakture)

Prekretnice se sada migriraju, a sustav je spreman za sljedeće korake u aktivnosti smanjenja.
