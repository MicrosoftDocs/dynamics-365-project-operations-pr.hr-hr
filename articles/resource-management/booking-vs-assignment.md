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
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896002"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="c1af7-103">Rezervacije u odnosu na dodjele</span><span class="sxs-lookup"><span data-stu-id="c1af7-103">Bookings vs assignments</span></span>

<span data-ttu-id="c1af7-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="c1af7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c1af7-105">Rezervacije mogu imati fiksno ili promjenjivo dodjeljivanje resursa projektu.</span><span class="sxs-lookup"><span data-stu-id="c1af7-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="c1af7-106">Fiksne rezervacije iskorištavaju kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="c1af7-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="c1af7-107">Dodjele predstavljaju dodjelu resursa zadacima projekta u rasporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="c1af7-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="c1af7-108">Resursi mogu biti stvarni ili generički resursi.</span><span class="sxs-lookup"><span data-stu-id="c1af7-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="c1af7-109">Rezervacije i dodjele za prave resurse trebale bi se podudarati jer se ne razlikuju.</span><span class="sxs-lookup"><span data-stu-id="c1af7-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="c1af7-110">Međutim, Microsoft Dynamics Project Operations ne primjenjuje to usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="c1af7-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="c1af7-111">U prikazu **Usklađivanje** možete vidjeti mjesta voditelja projekta gdje rezervacija i dodjele resursa nisu usklađeni.</span><span class="sxs-lookup"><span data-stu-id="c1af7-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
