---
title: Korištenje kategorija nabave s narudžbenicama za projekt i fakturama dobavljača na čekanju
description: U ovom se članku opisuje kako konfigurirati kategorije nabave koje se mogu koristiti s narudžbenicama za projekt i fakturama dobavljača na čekanju.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Korištenje kategorija nabave s narudžbenicama za projekt i fakturama dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Stručnjaci za nabavu mogu kreirati i održavati kataloge artikala i usluga koji se mogu koristiti u narudžbenicama za projekt i fakturama dobavljača na čekanju. [Katalozi nabave](/dynamics365/supply-chain/procurement/procurement-catalogs) pružaju vam jednostavan način kategorizacije kupnji bez potrebe za konfiguriranjem i korištenjem objavljenog kataloga proizvoda. Svaka kategorija nabave može se mapirati u kategoriju projekta za vrijeme, trošak ili transakcije artikla. Nakon knjiženja fakture dobavljača na čekanju koja koristi kategoriju nabave, sustav će kreirati stvarno stanje vremena, rashoda ili materijala, projektne transakcije i stavke podstavka.

## <a name="minimum-version-requirements"></a>Minimalni zahtjevi za verzijom

Sljedeće verzije potrebne su za korištenje kategorija nabave s narudžbenicama za projektne narudžbenice za Microsoftove Dynamics 365 Project Operations scenarije koji nisu opskrbljeni/resursi:

- Verzija rješenja project operations Dataverse 4.41.0.45 ili novija
- Financijsko i operativno okruženje verzija 10.0.26 ili novija

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Pokretanje karata s dvostrukim pisanjem za podršku u kategoriji nabave

Provjerite koristi li mapiranje za **izvoz retka fakture dobavljača projekta Project Operations za projektne operacije msdyn\_ projectvendorinvoicelines** verziju 1.0.0.4 ili noviju.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Omogućivanje ključa značajki za kategorije nabave

Slijedite ove korake da biste omogućili funkcionalnost korištenja kategorija nabave s narudžbenicama za projekt.

1. U Dynamics 365 Finance otvorite **radni prostor za upravljanje** značajkama.
1. Na popisu značajki pronađite **značajku Koristi kategorije nabave u programskim operacijama za scenarije koji se temelje na resursima/koji nisu obuhvaćeni** resursima, a zatim odaberite **Omogući**.

> [!IMPORTANT]
> Kao preduvjet morate omogućiti i značajku Omogući fakture dobavljačima na čekanju **na projektnim operacijama za scenarije temeljene na resursima/neutemeljenim scenarijima**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapiranje kategorija projekata u hijerarhiji kategorija Nabava

Slijedite ove korake da biste mapirali kategorije projekata u kategorije nabave u hijerarhiji kategorija **Nabava**:

1. Idite na **kategorije nabave i nabave nabave \>**.
1. Odaberite **Uređivanje hijerarhije** kategorija.
1. Odaberite željeni hijerarhijski čvor kategorija, a zatim na **kartici Dodjela kategorija projekta spojite** čvor s kategorijom projekta iz **kategorije Vrijeme**, **Trošak** ili **Projekt** artikla (tj **. kategorije Zadano vrijeme** ili **Zadani trošak**).
1. Odaberite **Spremi**.
1. Zatvorite stranicu.

> [!NOTE]
> Mapiranje kategorije nabave u kategoriju projekta nije obavezno. Ako kategorija nabave nije mapirana, sustav će koristiti vrijednost postavljenu u **polju Artikl** u **odjeljku Zadane vrijednosti kategorije** Projekt na kartici Operacije projekta u **sustavu Dynamics 365 Angažman** kupca **na stranici Parametri upravljanja projektom i računovodstva**.
