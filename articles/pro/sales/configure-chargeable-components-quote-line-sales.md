---
title: Konfiguriranje naplative komponente retka ponude
description: U ovoj temi nalaze se informacije o postavljanju naplativih i nenaplativih komponenti na retku ponude koji se temelji na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003757"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="b0377-103">Konfiguriranje naplative komponente retka ponude</span><span class="sxs-lookup"><span data-stu-id="b0377-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="b0377-104">_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="b0377-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b0377-105">Redak ponude koji se temelji na projektu ima koncept *uključenih* komponenti i *naplativih* komponenti.</span><span class="sxs-lookup"><span data-stu-id="b0377-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="b0377-106">Uključene komponente podliježu:</span><span class="sxs-lookup"><span data-stu-id="b0377-106">Included components are subject to:</span></span>

  - <span data-ttu-id="b0377-107">Način naplate i podjele klijenta</span><span class="sxs-lookup"><span data-stu-id="b0377-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="b0377-108">Ograničenja koja se ne smiju prekoračiti</span><span class="sxs-lookup"><span data-stu-id="b0377-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="b0377-109">Postavke učestalosti fakture definirane u retku ponude koji se temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="b0377-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="b0377-110">Podskup uključenih komponenti može se označiti kao naplativ s pomoću polja **Vrsta naplate**.</span><span class="sxs-lookup"><span data-stu-id="b0377-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="b0377-111">Polje **Vrsta naplate** skup je mogućnosti koji dopušta sljedeće vrijednosti u kontekstu retka ponude:</span><span class="sxs-lookup"><span data-stu-id="b0377-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="b0377-112">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-112">Chargeable</span></span>
  - <span data-ttu-id="b0377-113">Nenaplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-113">Non-chargeable</span></span>

<span data-ttu-id="b0377-114">Komponente koje se naplaćuju mogu se definirati u zadacima, ulogama i kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="b0377-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="b0377-115">Mogućnost naplate definirana je na zadacima za redak ponude i primjenjuje se na sve klase transakcija uključene u taj redak.</span><span class="sxs-lookup"><span data-stu-id="b0377-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="b0377-116">Ako je polje **Uključi zadatke** postavljeno na **Cijeli projekt** ili je ostavljeno prazno, kartica **Naplativi zadaci** nije dostupna.</span><span class="sxs-lookup"><span data-stu-id="b0377-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="b0377-117">Mogućnost naplate definirana je u ulogama za redak ponude i primjenjuje se samo na klasu transakcije **Vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="b0377-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="b0377-118">Ako je polje **Uključi vrijeme** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative uloge** nije dostupna.</span><span class="sxs-lookup"><span data-stu-id="b0377-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="b0377-119">Mogućnost naplate definirana je u kategorijama transakcije za redak ponude i primjenjuje se samo na klasu transakcije **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="b0377-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="b0377-120">Ako je polje **Uključi troškove** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative kategorije** nije dostupna.</span><span class="sxs-lookup"><span data-stu-id="b0377-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0377-121">Ažuriranje projektnog zadatka kako bi bio naplativ ili nenaplativ</span><span class="sxs-lookup"><span data-stu-id="b0377-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0377-122">Projektni zadatak može biti naplativ ili nenaplativ u kontekstu određenog retka ponude koji se temelji na projektu, što omogućuje sljedeće postavljanje.</span><span class="sxs-lookup"><span data-stu-id="b0377-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="b0377-123">Ako redak ponude koji se temelji na projektu uključuje **Vrijeme** i zadatak **T1**, zadatak je povezan s retkom ponude kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0377-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="b0377-124">Ako postoji drugi redak ponude koji uključuje stavku **Troškovi**, možete povezati zadatak **T1** s retkom ponude kao nenaplativ.</span><span class="sxs-lookup"><span data-stu-id="b0377-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="b0377-125">Rezultat je da se svo vrijeme zabilježeno na zadatku naplaćuje, dok se svi troškovi zabilježeni na zadatku ne naplaćuju.</span><span class="sxs-lookup"><span data-stu-id="b0377-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="b0377-126">Vrsta naplate zadatka može se konfigurirati na kartici **Naplativi zadaci** retka ponude koji se temelji na projektu ažuriranjem polja **Vrsta naplate** u podrešetki **Zadaci retka ponude**.</span><span class="sxs-lookup"><span data-stu-id="b0377-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="b0377-127">Umjesto toga, možete ažurirati vrstu naplate za projektni zadatak u polju **Vrsta naplate** na podrešetki, na postavci naplate zadatka projekta koja prikazuje retke ponude povezane sa zadatkom.</span><span class="sxs-lookup"><span data-stu-id="b0377-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0377-128">Ažuriranje uloge kako bi bila naplativa ili nenaplativa</span><span class="sxs-lookup"><span data-stu-id="b0377-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0377-129">Uloga može biti naplativa ili nenaplativa u kontekstu određenog retka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="b0377-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="b0377-130">Vrsta naplate uloge može se konfigurirati na kartici **Naplative uloge** retka ponude ažuriranjem polja **Vrsta naplate** u podrešetki **Naplative uloge**.</span><span class="sxs-lookup"><span data-stu-id="b0377-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0377-131">Ažuriranje kategorije transakcije kako bi bila naplativa ili nenaplativa</span><span class="sxs-lookup"><span data-stu-id="b0377-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0377-132">Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="b0377-133">Vrsta naplate transakcije može se konfigurirati na kartici **Naplative kategorije** retka ponude ažuriranjem polja **Vrsta naplate** u podrešetki **Naplative kategorije**.</span><span class="sxs-lookup"><span data-stu-id="b0377-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="b0377-134">Rješavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="b0377-134">Resolve chargeability</span></span>
<span data-ttu-id="b0377-135">Procjena ili stvarni podatak stvoren za vrijeme smatrat će se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="b0377-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="b0377-136">**Vrijeme** uključeno u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="b0377-137">**Uloga** konfigurirana kao naplativa u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="b0377-138">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="b0377-139">Ako su ove tri stvari točne, **Zadatak** je također konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0377-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="b0377-140">Procjena ili stvarni podatak stvoren za trošak smatra se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="b0377-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="b0377-141">**Trošak** uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="b0377-142">**Kategorija transakcije** konfigurirana kao naplativa u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="b0377-143">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="b0377-144">Ako su ove tri stvari točne, **Zadatak** je također konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0377-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="b0377-145">Procjena ili stvarni podatak stvoren za materijal smatrat će se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="b0377-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="b0377-146">**Materijal** uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="b0377-147">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="b0377-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="b0377-148">Ako su ove dvije stvari točne, **Zadatak** bi također trebao biti konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="b0377-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-149">
                    <strong>Uključuje Vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0377-150">
                    <strong>Uključuje Trošak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0377-151">
                    <strong>Obuhvaća materijale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="b0377-152">
                    <strong>Uključeni zadaci</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-153">
                    <strong>Uloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-154">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-155">
                    <strong>Zadatak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="b0377-156">
                    <strong>Učinak naplativosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-157">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-158">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-159">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-160">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="b0377-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-161">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-162">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-163">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-164">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-165">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-166">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-167">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-168">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-169">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-170">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0377-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-171">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-172">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-173">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-174">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-175">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-176">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-177">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-178">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-179">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-180">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0377-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-181">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-182">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-183">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-184">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-185">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-186">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-187">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-188">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-189">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-190">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0377-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-191">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-192">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-193">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-194">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-195">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-196">Vrsta naplate stvarnog materijala: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-197">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-198">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-199">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-200">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0377-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-201">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-202">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-203">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-204">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-205">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-206">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-207">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-208">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-209">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-210">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b0377-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-211">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-212">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-213">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-214">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-215">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-216">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-218">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-219">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-220">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="b0377-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-221">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-222">
                    <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-223">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-224">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-225">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-226">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-228">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-229">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-230">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="b0377-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-231">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-232">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-233">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-234">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-235">Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-236">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-237">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0377-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-239">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-240">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="b0377-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-241">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-242">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-243">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-244">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-245">Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-246">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-247">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0377-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0377-249">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-250">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="b0377-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-251">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-252">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-253">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-254">Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-255">Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-256">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-257">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-258">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0377-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-260">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="b0377-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-261">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-262">Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-263">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-264">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-265">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="b0377-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0377-266">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0377-267">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0377-268">Jest</span><span class="sxs-lookup"><span data-stu-id="b0377-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0377-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0377-270">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="b0377-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0377-271">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0377-272">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0377-273">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="b0377-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0377-274">Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-275">Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0377-276">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0377-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
