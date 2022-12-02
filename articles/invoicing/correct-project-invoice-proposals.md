---
title: Ispravljanje računovodstva za skice prijedloga faktura za projekt
description: U ovom se članku objašnjava način na koji se vrši prilagodba informacija povezanih s računovodstvom na skicu prijedloga fakture.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921201"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Ispravljanje računovodstva za skice prijedloga faktura za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

*Operativne pojedinosti* faktura za projekt vodi voditelj projekta na predračunu. Te pojedinosti uključuju odluku o radnom vremenu, troškovima, materijalima ili kontrolnim točkama koje se moraju fakturirati, cijenama te primjeni iznosa predujma i akontacija. Nakon što potvrdite izvorni predračun, možete prilagoditi operativne pojedinosti stvaranjem i potvrđivanjem [korektivnog predračuna](../proforma-invoicing/corrective-invoices.md).

*Računovodstvene pojedinosti* faktura za projekt vode se u dokumentu fakture namijenjene klijentu. Te pojedinosti uključuju izračun poreza na promet i financijske veličine koje se primjenjuju na fakturu. U ovom se članku navode pojedinosti o tome kako se te računovodstvene pojedinosti mogu prilagoditi u skici prijedloga fakture za projekt.

## <a name="adjust-sales-tax"></a>Prilagodba poreza na promet

Zadane grupe poreza na promet za naplatu i grupe poreza na promet za stavke mogu se prilagoditi izravno na dokumentu prijedloga fakture. Kako biste prilagodili ove grupe, odaberite **Uredi**, a zatim u svaki redak prijedloga fakture za projekt unesite novu vrijednost u polje **Grupa poreza na promet** ili **Grupa poreza na promet za stavku**.

## <a name="adjust-financial-dimensions"></a>Prilagodba financijskih veličina

### <a name="header-dimensions"></a>Dimenzije zaglavlja

Prema zadanim postavkama, financijske veličine fakture izvode se iz nenaplaćenih zapisa transakcija projekta koji se fakturiraju. Međutim, postavke sustava vam omogućuju korištenje financijskih veličina u zaglavlju prijedloga faktura projekta za knjiženje salda klijenata. Da biste omogućili ovu funkciju odaberite **Dopusti ažuriranja veličina projekta za potraživanja** na kartici **Financije** stranice **Upravljanje projektom i računovodstveni parametri**.

Financijske veličine u zaglavljima faktura mogu se urediti prije knjiženja fakture. Na stranici **Prijedlog fakture projekta** prijeđite na prikaz **Zaglavlje**, a zatim uredite vrijednosti na kartici **Financijske veličine**.

Prikaz **Zaglavlje** dostupan je samo nakon što administrator sustava omogući značajku **Upotreba Prijedloga faktura projekta i obrazaca dnevnika faktura s prikazom Zaglavlje i Redak** u radnom prostoru **Upravljanje značajkama**. Ova značajka zahtijeva verziju aplikacije Finance 10.0.25 ili noviju.

### <a name="line-dimensions"></a>Veličine retka

Financijske veličine ne mogu se uređivati izravno na retku prijedloga fakture za projekt. Umjesto toga, slijedite ove korake za prilagodbu financijskih veličina na prijedlogu fakture za projekt.

1. Na prijedlogu fakture za projekt odaberite **Izbriši sve** kako biste uklonili retke prijedloga fakture za projekt.

    Gumb **Izbriši sve** dostupan je samo nakon što administrator sustava omogući značajku **Izbriši retke prijedloga fakture pri uporabi aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha** u radnom prostoru **Upravljanje značajkama**.

2. Prilagodba financijskih veličina:

    - **Transakcije po obračunu (kontrolne točke za naplatu):** Idite na **Svi projekti** \> **Upravljaj** \> **Transakcije po obračunu** i odaberite kontrolnu točku koju treba prilagoditi. Zatim, na kartici **Financijske veličine** ažurirajte vrijednosti prema potrebi.
    - **Transakcije vremena, troška i materijala:** Na stranici **Proknjižene projektne transakcije** odaberite **Prilagodi računovodstvo** kako biste ažurirali financijske veličine.

3. Nakon što završite s prilagodbom vrijednosti financijskih veličina, idite na stavku **Upravljanje projektima i računovodstvo** \> **Povremeno** \> **Integracija aplikacije Project Operations** i odaberite **Uvoz iz tablice faza** kako biste pokrenuli povremeni postupak. Taj postupak upotrebljava ažurirane vrijednosti financijske veličine za ponovno stvaranje redaka prijedloga fakture za projekt. Ažurirane se vrijednosti zatim upotrebljavaju u sporednoj knjizi i glavnoj knjizi projekta kada se knjiži faktura za projekt.
