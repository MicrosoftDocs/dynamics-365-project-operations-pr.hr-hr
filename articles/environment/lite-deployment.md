---
title: Implementacija projektnih operacija Lite
description: U ovom se članku navode informacije o načinu instalacije implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810969"
---
# <a name="deploy-project-operations-lite"></a>Implementacija projektnih operacija Lite

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_



Project Operations podržava višestruke modele implementacije. Kako biste odredili najbolji model implementacije, pogledajte odjeljak [Vrste implementacije](determine-deployment-type.md).


> [!IMPORTANT]
> Ova implementacija, jednostavna implementacija – od sklapanja posla do predračuna, rezultira uslugom **Dataverse – uvođenje samo aplikacije Project Operations**.

- [Instalacija aplikacije Project Operations u novo Dataverse okruženje](#new)
- [Instalacija u postojeće Dataverse okruženje](#existing)
- [Instalirajte u postojeće Dataverse okruženje s dvostrukim komponentama pisanja](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Instalacija programa Project Operations Lite u novo Dataverse okruženje

1. Kao [Globalni administrator ili administrator aplikacije Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations izradite novo Dataverse okruženje u [Administratorskom centru aplikacije PowerPlatform](https://admin.powerplatform.com). Provjerite jesu li stavke **Izradi bazu podataka za ovo okruženje** i **Aplikacije Dynamics 365** omogućene. Dodatne informacije potražite u odjeljku [Stvaranje okruženja i upravljanje njima u centru za administratore usluge Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. S popisa za implementaciju aplikacija Dynamics 365 odaberite **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instalacija programa Project Operations Lite u postojeće Dataverse okruženje 
1. Kao [Globalni administrator ili administrator usluge Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations, pronađite okruženje u [Centru za administratore usluge PowerPlatform](https://admin.powerplatform.com) gdje želite instalirati aplikaciju Project Operations.
1. S popisa za implementaciju aplikacija Dynamics 365 instalirajte **Microsoft Dynamics 365 Project Operations**. Dodatne informacija potražite u članku [Upravljanje aplikacijama sustava Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Instalirajte Project Operations Lite u postojeće Dataverse okruženje u kojem su već prisutna rješenja za dvostruko pisanje

Ako želite nastaviti s pokretanjem projektnih operacija u načinu implementacije sustava Lite, slijedite ove korake:

1. Kao [Globalni administrator ili administrator usluge Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations, pronađite okruženje u [Centru za administratore usluge PowerPlatform](https://admin.powerplatform.com) gdje želite instalirati aplikaciju Project Operations.
1. S popisa za implementaciju aplikacija Dynamics 365 instalirajte **Microsoft Dynamics 365 Project Operations**. Dodatne informacija potražite u članku [Upravljanje aplikacijama sustava Dynamics 365](/power-platform/admin/manage-apps).
1. Budući da vaše okruženje ima instalirane dvostruke komponente pisanja koje pomažu u integraciji s instaliranim aplikacijama za financiranje i operacije, instalacija Project Operations također će instalirati mogućnosti i proširenja potrebna za integraciju podataka povezanih s projektom u financijske i operativne aplikacije. Budući da želite pokrenuti projektne operacije u implementaciji Litea, te komponente integracije treba ukloniti jer će stvoriti ograničenja i režijske troškove za scenarije implementacije Litea. Ručno deinstalirajte rješenja **Dynamics 365 Project Operations Karte dvostrukog pisanja** i **Dynamics 365 Project Operations dvostrukog pisanja da** biste uklonili te komponente.
1. Otvorite **Project Operations -> Settings -> Parametri**. Otvorite stranicu s detaljima o **parametru**  **projekta i postavite polje Ponašanje nadogradnje** rješenja samo na **Lite.** Time se osigurava da sve naknadne nadogradnje projektnih operacija neće vratiti komponente integracije u projektne operacije.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
