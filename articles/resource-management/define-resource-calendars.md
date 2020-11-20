---
title: Definiranje kalendara resursa
description: U ovoj temi nalaze se informacije o načinu definiranja kalendara radnog vremena za resurse u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123909"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="e8afc-103">Definiranje kalendara resursa</span><span class="sxs-lookup"><span data-stu-id="e8afc-103">Define resource calendars</span></span>

<span data-ttu-id="e8afc-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="e8afc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e8afc-105">Svaki resurs koji se može rezervirati, a radi na projektu, mora imati kalendar radnog vremena kako bi se definirala njegova dostupnost.</span><span class="sxs-lookup"><span data-stu-id="e8afc-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="e8afc-106">Radno vrijeme resursa može se definirati na dva načina:</span><span class="sxs-lookup"><span data-stu-id="e8afc-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="e8afc-107">Definiranje pojedinačnih kalendarskih pravila za resurs</span><span class="sxs-lookup"><span data-stu-id="e8afc-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="e8afc-108">Primjena postojećeg predloška kalendara za resurs</span><span class="sxs-lookup"><span data-stu-id="e8afc-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="e8afc-109">Definiranje radnog vremena resursa</span><span class="sxs-lookup"><span data-stu-id="e8afc-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="e8afc-110">U izborniku **Resursi** odaberite stavku **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="e8afc-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="e8afc-111">Iz prikaza rešetke odaberite mjerodavne **Resurse koji se mogu rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="e8afc-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="e8afc-112">Na stranici **Pojedinosti o resursu** odaberite karticu **Radno vrijeme**. Prema zadanim postavkama kalendar resursa koji se mogu rezervirati zadan je za radno vrijeme zadanog predloška radnog vremena koji je definiran za tvrtku ili ustanovu.</span><span class="sxs-lookup"><span data-stu-id="e8afc-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="e8afc-113">Kako biste ažurirali radno vrijeme, desnom tipkom miša kliknite datum početka predloženog pravila kalendara koji treba definirati.</span><span class="sxs-lookup"><span data-stu-id="e8afc-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="e8afc-114">S pomoću izbornika pravila kalendara definirajte pravilo kalendara za određeni dan, podsjetnik niza ili cijeli kalendar.</span><span class="sxs-lookup"><span data-stu-id="e8afc-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="e8afc-115">Nakon odabira mogućnosti možete definirati sljedeće:</span><span class="sxs-lookup"><span data-stu-id="e8afc-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="e8afc-116">Dan u tjednu u kojem će se primjenjivati radno vrijeme.</span><span class="sxs-lookup"><span data-stu-id="e8afc-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="e8afc-117">Radno vrijeme unutar svakog dana.</span><span class="sxs-lookup"><span data-stu-id="e8afc-117">The working times within each day.</span></span>
    - <span data-ttu-id="e8afc-118">Vremensku zonu za pravilo kalendara.</span><span class="sxs-lookup"><span data-stu-id="e8afc-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="e8afc-119">Ako je primjenjivo, za pravilo se može odrediti i neradno vrijeme.</span><span class="sxs-lookup"><span data-stu-id="e8afc-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="e8afc-120">Primjena predloška kalendara na resurs</span><span class="sxs-lookup"><span data-stu-id="e8afc-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="e8afc-121">U izborniku **Resursi** odaberite stavku **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="e8afc-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="e8afc-122">U prikazu rešetke odaberite do 25 **Resursa koji se mogu rezervirati** kako biste ih ažurirali.</span><span class="sxs-lookup"><span data-stu-id="e8afc-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="e8afc-123">Odaberite mogućnost **Postavi kalendar** i dijaloški okvir će vam osigurati popis dostupnih predložaka radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="e8afc-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="e8afc-124">Odaberite predložak koji želite upotrebljavati, a zatim odaberite mogućnost **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="e8afc-124">Select the template you want to use, and then select **Apply**.</span></span>
