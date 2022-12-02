---
title: Implementiranje aplikacije Project Operations – jednostavno
description: U ovom se članku navode informacije o načinu instalacije implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930309"
---
# <a name="deploy-project-operations---lite"></a>Implementiranje aplikacije Project Operations – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_



Project Operations podržava višestruke modele implementacije. Kako biste odredili najbolji model implementacije, pogledajte odjeljak [Vrste implementacije](determine-deployment-type.md).


> [!IMPORTANT]
> Ova implementacija, jednostavna implementacija – od sklapanja posla do predračuna, rezultira uslugom **Dataverse – uvođenje samo aplikacije Project Operations**.

- [Instalacija aplikacije Project Operations u novo Dataverse okruženje](#new)
- [Instalacija u postojeće Dataverse okruženje](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instalacija aplikacije Project Operations u novo Dataverse okruženje

1. Kao [Globalni administrator ili administrator aplikacije Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations izradite novo Dataverse okruženje u [Administratorskom centru aplikacije PowerPlatform](https://admin.powerplatform.com). Provjerite jesu li stavke **Izradi bazu podataka za ovo okruženje** i **Aplikacije Dynamics 365** omogućene. Dodatne informacije potražite u odjeljku [Stvaranje okruženja i upravljanje njima u centru za administratore usluge Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. S popisa za implementaciju aplikacija Dynamics 365 odaberite **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalacija aplikacije Project Operations u postojeće Dataverse okruženje
1. Uvjerite se da okruženje nije konfigurirano s [dvostrukim pisanjem](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) jer će instalacija tada instalirati mogućnosti [aplikacije Project Operations za scenarije temeljene na resursu / bez zaliha](project-operations-integrated-deployment-overview.md).
2. Kao [Globalni administrator ili administrator usluge Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations, pronađite okruženje u [Centru za administratore usluge PowerPlatform](https://admin.powerplatform.com) gdje želite instalirati aplikaciju Project Operations.
3. S popisa za implementaciju aplikacija Dynamics 365 instalirajte **Microsoft Dynamics 365 Project Operations**. Dodatne informacija potražite u članku [Upravljanje aplikacijama sustava Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
