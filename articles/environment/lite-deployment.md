---
title: Implementiranje aplikacije Project Operations – jednostavno
description: U ovoj temi nalaze se informacije o načinu instalacije implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950255"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="ec3f8-103">Implementiranje aplikacije Project Operations – jednostavno</span><span class="sxs-lookup"><span data-stu-id="ec3f8-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="ec3f8-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="ec3f8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ec3f8-105">Project Operations podržava višestruke modele implementacije.</span><span class="sxs-lookup"><span data-stu-id="ec3f8-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="ec3f8-106">Kako biste odredili najbolji model implementacije, pogledajte odjeljak [Vrste implementacije](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="ec3f8-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="ec3f8-107">Ova implementacija, jednostavna implementacija – od sklapanja posla do predračuna, rezultira uslugom **Common Data Service – uvođenje samo aplikacije Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="ec3f8-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="ec3f8-108">Instalacija aplikacije Project Operations u novo CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="ec3f8-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="ec3f8-109">Instalacija u postojeće CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="ec3f8-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="ec3f8-110">Instalacija aplikacije Project Operations u novo CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="ec3f8-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="ec3f8-111">Kao [Globalni administrator ili administrator aplikacije Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations stvorite novo CDS okruženje u [Administratorskom centru aplikacije PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="ec3f8-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="ec3f8-112">Provjerite jesu li omogućeni **CDS baza podataka** i **Aplikacije sustava Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ec3f8-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="ec3f8-113">Dodatne informacije potražite u odjeljku [Stvaranje okruženja i upravljanje njima u centru za administratore usluge Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="ec3f8-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="ec3f8-114">S popisa za implementaciju aplikacija Dynamics 365 odaberite **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="ec3f8-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="ec3f8-115">Instalacija aplikacije Project Operations u postojeće CDS okruženje</span><span class="sxs-lookup"><span data-stu-id="ec3f8-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="ec3f8-116">Kao [Globalni administrator ili administrator usluge Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencom za aplikaciju Project Operations, pronađite okruženje u [Centru za administratore usluge PowerPlatform](https://admin.powerplatform.com) gdje želite instalirati aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ec3f8-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="ec3f8-117">S popisa za implementaciju aplikacija Dynamics 365 instalirajte **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="ec3f8-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="ec3f8-118">Dodatne informacija potražite u članku [Upravljanje aplikacijama sustava Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="ec3f8-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]