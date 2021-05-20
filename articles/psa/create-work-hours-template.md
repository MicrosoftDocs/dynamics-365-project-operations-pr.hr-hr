---
title: Stvaranje predloška radnog vremena
description: U ovoj temi opisuje se način stvaranja predloška radnog vremena u aplikaciji Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981246"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="00f0f-103">Izradi predložak radnog vremena (Project Service)</span><span class="sxs-lookup"><span data-stu-id="00f0f-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="00f0f-104">Kako biste stvorili projekt i upravljali njime, na projekt morate primijeniti predložak kalendara.</span><span class="sxs-lookup"><span data-stu-id="00f0f-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="00f0f-105">Predložak kalendara definira sljedeće atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="00f0f-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="00f0f-106">Radno vrijeme, uključujući vrijeme početka i završetka</span><span class="sxs-lookup"><span data-stu-id="00f0f-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="00f0f-107">Radni dani</span><span class="sxs-lookup"><span data-stu-id="00f0f-107">Working days</span></span>
- <span data-ttu-id="00f0f-108">Iznimke kalendara poput neradnih dana</span><span class="sxs-lookup"><span data-stu-id="00f0f-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="00f0f-109">Predložak kalendara koji se primjenjuje na projekt kopija je predloška kalendara definiranog u postavkama vaše tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="00f0f-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="00f0f-110">Ako promijenite predložak kalendara, te se promjene neće proširiti na radno vrijeme projekta.</span><span class="sxs-lookup"><span data-stu-id="00f0f-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="00f0f-111">Kako biste promijenili radno vrijeme projekta, morate primijeniti novi obrazac.</span><span class="sxs-lookup"><span data-stu-id="00f0f-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="00f0f-112">Dva su osnovna zahtjeva za stvaranje predloška kalendara za vašu tvrtku ili ustanovu:</span><span class="sxs-lookup"><span data-stu-id="00f0f-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="00f0f-113">Definirajte željeno radno vrijeme predloška s pomoću novog ili postojećeg resursa koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="00f0f-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="00f0f-114">Stvorite novi predložak kalendara i povežite ga s resursom koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="00f0f-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="00f0f-115">**Definiranje radnog vremena predloška**</span><span class="sxs-lookup"><span data-stu-id="00f0f-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="00f0f-116">Otvorite **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="00f0f-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="00f0f-117">Stvorite novi resurs za referencu u predlošku kalendara ili odaberite postojeći.</span><span class="sxs-lookup"><span data-stu-id="00f0f-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="00f0f-118">Odaberite karticu **Radno vrijeme** resursa i dovršite upute iz članka [Postavljanje radnog vremena za resurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) kako biste konfigurirali pravila kalendara.</span><span class="sxs-lookup"><span data-stu-id="00f0f-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="00f0f-119">**Stvaranje novog predloška kalendara**</span><span class="sxs-lookup"><span data-stu-id="00f0f-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="00f0f-120">Idite na **Postavke** \> **Predložak kalendara**.</span><span class="sxs-lookup"><span data-stu-id="00f0f-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="00f0f-121">Odaberite **Novi** i unesite naziv, opis i resurs predloška.</span><span class="sxs-lookup"><span data-stu-id="00f0f-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="00f0f-122">Kada se u predlošku kalendara upućuje na resurs, kopija kalendara resursa povezuje se s predloškom kalendara.</span><span class="sxs-lookup"><span data-stu-id="00f0f-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="00f0f-123">Ako se promijeni radno vrijeme kopiranog predloška, te se promjene neće proširiti na predložak kalendara.</span><span class="sxs-lookup"><span data-stu-id="00f0f-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="00f0f-124">Pogledajte također</span><span class="sxs-lookup"><span data-stu-id="00f0f-124">See Also</span></span>  
 [<span data-ttu-id="00f0f-125">Postavljanje resursa</span><span class="sxs-lookup"><span data-stu-id="00f0f-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
