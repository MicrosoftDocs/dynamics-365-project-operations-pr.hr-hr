---
title: Uvođenje jednostavne aplikacije Project Operations – od sklapanja posla do predračuna
description: U ovoj temi nalaze se informacije o načinu instalacije uvođenja jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073252"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="246ae-103">Uvođenje jednostavne aplikacije Project Operations – od sklapanja posla do predračuna</span><span class="sxs-lookup"><span data-stu-id="246ae-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="246ae-104">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="246ae-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="246ae-105">Project Operations podržava višestruke modele uvođenja.</span><span class="sxs-lookup"><span data-stu-id="246ae-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="246ae-106">Kako biste odredili najbolji model uvođenja, pogledajte odjeljak [Vrste uvođenja](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="246ae-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="246ae-107">Ovo uvođenje, jednostavno uvođenje – od sklapanja posla do predračuna, rezultira uslugom **Common Data Service – uvođenje samo aplikacije Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="246ae-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="246ae-108">Instalacija aplikacije Project Operations u novo CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="246ae-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="246ae-109">Instalacija u postojeće CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="246ae-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="246ae-110">Instalacija aplikacije Project Operations u novo CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="246ae-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="246ae-111">Kao [Globalni administrator ili administrator aplikacije Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations stvorite novo CDS okruženje u [Administratorskom centru aplikacije PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="246ae-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="246ae-112">Provjerite jesu li omogućeni **CDS baza podataka** i **Aplikacije sustava Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="246ae-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="246ae-113">Dodatne informacije potražite u odjeljku [Stvaranje okruženja i upravljanje njima u centru za administratore usluge Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="246ae-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="246ae-114">Odaberite **Microsoft Dynamics 365 Project Operations** s popisa za uvođenje aplikacija sustava Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="246ae-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="246ae-115">Instalacija aplikacije Project Operations u postojeće CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="246ae-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="246ae-116">Kao [Globalni administrator ili administrator usluge Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations, pronađite okruženje u [Centru za administratore usluge PowerPlatform](https://admin.powerplatform.com) gdje želite instalirati aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="246ae-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="246ae-117">Instalirajte **Microsoft Dynamics 365 Project Operations** s popisa za uvođenje aplikacija sustava Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="246ae-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="246ae-118">Dodatne informacija potražite u članku [Upravljanje aplikacijama sustava Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="246ae-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


