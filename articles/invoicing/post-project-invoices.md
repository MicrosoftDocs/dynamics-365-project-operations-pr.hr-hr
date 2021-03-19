---
title: Pregled postupka fakturiranja
description: U ovoj se temi govori o pregledu postupka fakturiranja u aplikaciji Project Operations za scenarije temeljene na resursima / bez zaliha.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275798"
---
# <a name="invoicing-process-overview"></a>Pregled postupka fakturiranja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Scenariji aplikacije Project Operations koji se temelje na resursima /bez zaliha nude sveobuhvatne mogućnosti prilagođene potrebama i voditelja projekta i službenika za potraživanja / računovođe projekta. Za postupak fakturiranja, voditelj projekta upravlja zaostalom naplatom projekta, a službenik za potraživanja / računovođa projekta stvara sukladan i točan dokument fakture za slanje kupcima.

![Dijagram tijeka fakturiranja](./media/invoicing-flow.png)

Redak ugovora o projektu određuje način naplate za povezane projektne transakcije. Kada voditelj projekta odobri transakcije vremena i troškova, sustav bilježi transakcije u entitetu **Stvarni podaci o projektu** i podatke šalje modulu **Upravljanje projektima i računovodstvo** u aplikaciji Dynamics 365 Finance. Računovođa projekta pregledava i knjiži zapise s pomoću [dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md). Ovaj dnevnik uključuje bitne računovodstvene pojedinosti o stvarnim podacima u projektu, poput naplate, grupe poreza na promet, grupe poreza na promet stavki za naplatu i financijskih veličina.

Voditelj projekta može pregledati nefakturirane prodajne transakcije s pomoću načina naplate vremena i materijala u [zaostalim naplatama vremena i materijala](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) i naplate po fiksnoj cijeni u [Kontrolnim točkama fiksne cijene](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Ovi prikazi omogućuju filtriranje i odabir transakcija koje trebaju biti uključene u sljedeći ciklus naplate, a zatim ih označuje kao **Spremno za fakturiranje**.

Možete [ručno stvoriti predračun](../proforma-invoicing/create-manual-proforma-invoice.md) ili upotrijebiti [periodični postupak](../proforma-invoicing/configure-automated-invoice-creation.md). Voditelj projekta može po potrebi [prilagoditi nacrt predračuna](../proforma-invoicing/manage-proforma-invoice.md), a zatim ga potvrditi.

Potvrđeni predračun šalje se modulu **Upravljanje projektima i računovodstvo** u aplikaciji Financije. Računovođa projekta oblikuje i ažurira prijedlog fakture za projekt, a zatim knjiži i ispisuje dokument. Proknjižene fakture za projekt evidentiraju se u Glavnoj knjizi, kao i u pomoćnim knjigama Klijent i Projekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]