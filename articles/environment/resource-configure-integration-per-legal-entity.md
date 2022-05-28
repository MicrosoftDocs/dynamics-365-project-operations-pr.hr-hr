---
title: Konfiguriranje integracije aplikacije Project Operations po pravnoj osobi
description: U ovoj temi nalaze se informacije o postavljanju integracije po pravnoj osobi u aplikaciji Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585829"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfiguriranje integracije aplikacije Project Operations po pravnoj osobi 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi prolazite korake potrebne za konfiguriranje aplikacije Dynamics 365 Project Operations po pravnoj osobi.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Omogućivanje tipki sa značajkama u Dynamics 365 Finance

Poduzmite sljedeće korake kako biste omogućili potrebne značajke.

1. U Dynamics 365 Finance idite na **radni prostor za upravljanje** značajkama.
2. U mogućnosti **Popis značajki** pronađite i omogućite sljedeće značajke:
  
    - **Omogući više redaka ugovora za projekt**
    - **Omogući projektne operacije na Dynamics 365 Customer Engagement**

> [!NOTE]
> Ako ne vidite popis **Tipke značajki** provjerite ispunjava li vaša verzija programa Financije minimalni preduvjet (verzija aplikacije 10.0.13 sa svim primijenjenim kvalitativnim ažuriranjima ili novija). Odaberite **Provjeri ima li ažuriranja** za osvježavanje popisa značajki.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definirajte scenarij implementacije aplikacije Project Operations za pravnu osobu

Projektne operacije možete omogućiti na Dynamics 365 Customer Engagement na razini pravne osobe. Možete imati jednu pravnu osobu koja koristi projektne operacije na Dynamics 365 Customer Engagement za scenarije koji se temelje na resursima/neutemeljenim resursima. U istom okruženju možete imati drugu pravnu osobu koja upotrebljava aplikaciju Project Operations za scenarije na zalihi / proizvodni nalog.

1. U Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Global projektnih i računovodstvenih parametara**.
2. Na popisu dostupnih pravnih osoba odaberite entitete u kojima će biti omogućeno više redaka ugovora i projektnih operacija na Dynamics 365 Customer Engagement značajkama. Ostavite neodabrane pravne osobe koje će upotrebljavati aplikaciju Project Operations za scenarije na zalihi / proizvodni nalog.

> [!NOTE]
> Pravna osoba može se odabrati samo ako nema postojeće projekte.

## <a name="configure-project-management-and-accounting-parameters"></a>Parametri konfiguracije Upravljanja projektom i računovodstva

Svaka pravna osoba koja koristi projektne operacije na Dynamics 365 Customer Engagement treba skup zadanih parametara. Ovi su parametri konfigurirani na kartici **Projektne operacije** na stranici **Parametri Upravljanja projektom i računovodstva**. Parametri su sljedeći:

  - **Zadane postavke vrste naplate**: Project Operations upotrebljava fiksni skup zadanih postavki vrsta naplate koje se moraju mapirati u svojstva retka aplikacije Financije. Stvorite zapis za svaku vrstu naplate: **Nije specificirano**, **Naplativo**, **Nenaplativo**, **Besplatno** i **Nedostupno**.
  - **Zadane postavke kategorije projekta** : Odaberite zadane kategorije projekata koje će se upotrebljavati za svaku vrstu transakcije. Te će se zadane postavke upotrebljavati u stavci **Dnevnik integracije aplikacije Project Operations** i u procjenama kada za stvarni projekt nije navedena kategorija transakcije.
  - **Predviđanja**: Odaberite model predviđanja koji će se upotrebljavati za procjenu vremena i troškova.


[!INCLUDE[footer-include](../includes/footer-banner.md)]