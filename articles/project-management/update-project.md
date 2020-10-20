---
title: Ažuriranje projekta
description: U ovoj temi nalaze se informacije o ažuriranju projekata u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897803"
---
# <a name="update-a-project"></a><span data-ttu-id="62a43-103">Ažuriranje projekta</span><span class="sxs-lookup"><span data-stu-id="62a43-103">Update a project</span></span>

<span data-ttu-id="62a43-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="62a43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="62a43-105">U nastavku je sažetak polja koja se mogu ažurirati na projektu nakon što se on stvori i sve primjenjive implikacije ažuriranja.</span><span class="sxs-lookup"><span data-stu-id="62a43-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="62a43-106">Polja pojedinosti projekta</span><span class="sxs-lookup"><span data-stu-id="62a43-106">Project detail fields</span></span>

- <span data-ttu-id="62a43-107">**Naziv**: Naziv projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="62a43-108">**Opis**: Pregled projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="62a43-109">**Klijent**: Tvrtka kojoj će projekt biti isporučen.</span><span class="sxs-lookup"><span data-stu-id="62a43-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="62a43-110">**Predložak kalendara** : Radno vrijeme projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="62a43-111">Kada se polje promijeni, preračunava se cijeli raspored.</span><span class="sxs-lookup"><span data-stu-id="62a43-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="62a43-112">**Valuta**: Valutu projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="62a43-113">Zadana je za ovo polje na temelju valute definirane u ugovornoj jedinici.</span><span class="sxs-lookup"><span data-stu-id="62a43-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="62a43-114">Kada se ugovorna jedinica ažurira, ažurira se i polje.</span><span class="sxs-lookup"><span data-stu-id="62a43-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="62a43-115">**Ugovorna jedinica**: Organizacijska jedinica koja predstavlja grupu ili odjel poduzeća koja je prvenstveno odgovorna za ostvarivanje prodaje i upravljanje isporukom rada i usluga klijentu.</span><span class="sxs-lookup"><span data-stu-id="62a43-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="62a43-116">**Voditelj projekta**: Član projektnog tima koji ima ovlast pregledavati i odobravati unose vremena i troškove.</span><span class="sxs-lookup"><span data-stu-id="62a43-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="62a43-117">Polja za procjenu</span><span class="sxs-lookup"><span data-stu-id="62a43-117">Estimate fields</span></span>

- <span data-ttu-id="62a43-118">**Procijenjeni datum početka**: Datum kada će započeti projekt.</span><span class="sxs-lookup"><span data-stu-id="62a43-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="62a43-119">Kada se ovo polje ažurira, svi zadaci na projektu kretat će se proporcionalno s početkom novog datuma početka.</span><span class="sxs-lookup"><span data-stu-id="62a43-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="62a43-120">**Datum završetka**: Datum kada je planiran završetak projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="62a43-121">**Rad**: Procijenjeni rad na projektu.</span><span class="sxs-lookup"><span data-stu-id="62a43-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="62a43-122">Kada se zadaci dodaju u projekt, ovo se polje više ne može uređivati.</span><span class="sxs-lookup"><span data-stu-id="62a43-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="62a43-123">**Procijenjeni trošak rada**: Procijenjeni trošak rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="62a43-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="62a43-124">Kada se troškovi rada dodaju u projekt, ovo se polje više ne može uređivati.</span><span class="sxs-lookup"><span data-stu-id="62a43-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="62a43-125">**Procijenjeni troškovi**: Procijenjeni troškovi projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="62a43-126">Kada se troškovi dodaju u projekt, ovo se polje više ne može uređivati.</span><span class="sxs-lookup"><span data-stu-id="62a43-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="62a43-127">Polja projekta sa stvarnim podacima</span><span class="sxs-lookup"><span data-stu-id="62a43-127">Project actual fields</span></span>
- <span data-ttu-id="62a43-128">**Stvarni početak**: Datum početka projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="62a43-129">**Stvarni završetak**: Treba se ažurirati kada se projekt dovrši.</span><span class="sxs-lookup"><span data-stu-id="62a43-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="62a43-130">Statusna polja projekta</span><span class="sxs-lookup"><span data-stu-id="62a43-130">Project status fields</span></span>

- <span data-ttu-id="62a43-131">**Ukupni status projekta**: Ukupno stanje projekta koje osigurava voditelj projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="62a43-132">**Komentari**: Izvješće o trenutačnom stanju projekta koje daje voditelj projekta.</span><span class="sxs-lookup"><span data-stu-id="62a43-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

