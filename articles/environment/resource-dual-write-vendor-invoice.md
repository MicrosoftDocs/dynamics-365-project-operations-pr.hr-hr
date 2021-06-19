---
title: Integracija fakture dobavljača
description: U ovoj temi nalaze se informacije o integraciji fakture dobavljača u aplikaciji Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d4f1b0ad94b71dc4adc5b2b3423340c5fdb171eb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002247"
---
# <a name="vendor-invoice-integration"></a>Integracija fakture dobavljača

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Nabava vezana uz projekt u aplikaciji Dynamics 365 Project Operations može se evidentirati odlaskom na **Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju** i s pomoću dokumenta fakture dobavljača na čekanju. Dodatne informacija potražite u članku [Kupnja materijala koji nisu na zalihi s pomoću fakture dobavljača na čekanju](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Prije nego što upotrijebite funkcionalnost opisanu u ovoj temi, pregledajte i primijenite potrebne konfiguracije. Dodatne informacija potražite u članku [Omogućivanje materijala koji nisu na zalihi i fakture dobavljača na čekanju](../procurement/configure-materials-nonstocked.md).

Fakture dobavljača u aplikaciji Project Operations, koje se odnose na projekt, knjiže se s pomoću posebnih pravila knjiženja:

- Troškovi povezani s projektom (uključujući bespovratni porez) ne knjiže se odmah na račun troškova projekta u glavnoj knjizi. Umjesto toga, trošak se knjiži na **Račun za integraciju nabave**. Taj se račun konfigurira u **Upravljanje projektima i računovodstvo** > **Postavke** > **Upravljanje projektom i računovodstveni parametri** na kartici **Project Operations u aplikaciji Dynamics 365 Customer Engagement**.
- Dvostruko pisanje sinkronizira pojedinosti računa dobavljača s platformom Microsoft Dataverse s pomoću sljedećih karata tablice:

     - **Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoices)**: Ova karta tablice sinkronizira podatke o zaglavlju fakture dobavljača. Samo se fakture dobavljača s barem jednim retkom koji sadrži ID projekta sinkroniziraju s platformom Dataverse.
     - **Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoicelines)**: Ova karta tablice sinkronizira podatke o retku fakture dobavljača. Samo se redci koji sadrže ID projekta sinkroniziraju s platformom Dataverse.

     > [!NOTE]
     > Pojedinosti fakture dobavljača na platformi Dataverse ne mogu se uređivati.

Sporedne računovodstvene knjige za porez, dobavljača i ostala financijska knjiženja evidentiraju se prema potrebi u aplikaciji Dynamics 365 Finance nakon knjiženja fakture dobavljača.

![Integracija fakture dobavljača](media/DW7VendorInvoice.png)

Kada se zapisi upišu u entitet **Faktura dobavljača** na platformi Dataverse započinje postupak automatskog odobravanja zapisa. Ako je potrebno, stanje postupka automatskog odobrenja može se pregledati na platformi Dataverse tako da se ode na **Napredne postavke** > **Sustav** > **Poslovi sustava**. Nakon dovršetka postupka odobravanja, sustav stvara zapise klase transakcija materijala u entitetu **Stvarni podaci**.

Stvarni podaci povezani s materijalom zatim se obrađuju s pomoću karte tablice s dvostrukim pisanjem **Stvarni podaci o integraciji aplikacije Project Operations (msdyn_actuals)**. Dodatne informacije potražite u članku [Procjene i stvarni podaci o projektu](resource-dual-write-estimates-actuals.md).

Povremeni postupak **Uvoz iz pripreme** stvara retke dnevnika integracije aplikacije Project Operations povezane s fakturom dobavljača. Transakcijski je račun zadan za račun integracije nabave. Nakon knjiženja dnevnika integracije briše se saldo računa za transakciju fakture dobavljača i iznos retka premješta se na račun troškova za projekt. Stvaraju se i transakcije sporedne knjige projekta u svrhe nizvodnog fakturiranja i priznavanja prihoda.
