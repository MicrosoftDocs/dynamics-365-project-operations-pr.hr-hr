---
title: Uklonjene ili zastarjele značajke u sustavu Dynamics 365 Project Operations
description: Ovaj tema opisuje značajke koje su uklonjene ili koje su planirane za uklanjanje iz sustava Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601561"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Uklonjene ili zastarjele značajke u sustavu Dynamics 365 Project Operations

_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima / bez zaliha, jednostavne implementacije – od sklapanja posla do predračuna i Project Operations za scenarije koji se temelje na zalihama / proizvodnji_

Ovaj tema opisuje značajke koje su uklonjene ili koje su planirane za uklanjanje iz sustava Dynamics 365 Project Operations.

- Značajka *uklonjeno* više nije dostupna u proizvodu.
- Značajka *zastarjelo* ne nalazi se u aktivnom razvoju i u nekom budućem ažuriranju može biti uklonjena.

Namjena je ovog popisa da vam pomogne pri uzimanju u obzir tih uklanjanja i ukidanja za vlastito planiranje.

> [!NOTE]
> Detaljne informacije o objektima u aplikacijama Financije i operacije mogu se pronaći u tehničkim [**referentnim izvješćima**](/dynamics/s-e/global/axtechrefrep_61). Možete usporediti različite verzije tih izvješća da biste saznali više o objektima koji su se promijenili ili uklonili u svakoj verziji aplikacija Za financije i operacije.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Značajke uklonjene ili zastarjele u izdanju Projektne operacije u ožujku 2022.

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametar upravljanja projektima i računovodstva "Uvijek stvori transakciju prilagodbe"

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Transakcije prilagodbe potrebne su za potrebe revizije. Nakon ukidanja, ovaj parametar će biti skriven. Sustav će uvijek kreirati transakcije prilagodbe, baš kao što to trenutno čini kada je parametar postavljen na **Da**. |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Projektne operacije za proizvodne/opskrbljene scenarije |
| **Status** | Zastarjelo: Do 1. ožujka 2023. sakrit ćemo parametar i promijeniti ponašanje sustava tako da se uvijek stvaraju transakcije prilagodbe. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametar upravljanja projektima i računovodstva "Koristi datum prilagodbe kao novi datum projekta"

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Ovaj je parametar izvorno korišten za omogućavanje podešavanja prilikom zatvaranja poslovni period. Međutim, to više nije potrebno, jer se računovodstveni datum transakcije može promijeniti na prvi datum otvorenog razdoblja, ako je konfiguriran. Datum projekta ne smije se mijenjati jer predstavlja datum kada je došlo do transakcije. |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Projektne operacije za proizvodne/opskrbljene scenarije |
| **Status** | Zastarjelo: Do 1. ožujka 2023. sakrit ćemo parametar i promijeniti ponašanje sustava tako da se datum projekta nikada ne mijenja pri prilagodbama. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Tijek rada zahtjeva za resursom u operacijama projekta za scenarije temeljene na zalihama/proizvodnji

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Zastarjelo zbog niske upotrebe i ograničenja obujma transakcija. |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Projektne operacije za proizvodne/opskrbljene scenarije |
| **Status** | Zastarjelo: Do 1. ožujka 2023. onemogućit ćemo mogućnost traženja resursa za projekt pomoću tijeka rada. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stranica prijedloga fakture za projekt bez prikaza Zaglavlje i Reci

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Zastarjelo zbog poboljšanja stranice koja je uvedena zajedno s obrascima Koristi prijedlog fakture za projekt i temeljnice **faktura s ključem značajke Zaglavlja i Reci**. |
| **Zamijenjeno drugom značajkom?** | Jest |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Projektne operacije za proizvodne/opskrbljene scenarije; Projektne operacije za scenarije resursa/ nenaseljenih resursa |
| **Status** | Zastarjelo: Do 1. ožujka 2023. isključit ćemo raniju (naslijeđenu) stranicu i uključiti obrasce Koristi prijedlog fakture za projekt i temeljnicu **faktura pomoću ključa značajke Zaglavlja i Redaka** prema zadanim postavkama. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Značajke uklonjene ili zastarjele u izdanju Project Operations iz prosinca 2021.

### <a name="collaboration-workspaces"></a>Radni prostori za suradnju

[Stvaranje radnog prostora za suradnju (Project) ili povezivanje s njim](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Zastarjelo zbog niske uporabe. Korisnici koji koriste projektne operacije za scenarije resursa/ne zaliha mogu iskoristiti [suradnju s grupama](../project-management/collaboration-groups.md) sustava Office. |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija  |
| **Mogućnost implementacije** | Projektne operacije za proizvodne/opskrbljene scenarije |
| **Status** | Zastarjelo: Do 1. prosinca 2022. planiramo više ne podržavati radne prostore suradnje. |
