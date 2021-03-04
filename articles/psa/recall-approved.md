---
title: Opoziv odobrenih unosa vremena ili troškova
description: Ova tema pruža informacije o tome kako opozvati prethodno odobreno vrijeme ili transakciju troškova.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147824"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="fae47-103">Opoziv odobrenih unosa vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="fae47-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fae47-104">Član projektnog tima ili druga osoba koja pošalje Unos vremena ili troškova može opozvati taj Unos vremena ili troškova nakon što se odobri.</span><span class="sxs-lookup"><span data-stu-id="fae47-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="fae47-105">Postupak opoziva odobrenog unosa vremena ili troškova obuhvaća dva koraka:</span><span class="sxs-lookup"><span data-stu-id="fae47-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="fae47-106">Pošiljatelj zahtijeva opoziv.</span><span class="sxs-lookup"><span data-stu-id="fae47-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="fae47-107">Odobravatelj odobrava opoziv.</span><span class="sxs-lookup"><span data-stu-id="fae47-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="fae47-108">Zahtjev za opoziv</span><span class="sxs-lookup"><span data-stu-id="fae47-108">Request a recall</span></span>

<span data-ttu-id="fae47-109">Poduzmite ove korake da biste zatražili opoziv odobrenog unosa vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="fae47-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="fae47-110">Za vremenske unose idite na **Projekti** \> **Moj posao** \> **Unos vremena**.</span><span class="sxs-lookup"><span data-stu-id="fae47-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="fae47-111">–ili–</span><span class="sxs-lookup"><span data-stu-id="fae47-111">–or–</span></span>

    <span data-ttu-id="fae47-112">Za unose troškova idite na **Projekti** \> **Moj posao** \> **Troškovi**.</span><span class="sxs-lookup"><span data-stu-id="fae47-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="fae47-113">Za vremenske unose odaberite sve vremenske unose za određenu kombinaciju projekta i zadatka.</span><span class="sxs-lookup"><span data-stu-id="fae47-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="fae47-114">Ili u rešetki odaberite pojedinačne ćelije za vrijeme na određeni datum za određeni projekt.</span><span class="sxs-lookup"><span data-stu-id="fae47-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="fae47-115">–ili–</span><span class="sxs-lookup"><span data-stu-id="fae47-115">–or–</span></span>

    <span data-ttu-id="fae47-116">Za unose troškova odaberite redak za unos troškova za opoziv.</span><span class="sxs-lookup"><span data-stu-id="fae47-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="fae47-117">Odaberite **Opozovi**.</span><span class="sxs-lookup"><span data-stu-id="fae47-117">Select **Recall**.</span></span> <span data-ttu-id="fae47-118">Prikazat će se dijaloški okvir za potvrdu.</span><span class="sxs-lookup"><span data-stu-id="fae47-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="fae47-119">Ako su odabrani unosi vremena ili troškova već odobreni, od vas će se zatražiti da unesete razlog za opoziv.</span><span class="sxs-lookup"><span data-stu-id="fae47-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="fae47-120">Unesite razlog za opoziv, a zatim odaberite **U redu** da biste potvrdili operaciju.</span><span class="sxs-lookup"><span data-stu-id="fae47-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="fae47-121">Sustav šalje osobi koja je odobrila unose zahtjev za odobravanje opoziva.</span><span class="sxs-lookup"><span data-stu-id="fae47-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="fae47-122">Iako se odobreni unosi vremena ili troškova mogu opozvati, ako su odobreno vrijeme ili trošak već fakturirani klijentu, nije moguće stvoriti zahtjev za opoziv.</span><span class="sxs-lookup"><span data-stu-id="fae47-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="fae47-123">Korisnik koji pokuša stvoriti zahtjev za opoziv primit će poruku u kojoj se navodi da vrijeme ili trošak nije moguće opozvati jer su već fakturirani.</span><span class="sxs-lookup"><span data-stu-id="fae47-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="fae47-124">Odobravanje ili odbacivanje zahtjeva za opoziv</span><span class="sxs-lookup"><span data-stu-id="fae47-124">Approve or reject a recall request</span></span>

<span data-ttu-id="fae47-125">Poduzmite ove korake da biste odobrili ili odbacili zahtjev za opoziv.</span><span class="sxs-lookup"><span data-stu-id="fae47-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="fae47-126">Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="fae47-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="fae47-127">Na stranici popisa **Odobrenja** promijenite prikaz u **Zahtjevi za opoziv za odobrenje**.</span><span class="sxs-lookup"><span data-stu-id="fae47-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="fae47-128">Prikazat će se popis poslanih zahtjeva za opoziv.</span><span class="sxs-lookup"><span data-stu-id="fae47-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="fae47-129">Odaberite jedan ili više unosa, a zatim odaberite **Odobri** ili **Odbaci**.</span><span class="sxs-lookup"><span data-stu-id="fae47-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="fae47-130">Ako ste odabrali **Odobri**, primit ćete poruku upozorenja koja objašnjava učinak odobrenja.</span><span class="sxs-lookup"><span data-stu-id="fae47-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="fae47-131">Odaberite **U redu** da biste potvrdili operaciju.</span><span class="sxs-lookup"><span data-stu-id="fae47-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="fae47-132">Zahtjev za opoziv odobren je.</span><span class="sxs-lookup"><span data-stu-id="fae47-132">The recall request is approved.</span></span>

    <span data-ttu-id="fae47-133">–ili–</span><span class="sxs-lookup"><span data-stu-id="fae47-133">–or–</span></span>

    <span data-ttu-id="fae47-134">Ako ste odabrali **Odbaci**, zahtjev za opoziv odbacuje se.</span><span class="sxs-lookup"><span data-stu-id="fae47-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="fae47-135">Kao kada se zatraži opoziv, kada se opoziv odobri, sustav provjerava postoje li aktivnosti fakturiranja u vezi s unosima vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="fae47-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="fae47-136">Ako je unos već fakturiran ili je naveden u skici fakture, odobravatelj će primiti poruku o pogrešci u kojoj se navodi da se vrijeme ili trošak ne mogu odobriti za opoziv jer su već fakturirani.</span><span class="sxs-lookup"><span data-stu-id="fae47-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="fae47-137">Učinak zahtjeva za opoziv</span><span class="sxs-lookup"><span data-stu-id="fae47-137">Impact of a recall request</span></span>

<span data-ttu-id="fae47-138">Kada se odobrenje opozove, postoji operativni i financijski učinak.</span><span class="sxs-lookup"><span data-stu-id="fae47-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="fae47-139">Operativni učinak</span><span class="sxs-lookup"><span data-stu-id="fae47-139">Operational impact</span></span>

<span data-ttu-id="fae47-140">Ako se zahtjev za opoziv odobri, zapis odobravanja dobiva oznaku **Odbačeno**.</span><span class="sxs-lookup"><span data-stu-id="fae47-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="fae47-141">Status unosa mijenja se u **Vraćeno** ili **Odbačeno**, ovisno o tome je li riječ o unosu vremena ili troška.</span><span class="sxs-lookup"><span data-stu-id="fae47-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="fae47-142">Član projektnog tima može pregledati, urediti i zatim ponovno poslati unose ili ih u cijelosti izbrisati.</span><span class="sxs-lookup"><span data-stu-id="fae47-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="fae47-143">Ako se zahtjev za opoziv odbaci, status unosa ostaje **Odobreno**, a član projektnog tima ili odobravatelj za projekt ne može uređivati unos.</span><span class="sxs-lookup"><span data-stu-id="fae47-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="fae47-144">Financijski učinak</span><span class="sxs-lookup"><span data-stu-id="fae47-144">Financial impact</span></span>

<span data-ttu-id="fae47-145">Ako se zahtjev za opoziv odobri, odgovarajući stvarni podaci za troškove i prodaju ažuriraju se na sljedeći način:</span><span class="sxs-lookup"><span data-stu-id="fae47-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="fae47-146">Polje **Status prilagodbe** ažurira se na **Prilagođeno**.</span><span class="sxs-lookup"><span data-stu-id="fae47-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="fae47-147">Polje **Status naplate** ažurira se na **Prilagođeno**.</span><span class="sxs-lookup"><span data-stu-id="fae47-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="fae47-148">Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="fae47-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="fae47-149">Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="fae47-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="fae47-150">Jedine vrijednosti koje se ne kopiraju su vrijednosti količine.</span><span class="sxs-lookup"><span data-stu-id="fae47-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="fae47-151">Te su vrijednosti umjesto toga preokreću.</span><span class="sxs-lookup"><span data-stu-id="fae47-151">These values are reversed instead.</span></span> <span data-ttu-id="fae47-152">Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**.</span><span class="sxs-lookup"><span data-stu-id="fae47-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="fae47-153">Polje **Status prilagodbe** u poništenim stvarnim podacima postava se na **Nije moguće prilagoditi**, a polje **Status naplate** postavlja se na **Otkazano**.</span><span class="sxs-lookup"><span data-stu-id="fae47-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="fae47-154">Zbog tih promjena zabilježena potrošnja i zaostatak prihoda na projektu više neće pravdati iznose koje ti stvarni podaci predstavljaju.</span><span class="sxs-lookup"><span data-stu-id="fae47-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="fae47-155">Ako se zahtjev za opoziv odbaci, ne postoji financijski učinak na projekt.</span><span class="sxs-lookup"><span data-stu-id="fae47-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="fae47-156">Promjene zapisa unosa vremena</span><span class="sxs-lookup"><span data-stu-id="fae47-156">Changes to time entry records</span></span>

<span data-ttu-id="fae47-157">Sljedeća ilustracija prikazuje promjene do kojih dolazi prilikom opoziva odobrenih vremenskih unosa.</span><span class="sxs-lookup"><span data-stu-id="fae47-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Prijelazi stanja unosa vremena](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="fae47-159">Promjene zapisa unosa troškova</span><span class="sxs-lookup"><span data-stu-id="fae47-159">Changes to expense entry records</span></span>

<span data-ttu-id="fae47-160">Sljedeća ilustracija prikazuje promjene do kojih dolazi prilikom opoziva odobrenih unosa troškova.</span><span class="sxs-lookup"><span data-stu-id="fae47-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Prijelazi stanja unosa troškova](media/ExpenseEntryStateTransitions.png)
