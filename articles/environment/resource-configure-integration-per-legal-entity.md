---
title: Konfiguriranje integracije aplikacije Project Operations po pravnoj osobi
description: U ovoj temi nalaze se informacije o postavljanju integracije po pravnoj osobi u aplikaciji Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000067"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfiguriranje integracije aplikacije Project Operations po pravnoj osobi 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi prolazite korake potrebne za konfiguriranje aplikacije Dynamics 365 Project Operations po pravnoj osobi.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Omogućivanje tipki značajki u aplikaciji Dynamics 365 Finance

Poduzmite sljedeće korake kako biste omogućili potrebne značajke.

1. U aplikaciji Dynamics 365 Finance, idite na radni prostor **Upravljanje značajkama**.
2. U mogućnosti **Popis značajki** pronađite i omogućite sljedeće značajke:
  
    - **Omogući više redaka ugovora za projekt**
    - **Omogući aplikaciju Project Operations u sustavu Dynamics 365 Customer Engagement**

> [!NOTE]
> Ako ne vidite popis **Tipke značajki** provjerite ispunjava li vaša verzija programa Financije minimalni preduvjet (verzija aplikacije 10.0.13 sa svim primijenjenim kvalitativnim ažuriranjima ili novija). Odaberite **Provjeri ima li ažuriranja** za osvježavanje popisa značajki.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definirajte scenarij implementacije aplikacije Project Operations za pravnu osobu

Project Operations možete omogućiti u sustavu Dynamics 365 Customer Engagement na razini pravne osobe. Možete imati jednu pravnu osobu koja upotrebljava aplikaciju Project Operations u sutavu Dynamics 365 Customer Engagement za scenarije temeljene na resursima / bez zaliha. U istom okruženju možete imati drugu pravnu osobu koja upotrebljava aplikaciju Project Operations za scenarije na zalihi / proizvodni nalog.

1. U aplikaciji Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Parametri upravljanja projektom i računovodstva**.
2. Na popisu dostupnih pravnih osoba odaberite entitete u kojima će biti omogućeno više redaka ugovora i značajki rješenja Project Operations u aplikaciji Dynamics 365 Customer Engagement. Ostavite neodabrane pravne osobe koje će upotrebljavati aplikaciju Project Operations za scenarije na zalihi / proizvodni nalog.

> [!NOTE]
> Pravna osoba može se odabrati samo ako nema postojeće projekte.

## <a name="configure-project-management-and-accounting-parameters"></a>Parametri konfiguracije Upravljanja projektom i računovodstva

Svaka pravna osoba koja upotrebljava aplikaciju Project Operations u sustavu Dynamics 365 Customer Engagement treba skup zadanih parametara. Ovi su parametri konfigurirani na kartici **Projektne operacije** na stranici **Parametri Upravljanja projektom i računovodstva**. Parametri su sljedeći:

  - **Zadane postavke vrste naplate**: Project Operations upotrebljava fiksni skup zadanih postavki vrsta naplate koje se moraju mapirati u svojstva retka aplikacije Financije. Stvorite zapis za svaku vrstu naplate: **Nije specificirano**, **Naplativo**, **Nenaplativo**, **Besplatno** i **Nedostupno**.
  - **Zadane postavke kategorije projekta** : Odaberite zadane kategorije projekata koje će se upotrebljavati za svaku vrstu transakcije. Te će se zadane postavke upotrebljavati u stavci **Dnevnik integracije aplikacije Project Operations** i u procjenama kada za stvarni projekt nije navedena kategorija transakcije.
  - **Predviđanja**: Odaberite model predviđanja koji će se upotrebljavati za procjenu vremena i troškova.


[!INCLUDE[footer-include](../includes/footer-banner.md)]