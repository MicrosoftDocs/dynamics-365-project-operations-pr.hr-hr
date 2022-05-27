---
title: Ispravljanje računovodstva za skice prijedloga faktura za projekt
description: U ovoj se temi objašnjava način na koji se vrši prilagodba informacija povezanih s računovodstvom na nacrtu prijedloga fakture.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575065"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Ispravljanje računovodstva za skice prijedloga faktura za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

*Operativne pojedinosti* faktura za projekt vodi voditelj projekta na predračunu. Te pojedinosti uključuju odluku o radnom vremenu, troškovima, materijalima ili kontrolnim točkama koje se moraju fakturirati, cijenama te primjeni iznosa predujma i akontacija. Nakon što potvrdite izvorni predračun, možete prilagoditi operativne pojedinosti stvaranjem i potvrđivanjem [korektivnog predračuna](../proforma-invoicing/corrective-invoices.md).

*Računovodstvene pojedinosti* faktura za projekt vode se u dokumentu fakture namijenjene klijentu. Te pojedinosti uključuju izračun poreza na promet i financijske veličine koje se primjenjuju na fakturu. U ovoj temi nalaze se pojedinosti o tome kako se te računovodstvene pojedinosti mogu prilagoditi u nacrtu prijedloga fakture za projekt.

## <a name="adjust-sales-tax"></a>Prilagodba poreza na promet

Zadane grupe poreza na promet za naplatu i grupe poreza na promet za stavke mogu se prilagoditi izravno na dokumentu prijedloga fakture. Kako biste prilagodili ove grupe, odaberite **Uredi**, a zatim u svaki redak prijedloga fakture za projekt unesite novu vrijednost u polje **Grupa poreza na promet** ili **Grupa poreza na promet za stavku**.

## <a name="adjust-financial-dimensions"></a>Prilagodba financijskih veličina

### <a name="header-dimensions"></a>Dimenzije zaglavlja

Financijske dimenzije fakture po zadanom se izvode iz neplaćenih zapisa transakcija projekta koji se fakturiraju. Međutim, postavke sustava omogućuju vam korištenje financijskih dimenzija u zaglavlju prijedloga faktura za projekt za knjiženje salda kupaca. Da biste omogućili tu funkcionalnost, na kartici Financije **na stranici Parametri upravljanja projektom i parametri računovodstva** odaberite **Dopusti ažuriranja dimenzija projekta za potraživanja za potraživanja** **.**

Financijske dimenzije u zaglavljima faktura mogu se uređivati prije knjiženja fakture. Na stranici Prijedlog fakture **za projekt prijeđite u** prikaz Zaglavlje **, a zatim uredite vrijednosti na** kartici Financijske dimenzije **.**

**Prikaz Zaglavlja** dostupan je tek nakon što administrator sustava omogući obrasce **Koristi prijedlog fakture za projekt i temeljnicu faktura sa značajkom Prikaz** zaglavlja i redaka u **radnom prostoru za upravljanje** značajkama. Ova značajka zahtijeva ažuriranje financija 10.0.25 ili novije.

### <a name="line-dimensions"></a>Dimenzije retka

Financijske veličine ne mogu se uređivati izravno na retku prijedloga fakture za projekt. Umjesto toga, slijedite ove korake za prilagodbu financijskih veličina na prijedlogu fakture za projekt.

1. Na prijedlogu fakture za projekt odaberite **Izbriši sve** kako biste uklonili retke prijedloga fakture za projekt.

    Gumb **Izbriši sve** dostupan je samo nakon što administrator sustava omogući značajku **Izbriši retke prijedloga fakture pri uporabi aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha** u radnom prostoru **Upravljanje značajkama**.

2. Prilagodba financijskih veličina:

    - **Transakcije po obračunu (kontrolne točke za naplatu):** Idite na **Svi projekti** \> **Upravljaj** \> **Transakcije po obračunu** i odaberite kontrolnu točku koju treba prilagoditi. Zatim, na kartici **Financijske veličine** ažurirajte vrijednosti prema potrebi.
    - **Transakcije vremena, troška i materijala:** Na stranici **Proknjižene projektne transakcije** odaberite **Prilagodi računovodstvo** kako biste ažurirali financijske veličine.

3. Nakon što završite s prilagodbom vrijednosti financijskih veličina, idite na stavku **Upravljanje projektima i računovodstvo** \> **Povremeno** \> **Integracija aplikacije Project Operations** i odaberite **Uvoz iz tablice faza** kako biste pokrenuli povremeni postupak. Taj postupak upotrebljava ažurirane vrijednosti financijske veličine za ponovno stvaranje redaka prijedloga fakture za projekt. Ažurirane se vrijednosti zatim upotrebljavaju u sporednoj knjizi i glavnoj knjizi projekta kada se knjiži faktura za projekt.
