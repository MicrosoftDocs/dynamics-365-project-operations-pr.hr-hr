---
title: Konfiguriranje naplative komponente retka ponude
description: U ovoj temi nalaze se informacije o postavljanju naplativih i nenaplativih komponenti na retku ponude koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858284"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="48f68-103">Konfiguriranje naplative komponente retka ponude</span><span class="sxs-lookup"><span data-stu-id="48f68-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="48f68-104">_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="48f68-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="48f68-105">Redak ponude koji se temelji na projektu ima koncept *uključenih* komponenti i *naplativih* komponenti.</span><span class="sxs-lookup"><span data-stu-id="48f68-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="48f68-106">Uključene komponente podliježu:</span><span class="sxs-lookup"><span data-stu-id="48f68-106">Included components are subject to:</span></span>

  - <span data-ttu-id="48f68-107">Način naplate i podjele klijenta</span><span class="sxs-lookup"><span data-stu-id="48f68-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="48f68-108">Ograničenja koja se ne smiju prekoračiti</span><span class="sxs-lookup"><span data-stu-id="48f68-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="48f68-109">Postavke učestalosti fakture definirane u retku ponude koji se temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="48f68-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="48f68-110">Podskup uključenih komponenti može se označiti kao naplativ s pomoću polja **Vrsta naplate**.</span><span class="sxs-lookup"><span data-stu-id="48f68-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="48f68-111">Polje **Vrsta naplate** skup je mogućnosti koji dopušta sljedeće vrijednosti u kontekstu retka ponude:</span><span class="sxs-lookup"><span data-stu-id="48f68-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="48f68-112">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-112">Chargeable</span></span>
  - <span data-ttu-id="48f68-113">Nenaplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-113">Non-chargeable</span></span>

<span data-ttu-id="48f68-114">Komponente koje se naplaćuju mogu se definirati u zadacima, ulogama i kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="48f68-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="48f68-115">Mogućnost naplate definirana je na zadacima za redak ponude i primjenjuje se na sve klase transakcija uključene u taj redak.</span><span class="sxs-lookup"><span data-stu-id="48f68-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="48f68-116">Ako je polje **Uključi zadatke** postavljeno na **Cijeli projekt** ili je ostavljeno prazno, kartica **Naplativi zadaci** nije dostupna.</span><span class="sxs-lookup"><span data-stu-id="48f68-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="48f68-117">Mogućnost naplate definirana je u ulogama za redak ponude i primjenjuje se samo na klasu transakcije **Vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="48f68-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="48f68-118">Ako je polje **Uključi vrijeme** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative uloge** nije dostupna.</span><span class="sxs-lookup"><span data-stu-id="48f68-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="48f68-119">Mogućnost naplate definirana je u kategorijama transakcije za redak ponude i primjenjuje se samo na klasu transakcije **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="48f68-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="48f68-120">Ako je polje **Uključi troškove** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative kategorije** nije dostupna.</span><span class="sxs-lookup"><span data-stu-id="48f68-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="48f68-121">Ažuriranje projektnog zadatka kako bi bio naplativ ili nenaplativ</span><span class="sxs-lookup"><span data-stu-id="48f68-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="48f68-122">Projektni zadatak može biti naplativ ili nenaplativ u kontekstu određenog retka ponude koji se temelji na projektu, što omogućuje sljedeće postavljanje.</span><span class="sxs-lookup"><span data-stu-id="48f68-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="48f68-123">Ako redak ponude koji se temelji na projektu uključuje **Vrijeme** i zadatak **T1**, zadatak je povezan s retkom ponude kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="48f68-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="48f68-124">Ako postoji drugi redak ponude koji uključuje stavku **Troškovi**, možete povezati zadatak **T1** s retkom ponude kao nenaplativ.</span><span class="sxs-lookup"><span data-stu-id="48f68-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="48f68-125">Rezultat je da se svo vrijeme zabilježeno na zadatku naplaćuje, dok se svi troškovi zabilježeni na zadatku ne naplaćuju.</span><span class="sxs-lookup"><span data-stu-id="48f68-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="48f68-126">Vrsta naplate zadatka može se konfigurirati na kartici **Naplativi zadaci** retka ponude koji se temelji na projektu ažuriranjem polja **Vrsta naplate** u podrešetki **Zadaci retka ponude**.</span><span class="sxs-lookup"><span data-stu-id="48f68-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="48f68-127">Umjesto toga, možete ažurirati vrstu naplate za projektni zadatak u polju **Vrsta naplate** na podrešetki, na postavci naplate zadatka projekta koja prikazuje retke ponude povezane sa zadatkom.</span><span class="sxs-lookup"><span data-stu-id="48f68-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="48f68-128">Ažuriranje uloge kako bi bila naplativa ili nenaplativa</span><span class="sxs-lookup"><span data-stu-id="48f68-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="48f68-129">Uloga može biti naplativa ili nenaplativa u kontekstu određenog retka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="48f68-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="48f68-130">Vrsta naplate uloge može se konfigurirati na kartici **Naplative uloge** retka ponude ažuriranjem polja **Vrsta naplate** u podrešetki **Naplative uloge**.</span><span class="sxs-lookup"><span data-stu-id="48f68-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="48f68-131">Ažuriranje kategorije transakcije kako bi bila naplativa ili nenaplativa</span><span class="sxs-lookup"><span data-stu-id="48f68-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="48f68-132">Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="48f68-133">Vrsta naplate transakcije može se konfigurirati na kartici **Naplative kategorije** retka ponude ažuriranjem polja **Vrsta naplate** u podrešetki **Naplative kategorije**.</span><span class="sxs-lookup"><span data-stu-id="48f68-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="48f68-134">Rješavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="48f68-134">Resolve chargeability</span></span>
<span data-ttu-id="48f68-135">Procjena ili stvarni podatak stvoren za vrijeme smatrat će se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="48f68-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="48f68-136">**Vrijeme** uključeno u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="48f68-137">**Uloga** konfigurirana kao naplativa u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="48f68-138">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="48f68-139">Ako su ove tri stvari točne, **Zadatak** je također konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="48f68-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="48f68-140">Procjena ili stvarni podatak stvoren za trošak smatra se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="48f68-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="48f68-141">**Trošak** uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="48f68-142">**Kategorija transakcije** konfigurirana kao naplativa u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="48f68-143">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="48f68-144">Ako su ove tri stvari točne, **Zadatak** je također konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="48f68-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="48f68-145">Procjena ili stvarni podatak stvoren za materijal smatrat će se naplativim samo ako je:</span><span class="sxs-lookup"><span data-stu-id="48f68-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="48f68-146">**Materijal** uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="48f68-147">Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="48f68-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="48f68-148">Ako su ove dvije stvari točne, **Zadatak** bi također trebao biti konfiguriran kao naplativ.</span><span class="sxs-lookup"><span data-stu-id="48f68-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-149">
                    <strong>Uključuje Vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="48f68-150">
                    <strong>Uključuje Trošak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="48f68-151">
                    <strong>Obuhvaća materijale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="48f68-152">
                    <strong>Uključeni zadaci</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-153">
                    <strong>Uloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-154">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-155">
                    <strong>Zadatak</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="48f68-156">
                    <strong>Učinak naplativosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-157">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-158">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-159">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-160">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="48f68-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-161">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-162">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-163">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-164">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-165">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-166">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-167">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-168">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-169">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-170">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="48f68-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-171">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-172">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-173">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-174">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-175">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-176">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-177">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-178">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-179">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-180">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="48f68-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-181">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-182">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-183">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-184">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-185">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-186">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-187">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-188">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-189">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-190">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="48f68-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-191">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-192">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-193">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-194">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-195">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-196">Vrsta naplate stvarnog materijala: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-197">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-198">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-199">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-200">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="48f68-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-201">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-202">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-203">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-204">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-205">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-206">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-207">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-208">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-209">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-210">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="48f68-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-211">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-212">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-213">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-214">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-215">Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-216">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-218">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-219">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-220">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="48f68-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-221">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-222">
                    <strong>Naplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-223">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-224">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-225">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-226">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-228">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-229">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-230">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="48f68-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-231">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-232">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-233">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-234">Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-235">Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-236">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-237">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="48f68-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-239">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-240">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="48f68-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-241">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-242">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-243">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-244">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-245">Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-246">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-247">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="48f68-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="48f68-249">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-250">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="48f68-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-251">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-252">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-253">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-254">Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-255">Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-256">Vrsta naplate stvarnog materijala: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-257">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-258">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="48f68-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-260">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="48f68-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-261">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-262">Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-263">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-264">Naplata za stvarno vrijeme: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-265">Vrsta naplate na stvarnom trošku: Naplativo</span><span class="sxs-lookup"><span data-stu-id="48f68-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="48f68-266">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="48f68-267">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="48f68-268">Jest</span><span class="sxs-lookup"><span data-stu-id="48f68-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="48f68-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="48f68-270">Cijeli projekt</span><span class="sxs-lookup"><span data-stu-id="48f68-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="48f68-271">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="48f68-272">
                    <strong>Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="48f68-273">Nije moguće postaviti</span><span class="sxs-lookup"><span data-stu-id="48f68-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="48f68-274">Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-275">Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="48f68-276">Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48f68-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
