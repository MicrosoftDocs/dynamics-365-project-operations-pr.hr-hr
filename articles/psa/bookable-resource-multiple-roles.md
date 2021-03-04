---
title: Procjena prodaje i troškova projekta kada resurs koji se može rezervirati ispunjava više uloga za projekt
description: U ovoj se temi pružaju informacije o načinu uporabe veličina za određivanje cijena za podršku određivanju cijena i troškova za resurs koji ispunjava više uloga u projektu.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 67e24156e960b9b09cf92f7f0cd77f6c74a982b8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145034"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="c5e2f-103">Procjena prodaje i troškova projekta kada resurs koji se može rezervirati ispunjava više uloga za projekt</span><span class="sxs-lookup"><span data-stu-id="c5e2f-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c5e2f-104">Tvrtke koje se temelje na projektu često imaju potrebu za jednim resursom koji bi izvršavao više uloga u projektu.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="c5e2f-105">Svaka od ovih uloga može imati različitu cijenu i troškove, što znači da vrijeme istog resursa na projektu može dobiti različitu financijsku procjenu, ovisno o računu i troškovima za svaku od uloga.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="c5e2f-106">Project Service Automation omogućuje postavljanje vrijednosti u zapisu o članu tima za imenovani resurs i omogućuje različite izmjene svakog zadatka kojem je član tima dodijeljen.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="c5e2f-107">Sljedeći primjer objašnjava kako jednostavna izmjena ove vrijednosti omogućuje resursu da ima više uloga na projektu s različitim cijenama troška i računa.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="c5e2f-108">Stvaranje zadatka</span><span class="sxs-lookup"><span data-stu-id="c5e2f-108">Create tasks</span></span>
<span data-ttu-id="c5e2f-109">Stvorite dva projektna zadatka, svaki po 40 sati, Zadatak A i Zadatak B. Odaberite Zadatak A kao prethodnika Zadataka B.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="c5e2f-110">Postavljanje jedinice za generičkog člana projektnog tima za ulogu i tvrtku ili ustanovu</span><span class="sxs-lookup"><span data-stu-id="c5e2f-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="c5e2f-111">Na stranici **Raspored** odaberite redak **Zadatak** za zadatak A.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="c5e2f-112">S padajućeg popisa u polju **Resursi** odaberite **Stvori**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="c5e2f-113">Na stranici **Brzo stvaranje člana tima** navedite atribute generičkog člana tima koji može izvršiti taj zadatak.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="c5e2f-114">Odaberite odgovarajuću ulogu i organizacijsku jedinicu, a zatim odaberite mogućnost **Spremi i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="c5e2f-115">Stvara se generički član tima koji se dodjeljuje ovom zadatku.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="c5e2f-116">Ponovite ove korake za zadatak B i provjerite da se uloga i organizacijska jedinica generičkog člana tima stvorenog za zadatak B razlikuje od onog za zadatak A.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="c5e2f-117">Postavljanje uloge i organizacijske jedinice za projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="c5e2f-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="c5e2f-118">Nakon što stvorite zadatak A, odaberite zadatak, a zatim odaberite mogućnost **Uredi zadatak**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="c5e2f-119">Na stranici **Pojedinosti zadatka** pronađite polja **Uloga** i **Organizacijska jedinica** i dodajte vrijednosti potrebne za resurs koji bi trebao izvršiti ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="c5e2f-120">Ako dovršavate ovaj scenarij s pomoću pokaznih podataka aplikacije Project Service Automation, odaberite stavku **Voditelj savjetovanja** za ulogu, a **Fabrikam US** kao organizacijsku jedinicu.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="c5e2f-121">Odaberite Zadatak B, a zatim odaberite mogućnost **Uredi zadatak**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="c5e2f-122">Na stranici **Pojedinosti zadatka** pronađite polja **Uloga** i **Organizacijska jedinica** i dodajte vrijednosti potrebne za resurs koji bi trebao izvršiti ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="c5e2f-123">Provjerite razlikuju li se vrijednosti u poljima **Uloga** i **Organizacijska jedinica** za zadatak B od vrijednosti za zadatak A.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="c5e2f-124">Ako dovršavate ovaj scenarij s pomoću pokaznih podataka aplikacije Project Service Automation, odaberite stavku **Tehničar za mrežu** za ulogu, a **Fabrikam US** kao organizacijsku jedinicu.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="c5e2f-125">Spremite i zatvorite stranicu **Pojedinosti zadatka**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="c5e2f-126">Član tima i procjene ponašanja</span><span class="sxs-lookup"><span data-stu-id="c5e2f-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="c5e2f-127">Na stranici **Pojedinosti zadatka**, na stavci **Član tima**, odaberite dva člana generičkog tima, a zatim odaberite **Generiraj zahtjeve**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="c5e2f-128">Odaberite redak člana tima za stavku **Voditelj savjetovanja** a zatim odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="c5e2f-129">Otvara se ploča s rasporedom i rezervira resurs za taj zahtjev.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="c5e2f-130">Odaberite redak člana tima za stavku **Tehničar za mrežu** a zatim odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="c5e2f-131">Otvara se ploča s rasporedom i rezervira isti resurs za taj zahtjev.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="c5e2f-132">Rešetka člana tima</span><span class="sxs-lookup"><span data-stu-id="c5e2f-132">Team Member grid</span></span> 
<span data-ttu-id="c5e2f-133">Na rešetki **Član tima** primijetit ćete kako su dva zapisa o članu generičkog tima izbrisana i zamijenjene jednim resursom.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="c5e2f-134">Postoji jedan skup vrijednosti za taj resurs koji prikazuje zadani skup vrijednosti za stavke **Uloga** i **Organizacijska jedinica**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="c5e2f-135">Kada proširite red tog zapisa o članu tima, na tom zapisu možete vidjeti različite zadatke za oba ta zadatka.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="c5e2f-136">Svaki redak zadatka ima vrijednosti specifične za mogućnosti **Uloga** i **Organizacijska jedinica**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="c5e2f-137">Rešetka procjena</span><span class="sxs-lookup"><span data-stu-id="c5e2f-137">Estimates grid</span></span> 
<span data-ttu-id="c5e2f-138">Kada prijeđete na rešetku **Procjene**, primijetit ćete kako oba zadatka za isti resurs imaju različitu cijenu.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="c5e2f-139">Cijena zadaka resursa u Zadatku A određuje se s pomoću vrijednost atributa **Uloga** stavke **Voditelj savjetovanja**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="c5e2f-140">Cijena zadaka istog resursa u Zadatku B određuje se s pomoću vrijednost atributa **Uloga** stavke **Tehničar za mrežu**.</span><span class="sxs-lookup"><span data-stu-id="c5e2f-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>

