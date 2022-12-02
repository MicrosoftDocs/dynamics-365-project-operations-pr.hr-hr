---
title: Migriranje u potpunosti fakturiranih kontrolnih točki naplate prilikom prijelaza
description: U ovom se članku objašnjava kako migrirati ključne točke naplate s fiksnom cijenom koje su fakturirane kliknetu za otvorene projektne ugovore prije datuma aktiviranja.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migriranje u potpunosti fakturiranih kontrolnih točki naplate prilikom prijelaza

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

## <a name="scenario"></a>Scenarij

Contoso aktivira uslugu Microsoft Dynamics 365 Project Operations za scenarije temeljene na resursima / bez zaliha. U sklopu aktivnosti prijelaza, implementacijski tim mora migrirati otvorene projektne ugovore iz starog sustava. Neki od projektnih ugovora uključuju retke ugovora za koje se upotrebljava način naplate s fiksnom cijenom i već su djelomično fakturirane krajnjem klijentu. Implementacijski tim mora migrirati ove kontrolne točke naplate kao **Faktura za klijenta proknjižena** jer moraju biti obuhvaćene u ukupnu vrijednost ugovora u svrhu priznavanja prihoda. Međutim, to ne smije utjecati na salsa klijenata u Potraživanjima i Glavnoj knjizi.

## <a name="solution"></a>Rješenje

### <a name="prerequisites"></a>Preduvjeti

- Mora biti instalirana platforma Dynamics 365 Finance 10.0.24 ili novija.
- Okruženje u kojoj će se dovršiti koraci migracije mora biti u načinu održavanja. Nikakve druge aktivnosti ne smiju se izvoditi tijekom migracije kontrolnih točaka.
- Koraci migracije moraju se slijediti točno kako je ovdje opisano i mogu se upotrebljavati samo za aktivnost prijelaza. Microsoft ne podržava nikakvu drugu upotrebu ove mogućnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Stvorite prijelaznu verziju karte s dvostrukim pisanjem kontrolnih točaka retka ugovora za integraciju aplikacije Project Operations 

1. Provjerite je li ciljno mapiranje za entitet **Kontrolne točke retka ugovora za integraciju aplikacije Project Operations** ažurirano. 

    1. U Financijama idite na **Upravljanje podatcima** \> **Entiteti podataka** i odaberite entitet **Kontrolne točke retka ugovora za integraciju aplikacije Project Operations**. 
    2. Odaberi **Izmijeni ciljna mapiranja**. 
    3. Na stranici **Priprema karte za cilj**, odaberite **Generiraj mapiranje**, a zatim potvrdite da želite generirati mapiranje.

2. Zaustavite i osvježite kartu s dvostrukim pisanjem **Kontrolnih točaka retka ugovora za integraciju aplikacije Project Operations** (**msdyn\_contractlinescheduleofvalues**) 

    1. Idite na **Upravljanje podacima** \> **Dvostruko pisanje**, odaberite kartu i otvorite njezine pojedinosti. 
    2. Odaberite **Zaustavi** i pričekajte dok sustav ne zaustavi kartu. 
    3. Odaberite **Osvježi tablice**.

3. Dodajte mapiranje za status transakcije.

    1. Odaberite **Dodaj mapiranje**.
    2. U novom retku, u stupcu **Aplikacije za financije i operacije**, odaberite polje **TRANSSTATUS \[TRANSSTATUS\]**.
    3. U stupcu **Microsoft Dataverse**, odaberite **msdyn\_invoicestatus \[Status fakture\]**.
    4. U stupcu **Vrsta karte** odaberite desnu strelicu (**\>**).
    5. U dijaloškom okviru koji se pojavi, u polju **Smjer sinkronizacije** odaberite **Dataverse u aplikacije za financije i operacije**.
    6. Odaberite **Dodaj pretvorbu**.
    7. U polju **Vrsta pretvorbe** odaberite **ValueMap**.
    8. Odaberite **Dodaj mapiranje vrijednosti**.
    9. U lijevo polje unesite **4**. U desno polje unesite **192350001**. 
    10. Odaberite **Spremi** i zatvorite dijaloški okvir.

4. Odaberite **Spremi kao** za spremanje verzije karte s dvostrukim pisanjem. 
5. U oknu **Dodaj tablicu**, u polju **Izdavač**, odaberite **Zadani izdavač**.
6. U polje **Verzija** unesite verziju.
7. U polje **Opis** unesite bilješku o ovoj prijelaznoj verziji karte. 
8. Odaberite **Spremi**.
9. Pokrenite kartu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migriranje fakturiranih kontrolnih točaka u okruženje Dataverse

1. U okruženju Dataverse aplikacije Project Operations izradite kontrolne točke koje imaju status fakture **Spremno za fakturiranje**. U ovom trenutku nemojte migrirati nijednu kontrolnu točku koja nije fakturirana.

    > [!NOTE]
    > Prije nego što migrirate ključne točke naplate, provjerite jesu li financijske dimenzije koje se odnose na redak ugovora postavljene prema očekivanjima. Financijske dimenzije nije moguće uređivati nakon dovršetka migracije.

2. Nakon što se migriraju svi kontrolne točke, zaustavite sljedeće karte s dvostrukim pisanjem:

    - Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinescheduleofvalues)
    - Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)
    - Prijedlog fakture za projekt V2 (fakture)

    Da biste zaustavili karte, slijedite korake u nastavku:

    1. U Financijama idite na **Upravljanje podacima** \> **Dvostruko pisanje**, odaberite kartu i otvorite njezine pojedinosti.
    2. Odaberite **Zaustavi** i pričekajte dok sustav ne zaustavi kartu.

3. U okruženju Dataverse aplikacije Project Operations izraditi i potvrditi predračune za kontrolne točke naplate. 

    1. Na karti web-mjesta idite na projektne ugovore, odaberite ugovore, a zatim odaberite **Izradi fakturu**.
    2. Nakon što se fakture izrade, otvorite ih iz izbornika **Fakture** na karti web-mjesta, a zatim odaberite **Potvrdi**.

    Ovim se korakom izrađuju potrebni zapisi u okruženju Dataverse. Međutim, to ne utječe na financije i potraživanja, jer su prethodno navedene karte s dvostrukim pisanjem zaustavljene.

4. Nakon potvrde svih predračuna, vratite sve karte s dvostrukim pisanjem u početno stanje.

    1. Ažurirajte verziju kartu s dvostrukim pisanjem **Kontrolnih točaka retka ugovora za integraciju aplikacije Project Operations** (**msdyn\_contractlinescheduleofvalues**) na izvornu verziju. 
    2. Odaberite kartu s dvostrukim pisanjem na popisu karata, odaberite **Verzija karte tablite**, a zatim odaberite izvornu verziju karte tablice.
    3. Odaberite **Spremi**.
    4. Ponovno pokrenite sljedeće karte s dvostrukim pisanjem:

        - Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinescheduleofvalues)
        - Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)
        - Prijedlog fakture za projekt V2 (fakture)

Migracija kontrolnih točaka je završena i sustav je spreman za sljedeće korake u aktivnosti prijelaza.
