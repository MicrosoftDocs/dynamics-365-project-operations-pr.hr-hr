---
title: Grupe jedinica i jedinice
description: Ova tema pruža informacije o grupama jedinica i jedinicama.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145574"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="1a9fd-103">Grupe jedinica i jedinice</span><span class="sxs-lookup"><span data-stu-id="1a9fd-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1a9fd-104">Grupe jedinica i jedinice osnovni su entiteti u Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="1a9fd-105">Jedinica je pojedinačna jedinica mjere, a više jedinica može se grupirati u grupe jedinica.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="1a9fd-106">Grupa jedinica ponekad se naziva jediničnim rasporedom u korisničkom sučelju sustava Dynamics 365 (UI).</span><span class="sxs-lookup"><span data-stu-id="1a9fd-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="1a9fd-107">Evo nekoliko primjera jedinica i grupa jedinica:</span><span class="sxs-lookup"><span data-stu-id="1a9fd-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="1a9fd-108">**Grupa jedinica**: Udaljenost</span><span class="sxs-lookup"><span data-stu-id="1a9fd-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="1a9fd-109">**Jedinice**: milja, kilometar, i tako dalje.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="1a9fd-110">**Grupa jedinica**: Vrijeme</span><span class="sxs-lookup"><span data-stu-id="1a9fd-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="1a9fd-111">**Jedinice**: sat, dan, tjedan, i tako dalje.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="1a9fd-112">Kada postavite više jedinica u grupi jedinica, također morate postaviti faktor konverzije između njih tako da odredite prvu jedinicu koju ste postavili kao zadanu ili primarnu jedinicu za grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="1a9fd-113">Na primjer, u grupi jedinica **Vrijeme**, ako postavite **Sat** kao prvu jedinicu, sustav označava **Sat** kao zadanu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="1a9fd-114">Ako je sljedeća jedinica koju postavljate **Dan**, morate postaviti faktor konverzije za **Dan** u **Sat.**</span><span class="sxs-lookup"><span data-stu-id="1a9fd-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="1a9fd-115">Ako zatim dodate **Tjedan** kao treću jedinicu, morate postaviti faktor konverzije za **Tjedan** u smislu **Dana** ili **Sata**.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="1a9fd-116">Sljedeća slika prikazuje primjer postavljanja za jedinicu **Dan**, gdje polje **Količina** prikazuje broj sati koji su u danu i **Tjednu**, gdje polje **Količina** prikazuje broj dana u tjednu.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Grupa jedinica: informacijska stranica](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="1a9fd-118">Korištenje jedinica i grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-118">Using units and unit groups</span></span>

<span data-ttu-id="1a9fd-119">Dynamics 365 Project Service Automation koristi jedinice i grupe jedinica za obradu procjena i unosa za troškove i vrijeme.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="1a9fd-120">Za troškove, svaka kategorija troška ima zadanu grupu jedinica i jedinicu.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="1a9fd-121">Te se vrijednosti unose kao zadane vrijednosti u unosima cjenika za kategorije troškova.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="1a9fd-122">Na primjer, imate kategoriju troška koja se zove **Kilometraža**.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="1a9fd-123">Ima grupu jedinica koja se zove **Udaljenost** i zadanu jedinicu koja se zove **Milja.**</span><span class="sxs-lookup"><span data-stu-id="1a9fd-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="1a9fd-124">Ako postavite grupu jedinica **Udaljenost** tako da ima dvije jedinice (**Milja** i **Kilometar**), možete postaviti dvije cijene za kategoriju **Kilometraža** na jednom cjeniku: cijena po milji i cijena po kilometru.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="1a9fd-125">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="1a9fd-125">Expense category</span></span>  | <span data-ttu-id="1a9fd-126">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-126">Unit group</span></span>  | <span data-ttu-id="1a9fd-127">Jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-127">Unit</span></span>      | <span data-ttu-id="1a9fd-128">Način određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-128">Pricing method</span></span>  | <span data-ttu-id="1a9fd-129">Jedin. cijena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="1a9fd-130">Kilometraža</span><span class="sxs-lookup"><span data-stu-id="1a9fd-130">Mileage</span></span>           | <span data-ttu-id="1a9fd-131">Udaljenost</span><span class="sxs-lookup"><span data-stu-id="1a9fd-131">Distance</span></span>      | <span data-ttu-id="1a9fd-132">Milja</span><span class="sxs-lookup"><span data-stu-id="1a9fd-132">Mile</span></span>      | <span data-ttu-id="1a9fd-133">Jedin. cijena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-133">Price per unit</span></span>    | <span data-ttu-id="1a9fd-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="1a9fd-134">10 USD</span></span>            |
| <span data-ttu-id="1a9fd-135">Kilometraža</span><span class="sxs-lookup"><span data-stu-id="1a9fd-135">Mileage</span></span>           | <span data-ttu-id="1a9fd-136">Udaljenost</span><span class="sxs-lookup"><span data-stu-id="1a9fd-136">Distance</span></span>      | <span data-ttu-id="1a9fd-137">kilometar</span><span class="sxs-lookup"><span data-stu-id="1a9fd-137">Kilometer</span></span> | <span data-ttu-id="1a9fd-138">Jedin. cijena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-138">Price per unit</span></span>    |  <span data-ttu-id="1a9fd-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="1a9fd-139">6 USD</span></span>            |

<span data-ttu-id="1a9fd-140">Kada unesete trošak u projekt, sustav određuje cijenu kroz kombinaciju kategorije i jedinice za trošak.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="1a9fd-141">Opis troška</span><span class="sxs-lookup"><span data-stu-id="1a9fd-141">Expense description</span></span>        | <span data-ttu-id="1a9fd-142">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="1a9fd-142">Expense category</span></span>  | <span data-ttu-id="1a9fd-143">Jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-143">Unit</span></span>  | <span data-ttu-id="1a9fd-144">Količina</span><span class="sxs-lookup"><span data-stu-id="1a9fd-144">Quantity</span></span>  | <span data-ttu-id="1a9fd-145">Jedinična cijena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="1a9fd-146">Vozi do lokacije klijenta</span><span class="sxs-lookup"><span data-stu-id="1a9fd-146">Drive to client location</span></span> | <span data-ttu-id="1a9fd-147">Kilometraža</span><span class="sxs-lookup"><span data-stu-id="1a9fd-147">Mileage</span></span>             | <span data-ttu-id="1a9fd-148">Milja</span><span class="sxs-lookup"><span data-stu-id="1a9fd-148">Mile</span></span>  | <span data-ttu-id="1a9fd-149">1,0</span><span class="sxs-lookup"><span data-stu-id="1a9fd-149">10</span></span>        | <span data-ttu-id="1a9fd-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="1a9fd-150">10 USD</span></span>         |

<span data-ttu-id="1a9fd-151">Za vrijeme, svako zaglavlje cjenika ima polje **Zadana vremenska jedinica**.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="1a9fd-152">Vrijednost se postavlja kada izradite zaglavlje cjenika.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="1a9fd-153">Ta se jedinica zatim koristi za postavljanje svih cijena koje se temelje na ulozi na tom cjeniku.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="1a9fd-154">Reci procjene za polje **Vrijeme na ponudi** mogu se izraziti u bilo kojoj jedinici vremena.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="1a9fd-155">Međutim, reci procjene projekata i unosa vremena za projekte mogu koristiti samo jedinicu vremena **Sat**.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="1a9fd-156">Ako jedinica unosa vremena ili procjene ne odgovara jedinici u retku cjenika za tu ulogu, sustav pretvara cijenu u jedinice koje su definirane u procjeni projekta ili stvarnoj transakciji projekta.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="1a9fd-157">Sljedeći primjer pokazuje kako sustav PSA koristi grupu jedinica, jedinice i čimbenike konverzije.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="1a9fd-158">Jedinice</span><span class="sxs-lookup"><span data-stu-id="1a9fd-158">Units</span></span>

   - <span data-ttu-id="1a9fd-159">**Grupa jedinica**: Vrijeme</span><span class="sxs-lookup"><span data-stu-id="1a9fd-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="1a9fd-160">**Jedinice**: Sat</span><span class="sxs-lookup"><span data-stu-id="1a9fd-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="1a9fd-161">**Dan** - Faktor konverzije: 8 sati</span><span class="sxs-lookup"><span data-stu-id="1a9fd-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="1a9fd-162">**Tjedan** - Faktor konverzije: 40 sati</span><span class="sxs-lookup"><span data-stu-id="1a9fd-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="1a9fd-163">Postavljanje cjenika na projektu A:</span><span class="sxs-lookup"><span data-stu-id="1a9fd-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="1a9fd-164">**Naziv**: Prodajne cijene u UK-u za 2016.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="1a9fd-165">**Zadana vremenska jedinica**: Dan</span><span class="sxs-lookup"><span data-stu-id="1a9fd-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="1a9fd-166">**Valuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="1a9fd-166">**Currency**: GBP</span></span>

| <span data-ttu-id="1a9fd-167">Uloga</span><span class="sxs-lookup"><span data-stu-id="1a9fd-167">Role</span></span>      | <span data-ttu-id="1a9fd-168">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-168">Unit group</span></span> | <span data-ttu-id="1a9fd-169">Jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-169">Unit</span></span> | <span data-ttu-id="1a9fd-170">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-170">Organizational unit</span></span> | <span data-ttu-id="1a9fd-171">Cijena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="1a9fd-172">Razvojni inženjer</span><span class="sxs-lookup"><span data-stu-id="1a9fd-172">Developer</span></span> | <span data-ttu-id="1a9fd-173">Vrijeme</span><span class="sxs-lookup"><span data-stu-id="1a9fd-173">Time</span></span>       | <span data-ttu-id="1a9fd-174">Dan</span><span class="sxs-lookup"><span data-stu-id="1a9fd-174">Day</span></span>  | <span data-ttu-id="1a9fd-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="1a9fd-175">Contoso UK</span></span>          | <span data-ttu-id="1a9fd-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="1a9fd-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="1a9fd-177">Unos vremena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-177">Time entry</span></span>

<span data-ttu-id="1a9fd-178">Sljedeća tablica prikazuje dobivenu transakciju na strani prodaje koju je izradio sustav PSA za trosatni projekt.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="1a9fd-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="1a9fd-179">Project</span></span>   | <span data-ttu-id="1a9fd-180">Zadatak</span><span class="sxs-lookup"><span data-stu-id="1a9fd-180">Task</span></span>    | <span data-ttu-id="1a9fd-181">Uloga</span><span class="sxs-lookup"><span data-stu-id="1a9fd-181">Role</span></span>      | <span data-ttu-id="1a9fd-182">Količina</span><span class="sxs-lookup"><span data-stu-id="1a9fd-182">Quantity</span></span> | <span data-ttu-id="1a9fd-183">Jedinica</span><span class="sxs-lookup"><span data-stu-id="1a9fd-183">Unit</span></span>  | <span data-ttu-id="1a9fd-184">Jedinična cijena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-184">Unit price</span></span> | <span data-ttu-id="1a9fd-185">Nenaplaćeni iznos prodaje</span><span class="sxs-lookup"><span data-stu-id="1a9fd-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="1a9fd-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="1a9fd-186">Project A</span></span> | <span data-ttu-id="1a9fd-187">Dizajn</span><span class="sxs-lookup"><span data-stu-id="1a9fd-187">Design</span></span>  | <span data-ttu-id="1a9fd-188">Razvojni inženjer</span><span class="sxs-lookup"><span data-stu-id="1a9fd-188">Developer</span></span> | <span data-ttu-id="1a9fd-189">3</span><span class="sxs-lookup"><span data-stu-id="1a9fd-189">3</span></span>        | <span data-ttu-id="1a9fd-190">Sat</span><span class="sxs-lookup"><span data-stu-id="1a9fd-190">Hour</span></span>  | <span data-ttu-id="1a9fd-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="1a9fd-191">100 GBP</span></span>    | <span data-ttu-id="1a9fd-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="1a9fd-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="1a9fd-193">Često postavljena pitanja za jedinicu vremena</span><span class="sxs-lookup"><span data-stu-id="1a9fd-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="1a9fd-194">Pretvara li PSA u različite jedinice u slučaju troškova?</span><span class="sxs-lookup"><span data-stu-id="1a9fd-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="1a9fd-195">Ne.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-195">No.</span></span> <span data-ttu-id="1a9fd-196">Konverzija jedinica radi samo za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-196">Unit conversion works only for time.</span></span> <span data-ttu-id="1a9fd-197">Za troškove, ako sustav ne može pronaći cijenu za kombinaciju kategorije troška i jedinice, cijena je postavljena na 0,00 prema zadanim postavkama.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="1a9fd-198">Zašto PSA pretvara vremenske jedinice?</span><span class="sxs-lookup"><span data-stu-id="1a9fd-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="1a9fd-199">U nekim zemljama ili regijama postoji pravna obveza da se stope naplaćivanja postavljaju u danima.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="1a9fd-200">Pregovaranje o cijenama i disceniranje tijekom ciklusa ponude izvodi se koristeći dnevne stope za svaku naplativu ulogu.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="1a9fd-201">Procjena rasporeda i unos vremena izvode se u satima.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="1a9fd-202">Za podršku ove razlike u vremenskim jedinicama, PSA pretvara vremenske jedinice.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="1a9fd-203">Mogu li se vremenske jedinice promijeniti na procjenama projekta?</span><span class="sxs-lookup"><span data-stu-id="1a9fd-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="1a9fd-204">Ne.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-204">No.</span></span> <span data-ttu-id="1a9fd-205">Procjena rasporeda trenutačno je ograničena na sate i ne može se mijenjati.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="1a9fd-206">Mogu li se jedinice i grupe jedinica uređivati, brisati i dodavati?</span><span class="sxs-lookup"><span data-stu-id="1a9fd-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="1a9fd-207">Da.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-207">Yes.</span></span> <span data-ttu-id="1a9fd-208">Uz iznimku grupe jedinica **Vrijeme** i jedinice **Sat**, sve jedinice mogu se brisati ili uređivati, a mogu se dodati i nove jedinice.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="1a9fd-209">U sustavu PSA, grupa jedinica **Vrijeme** i jedinica **Sat** ne mogu se brisati.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="1a9fd-210">Međutim, oni se mogu ažurirati s prevedenim tekstom za polje **Naziv**.</span><span class="sxs-lookup"><span data-stu-id="1a9fd-210">However, they can be updated with a translated text for the **Name** field.</span></span>
