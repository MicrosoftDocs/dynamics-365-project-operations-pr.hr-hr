---
title: Rezervacije u odnosu na dodjele
description: U ovoj temi nalaze se informacije o razlikama između rezervacija i dodjela resursa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073237"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="e2cae-103">Rezervacije u odnosu na dodjele</span><span class="sxs-lookup"><span data-stu-id="e2cae-103">Bookings vs assignments</span></span>

<span data-ttu-id="e2cae-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="e2cae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e2cae-105">Rezervacije mogu imati fiksno ili promjenjivo dodjeljivanje resursa projektu.</span><span class="sxs-lookup"><span data-stu-id="e2cae-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="e2cae-106">Fiksne rezervacije iskorištavaju kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="e2cae-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="e2cae-107">Dodjele predstavljaju dodjelu resursa zadacima projekta u rasporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="e2cae-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="e2cae-108">Resursi mogu biti stvarni ili generički resursi.</span><span class="sxs-lookup"><span data-stu-id="e2cae-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="e2cae-109">Rezervacije i dodjele za prave resurse trebale bi se podudarati jer se ne razlikuju.</span><span class="sxs-lookup"><span data-stu-id="e2cae-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="e2cae-110">Međutim, Microsoft Dynamics Project Operations ne primjenjuje to usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="e2cae-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="e2cae-111">U prikazu **Usklađivanje** možete vidjeti mjesta voditelja projekta gdje rezervacija i dodjele resursa nisu usklađeni.</span><span class="sxs-lookup"><span data-stu-id="e2cae-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
