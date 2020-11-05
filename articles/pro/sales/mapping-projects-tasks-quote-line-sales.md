---
title: Mapiranje projekata i zadataka u redak ponude koji se temelji na projektu
description: U ovoj temi nalaze se informacije o načinu mapiranja projekata i zadataka u redak zadatka koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073280"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="d0d79-103">Mapiranje projekata i zadataka u redak ponude koji se temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="d0d79-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="d0d79-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="d0d79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0d79-105">U retke ponude koji se temelje na projektu možete mapirati određene zadatke projekta koji su već povezani s retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="d0d79-106">Kada mapirate zadatke u redak ponude, sljedeće će se stavke koje ste definirali u retku ponude primijeniti samo na te zadatke:</span><span class="sxs-lookup"><span data-stu-id="d0d79-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="d0d79-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="d0d79-107">Billing method</span></span>
- <span data-ttu-id="d0d79-108">Mogućnosti naplate</span><span class="sxs-lookup"><span data-stu-id="d0d79-108">Chargeability options</span></span>
- <span data-ttu-id="d0d79-109">Ograničenja koja se ne smiju prekoračiti</span><span class="sxs-lookup"><span data-stu-id="d0d79-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="d0d79-110">Klijenti</span><span class="sxs-lookup"><span data-stu-id="d0d79-110">Customers</span></span>

<span data-ttu-id="d0d79-111">Na primjer, možda imate projekt u kojem je jedna faza nepromjenjiva cijena, a sve ostale faze su vrijeme i materijali.</span><span class="sxs-lookup"><span data-stu-id="d0d79-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="d0d79-112">U tom slučaju, prvu fazu i sve njezine podređene zadatke možete povezati s retkom ponude za tu fazu uz način naplate s fiksnom cijenom.</span><span class="sxs-lookup"><span data-stu-id="d0d79-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="d0d79-113">Zatim možete povezati sve ostale faze s retkom ponude koji se temelji na vremenu i materijalu.</span><span class="sxs-lookup"><span data-stu-id="d0d79-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="d0d79-114">Povezivanje zadataka s redcima ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="d0d79-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="d0d79-115">Zadatke možete povezati s redcima ponude sa sljedećih lokacija:</span><span class="sxs-lookup"><span data-stu-id="d0d79-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="d0d79-116">Stranica **Projekt** > kartica **Naplata zadatka** (optimalno)</span><span class="sxs-lookup"><span data-stu-id="d0d79-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="d0d79-117">Stranica **Redak ponude** > kartica **Zadaci koji se naplaćuju**</span><span class="sxs-lookup"><span data-stu-id="d0d79-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="d0d79-118">Sa stranice projekta</span><span class="sxs-lookup"><span data-stu-id="d0d79-118">From the Project page</span></span>

<span data-ttu-id="d0d79-119">Stranica **Projekt** pruža optimalno iskustvo za povezivanje zadataka s redcima ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="d0d79-120">Ovu stranicu možete upotrijebiti za odabir više zadataka i povezivanje svih njih, kao i njihovih podređenih zadataka s odabranim retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="d0d79-121">Na kartici **Općenito** retka ponude koji se temelji na projektu, provjerite je li popunjeno polje **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="d0d79-122">U polju **Uključeni zadaci** odaberite mogućnost **Samo odabrani zadaci**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="d0d79-123">Spremanje retka ponude utemeljenog na projektu</span><span class="sxs-lookup"><span data-stu-id="d0d79-123">Save the project-based quote line.</span></span> <span data-ttu-id="d0d79-124">Kada se obrazac osvježi, prikazuje se kartica **Zadaci koji se naplaćuju**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="d0d79-125">Na kartici **Općenito** odaberite vezu za projekt iz polja **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="d0d79-126">Na stranici **Projekt** odaberite karticu **Naplata zadatka**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="d0d79-127">U drugoj rešetki, koja se odnosi na postavke naplate određenih zadataka, odaberite jedan ili više zadataka, a zatim odaberite **Poveži retke ponude**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="d0d79-128">Na dijaloškoj stranici koja se prikaže odaberite redak ponude koji na ponudi prikazuje retke ponude koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="d0d79-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="d0d79-129">U polju **Vrsta naplate** naznačite jesu li ti zadaci naplativi ili nenaplativi.</span><span class="sxs-lookup"><span data-stu-id="d0d79-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="d0d79-130">Označite potvrdni okvir kako biste naznačili treba li povezanost uključivati podređene zadatke odabranih zadataka.</span><span class="sxs-lookup"><span data-stu-id="d0d79-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="d0d79-131">Označavanjem okvira povezat će se podređeni zadaci odabranih zadataka s retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="d0d79-132">Odaberite **U redu** kako biste zatvorili dijaloški okvir.</span><span class="sxs-lookup"><span data-stu-id="d0d79-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="d0d79-133">Sa stranice retka ponude</span><span class="sxs-lookup"><span data-stu-id="d0d79-133">From the Quote line page</span></span>

<span data-ttu-id="d0d79-134">Projektne zadatke možete povezati s redcima ponude iz kartice **Zadaci koji se naplaćuju** na stranici **Redak ponude**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="d0d79-135">Optimalno mjesto za povezivanje projektnih zadataka s redcima ponude jest na kartici **Naplata zadatka** na stranici **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="d0d79-136">Ako povezujete zadatke iz kartice **Zadaci koji se naplaćuju** na stranici **Redak ponude** , svaki projekt morate ručno povezati.</span><span class="sxs-lookup"><span data-stu-id="d0d79-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="d0d79-137">Na kartici **Općenito** retka ponude koji se temelji na projektu, provjerite je li u polju **Projekt** odabran projekt.</span><span class="sxs-lookup"><span data-stu-id="d0d79-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="d0d79-138">U polju **Uključeni zadaci** odaberite mogućnost **Samo odabrani zadaci**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="d0d79-139">Spremanje retka ponude utemeljenog na projektu</span><span class="sxs-lookup"><span data-stu-id="d0d79-139">Save the project-based quote line.</span></span> <span data-ttu-id="d0d79-140">Kada se obrazac osvježi, prikazuje se kartica **Zadaci koji se naplaćuju**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="d0d79-141">Na kartici **Zadaci koji se naplaćuju** odaberite **Dodaj zadatak retka ponude**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="d0d79-142">Na stranici **Zadatak retka ponude** u polju **Zadaci** , odaberite zadatak i u polju **Vrsta naplate** odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="d0d79-143">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="d0d79-143">Close the page.</span></span> <span data-ttu-id="d0d79-144">Odabrani zadatak sada je povezan s retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="d0d79-145">Prekidanje veze zadataka od redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="d0d79-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="d0d79-146">Sa stranice projekta</span><span class="sxs-lookup"><span data-stu-id="d0d79-146">From the Project page</span></span>

<span data-ttu-id="d0d79-147">Ovaj način pruža najoptimalnije iskustvo za prekidanje veze zadataka od redaka ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="d0d79-148">Možete odabrati više zadataka, kao i njihove podređene zadatke, i prekinuti njihovu vezu s odabranim redcima ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="d0d79-149">Na kartici **Općenito** retka ponude koji se temelji na projektu, u polju **Projekt** , odaberite vezu na projekt.</span><span class="sxs-lookup"><span data-stu-id="d0d79-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="d0d79-150">Na stranici **Projekt** odaberite karticu **Naplata zadatka**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="d0d79-151">U drugoj rešetki, koja se odnosi na postavke naplate određenih zadataka, odaberite jedan ili više zadataka, a zatim odaberite **Prekini vezu s redcima ponude**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="d0d79-152">Na dijaloškoj stranici koja se prikaže odaberite redak ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="d0d79-153">Označite potvrdni okvir kako biste naznačili treba li se povezanost ukloniti i s podređenih zadataka odabranih zadataka.</span><span class="sxs-lookup"><span data-stu-id="d0d79-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="d0d79-154">Označavanjem okvira prekinut ćete i vezu podređenih zadataka odabranih zadataka s retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="d0d79-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="d0d79-155">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-155">Select **OK**.</span></span> <span data-ttu-id="d0d79-156">Poruka upozorenja izvješćuje vas da ako uklonite ovu povezanost, svi stvarni podaci koji su prethodno zabilježeni u zadatku mogu se poništiti.</span><span class="sxs-lookup"><span data-stu-id="d0d79-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="d0d79-157">Odaberite **U redu** za nastavak i uklanjanje povezanosti između zadatka i retka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="d0d79-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="d0d79-158">Sa stranice retka ponude</span><span class="sxs-lookup"><span data-stu-id="d0d79-158">From the Quote line page</span></span>

<span data-ttu-id="d0d79-159">Projektnim zadacima možete i prekinuti vezu s redcima ponude iz kartice **Zadaci koji se naplaćuju** na stranici **Redak ponude**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="d0d79-160">Na kartici **Zadaci koji se naplaćuju** odaberite **Izbriši zadatak retka ponude**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="d0d79-161">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="d0d79-161">Select **OK**.</span></span> <span data-ttu-id="d0d79-162">Poruka upozorenja izvješćuje vas da ako uklonite ovu povezanost, svi stvarni podaci koji su prethodno zabilježeni u zadatku mogu se poništiti.</span><span class="sxs-lookup"><span data-stu-id="d0d79-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="d0d79-163">Odaberite **U redu** za nastavak i uklanjanje povezanosti između zadatka i retka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="d0d79-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="d0d79-164">Ovim postupkom zadatak se ne briše iz projekta.</span><span class="sxs-lookup"><span data-stu-id="d0d79-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="d0d79-165">Time se samo uklanja povezanost zadataka iz retka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="d0d79-165">It only removes the task association from the project-based quote line.</span></span>
