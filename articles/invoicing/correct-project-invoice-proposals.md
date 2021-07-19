---
title: Ispravljanje računovodstva za skice prijedloga faktura za projekt
description: U ovoj se temi objašnjava način na koji se vrši prilagodba informacija povezanih s računovodstvom na nacrtu prijedloga fakture.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251189"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Ispravljanje računovodstva za skice prijedloga faktura za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

*Operativne pojedinosti* faktura za projekt vodi voditelj projekta na predračunu. Te pojedinosti uključuju odluku o radnom vremenu, troškovima, materijalima ili kontrolnim točkama koje se moraju fakturirati, cijenama te primjeni iznosa predujma i akontacija. Nakon što potvrdite izvorni predračun, možete prilagoditi operativne pojedinosti stvaranjem i potvrđivanjem [korektivnog predračuna](../proforma-invoicing/corrective-invoices.md).

*Računovodstvene pojedinosti* faktura za projekt vode se u dokumentu fakture namijenjene klijentu. Te pojedinosti uključuju izračun poreza na promet i financijske veličine koje se primjenjuju na fakturu. U ovoj temi nalaze se pojedinosti o tome kako se te računovodstvene pojedinosti mogu prilagoditi u nacrtu prijedloga fakture za projekt.

## <a name="adjust-sales-tax"></a>Prilagodba poreza na promet

Zadane grupe poreza na promet za naplatu i grupe poreza na promet za stavke mogu se prilagoditi izravno na dokumentu prijedloga fakture. Kako biste prilagodili ove grupe, odaberite **Uredi**, a zatim u svaki redak prijedloga fakture za projekt unesite novu vrijednost u polje **Grupa poreza na promet** ili **Grupa poreza na promet za stavku**.

## <a name="adjust-financial-dimensions"></a>Prilagodba financijskih veličina

Financijske veličine ne mogu se uređivati izravno na retku prijedloga fakture za projekt. Umjesto toga, slijedite ove korake za prilagodbu financijskih veličina na prijedlogu fakture za projekt.

1. Na prijedlogu fakture za projekt odaberite **Izbriši sve** kako biste uklonili retke prijedloga fakture za projekt.

    > [!NOTE]
    > Gumb **Izbriši sve** dostupan je samo nakon što administrator sustava omogući značajku **Izbriši retke prijedloga fakture pri uporabi aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha** u radnom prostoru **Upravljanje značajkama**.

2. Prilagodba financijskih veličina:

    - **Transakcije po obračunu (kontrolne točke za naplatu):** Idite na **Svi projekti** \> **Upravljaj** \> **Transakcije po obračunu** i odaberite kontrolnu točku koju treba prilagoditi. Zatim, na kartici **Financijske veličine** ažurirajte vrijednosti prema potrebi.
    - **Transakcije vremena, troška i materijala:** Na stranici **Proknjižene projektne transakcije** odaberite **Prilagodi računovodstvo** kako biste ažurirali financijske veličine.

3. Nakon što završite s prilagodbom vrijednosti financijskih veličina, idite na stavku **Upravljanje projektima i računovodstvo** \> **Povremeno** \> **Integracija aplikacije Project Operations** i odaberite **Uvoz iz tablice faza** kako biste pokrenuli povremeni postupak. Taj postupak upotrebljava ažurirane vrijednosti financijske veličine za ponovno stvaranje redaka prijedloga fakture za projekt. Ažurirane se vrijednosti zatim upotrebljavaju u sporednoj knjizi i glavnoj knjizi projekta kada se knjiži faktura za projekt.
