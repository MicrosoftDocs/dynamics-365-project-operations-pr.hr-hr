---
title: Implementiranje aplikacije Project Operations – jednostavno
description: U ovoj temi nalaze se informacije o načinu instalacije implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 14912c612bbf04e232ce712e52330c7bb43eab9f3f8ffa9223a2d2f9ce95eb72
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991567"
---
# <a name="deploy-project-operations---lite"></a>Implementiranje aplikacije Project Operations – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations podržava višestruke modele implementacije. Kako biste odredili najbolji model implementacije, pogledajte odjeljak [Vrste implementacije](determine-deployment-type.md).


> [!IMPORTANT]
> Ova implementacija, jednostavna implementacija – od sklapanja posla do predračuna, rezultira uslugom **Common Data Service – uvođenje samo aplikacije Project Operations**.

- [Instalacija aplikacije Project Operations u novo CDS okruženje](#new)
- [Instalacija u postojeće CDS okruženje](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Instalacija aplikacije Project Operations u novo CDS okruženje

1. Kao [Globalni administrator ili administrator aplikacije Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations stvorite novo CDS okruženje u [Administratorskom centru aplikacije PowerPlatform](https://admin.powerplatform.com). Provjerite jesu li omogućeni **CDS baza podataka** i **Aplikacije sustava Dynamics 365**. Dodatne informacije potražite u odjeljku [Stvaranje okruženja i upravljanje njima u centru za administratore usluge Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. S popisa za implementaciju aplikacija Dynamics 365 odaberite **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Instalacija aplikacije Project Operations u postojeće CDS okruženje

1. Kao [Globalni administrator ili administrator usluge Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations, pronađite okruženje u [Centru za administratore usluge PowerPlatform](https://admin.powerplatform.com) gdje želite instalirati aplikaciju Project Operations.
2. S popisa za implementaciju aplikacija Dynamics 365 instalirajte **Microsoft Dynamics 365 Project Operations**. Dodatne informacija potražite u članku [Upravljanje aplikacijama sustava Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]