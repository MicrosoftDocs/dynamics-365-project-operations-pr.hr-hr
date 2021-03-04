---
title: Rezervacije u odnosu na dodjele
description: U ovoj temi nalaze se informacije o razlikama između rezervacija i dodjela resursa.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841163"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="03755-103">Rezervacije u odnosu na dodjele</span><span class="sxs-lookup"><span data-stu-id="03755-103">Bookings vs assignments</span></span>

<span data-ttu-id="03755-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="03755-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="03755-105">Rezervacije mogu imati fiksno ili promjenjivo dodjeljivanje resursa projektu.</span><span class="sxs-lookup"><span data-stu-id="03755-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="03755-106">Fiksne rezervacije iskorištavaju kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="03755-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="03755-107">Rezervacije predstavljaju organizacijske koncepte timova kako bi mogli razumjeti način na koji će se resursi angažirati na različitim projektima.</span><span class="sxs-lookup"><span data-stu-id="03755-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="03755-108">Dynamics 365 Project Operations tretira rezervacije kao koncept na razini projekta.</span><span class="sxs-lookup"><span data-stu-id="03755-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="03755-109">Za razliku od rezervacija, dodjele predstavljaju zaduženje resursa zadacima projekta u rasporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="03755-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="03755-110">Resursi mogu biti imenovani ili generički.</span><span class="sxs-lookup"><span data-stu-id="03755-110">The resources can be named or generic.</span></span>  <span data-ttu-id="03755-111">Kada se zahtjev za resursom izvede iz dodjele projektnog zadatka, Project Operations upotrebljava konture napora zadatka resursa za izgradnju kontura pojedinosti preduvjeta za resurs.</span><span class="sxs-lookup"><span data-stu-id="03755-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="03755-112">Međutim, upućivanje na zadatke resursa ne održava se.</span><span class="sxs-lookup"><span data-stu-id="03755-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="03755-113">Ažuriranja rezervacija izvedenih iz preduvjeta za resurs ne ažuriraju nikakve zadatke resursa.</span><span class="sxs-lookup"><span data-stu-id="03755-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="03755-114">Uobičajeno je zbroj rezervacija za resurs jednak zbroju dodjela resursa jednom ili većem broju zadataka.</span><span class="sxs-lookup"><span data-stu-id="03755-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="03755-115">Međutim, Project Operations ne nameće takvu podudarnost.</span><span class="sxs-lookup"><span data-stu-id="03755-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="03755-116">U prikazu **Usklađivanje** možete vidjeti mjesta voditelja projekta gdje se rezervacija i dodjele resursa ne podudaraju.</span><span class="sxs-lookup"><span data-stu-id="03755-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


