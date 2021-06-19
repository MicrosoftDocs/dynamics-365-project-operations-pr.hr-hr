---
title: Najčešća pitanja o upravljanju resursima
description: Ova tema pruža odgovore na najčešća pitanja o upravljanju resursima.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008752"
---
# <a name="resource-management-faq"></a><span data-ttu-id="7b01d-103">Najčešća pitanja o upravljanju resursima</span><span class="sxs-lookup"><span data-stu-id="7b01d-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="7b01d-104">Koja je razlika između člana tima i preduvjeta resursa?</span><span class="sxs-lookup"><span data-stu-id="7b01d-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="7b01d-105">Član projektnog tima može se dodijeliti zadacima, biti rezerviran ili prekomjerno rezerviran te se postaviti kao odobravatelj.</span><span class="sxs-lookup"><span data-stu-id="7b01d-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="7b01d-106">Preduvjet resursa može postojati bez člana projektnog tima, kao skica bilješke o potražnji.</span><span class="sxs-lookup"><span data-stu-id="7b01d-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="7b01d-107">Koja je razlika između predloženih i promjenjivo rezerviranih sati?</span><span class="sxs-lookup"><span data-stu-id="7b01d-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="7b01d-108">Predloženi sati i promjenjivo rezervirani sati razlikuju se u vidljivosti.</span><span class="sxs-lookup"><span data-stu-id="7b01d-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="7b01d-109">Predloženi sati vidljivi su samo upraviteljima resursa i voditelju projekta koji je pokrenuo potražnju pomoću zahtjeva za resurs.</span><span class="sxs-lookup"><span data-stu-id="7b01d-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="7b01d-110">Promjenjivo rezervirani sati vidljivi su svakome tko ima pristup ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="7b01d-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="7b01d-111">Kako mogu vidjeti promjenjivo rezervirane sate za resurse u timu?</span><span class="sxs-lookup"><span data-stu-id="7b01d-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="7b01d-112">Promjenjive rezervacije moguće su prilikom rezerviranja preduvjeta resursa.</span><span class="sxs-lookup"><span data-stu-id="7b01d-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="7b01d-113">Resursi koji su promjenjivo rezervirani u projektnom timu prikazuju se kao članovi tima koji imaju promjenjivo rezervirane sate.</span><span class="sxs-lookup"><span data-stu-id="7b01d-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="7b01d-114">Prikazuju se i na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="7b01d-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="7b01d-115">Kako promijeniti potrebne sate te datume početka i završetka za resurs (generički ili imenovani) koji sam rezervirao?</span><span class="sxs-lookup"><span data-stu-id="7b01d-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="7b01d-116">Nakon što se resursi rezerviraju, odaberite **Zadrži rezervacije** da biste uveli sve potrebne promjene.</span><span class="sxs-lookup"><span data-stu-id="7b01d-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="7b01d-117">Koje vrste resursa podržava Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="7b01d-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="7b01d-118">**Korisnik** i **Kontakt** jedine su vrste resursa koje su podržane u aplikaciji Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7b01d-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="7b01d-119">Iako možete stvoriti druge vrste resursa (na primjer, **Oprema** i **Grupa**), za njih nije podržan nijedan slučaj sveobuhvatne upotrebe.</span><span class="sxs-lookup"><span data-stu-id="7b01d-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="7b01d-120">Koja je razlika između dodjele i rezervacije?</span><span class="sxs-lookup"><span data-stu-id="7b01d-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="7b01d-121">Dodjele predstavljaju dodjelu resursa zadacima projekta u rasporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="7b01d-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="7b01d-122">Resursi mogu biti pravi ili generički resursi.</span><span class="sxs-lookup"><span data-stu-id="7b01d-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="7b01d-123">Rezervacije mogu imati fiksno ili promjenjivo dodjeljivanje resursa projektu.</span><span class="sxs-lookup"><span data-stu-id="7b01d-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="7b01d-124">Fiksne rezervacije iskorištavaju kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="7b01d-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="7b01d-125">Rezervacije i dodjele za prave resurse trebale bi se podudarati jer se ne razlikuju.</span><span class="sxs-lookup"><span data-stu-id="7b01d-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="7b01d-126">No u PSA-u to podudaranje nije obavezno.</span><span class="sxs-lookup"><span data-stu-id="7b01d-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="7b01d-127">U prikazu Usklađivanje možete vidjeti mjesta voditelja projekta gdje se rezervacija i dodjele resursa ne podudaraju.</span><span class="sxs-lookup"><span data-stu-id="7b01d-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]