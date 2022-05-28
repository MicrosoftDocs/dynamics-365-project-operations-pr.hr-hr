---
title: Implementiranje aplikacije Project Operations – jednostavno
description: U ovoj temi nalaze se informacije o načinu instalacije implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580723"
---
# <a name="deploy-project-operations---lite"></a>Implementiranje aplikacije Project Operations – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_



Project Operations podržava višestruke modele implementacije. Kako biste odredili najbolji model implementacije, pogledajte odjeljak [Vrste implementacije](determine-deployment-type.md).


> [!IMPORTANT]
> Ova implementacija, jednostavna implementacija – od sklapanja posla do predračuna, rezultira uslugom **Dataverse – uvođenje samo aplikacije Project Operations**.

- [Instalacija projektnih operacija u novo Dataverse okruženje](#new)
- [Instalacija u postojeće Dataverse okruženje](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Instalacija operacija projekta u novo Dataverse okruženje

1. [Kao globalna ili Power Platform administratorska](/power-platform/admin/global-service-administrators-can-administer-without-license) licenca s programom Project Operations stvorite novo Dataverse okruženje u centru [za administratore dodatka](https://admin.powerplatform.com) PowerPlatform. Provjerite je **li omogućeno stvaranje baze podataka za ovo okruženje** i **aplikacije** sustava Dynamics 365. Dodatne informacije potražite u odjeljku [Stvaranje okruženja i upravljanje njima u centru za administratore usluge Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. S popisa za implementaciju aplikacija Dynamics 365 odaberite **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instalacija operacija projekta u postojeće Dataverse okruženje
1. Provjerite nije li okruženje konfigurirano s dvostrukim [pisanjem](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) jer će instalacija instalirati [projektne operacije za mogućnosti scenarija koji se temelje na resursima/nesadržanim](project-operations-integrated-deployment-overview.md) resursima.
2. Kao [Globalni administrator ili administrator usluge Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations, pronađite okruženje u [Centru za administratore usluge PowerPlatform](https://admin.powerplatform.com) gdje želite instalirati aplikaciju Project Operations.
3. S popisa za implementaciju aplikacija Dynamics 365 instalirajte **Microsoft Dynamics 365 Project Operations**. Dodatne informacija potražite u članku [Upravljanje aplikacijama sustava Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
