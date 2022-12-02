---
title: Uklonjene ili zastarjele značajke u aplikaciji Dynamics 365 Project Operations
description: U ovom se članku opisuju značajke koje su uklonjene ili je planirano njihovo uklanjanje iz aplikacije Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028320"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Uklonjene ili zastarjele značajke u aplikaciji Dynamics 365 Project Operations

_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima / bez zaliha, jednostavne implementacije – od sklapanja posla do predračuna i Project Operations za scenarije koji se temelje na zalihama / proizvodnji_

U ovom se članku opisuju značajke koje su uklonjene ili je planirano njihovo uklanjanje iz aplikacije Dynamics 365 Project Operations.

- Značajka *uklonjeno* više nije dostupna u proizvodu.
- Značajka *zastarjelo* ne nalazi se u aktivnom razvoju i u nekom budućem ažuriranju može biti uklonjena.

Namjena je ovog popisa da vam pomogne pri uzimanju u obzir tih uklanjanja i ukidanja za vlastito planiranje.

> [!NOTE]
> Podrobne informacije o objektima u aplikacijama za financije i operacije možete pronaći u članku [**Tehnička referentna izvješća**](/dynamics/s-e/global/axtechrefrep_61). Možete usporediti različite verzije ovih izvješća kako biste saznali više o objektima koji su promijenjeni ili uklonjeni u svakoj verziji aplikacija za financije i operacije.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Značajke koje su uklonjene ili zastarjele u izdanju aplikacije Project Operations iz ožujka 2022.

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametar „Uvijek stvori transakciju usklađenja” u Upravljanju projektima i računovodstvu

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Transakcije usklađenja potrebne su u svrhe revizije. Taj će parametar biti skriven nakon ukidanja. Sustav će uvijek stvarati transakcije usklađenja, baš kao što to trenutačno čini kada je parametar postavljen na **Da**. |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Project Operations za scenarije utemeljene na proizvodnji/zalihama |
| **Stanje** | Zastarjelo: do 1. ožujka 2023. sakrit ćemo parametar i promijeniti ponašanje sustava tako da se transakcije usklađivanja uvijek stvaraju. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametar „Koristi datum usklađivanja kao novi datum projekta” u Upravljanju projektima i računovodstvu

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Ovaj je parametar izvorno korišten da omogući usklađivanja dok je poslovni period zatvoren. Međutim, to više nije potrebno jer se računovodstveni datum transakcije može promijeniti na prvi datum otvorenog razdoblja, ako je konfiguriran. Datum projekta ne smije se mijenjati jer predstavlja datum kada je transakcija izvršena. |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Project Operations za scenarije utemeljene na proizvodnji/zalihama |
| **Stanje** | Zastarjelo: do 1. ožujka 2023. sakrit ćemo parametar i promijeniti ponašanje sustava tako da se datum projekta nikad ne mijenja prilikom usklađivanja. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Tijek rada zahtjeva za resurs u aplikaciji Project Operations za scenarije koji se temelje na zalihama/proizvodnji

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Zastarjelo zbog rijetkog korištenja i ograničenja količine transakcija. |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Project Operations za scenarije utemeljene na proizvodnji/zalihama |
| **Stanje** | Zastarjelo: do 1. ožujka 2023. onemogućit ćemo opciju zahtijevanja resursa za projekt putem tijeka rada. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stranica prijedloga fakture za projekt bez prikaza zaglavlja i redaka

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Zastarjelo zbog poboljšanja stranice koja su uvedena zajedno s ključem značajke **Koristi obrasce prijedloga projektne fakture i dnevnika faktura s prikazom zaglavlja i redaka**. |
| **Zamijenjeno drugom značajkom?** | Jest |
| **Područja proizvoda na koja se odnosi** | Aplikacija |
| **Mogućnost implementacije** | Project Operations za scenarije proizvodnje/zaliha; Project Operations za scenarije resursa / bez zaliha |
| **Stanje** | Zastarjelo: do 1. ožujka 2023. isključit ćemo raniju (naslijeđenu) stranicu i prema zadanim postavkama uključiti ključ značajke **Koristi obrasce prijedloga projektne fakture i dnevnika faktura s prikazom zaglavlja i redaka**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Značajke koje su uklonjene ili zastarjele u izdanju aplikacije Project Operations iz prosinca 2021.

### <a name="collaboration-workspaces"></a>Radni prostori za suradnju

[Stvaranje ili povezivanje radnog prostora za suradnju (Projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za ukidanje/uklanjanje** | Zastarjelo zbog rijetkog korištenja. Korisnici koji koriste Project Operations za scenarije resursa / bez zaliha mogu iskoristiti značajku [Suradnja s Office grupama](../project-management/collaboration-groups.md). |
| **Zamijenjeno drugom značajkom?** | No |
| **Područja proizvoda na koja se odnosi** | Aplikacija  |
| **Mogućnost implementacije** | Project Operations za scenarije utemeljene na proizvodnji/zalihama |
| **Stanje** | Zastarjelo: do 1. prosinca 2022. planiramo prestati podržavati radne prostore za suradnju. |
