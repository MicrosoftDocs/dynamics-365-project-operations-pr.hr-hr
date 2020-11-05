---
title: Upravljanje resursima
description: Ova tema pruža informacije o tome kako možete upravljati resursima.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073589"
---
# <a name="manage-resources"></a><span data-ttu-id="4e517-103">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="4e517-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4e517-104">Dynamics 365 Project Service Automation uključuje nadzornu ploču upravitelja resursa koja pruža vizualni pregled potražnje resursa i korištenja na svim razinama ustanove.</span><span class="sxs-lookup"><span data-stu-id="4e517-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="4e517-105">Grafikone na toj nadzornoj ploči možete koristiti za vizualizaciju sljedećih informacija:</span><span class="sxs-lookup"><span data-stu-id="4e517-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="4e517-106">**Potražnja za resursima** – grafikon **Zahtjevi za aktivne resurse** prikazuje poslane resurse.</span><span class="sxs-lookup"><span data-stu-id="4e517-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="4e517-107">Resursi se agregiraju prema ulozi ili projektu.</span><span class="sxs-lookup"><span data-stu-id="4e517-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="4e517-108">**Potražnja za neposlanim resursima** – grafikon **Potražnja za nedodijeljenim resursima** prikazuje sve preduvjete resursa koji nisu poslani.</span><span class="sxs-lookup"><span data-stu-id="4e517-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="4e517-109">Pomaže upraviteljima resursa da pregledaju potražnju koja nije utvrđena i može se poslati putem zahtjeva za resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="4e517-110">**Naplativo korištenje za protekli tjedan** – grafikon **Korištenje po ulozi** prikazuje postotak stvarnog naplativog korištenja ustanove po ulozi u odnosu na ciljano naplativo korištenje po ulozi.</span><span class="sxs-lookup"><span data-stu-id="4e517-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4e517-111">Da bi grafikon **Korištenje po ulozi** učinili dostupnim, stvorite posao koji izvodi tijek rada UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="4e517-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="4e517-112">Taj ponavljajući posao izvodi se svakih sedam dana radi izračuna naplativog korištenja za prethodnih sedam dana.</span><span class="sxs-lookup"><span data-stu-id="4e517-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="4e517-113">Rezultati su agregirani po ulozi.</span><span class="sxs-lookup"><span data-stu-id="4e517-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="4e517-114">Upravljanje članovima projektnog tima</span><span class="sxs-lookup"><span data-stu-id="4e517-114">Manage project team members</span></span>

<span data-ttu-id="4e517-115">Upravitelji projekata mogu koristiti nadzornu ploču upravitelja resursa za upravljanje resursima u projektima.</span><span class="sxs-lookup"><span data-stu-id="4e517-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="4e517-116">Na primjer, mogu dodati člana tima izravno u projekt i rezervirati člana tima kako bi se ispunili preduvjeti resursa koje je zabilježio generički resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="4e517-117">Dodavanje člana tima izravno u projekt</span><span class="sxs-lookup"><span data-stu-id="4e517-117">Add a team member directly to a project</span></span>

<span data-ttu-id="4e517-118">Da biste člana tima dodali izravno u projekt, na stranici **Projekti** na kartici **Tim** odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="4e517-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="4e517-119">Prikazat će se dijaloški okvir **Brza izrada: član projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="4e517-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="4e517-120">U tom dijaloškom okviru možete izvršiti sljedeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="4e517-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="4e517-121">**Rezervirajte imenovani resurs** – u polju **Resurs koji je moguće rezervirati** odaberite naziv resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="4e517-122">Zatim odaberite ulogu, postavite razdoblje i odaberite način dodjele.</span><span class="sxs-lookup"><span data-stu-id="4e517-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="4e517-123">Imenovani resurs koji ste odabrali dodaje se projektu pomoću odabranog načina dodjele i kalendara resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="4e517-124">**Dodajte generički resurs** – ostavite polje **Resurs koji je moguće rezervirati** prazno, a zatim odaberite ulogu, postavite razdoblje i odaberite željeni način dodjele.</span><span class="sxs-lookup"><span data-stu-id="4e517-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="4e517-125">Generički se resurs dodaje timu kao rezervirano mjesto radi zadržavanja uzorka potražnje koji se koristi za rezerviranje imenovanih resursa u timu.</span><span class="sxs-lookup"><span data-stu-id="4e517-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="4e517-126">Preduvjet se izrađuje prema kalendaru projekta.</span><span class="sxs-lookup"><span data-stu-id="4e517-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="4e517-127">**Dodajte imenovani resurs timu bez potrošnje kapaciteta resursa** – u polju **Resurs koji je moguće rezervirati** odaberite resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="4e517-128">Zatim odaberite razdoblje pa kao način dodjele odaberite **Ništa**.</span><span class="sxs-lookup"><span data-stu-id="4e517-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="4e517-129">Resurs se dodaje timu, no kapacitet resursa ne iskorištava se putem rezervacije.</span><span class="sxs-lookup"><span data-stu-id="4e517-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="4e517-130">Rezerviranje člana tima radi ispunjavanja preduvjeta resursa za generički resurs</span><span class="sxs-lookup"><span data-stu-id="4e517-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="4e517-131">U PSA-u možete rezervirati generički resurs u projektnom timu i možete odrediti ulogu, potreban kapacitet i način distribucije tog kapaciteta.</span><span class="sxs-lookup"><span data-stu-id="4e517-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="4e517-132">U preduvjetu resursa možete odrediti atribute koji su pridruženi generičkom resursu.</span><span class="sxs-lookup"><span data-stu-id="4e517-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="4e517-133">Ti atributi uključuju potrebne vještine, željenu organizacijsku jedinicu i željene resurse.</span><span class="sxs-lookup"><span data-stu-id="4e517-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="4e517-134">Poduzmite ove korake da biste naveli potrebne vještine u generičkom resursu za razvojnog programera.</span><span class="sxs-lookup"><span data-stu-id="4e517-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="4e517-135">Da biste rezervirali generički resurs, na stranici **Projekti** na kartici **Tim** odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="4e517-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Generički resurs rezerviran u timu](media/Resource-Management-image9.png)

2. <span data-ttu-id="4e517-137">U prikazu **Svi članovi tima** u stupcu **Preduvjet resursa** odaberite vezu za dodavanje potrebnih vještina za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Veza preduvjeta](media/Resource-Management-image10.png)

3. <span data-ttu-id="4e517-139">Da biste dodali potrebne vještine za razvojnog programera, na stranici **Preduvjet resursa** koja se prikaže u rešetki **Vještine** odaberite tri točke ( **...** ), a zatim odaberite **Dodaj novu značajku preduvjeta**.</span><span class="sxs-lookup"><span data-stu-id="4e517-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Naredba za dodavanje nove značajke uvjeta](media/Resource-Management-image11.png)

4. <span data-ttu-id="4e517-141">U dijaloškom okviru **Brza izrada: značajka preduvjeta** koji se prikaže, u polju **Značajka** odaberite potrebnu vještinu.</span><span class="sxs-lookup"><span data-stu-id="4e517-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="4e517-142">Zatim u polju **Vrijednost ocjene** odaberite razinu stručnosti za tu vještinu.</span><span class="sxs-lookup"><span data-stu-id="4e517-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="4e517-143">Na kraju u polju **Preduvjet resursa** postavite preduvjet na izvorne resurse iz organizacijskih jedinica ili čak imenovanih resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="4e517-144">Kada dovršite, odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="4e517-144">When you've finished, select **Save**.</span></span>

    ![Brza izrada: dijaloški okvir Značajka preduvjeta](media/Resource-Management-image12.png)

5. <span data-ttu-id="4e517-146">Na stranici **Preduvjet resursa** odaberite **Rezerviraj** da biste ispunili preduvjet resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Gumb Rezerviraj na stranici Preduvjet resursa](media/Resource-Management-image13.png)

    <span data-ttu-id="4e517-148">Možete također odabrati generički resurs u rešetki **Svi članovi tima** , a zatim odabrati **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="4e517-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Gumb Rezerviraj iznad rešetke Svi članovi tima](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="4e517-150">U ovom primjeru navedeno je 40 potrebnih sati, ali nema stvarnih rezerviranih sati jer generički resursi nemaju rezervacije.</span><span class="sxs-lookup"><span data-stu-id="4e517-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="4e517-151">Osim toga, ne postoje dodijeljeni sati jer je generički resurs izravno dodan timu.</span><span class="sxs-lookup"><span data-stu-id="4e517-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="4e517-152">Nije dodan pomoću dodjele zadatka.</span><span class="sxs-lookup"><span data-stu-id="4e517-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="4e517-153">Na stranici **Pomoćnik za raspored** možete filtrirati dostupne resurse prema preduvjetima navedenim u preduvjetu resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="4e517-154">Resursi se sortiraju prema parametrima sortiranja koji su navedeni na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="4e517-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Stranica Pomoćnik za raspored](media/Resource-Management-image15.png)

    <span data-ttu-id="4e517-156">Evo nekih filtara koji se često koriste:</span><span class="sxs-lookup"><span data-stu-id="4e517-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="4e517-157">**Karakteristike s ocjenom** – filtriranje po vještinama, certifikatima i drugim kvalitetama resursa, uz ocjene stručnosti.</span><span class="sxs-lookup"><span data-stu-id="4e517-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="4e517-158">**Uloge** – filtriranje po zadanim ulogama koje su dodijeljene resursima koje je moguće rezervirati.</span><span class="sxs-lookup"><span data-stu-id="4e517-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="4e517-159">**Organizacijske jedinice** – filtriranje resursa koje je moguće rezervirati prema organizacijskim jedinicama kojima su dodijeljeni.</span><span class="sxs-lookup"><span data-stu-id="4e517-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="4e517-160">Ako niste zadovoljni rezultatima početnog pretraživanja preduvjeta, možete izmijeniti kriterije filtra.</span><span class="sxs-lookup"><span data-stu-id="4e517-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="4e517-161">Proširite okno **Prikaz filtra** na lijevoj strani, a zatim odaberite **Pretraži** da biste pronašli dodatne resurse.</span><span class="sxs-lookup"><span data-stu-id="4e517-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Okno Prikaz filtra](media/Resource-Management-image16.png)

7. <span data-ttu-id="4e517-163">Da biste promijenili način sortiranja rezultata, odaberite **Sortiraj**.</span><span class="sxs-lookup"><span data-stu-id="4e517-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Naredba za sortiranje](media/Resource-Management-image17.png)

8. <span data-ttu-id="4e517-165">Odaberite resurse prema potražnji koja je navedena u preduvjetu, kako je naznačeno na vrhu rešetke.</span><span class="sxs-lookup"><span data-stu-id="4e517-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="4e517-166">Možete ukloniti odabir ćelija u rešetki i ostaviti taj kapacitet resursa otvorenim.</span><span class="sxs-lookup"><span data-stu-id="4e517-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="4e517-167">Istodobno je moguće odabrati samo jedan resurs kao rezerviran.</span><span class="sxs-lookup"><span data-stu-id="4e517-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="4e517-168">Odaberite **Rezerviraj** da biste rezervirali odabrani resurs i ostavite ploču s rasporedom otvorenom, tako da možete odabrati dodatne resurse.</span><span class="sxs-lookup"><span data-stu-id="4e517-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="4e517-169">Ili odaberite **Rezerviraj i izađi** da biste rezervirali odabrani resurs i zatvorite ploču s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="4e517-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Resurs za rezerviranje](media/Resource-Management-image19.png)

    <span data-ttu-id="4e517-171">Primit ćete obavijest o rezerviranim satima.</span><span class="sxs-lookup"><span data-stu-id="4e517-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="4e517-172">Pokazatelji potražnje prikazuju u kojoj je mjeri preduvjet rezervacije ispunjen i koliko je preostalo do ispunjavanja.</span><span class="sxs-lookup"><span data-stu-id="4e517-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="4e517-173">Možete vidjeti i koliko je kapaciteta odabranog resursa iskorišteno.</span><span class="sxs-lookup"><span data-stu-id="4e517-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="4e517-174">Odaberite **Proširi** da biste vidjeli više pojedinosti o rezervacijama resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="4e517-175">Vratite se na prikaz **Svi članovi tima**.</span><span class="sxs-lookup"><span data-stu-id="4e517-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="4e517-176">U rešetki možete vidjeti da je generički resurs zamijenjen imenovanim resursom, a 40 sati navedeno je kao rezervirano za taj resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Ažurirana rešetka Svi članovi tima](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="4e517-178">Dodijeljeni se sati ne prikazuju jer su izravno rezervirani u timu.</span><span class="sxs-lookup"><span data-stu-id="4e517-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="4e517-179">Nisu rezervirani pomoću dodjele zadatka.</span><span class="sxs-lookup"><span data-stu-id="4e517-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="4e517-180">Dodjeljivanje generičkih resursa zadacima i generiranje preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="4e517-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="4e517-181">U PSA-u možete izraditi zadatke, a zatim im dodijeliti generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="4e517-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="4e517-182">Na taj način potražnju resursa mogu predstavljati rezervirana mjesta dok procjenjujete svoj raspored i financijske brojeve.</span><span class="sxs-lookup"><span data-stu-id="4e517-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="4e517-183">Zatim možete generirati preduvjete resursa za generičke resurse i ispuniti ih.</span><span class="sxs-lookup"><span data-stu-id="4e517-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="4e517-184">Na stranici **Projekti** na kartici **Raspored** odaberite **Dodaj** da biste izradili zadatak.</span><span class="sxs-lookup"><span data-stu-id="4e517-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Izrađen je novi zadatak](media/Resource-Management-image21.png)

2. <span data-ttu-id="4e517-186">U polju **Resursi** odaberite simbol **Odabir resursa**.</span><span class="sxs-lookup"><span data-stu-id="4e517-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="4e517-187">Prikazat će se odabir resursa i postojeći članovi tima za projekt.</span><span class="sxs-lookup"><span data-stu-id="4e517-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Odabir resursa](media/Resource-Management-image22.png)

3. <span data-ttu-id="4e517-189">Unesite naziv novog generičkog resursa, a zatim odaberite **Izradi**.</span><span class="sxs-lookup"><span data-stu-id="4e517-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Unesen je naziv novog generičkog resursa](media/Resource-Management-image23.png)

4. <span data-ttu-id="4e517-191">U dijaloškom okviru **Brza izrada: član projektnog tima** koji se prikaže, u polju **Značajka** odaberite ulogu generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="4e517-192">U polju **Jedinica za resurse** odaberite organizacijsku jedinicu za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="4e517-193">Zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="4e517-193">Then select **Save**.</span></span>

    ![Dijaloški okvir Brza izrada: član projektnog tima](media/Resource-Management-image24.png)

    <span data-ttu-id="4e517-195">Generički član tima sada je dodijeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="4e517-195">The generic team member is now assigned to the task.</span></span>

    ![Generički član tima dodijeljen zadatku](media/Resource-Management-image25.png)

    <span data-ttu-id="4e517-197">Na kartici **Tim** vidjet ćete novog generičkog člana tima.</span><span class="sxs-lookup"><span data-stu-id="4e517-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="4e517-198">Imajte na umu da ima samo dodijeljene sate.</span><span class="sxs-lookup"><span data-stu-id="4e517-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="4e517-199">Ti su sati zbroj svih zadataka koji su dodijeljeni generičkom članu tima.</span><span class="sxs-lookup"><span data-stu-id="4e517-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="4e517-200">Generički član tima još uvijek nema potrebne sate ili preduvjet resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Generički član tima na kartici Tim](media/Resource-Management-image26.png)

5. <span data-ttu-id="4e517-202">Sada možete dodijeliti generičkog člana tima drugim zadacima pomoću odabira resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Generički član tima u odabiru resursa](media/Resource-Management-image27.png)

    <span data-ttu-id="4e517-204">Kada dovršite dodjeljivanje generičkog resursa zadacima, možete generirati preduvjet resursa za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="4e517-205">Na kartici **Tim** odaberite generički resurs, a zatim odaberite **Generiraj preduvjet**.</span><span class="sxs-lookup"><span data-stu-id="4e517-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Naredba za generiranje preduvjeta](media/Resource-Management-image28.png)

    <span data-ttu-id="4e517-207">Kada se preduvjet generira, generički član tima imat će potrebne sate i vezu na preduvjet resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Veza na preduvjet resursa](media/Resource-Management-image29.png)

    <span data-ttu-id="4e517-209">Nakon što rezervirate imenovani resurs, generički resurs uklanja se iz tima i zamjenjuje imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="4e517-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Generički resurs zamijenjen je imenovanim resursom](media/Resource-Management-image30.png)

    <span data-ttu-id="4e517-211">Na kartici **Raspored** dodjele generičkih resursa uklonjene su i zamijenjene imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="4e517-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Dodjele generičkih resursa zamijenjene imenovanim resursom na kartici Raspored](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="4e517-213">To se događa samo kada je imenovani resurs u potpunosti rezerviran za preduvjet generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="4e517-214">Kada imenovani resurs djelomično zamjenjuje generički uvjet resursa ili više imenovanih resursa zamjenjuje preduvjet generičkog resursa, generički resurs ostaje dodijeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="4e517-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="4e517-215">Na sljedećoj ilustraciji 80-satni zadatak planiran je za trajanje od pet dana (16 sati dnevno tijekom pet dana) i dodijeljen generičkom resursu koji naziva **Funkcionalno**.</span><span class="sxs-lookup"><span data-stu-id="4e517-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-satni, petodnevni zadatak dodijeljen generičkom resursu naziva Funkcionalno](media/Resource-Management-image32.png)

    <span data-ttu-id="4e517-217">Kada generirate preduvjet, on se odnosi na 80 sati tijekom pet dana.</span><span class="sxs-lookup"><span data-stu-id="4e517-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Preduvjet generiran za 80 sati tijekom pet dana](media/Resource-Management-image33.png)

    <span data-ttu-id="4e517-219">Budući da dostupni resursi funkcioniraju samo osam sati dnevno, za ispunjavanje preduvjeta potrebna su dva resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Drugi resurs](media/Resource-Management-image35.png)

    <span data-ttu-id="4e517-221">Na kartici **Tim** sada možete vidjeti da generički resurs nema potrebne sate, ali dodijeljeni sati i dalje se prikazuju s dva imenovana resursa koji su potrebni za ispunjavanje preduvjeta.</span><span class="sxs-lookup"><span data-stu-id="4e517-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dva imenovana resursa na kartici Tim](media/Resource-Management-image36.png)

    <span data-ttu-id="4e517-223">Na kartici **Raspored** generički resurs ostaje dodijeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="4e517-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Generički resursi na kartici Raspored](media/Resource-Management-image37.png)

<span data-ttu-id="4e517-225">PSA ne dodjeljuje oba resursa zadatku jer bi to ponašanje rezultiralo manje predvidljivim rasporedom.</span><span class="sxs-lookup"><span data-stu-id="4e517-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="4e517-226">U ovom jednostavnom primjeru lako je podijeliti sate jednako između dva resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="4e517-227">Međutim, u složenijim scenarijima koji uključuju više zadataka i više resursa, PSA bi morao donijeti pretpostavke o tome kako bi trebao dodijeliti rezervacije koje su primljene za više resursa u više zadataka.</span><span class="sxs-lookup"><span data-stu-id="4e517-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="4e517-228">Stoga je u tim scenarijima upravitelj projekta odgovoran za raščlanjivanje više rezervacija i njihovo dodjeljivanje po potrebi.</span><span class="sxs-lookup"><span data-stu-id="4e517-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="4e517-229">Da bi dodijelio rezervacije, upravitelj projekta dodjeljuje zadatke iz generičkih resursa imenovanom resursu i zatim koristi prikaz **Usklađivanje** kako bi se osiguralo da dodjela funkcionira s rezervacijama.</span><span class="sxs-lookup"><span data-stu-id="4e517-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="4e517-230">Uređiivanje preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="4e517-230">Edit a resource requirement</span></span>

<span data-ttu-id="4e517-231">Nakon izrade preduvjeta resursa upravitelj projekta ili upravitelj resursa možda će htjeti urediti pojedinosti kako bi precizirao kriterije pretraživanja pri upotrebi ploče s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="4e517-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="4e517-232">Da biste uredili preduvjet resursa, poduzmite ove korake.</span><span class="sxs-lookup"><span data-stu-id="4e517-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="4e517-233">Na stranici **Projekti** na kartici **Tim** odaberite vezu na bilo koji preduvjet generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="4e517-234">Na stranici **Preduvjet resursa** koja se prikaže možete ažurirati nekoliko atributa.</span><span class="sxs-lookup"><span data-stu-id="4e517-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="4e517-235">Evo nekoliko primjera:</span><span class="sxs-lookup"><span data-stu-id="4e517-235">Here are some examples:</span></span>

    - <span data-ttu-id="4e517-236">naziv</span><span class="sxs-lookup"><span data-stu-id="4e517-236">Name</span></span>
    - <span data-ttu-id="4e517-237">Od datuma</span><span class="sxs-lookup"><span data-stu-id="4e517-237">From Date</span></span>
    - <span data-ttu-id="4e517-238">Do datuma</span><span class="sxs-lookup"><span data-stu-id="4e517-238">To Date</span></span>
    - <span data-ttu-id="4e517-239">Trajanje</span><span class="sxs-lookup"><span data-stu-id="4e517-239">Duration</span></span>
    - <span data-ttu-id="4e517-240">Vrsta resursa</span><span class="sxs-lookup"><span data-stu-id="4e517-240">Resource Type</span></span>

<span data-ttu-id="4e517-241">Na stranici **Preduvjet resursa** upravitelj projekta ili upravitelj resursa može definirati i sljedeće podatke:</span><span class="sxs-lookup"><span data-stu-id="4e517-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="4e517-242">Vještine</span><span class="sxs-lookup"><span data-stu-id="4e517-242">Skills</span></span>
- <span data-ttu-id="4e517-243">Uloge</span><span class="sxs-lookup"><span data-stu-id="4e517-243">Roles</span></span>
- <span data-ttu-id="4e517-244">Preference resursa</span><span class="sxs-lookup"><span data-stu-id="4e517-244">Resource preferences</span></span>
- <span data-ttu-id="4e517-245">Željena organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="4e517-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="4e517-246">Ažuriranje rezervacija resursa nakon što su rezervirane u projektu</span><span class="sxs-lookup"><span data-stu-id="4e517-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="4e517-247">Nakon što dodate generički ili imenovani resurs u projektni tim, možete promijeniti rezervacije resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="4e517-248">Na stranici **Projekti** na kartici **Tim** odaberite člana tima, a zatim odaberite **Zadrži rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="4e517-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Ploča s rasporedom otvorena za odabranog člana tima](media/Resource-Management-image40.png)

    <span data-ttu-id="4e517-250">Prikazuju se ploča s rasporedom i rezervacije člana projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="4e517-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="4e517-251">Proširite zapis člana tima da biste vidjeli sate koji su rezervirane za taj projekt i druge projekte koji koriste kapacitet člana tima.</span><span class="sxs-lookup"><span data-stu-id="4e517-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="4e517-252">Odaberite i povucite rezervaciju da biste je produljili ili skratili.</span><span class="sxs-lookup"><span data-stu-id="4e517-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="4e517-253">Prikazuje se dijaloški okvir **Izrada rezervacije resursa** koji vam omogućuje prilagodbu rezervacije.</span><span class="sxs-lookup"><span data-stu-id="4e517-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dijaloški okvir Izrada rezervacije resursa](media/Resource-Management-image41.png)

3. <span data-ttu-id="4e517-255">Desnom tipkom miša kliknite rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="4e517-255">Right-click the booking.</span></span> <span data-ttu-id="4e517-256">Zatim možete koristiti izbornik prečaca da biste dovršili sljedeće radnje:</span><span class="sxs-lookup"><span data-stu-id="4e517-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="4e517-257">Izmijenite status rezervacije.</span><span class="sxs-lookup"><span data-stu-id="4e517-257">Change the booking status.</span></span>
    - <span data-ttu-id="4e517-258">Uredite rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="4e517-258">Edit the booking.</span></span>
    - <span data-ttu-id="4e517-259">Zamijenite resurs u projektnom timu.</span><span class="sxs-lookup"><span data-stu-id="4e517-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="4e517-260">Izmjena statusa rezervacije</span><span class="sxs-lookup"><span data-stu-id="4e517-260">Change the booking status</span></span>

<span data-ttu-id="4e517-261">Možete izmijeniti bilo koji zadani ili prilagođeni status rezervacije.</span><span class="sxs-lookup"><span data-stu-id="4e517-261">You can change any default or custom booking status.</span></span>

![Naredba za status izmjene](media/Resource-Management-image42.png)

<span data-ttu-id="4e517-263">PSA obuhvaća sljedeće statuse:</span><span class="sxs-lookup"><span data-stu-id="4e517-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="4e517-264">**Otkazano** – ovaj status poništava rezervaciju resursa i oslobađa kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="4e517-265">**Fiksna rezervacija** – ovaj status koristi kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="4e517-266">Rezervacija obično ima taj status kada otvorite **Zadržavanje rezervacija** iz rešetke **Svi članovi tima** na stranici **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="4e517-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="4e517-267">**Promjenjiva rezervacija** – ovaj status dodaje resurs timu, ali ne koristi kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="4e517-268">To označava da je resurs rezerviran za potencijalni rad, ali još uvijek ima kapacitet ako je potreban za druge poslove.</span><span class="sxs-lookup"><span data-stu-id="4e517-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="4e517-269">U prikazu ukupne dostupnosti resursa promjenjive rezervacije imaju različit status od fiksnih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="4e517-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="4e517-270">**Predloženo** – ovaj status predstavlja prijedlog upravitelja resursa ili upravitelja projekta za resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="4e517-271">Prijedlozi ne koriste kapacitet resursa, a resurs nije dodan u projektni tim.</span><span class="sxs-lookup"><span data-stu-id="4e517-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="4e517-272">Da biste fiksno rezervirali resurs u timu, upravitelj projekta mora prihvatiti prijedlog.</span><span class="sxs-lookup"><span data-stu-id="4e517-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="4e517-273">Pošalji zahtjeve za resurs</span><span class="sxs-lookup"><span data-stu-id="4e517-273">Submit resource requests</span></span>

<span data-ttu-id="4e517-274">Zahtjevi za resurse koriste se za prijenos potražnje (preduvjet resursa) koji upravitelj resursa mora ispuniti.</span><span class="sxs-lookup"><span data-stu-id="4e517-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="4e517-275">Za generički resurs koji je već u timu možete izravno poslati zahtjev za resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="4e517-276">Zahtjev za resurs može se ispuniti na dva načina:</span><span class="sxs-lookup"><span data-stu-id="4e517-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="4e517-277">Upravitelj resursa izravno ispunjava zahtjev.</span><span class="sxs-lookup"><span data-stu-id="4e517-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="4e517-278">U tom slučaju generički resurs zamjenjuje se fiksnom rezervacijom koja sadrži imenovani resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="4e517-279">Upravitelj resursa predlaže resurs upravitelju projekta, a upravitelj projekta odobrava ili odbacuje predloženi resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="4e517-280">Izravno ispunjavanje zahtjeva za resurse</span><span class="sxs-lookup"><span data-stu-id="4e517-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="4e517-281">Kada se generira preduvjet resursa, upravitelj projekta može poslati zahtjev za resurs za generički resurs tako da odabere resurs, a zatim **Pošalji zahtjev**.</span><span class="sxs-lookup"><span data-stu-id="4e517-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Gumb Pošalji zahtjev](media/Resource-Management-image45.png)

<span data-ttu-id="4e517-283">Komentari o resursu mogu se pružiti upravitelju resursa koji ispunjava zahtjev.</span><span class="sxs-lookup"><span data-stu-id="4e517-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="4e517-284">Nakon podnošenja zahtjeva polje **Status** za člana tima mijenja se u **Poslano.**</span><span class="sxs-lookup"><span data-stu-id="4e517-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Unos neobaveznih komentara](media/Resource-Management-image46.png)

<span data-ttu-id="4e517-286">Kada upravitelj resursa ispuni zahtjev, generički član tima zamjenjuje se imenovanim resursom u rešetki **Svi članovi tima**.</span><span class="sxs-lookup"><span data-stu-id="4e517-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Generički član tima zamijenjen imenovanim resursom u rešetki Svi članovi tima](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="4e517-288">Upotreba prijedloga resursa za zahtjeve za resurse</span><span class="sxs-lookup"><span data-stu-id="4e517-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="4e517-289">Umjesto izravnog rezerviranja resursa u zahtjevu resursa, upravitelj resursa može predložiti resurs upravitelju projekta.</span><span class="sxs-lookup"><span data-stu-id="4e517-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="4e517-290">Upravitelj resursa može koristiti ovu mogućnost kada točno podudaranje za zahtjeve nije dostupno.</span><span class="sxs-lookup"><span data-stu-id="4e517-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="4e517-291">Kada upravitelj resursa predloži resurs, upravitelj projekta vidi da se polje **Status** za generičkog člana tima izmijenilo u **Potreban pregled**.</span><span class="sxs-lookup"><span data-stu-id="4e517-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Status generičkog člana tima izmijenjen u Potreban pregled](media/Resource-Management-image48.png)

<span data-ttu-id="4e517-293">Za prikaz predloženog resursa zajedno s vizualizacijom učinka rezervacije prijedloga dvaput kliknite člana tima koji ima status pregleda **Potreban pregled**.</span><span class="sxs-lookup"><span data-stu-id="4e517-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="4e517-294">Zatim odaberite karticu **Predloženi resursi**.</span><span class="sxs-lookup"><span data-stu-id="4e517-294">Then select the **Proposed Resources** tab.</span></span>

![Kartica Predloženi resursi](media/Resource-Management-image49.png)

<span data-ttu-id="4e517-296">Odaberite **Prihvati sve prijedloge** kako biste prihvatili sve predložene resurse ili **Odbaci sve prijedloge** kako biste ih odbacili.</span><span class="sxs-lookup"><span data-stu-id="4e517-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="4e517-297">Ako prihvatite predložene resurse, oni se fiksno rezerviraju u projektu kao članovi tima i zamjenjuju generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="4e517-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="4e517-298">Morate prihvatiti ili odbaciti sve predložene resurse.</span><span class="sxs-lookup"><span data-stu-id="4e517-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="4e517-299">Ne možete ih djelomično prihvatiti ili odbaciti.</span><span class="sxs-lookup"><span data-stu-id="4e517-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="4e517-300">Zamjena resursa u projektnom timu.</span><span class="sxs-lookup"><span data-stu-id="4e517-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="4e517-301">Ponekad upravitelj projekta mora zamijeniti rezerviranog člana tima na projektu.</span><span class="sxs-lookup"><span data-stu-id="4e517-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="4e517-302">Na stranici **Projekti** na kartici **Tim** odaberite resurs koji je potrebno zamijeniti, a zatim odaberite **Zadrži rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="4e517-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="4e517-303">Proširite resurs da biste vidjeli projekte kojima je dodijeljen.</span><span class="sxs-lookup"><span data-stu-id="4e517-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Resurs proširen za prikaz dodijeljenih projekata](media/Resource-Management-image50.png)

3. <span data-ttu-id="4e517-305">Desnom tipkom miša kliknite projekt, a zatim odaberite **Zamijeni resurs**.</span><span class="sxs-lookup"><span data-stu-id="4e517-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="4e517-306">Ako znate kojim resursom želite želite zamijeniti trenutačni resurs, odaberite ili unesite naziv, a zatim odaberite **Ponovno dodijeli**.</span><span class="sxs-lookup"><span data-stu-id="4e517-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Određivanje zamjenskog resursa](media/Resource-Management-image51.png)

    <span data-ttu-id="4e517-308">Umjesto toga, poduzmite ove korake da biste pretražili resurs:</span><span class="sxs-lookup"><span data-stu-id="4e517-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="4e517-309">Odaberite **Pronađi zamjenu**.</span><span class="sxs-lookup"><span data-stu-id="4e517-309">Select **Find Substitution**.</span></span>

        ![Pretraživanje zamjenskog resursa](media/Resource-Management-image52.png)

        <span data-ttu-id="4e517-311">Pomoćnik za raspored vraća popis dostupnih zamjena.</span><span class="sxs-lookup"><span data-stu-id="4e517-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="4e517-312">U pomoćniku za raspored možete dodatno filtrirati dostupne resurse kako biste pronašli odgovarajuću zamjenu.</span><span class="sxs-lookup"><span data-stu-id="4e517-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Popis dostupnih zamjena](media/Resource-Management-image53.png)

    2. <span data-ttu-id="4e517-314">Da biste zamijenili resurs, odaberite željeni resurs, a zatim odaberite **Zamijeni**.</span><span class="sxs-lookup"><span data-stu-id="4e517-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Zamjenski resurs odabran](media/Resource-Management-image54.png)

    <span data-ttu-id="4e517-316">Rezervacije i dodjele zamjenjuju se novim resursom.</span><span class="sxs-lookup"><span data-stu-id="4e517-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervacije i dodjele zamijenjene novim resursom](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="4e517-318">Usklađivanje rezervacija i dodjela člana tima</span><span class="sxs-lookup"><span data-stu-id="4e517-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="4e517-319">Za članove tima rezervacije i dodjele slobodno se uparuju.</span><span class="sxs-lookup"><span data-stu-id="4e517-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="4e517-320">Drugim riječima, resursi mogu imati dodjele, ali ne i rezervacije ili pak mogu imati rezervacije, ali ne i dodjele.</span><span class="sxs-lookup"><span data-stu-id="4e517-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="4e517-321">U idealnom slučaju rezervacije i dodjele trebaju biti usklađene, tako da resursi imaju potvrđeni kapacitet za izvođenje dodjela zadataka.</span><span class="sxs-lookup"><span data-stu-id="4e517-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="4e517-322">Međutim, rezervacije se mogu temeljiti na dostupnosti, a vremenski rasporedi zadataka mogu se promijeniti tijekom nastavka projekta.</span><span class="sxs-lookup"><span data-stu-id="4e517-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="4e517-323">Stoga slobodno uparivanje rezervacija i dodjela pruža fleksibilnost.</span><span class="sxs-lookup"><span data-stu-id="4e517-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="4e517-324">PSA ima karticu **Usklađivanje** koja upraviteljima projekata omogućuje usklađivanje rezervacija članova tima i njihovih zadataka za projektne timove.</span><span class="sxs-lookup"><span data-stu-id="4e517-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Kartica Usklađivanje](media/Resource-Management-image56.png)

<span data-ttu-id="4e517-326">Kartica **Usklađivanje** prikazuje rezervacije i dodjele na razini dodjele pojedinačnog zadatka za svakog člana tima.</span><span class="sxs-lookup"><span data-stu-id="4e517-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="4e517-327">Prikazuje sate u ćelijama koje predstavljaju vremensko razdoblje od mjeseci do dana.</span><span class="sxs-lookup"><span data-stu-id="4e517-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="4e517-328">Kartica također prikazuje ukupni neto iznos za projekt, zajedno sa stupcem ukupne vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="4e517-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="4e517-329">Za svaki resurs kartica izračunava razliku između rezervacija člana tima i skupnu vrijednost dodjela zadataka člana tima.</span><span class="sxs-lookup"><span data-stu-id="4e517-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="4e517-330">Ta bi razlika idealno trebala iznositi 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="4e517-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="4e517-331">Drugim riječima, ne bi trebalo biti razlike između rezervacija i dodjela.</span><span class="sxs-lookup"><span data-stu-id="4e517-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="4e517-332">Razlike su obojene i zasjenjene kako bi privukle pozornost na dva uvjeta:</span><span class="sxs-lookup"><span data-stu-id="4e517-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="4e517-333">**Nedostatak rezervacija** – nedostatak rezervacija događa se kada resurs ima više dodjela nego rezervacija.</span><span class="sxs-lookup"><span data-stu-id="4e517-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="4e517-334">Budući da taj kapacitet nije rezerviran, upravitelj projekta možda će htjeti ispraviti taj uvjet produljivanjem rezervacija resursa kako bi se pokrio manjak.</span><span class="sxs-lookup"><span data-stu-id="4e517-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="4e517-335">**Previše rezervacija** – previše se rezervacija pojavljuje kada je resurs rezerviran za projekt, ali nije dodijeljen zadacima.</span><span class="sxs-lookup"><span data-stu-id="4e517-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="4e517-336">Taj uvjet može biti prihvatljiv u slučajevima kada je resurs rezerviran za projekt prije dodjele zadataka.</span><span class="sxs-lookup"><span data-stu-id="4e517-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="4e517-337">Međutim, u drugim slučajevima resurs nije planiran za dodjelu zadacima.</span><span class="sxs-lookup"><span data-stu-id="4e517-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="4e517-338">U tim slučajevima upravitelj projekta trebao bi razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekt.</span><span class="sxs-lookup"><span data-stu-id="4e517-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="4e517-339">U nekim slučajevima, kada pregledate vrijeme na razini koja je viša od dnevne (na primjer, razina mjeseca), možda ćete vidjeti neto razliku u iznosu nula za resurs (drugim riječima, rezervacije = dodjele).</span><span class="sxs-lookup"><span data-stu-id="4e517-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="4e517-340">Međutim, ako pogledate vrijeme na razini tjedna, možda ćete vidjeti da postoje dodjele od nula sati i rezervacije od 40 sati u prvom tjednu, no dodjele od 40 sati i rezervacije od nula sati u drugom tjednu.</span><span class="sxs-lookup"><span data-stu-id="4e517-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="4e517-341">Sveukupno, rezervacije i dodjele usklađene su, ali se razlikuju od jednog do drugog tjedna.</span><span class="sxs-lookup"><span data-stu-id="4e517-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="4e517-342">Kada pogledate vrijeme na višim razinama, ćelije na kartici **Usklađivanje** imaju pokazatelj koji će vas obavijestiti da postoje razlike na nižim razinama.</span><span class="sxs-lookup"><span data-stu-id="4e517-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="4e517-343">Dvostrukim klikom na ćeliju možete povećati prikaz razlike.</span><span class="sxs-lookup"><span data-stu-id="4e517-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="4e517-344">Zatim desnom tipkom miša možete pritisnuti gumb da biste smanjili prikaz. Odabirom resursa i korištenjem kontrole **Sljedeća razlika** na alatnoj traci rešetke možete ići na sljedeću razliku između rezervacija i dodjela za taj resurs.</span><span class="sxs-lookup"><span data-stu-id="4e517-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="4e517-345">Zatim možete koristiti kontrolu **Prethodna razlika** da biste se vratili.</span><span class="sxs-lookup"><span data-stu-id="4e517-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="4e517-346">Možete i isključiti pokazatelj razlike i ponašanje navigacije u odjeljku **Postavke.**</span><span class="sxs-lookup"><span data-stu-id="4e517-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Pokazatelj razlike](media/Resource-Management-image57.png)

<span data-ttu-id="4e517-348">Ako imate dodjele zadataka za resurs, ali bez rezervacija, na stranici **Projekti** na kartici **Usklađivanje** odaberite manjak rezervacija, a zatim odaberite **Produlji rezervaciju**.</span><span class="sxs-lookup"><span data-stu-id="4e517-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="4e517-349">Prikazat će se dijaloški okvir **Produlji rezervaciju** produljivanje rezervacije i rezervacija koju je potrebna za rješavanje manjka resursa.</span><span class="sxs-lookup"><span data-stu-id="4e517-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="4e517-350">Prikazuju se i postojeće rezervacije resursa u svim projektima ili drugim entitetima koji se mogu zakazati.</span><span class="sxs-lookup"><span data-stu-id="4e517-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="4e517-351">Ako odaberete **U redu** da biste izradili rezervaciju za resurs, bez obzira na dostupnost tog resursa, može doći do prebukiranosti.</span><span class="sxs-lookup"><span data-stu-id="4e517-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dijaloški okvir Produlji rezervaciju](media/Resource-Management-image58.png)

<span data-ttu-id="4e517-353">Upravitelj projekta ili upravitelj resursa zatim može koristiti ploču s rasporedom kako bi upravljao svim situacijama u kojima je resurs prebukiran izvan svog kapaciteta.</span><span class="sxs-lookup"><span data-stu-id="4e517-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
