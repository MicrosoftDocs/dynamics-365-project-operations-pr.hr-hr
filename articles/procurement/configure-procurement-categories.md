---
title: Kategorije nabave upotrebljavajte s projektnim narudžbenicama i fakturama dobavljača na čekanju
description: U ovom se članku opisuje kako konfigurirati kategorije nabave koje se mogu upotrebljavati s projektnim narudžbenicama i fakturama dobavljača na čekanju.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028601"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Kategorije nabave upotrebljavajte s projektnim narudžbenicama i fakturama dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Stručnjaci za nabavu mogu izraditi i održavati kataloge artikala i usluga koji se mogu koristiti u projektnim narudžbenicama i fakturama dobavljača na čekanju. [Katalozi nabave](/dynamics365/supply-chain/procurement/procurement-catalogs) pružaju vam jednostavan način kategoriziranja kupnji bez potrebe za konfiguriranjem i korištenjem objavljenog kataloga proizvoda. Svaka kategorija nabave može se preslikati u kategoriju projekta za transakcije vremena, troškova ili stavki. Nakon knjiženja fakture dobavljača na čekanju koja koristi kategoriju nabave, sustav će izraditi stvarne podatke o vremenu, trošku ili materijalu, projektne transakcije i unose u pomoćnu knjigu.

## <a name="minimum-version-requirements"></a>Zahtjevi za minimalnom verzijom

Sljedeće su verzije potrebne za upotrebu kategorija nabave s projektnim narudžbenicama za scenarije bez zaliha/temeljene na resursima u sustavu Microsoft Dynamics 365 Project Operations:

- Verzija rješenja Project Operations Dataverse 4.41.0.45 ili novija
- Verzija okruženja Financije i operacije 10.0.26 ili novija

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Pokretanje karata dvostrukog zapisivanja za podršku za kategoriju nabave

Uvjerite se da se za preslikavanje entiteta izvoza retka fakture dobavljača projekata integracije aplikacije **Project Operations msdyn\_projectvendorinvoicelines** upotrebljava verzija 1.0.0.4 ili novija.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Omogućivanje značajke ključa za kategorije nabave

Slijedite ove korake kako biste omogućili funkcije za korištenje kategorija nabave s narudžbenicama projekta.

1. U aplikaciji Dynamics 365 Finance otvorite radni prostor **Upravljanje značajkama**.
1. Na popisu značajki pronađite značajku **Upotrijebi kategorije nabave u aplikaciji Project Operations za scenarije koji se temelje na resursima / bez zaliha**, a zatim odaberite **Omogući**.

> [!IMPORTANT]
> Kao preduvjet, također morate omogućiti značajku **Omogući fakture dobavljača na čekanju u aplikaciji Project Operations za scenarije koji se temelje na resursima / bez zaliha**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Preslikavanje kategorija projekta u hijerarhiji kategorija nabave

Slijedite ove korake za preslikavanje kategorija projekta u kategorije nabave u hijerarhiji **Kategorija nabave**:

1. Idite na **Nabava i dobavljanje \> Kategorije nabave**.
1. Odaberite **Uredi hijerarhiju kategorije**.
1. Odaberite željeni čvor hijerarhije kategorije, a zatim na kartici **Dodijeli kategorije projekta** povežite čvor s kategorijom projekta iz kategorije **Vrijeme**, **Trošak** ili **Stavka projekta** (to jest, kategoriju **Zadano vrijeme** ili **Zadani trošak**).
1. Odaberite **Spremi**.
1. Zatvorite stranicu.

> [!NOTE]
> Preslikavanje kategorije nabave u kategoriju projekta nije obavezno. Ako kategorija nabave nije preslikana, sustav će upotrijebiti vrijednosti određenu u polju **Stavka** u odjeljku **Zadane postavke kategorije projekta** na kartici **Project Operations u sustavu Dynamics 365 Customer engagement** na stranici **Upravljanje projektom i računovodstveni parametri**.
