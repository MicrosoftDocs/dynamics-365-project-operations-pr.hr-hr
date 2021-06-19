---
title: Načini planiranja
description: U ovoj temi nalaze se informacije o načinima planiranja.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116698"
---
# <a name="scheduling-modes"></a><span data-ttu-id="9cb1b-103">Načini planiranja</span><span class="sxs-lookup"><span data-stu-id="9cb1b-103">Scheduling modes</span></span>

<span data-ttu-id="9cb1b-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="9cb1b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9cb1b-105">Dynamics 365 Project Operations pruža tvrtkama i ustanovama mogućnost definiranja načina upravljanja promjenama ključnih varijabli u zadacima unutar strukture analize rada.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="9cb1b-106">Na temelju specifičnih potreba tvrtke ili ustanove, voditelji projekata mogu nakon stvaranja projekta napraviti promjene načina planiranja.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="9cb1b-107">U aplikaciji Project Operations dostupna su tri načina planiranja:</span><span class="sxs-lookup"><span data-stu-id="9cb1b-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="9cb1b-108">Nepromjenjivo trajanje (ovo je zadani način)</span><span class="sxs-lookup"><span data-stu-id="9cb1b-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="9cb1b-109">Fiksni napor (*Rad*)</span><span class="sxs-lookup"><span data-stu-id="9cb1b-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="9cb1b-110">Fiksne jedinice</span><span class="sxs-lookup"><span data-stu-id="9cb1b-110">Fixed units</span></span>

<span data-ttu-id="9cb1b-111">Vrijednosti na koje utječe definicija određenog načina planiranja određuju se prema sljedećoj formuli:</span><span class="sxs-lookup"><span data-stu-id="9cb1b-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="9cb1b-112">Napor = Trajanje x Jedinice</span><span class="sxs-lookup"><span data-stu-id="9cb1b-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="9cb1b-113">Kada definirate način planiranja projekta, postavljate jednu od ovih vrijednosti koje se potom ne mogu mijenjati.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="9cb1b-114">Držanje ove vrijednosti kao konstante stavlja prioritet na tu vrijednost, što izvješćuje sustav da je ne mijenja kada se promijene druge dvije vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="9cb1b-115">Sljedeća tablica pruža informacije o utjecajima odabira određenog načina.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="9cb1b-116">**U ovom zadatku**</span><span class="sxs-lookup"><span data-stu-id="9cb1b-116">**In this task**</span></span>             | <span data-ttu-id="9cb1b-117">**Ako promijenite jedinice**</span><span class="sxs-lookup"><span data-stu-id="9cb1b-117">**If you revise units**</span></span>   | <span data-ttu-id="9cb1b-118">**Ako promijenite trajanje**</span><span class="sxs-lookup"><span data-stu-id="9cb1b-118">**If you revise duration**</span></span> | <span data-ttu-id="9cb1b-119">**Ako promijenite napor**</span><span class="sxs-lookup"><span data-stu-id="9cb1b-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="9cb1b-120">Nepromjenjive jedinice zadatka</span><span class="sxs-lookup"><span data-stu-id="9cb1b-120">Fixed units task</span></span>     | <span data-ttu-id="9cb1b-121">Trajanje se preračunava.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-121">Duration is recalculated.</span></span> | <span data-ttu-id="9cb1b-122">Napor se preračunava.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-122">Effort is recalculated.</span></span>    | <span data-ttu-id="9cb1b-123">Trajanje se preračunava.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="9cb1b-124">Zadatak nepromjenjivog napora</span><span class="sxs-lookup"><span data-stu-id="9cb1b-124">Fixed effort task</span></span>    | <span data-ttu-id="9cb1b-125">Trajanje se preračunava.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-125">Duration is recalculated.</span></span> | <span data-ttu-id="9cb1b-126">Jedinice se preračunavaju.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-126">Units are recalculated.</span></span>    | <span data-ttu-id="9cb1b-127">Trajanje se preračunava.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="9cb1b-128">Zadatak nepromjenjivog trajanja</span><span class="sxs-lookup"><span data-stu-id="9cb1b-128">Fixed duration task</span></span>  | <span data-ttu-id="9cb1b-129">Napor se preračunava.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-129">Effort is recalculated.</span></span>   | <span data-ttu-id="9cb1b-130">Napor se preračunava.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-130">Effort is recalculated.</span></span>    | <span data-ttu-id="9cb1b-131">Jedinice se preračunavaju.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-131">Units are recalculated.</span></span>   |

<span data-ttu-id="9cb1b-132">Dodatne informacije o implikacijama određenog načina potražite u članku [Promjena vrste zadatka za preciznije planiranje](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="9cb1b-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="9cb1b-133">U temi se pojam **Rad** upotrebljava umjesto pojma **Napor**.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="9cb1b-134">Promjena načina planiranja u tvrtki ili ustanovi</span><span class="sxs-lookup"><span data-stu-id="9cb1b-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="9cb1b-135">Poduzmite sljedeće korake kako biste definirali način planiranja u tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="9cb1b-136">Idite na **Postavke** \> **Općenito** \> **Parametri**, a zatim odaberite parametar projekta.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="9cb1b-137">Na stranici **Parametri projekta** odaberite zadani način planiranja za tvrtku ili ustanovu, a zatim definirajte mogućnost da upravitelj projekta nadjača postavku tijekom stvaranja novog projekta.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="9cb1b-138">Promjena postavke načina planiranja u projektu</span><span class="sxs-lookup"><span data-stu-id="9cb1b-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="9cb1b-139">Ako tvrtka ili ustanova dozvoljava voditelju projekta da nadjača zadani način planiranja, voditelj projekta može izvršiti tu promjenu tijekom stvaranja novog projekta.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="9cb1b-140">Međutim, nakon što se projekt spremi, način planiranja ne može se promijeniti.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="9cb1b-141">Kopirani projekti</span><span class="sxs-lookup"><span data-stu-id="9cb1b-141">Copied projects</span></span>

<span data-ttu-id="9cb1b-142">Budući da se projekt stvara kad se poduzme radnja kopiranja, voditelj projekta ne može postaviti način planiranja.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="9cb1b-143">Odredišni projekt uvijek će biti zadan za način definiran na razini tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="9cb1b-144">Kopirani zadaci</span><span class="sxs-lookup"><span data-stu-id="9cb1b-144">Copied tasks</span></span>

<span data-ttu-id="9cb1b-145">Kada se zadatak kopira iz jednog projekta u drugi, zadatak nasljeđuje način planiranja odredišnog projekta.</span><span class="sxs-lookup"><span data-stu-id="9cb1b-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
