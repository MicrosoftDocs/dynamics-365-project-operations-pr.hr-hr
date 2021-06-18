---
title: Definiranje kalendara projekata
description: U ovoj temi nalaze se informacije o tome kako primijeniti predložak kalendara na projekt kako bi se pratio raspored projekta.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998987"
---
# <a name="define-project-calendars"></a><span data-ttu-id="b0a64-103">Definiranje kalendara projekata</span><span class="sxs-lookup"><span data-stu-id="b0a64-103">Define project calendars</span></span>

<span data-ttu-id="b0a64-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b0a64-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0a64-105">Kako biste stvorili projekt i upravljali njime, na projekt morate primijeniti predložak kalendara.</span><span class="sxs-lookup"><span data-stu-id="b0a64-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="b0a64-106">Predložak kalendara definira sljedeće atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="b0a64-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="b0a64-107">Radno vrijeme, uključujući vrijeme početka i završetka</span><span class="sxs-lookup"><span data-stu-id="b0a64-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="b0a64-108">Radni dani</span><span class="sxs-lookup"><span data-stu-id="b0a64-108">Working days</span></span>
- <span data-ttu-id="b0a64-109">Iznimke kalendara poput neradnih dana</span><span class="sxs-lookup"><span data-stu-id="b0a64-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="b0a64-110">Predložak kalendara koji se primjenjuje na projekt kopija je predloška kalendara definiranog u postavkama vaše tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="b0a64-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="b0a64-111">Ako promijenite predložak kalendara, te se promjene neće proširiti na radno vrijeme projekta.</span><span class="sxs-lookup"><span data-stu-id="b0a64-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="b0a64-112">Kako biste promijenili radno vrijeme projekta, morate primijeniti novi obrazac.</span><span class="sxs-lookup"><span data-stu-id="b0a64-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="b0a64-113">Dva su osnovna zahtjeva za stvaranje predloška kalendara za vašu tvrtku ili ustanovu:</span><span class="sxs-lookup"><span data-stu-id="b0a64-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="b0a64-114">Definirajte željeno radno vrijeme predloška s pomoću novog ili postojećeg resursa koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="b0a64-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="b0a64-115">Stvorite novi predložak kalendara i povežite ga s resursom koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="b0a64-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="b0a64-116">**Definiranje radnog vremena predloška**</span><span class="sxs-lookup"><span data-stu-id="b0a64-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="b0a64-117">Otvorite **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="b0a64-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="b0a64-118">Stvorite novi resurs za referencu u predlošku kalendara ili odaberite postojeći.</span><span class="sxs-lookup"><span data-stu-id="b0a64-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="b0a64-119">Odaberite karticu **Radno vrijeme** resursa i dovršite upute iz članka [Postavljanje radnog vremena za resurs](/dynamics365/field-service/set-work-hours-resource.md) kako biste konfigurirali pravila kalendara.</span><span class="sxs-lookup"><span data-stu-id="b0a64-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="b0a64-120">**Stvaranje novog predloška kalendara**</span><span class="sxs-lookup"><span data-stu-id="b0a64-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="b0a64-121">Idite na **Postavke** \> **Predložak kalendara**.</span><span class="sxs-lookup"><span data-stu-id="b0a64-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="b0a64-122">Odaberite **Novi** i unesite naziv, opis i resurs predloška.</span><span class="sxs-lookup"><span data-stu-id="b0a64-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="b0a64-123">Kada se u predlošku kalendara upućuje na resurs, kopija kalendara resursa povezuje se s predloškom kalendara.</span><span class="sxs-lookup"><span data-stu-id="b0a64-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="b0a64-124">Ako se promijeni radno vrijeme kopiranog predloška, te se promjene neće proširiti na predložak kalendara.</span><span class="sxs-lookup"><span data-stu-id="b0a64-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="b0a64-125">Sada možete povezati predložak rada s predloškom kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="b0a64-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

