---
title: Definiranje kalendara projekata
description: U ovoj se temi nalaze informacije o načinu uporabe kalendara projekta za praćenje rasporeda projekata.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073562"
---
# <a name="define-project-calendars"></a><span data-ttu-id="78233-103">Definiranje kalendara projekata</span><span class="sxs-lookup"><span data-stu-id="78233-103">Define project calendars</span></span>

<span data-ttu-id="78233-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="78233-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="78233-105">Da biste stvorili raspored projekta, stvorite predložak kalendara projekta koji definira radno vrijeme po danu i neradno vrijeme.</span><span class="sxs-lookup"><span data-stu-id="78233-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="78233-106">Da biste stvorili predložak kalendara projekta, povežite radni predložak s poljem **Predložak kalendara** za projekt.</span><span class="sxs-lookup"><span data-stu-id="78233-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="78233-107">Poduzmite ove korake da biste stvorili radni predložak.</span><span class="sxs-lookup"><span data-stu-id="78233-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="78233-108">U lijevom navigacijskom oknu odaberite **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="78233-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="78233-109">Na stranici popisa **Resursi** otvorite zapis korisnika, a zatim odaberite **Prikaži radno vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="78233-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="78233-110">Provjerite jeste li omogućili skočne prozore na stranici preglednika.</span><span class="sxs-lookup"><span data-stu-id="78233-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="78233-111">To vam omogućuje da vidite radno vrijeme postavljeno za resurs.</span><span class="sxs-lookup"><span data-stu-id="78233-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="78233-112">Na kartici **Mjesečni prikaz** odaberite **Postavi**.</span><span class="sxs-lookup"><span data-stu-id="78233-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="78233-113">Prikazat će se popis s tri mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="78233-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="78233-114">Novi tjedni raspored</span><span class="sxs-lookup"><span data-stu-id="78233-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="78233-115">Radni raspored za jedan dan</span><span class="sxs-lookup"><span data-stu-id="78233-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="78233-116">Slobodno vrijeme</span><span class="sxs-lookup"><span data-stu-id="78233-116">Time Off</span></span>

4. <span data-ttu-id="78233-117">Odaberite **Novi tjedni raspored** , a zatim postavite mogućnosti za ovaj raspored resursa.</span><span class="sxs-lookup"><span data-stu-id="78233-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="78233-118">Možete postaviti tjedni raspored s ponavljanjem, parametre dnevnih sati, neradno vrijeme itd.</span><span class="sxs-lookup"><span data-stu-id="78233-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="78233-119">Postavite datumski raspon, odaberite **Spremi** , a zatim odaberite **Zatvori**.</span><span class="sxs-lookup"><span data-stu-id="78233-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="78233-120">Vratite se na stranicu popisa **Resursi** i odaberite resurs za koji ste postavili radno vrijeme.</span><span class="sxs-lookup"><span data-stu-id="78233-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="78233-121">Odaberite **Postavi kalendar kao** da biste postavili predložak rada.</span><span class="sxs-lookup"><span data-stu-id="78233-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="78233-122">U dijaloškom okviru **Radni predložak** unesite naziv radnog predloška, a zatim odaberite **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="78233-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="78233-123">Sada možete povezati predložak rada s predloškom kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="78233-123">You can now associate the work template with a project calendar template.</span></span>
