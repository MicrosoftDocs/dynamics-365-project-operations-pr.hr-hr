---
title: Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu
description: U ovoj temi nalaze se informacije o načinu dodavanja naplatnih komponenti u retke ugovora u projektnim operacijama.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003712"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="23753-103">Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="23753-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="23753-104">_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="23753-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="23753-105">Redak ugovora koji se temelji na projektu ima *naplative* komponente i *naplative* komponente.</span><span class="sxs-lookup"><span data-stu-id="23753-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="23753-106">Uključene komponente, komponente su koje podliježu:</span><span class="sxs-lookup"><span data-stu-id="23753-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="23753-107">Način naplate i podjele klijenta</span><span class="sxs-lookup"><span data-stu-id="23753-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="23753-108">Ograničenja koja se ne smiju prekoračiti</span><span class="sxs-lookup"><span data-stu-id="23753-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="23753-109">Postavke učestalosti fakture definirane u retku ugovora koji se temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="23753-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="23753-110">Podskup uključenih komponenti može se označiti kao naplativ s pomoću polja **Vrsta naplate**.</span><span class="sxs-lookup"><span data-stu-id="23753-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="23753-111">Polje **Vrsta naplate** skup je mogućnosti koji dopušta sljedeće vrijednosti u kontekstu retka ugovora:</span><span class="sxs-lookup"><span data-stu-id="23753-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="23753-112">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-112">Chargeable</span></span>
  - <span data-ttu-id="23753-113">Nenaplativo</span><span class="sxs-lookup"><span data-stu-id="23753-113">Non-chargeable</span></span>

<span data-ttu-id="23753-114">Komponente koje se naplaćuju mogu se definirati u zadacima, ulogama i kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="23753-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="23753-115">Mogućnost naplate definirana je na zadacima za redak ugovora o projektu i primjenjuje se na sve klase transakcija uključene u redak.</span><span class="sxs-lookup"><span data-stu-id="23753-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="23753-116">Ako je polje **Uključi zadatke** u retku ugovora prazno ili postavljeno na **Cijeli projekt**, kartica **Naplativi zadaci** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="23753-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="23753-117">Mogućnost naplate definirana u ulogama za redak ugovora o projektu odnosi se samo na klasu transakcije **Vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="23753-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="23753-118">Ako je polje **Uključi vrijeme** u retku ugovora o projektu postavljeno na **Ne**, kartica **Naplative uloge** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="23753-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="23753-119">Mogućnost naplate definirana je u kategorijama transakcije za redak ugovora o projektu i primjenjuje se samo na klasu transakcije **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="23753-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="23753-120">Ako je polje **Uključi troškove** postavljeno na **Ne**, kartica **Naplative kategorije** neće biti dostupna.</span><span class="sxs-lookup"><span data-stu-id="23753-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="23753-121">Ažuriranje projektnog zadatka kao naplativog ili nenaplativog</span><span class="sxs-lookup"><span data-stu-id="23753-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="23753-122">Projektni zadatak može biti naplativ ili nenaplativ u određenom retku ugovora koji omogućuje sljedeće postavljanje:</span><span class="sxs-lookup"><span data-stu-id="23753-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="23753-123">Ako redak ugovora koji se temelji na projektu uključuje **Vrijeme** i određeni zadatak, **T1** povezan je s njim kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="23753-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="23753-124">Ako postoji drugi redak ugovora koji uključuje stavku **Trošak**, možete povezati zadatak T1 s retkom ugovora kao nenaplativ.</span><span class="sxs-lookup"><span data-stu-id="23753-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="23753-125">Rezultat je da se svo vrijeme zabilježeno na zadatku naplaćuje, dok su svi troškovi nenaplativi.</span><span class="sxs-lookup"><span data-stu-id="23753-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="23753-126">Vrsta naplate zadatka može se konfigurirati na kartici **Naplativi zadaci** retka ugovora ažuriranjem polja **Vrsta naplate** u podrešetki zadataka retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="23753-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="23753-127">Umjesto toga, možete ažurirati polje **Vrsta naplate** na podrešetki postavke naplate zadatka projekta koja prikazuje retke povezane sa zadatkom.</span><span class="sxs-lookup"><span data-stu-id="23753-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="23753-128">Ažuriranje uloge kao naplative ili nenaplative</span><span class="sxs-lookup"><span data-stu-id="23753-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="23753-129">Uloga može biti naplativa ili nenaplativa u određenom retku ugovora.</span><span class="sxs-lookup"><span data-stu-id="23753-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="23753-130">Vrsta naplate za ulogu može se konfigurirati na kartici **Naplative uloge** retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="23753-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="23753-131">Kako biste to učinili, ažurirajte polje **Vrsta naplate** u podrešetki **Naplative uloge**.</span><span class="sxs-lookup"><span data-stu-id="23753-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="23753-132">Ažuriranje kategorije transakcije kao naplativa ili nenaplativa</span><span class="sxs-lookup"><span data-stu-id="23753-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="23753-133">Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ugovora.</span><span class="sxs-lookup"><span data-stu-id="23753-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="23753-134">Vrsta naplate transakcije može se konfigurirati na kartici **Naplative kategorije** retka ugovora koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="23753-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="23753-135">Kako biste to učinili, ažurirajte polje **Vrsta naplate** u podrešetki **Naplative kategorije**.</span><span class="sxs-lookup"><span data-stu-id="23753-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="23753-136">Rješavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="23753-136">Resolve chargeability</span></span>

<span data-ttu-id="23753-137">Procjena ili stvarni podatak stvoren za vrijeme smatra se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="23753-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="23753-138">**Vrijeme** uključeno u redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="23753-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="23753-139">**Uloga** konfigurirana kao naplativa u retku ugvora.</span><span class="sxs-lookup"><span data-stu-id="23753-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="23753-140">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ugovora.</span><span class="sxs-lookup"><span data-stu-id="23753-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="23753-141">Ako su ove tri stvari točne, zadatak je konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="23753-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="23753-142">Procjena ili stvarni podatak stvoren za trošak smatra se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="23753-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="23753-143">**Trošak** uključeno u redak ugovora</span><span class="sxs-lookup"><span data-stu-id="23753-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="23753-144">**Kategorija transakcije** konfigurirana kao naplativa u retku ugovora</span><span class="sxs-lookup"><span data-stu-id="23753-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="23753-145">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadatak** u retku ugovora</span><span class="sxs-lookup"><span data-stu-id="23753-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="23753-146">Ako su ove tri stvari točne, **Zadatak** je konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="23753-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="23753-147">Procjena ili stvarni podatak stvoren za materijal smatra se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="23753-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="23753-148">Stavka **Materijali** uključena u redak ugovora</span><span class="sxs-lookup"><span data-stu-id="23753-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="23753-149">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ugovora</span><span class="sxs-lookup"><span data-stu-id="23753-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="23753-150">Ako su ove dvije stvari točne, **Zadatak** je konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="23753-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-151">
                    <strong>Uključuje Vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="23753-152">
                    <strong>Uključuje Trošak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="23753-153">
                    <strong>Obuhvaća materijale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="23753-154">
                    <strong>Uključeni zadaci</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-155">
                    <strong>Uloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-156">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-157">
                    <strong>Zadatak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="23753-158">
                    <strong>Učinak naplativosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-159">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-160">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-161">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-162">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="23753-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-163">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-164">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-165">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-166">Naplata za stvarno vrijeme: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-167">Vrsta naplate stvarnog troška: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-168">Vrsta naplate stvarnog materijala: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-169">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-170">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-171">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-172">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="23753-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-173">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-174">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-175">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-176">Naplata za stvarno vrijeme: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-177">Vrsta naplate stvarnog troška: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-178">Vrsta naplate stvarnog materijala: <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-179">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-180">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-181">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-182">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="23753-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-183">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-184">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-185">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-186">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-187">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23753-188">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-189">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-190">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-191">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-192">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="23753-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-193">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-194">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-195">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-196">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-197">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-198">Vrsta naplate stvarnog materijala: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-199">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-200">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-201">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-202">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="23753-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-203">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-204">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-205">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-206">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-207">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-208">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-209">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-210">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-211">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-212">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="23753-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-213">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-214">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-215">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-216">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-217">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-218">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-220">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-221">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-222">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="23753-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-223">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-224">
                    <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-225">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-226">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-227">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23753-228">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-230">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-231">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-232">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="23753-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-233">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-234">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-235">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-236">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-237">Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-238">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-239">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="23753-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-241">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-242">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="23753-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-243">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-244">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-245">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-246">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23753-247">Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-248">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-249">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="23753-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="23753-251">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-252">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="23753-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-253">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-254">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-255">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-256">Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-257">Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-258">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-259">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-260">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="23753-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-262">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="23753-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-263">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-264">Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-265">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-266">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23753-267">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="23753-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="23753-268">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="23753-269">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="23753-270">Jest</span><span class="sxs-lookup"><span data-stu-id="23753-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="23753-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="23753-272">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="23753-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="23753-273">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="23753-274">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="23753-275">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="23753-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="23753-276">Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-277">Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="23753-278">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23753-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
