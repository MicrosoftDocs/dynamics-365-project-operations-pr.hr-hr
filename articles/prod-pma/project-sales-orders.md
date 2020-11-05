---
title: Projektni prodajni nalozi za vremenske i materijalne projekte
description: U ovoj se temi objašnjava način stvaranja prodajnih naloga na temelju projekata za vremenske i materijalne projekte.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073373"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="f1acf-103">Projektni prodajni nalozi za vremenske i materijalne projekte</span><span class="sxs-lookup"><span data-stu-id="f1acf-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f1acf-104">U ovoj temi opisuje se način stvaranja prodajnog naloga za projekt.</span><span class="sxs-lookup"><span data-stu-id="f1acf-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="f1acf-105">Prodajni nalozi mogu se stvarati samo za projekte vrste **vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="f1acf-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="f1acf-106">Ako projekt za vrijeme i materijal ima više izvora financiranja na ugovoru o projektu, morate omogućiti parametar **Omogući prodajne naloge za projekte s više izvora financiranja** na stranici **Parametri upravljanja projektom i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="f1acf-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="f1acf-107">Podrška za projektne prodajne naloge s više izvora financiranja dostupna je počevši od izdanja aplikacije 10.0.2 i novijeg.</span><span class="sxs-lookup"><span data-stu-id="f1acf-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="f1acf-108">Parametar za omogućivanje podrške za projektne prodajne naloge s više izvora financiranja uklonit će se u valu izdanja za travanj 2020., nakon čega će funkcionalnost uvijek biti omogućena.</span><span class="sxs-lookup"><span data-stu-id="f1acf-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="f1acf-109">Prodajne naloge na temelju projekta možete stvoriti na dva načina:</span><span class="sxs-lookup"><span data-stu-id="f1acf-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="f1acf-110">Idite na sam projekt.</span><span class="sxs-lookup"><span data-stu-id="f1acf-110">Go to the project itself.</span></span> <span data-ttu-id="f1acf-111">U Oknu radnji odaberite **Upravljanje > Zadaci stavke > Prodajni nalog**.</span><span class="sxs-lookup"><span data-stu-id="f1acf-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="f1acf-112">Podaci o projektu zadavat će se prodajnom nalogu iz projekta.</span><span class="sxs-lookup"><span data-stu-id="f1acf-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="f1acf-113">Ako ugovor o projektu ima više izvora financiranja, morat ćete odabrati izvor financiranja kako biste postavili klijenta za prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="f1acf-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="f1acf-114">Ako postoji samo jedan izvor financiranja projekta, klijent će se automatski postaviti.</span><span class="sxs-lookup"><span data-stu-id="f1acf-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="f1acf-115">Idite na stranicu s popisom **Svi prodajni nalozi** i stvorite novi prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="f1acf-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="f1acf-116">Morat ćete odabrati projekt za prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="f1acf-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="f1acf-117">Nakon odabira projekta postavit će se klijent iz izvora financiranja ili, ako ugovor o projektu ima više izvora financiranja, morat ćete odabrati izvor financiranja.</span><span class="sxs-lookup"><span data-stu-id="f1acf-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

