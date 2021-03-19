---
title: Poništi prethodno odobrene unose vremena i troškova
description: Ova tema pruža informacije o tome kako poništiti odobreno vrijeme projekta i transakciju troškova.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 40ac37c1070e1c4da01e96bbc4248977b2b6d284
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290845"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="90144-103">Poništi prethodno odobrene unose vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="90144-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90144-104">U posljednjoj verziji sustava Dynamics 365 Project Service Automation, odobravatelji mogu poništiti unose vremena ili troškova koje su prethodno odobrili.</span><span class="sxs-lookup"><span data-stu-id="90144-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="90144-105">Poništi prethodno odobreni unos vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="90144-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="90144-106">Slijedite ove korake da biste poništili unos vremena ili troškova koji ste prethodno odobrili.</span><span class="sxs-lookup"><span data-stu-id="90144-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="90144-107">Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="90144-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="90144-108">Na stranici popisa **Odobrenja** promijenite prikaz u **Moja prošla odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="90144-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="90144-109">Prikazuje se popis unosa vremena i troškova koje ste prethodno odobrili.</span><span class="sxs-lookup"><span data-stu-id="90144-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="90144-110">Odaberite jednu ili više unosa, a zatim odaberite **Otkaži odobrenje**.</span><span class="sxs-lookup"><span data-stu-id="90144-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="90144-111">Primit ćete poruku upozorenja.</span><span class="sxs-lookup"><span data-stu-id="90144-111">You receive a warning message.</span></span>
4. <span data-ttu-id="90144-112">Odaberite **U redu** da biste poništili odobrenje.</span><span class="sxs-lookup"><span data-stu-id="90144-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="90144-113">Razumijevanje učinka poništavanja odobrenja za unos vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="90144-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="90144-114">Kada se odobrenje poništi, učinak je i operativni i financijski.</span><span class="sxs-lookup"><span data-stu-id="90144-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="90144-115">Operativni učinak</span><span class="sxs-lookup"><span data-stu-id="90144-115">Operational impact</span></span>

<span data-ttu-id="90144-116">S operativne strane, kada se odobrenje poništi, status zapisa vraća se na **Skica**, a odobrenje se više ne pojavljuje u prikazu **Moja prošla odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="90144-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="90144-117">Umjesto toga, poništeno odobrenje pojavljuje se u prikazu **Unosi vremena za odobrenje** ili **Unosi troškova za odobrenje**, ovisno o tome je li to bio unos vremena ili izdatka.</span><span class="sxs-lookup"><span data-stu-id="90144-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="90144-118">Osim toga, status povezanog unosa vremena ili unosa troškova mijenja se u **Poslano**, tako da je povezani unos u skladu s odobrenjima koja imaju status **Skica**.</span><span class="sxs-lookup"><span data-stu-id="90144-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="90144-119">Kao odobravatelj, možete urediti neka polja odobrenja koja ima status **Skica**.</span><span class="sxs-lookup"><span data-stu-id="90144-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="90144-120">Ta polja uključuju **Vrsta naplate** i **Naplativi sati za unose vremena**.</span><span class="sxs-lookup"><span data-stu-id="90144-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="90144-121">Nakon što izvršite promjene, ponovno možete odobriti zapis.</span><span class="sxs-lookup"><span data-stu-id="90144-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="90144-122">Alternativno, možete odbiti unos.</span><span class="sxs-lookup"><span data-stu-id="90144-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="90144-123">Ako odbijete odobrenje unosa vremena, status unosa mijenja se u **Vraćeno**.</span><span class="sxs-lookup"><span data-stu-id="90144-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="90144-124">Ako odbijete odobrenje unosa troškova, status se mijenja u **Odbijeno**.</span><span class="sxs-lookup"><span data-stu-id="90144-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="90144-125">S funkcionalne strane, i vraćeni i odbijeni unosi ponašaju se isto kao i unos koji ima status **Skica**.</span><span class="sxs-lookup"><span data-stu-id="90144-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="90144-126">Član tima projekta može izvršiti bilo kakve potrebne promjene unosa, a zatim ga ponovno poslati na odobrenje ili u cijelosti izbrisati unos.</span><span class="sxs-lookup"><span data-stu-id="90144-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="90144-127">Financijski učinak</span><span class="sxs-lookup"><span data-stu-id="90144-127">Financial impact</span></span>

<span data-ttu-id="90144-128">Projekt je također zahvaćen financijski kada se poništava odobrenje.</span><span class="sxs-lookup"><span data-stu-id="90144-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="90144-129">Najprije, odgovarajuće stvarne vrijednosti za troškove i prodaju ažuriraju se na sljedeći način:</span><span class="sxs-lookup"><span data-stu-id="90144-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="90144-130">Status prilagodbe postavlja se na **Prilagođeno**.</span><span class="sxs-lookup"><span data-stu-id="90144-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="90144-131">Status naplate postavlja se na **Poništeno**.</span><span class="sxs-lookup"><span data-stu-id="90144-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="90144-132">Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="90144-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="90144-133">Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="90144-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="90144-134">Jedine vrijednosti koje se ne kopiraju su vrijednosti količine.</span><span class="sxs-lookup"><span data-stu-id="90144-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="90144-135">Te su vrijednosti umjesto toga preokreću.</span><span class="sxs-lookup"><span data-stu-id="90144-135">These values are reversed instead.</span></span> <span data-ttu-id="90144-136">Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**.</span><span class="sxs-lookup"><span data-stu-id="90144-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="90144-137">Polje **Status prilagodbe** na preokrenutim stvarnim vrijednostima postavlja se na **Nepodesivo**, a status naplate postavlja se na **Poništeno**.</span><span class="sxs-lookup"><span data-stu-id="90144-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="90144-138">Nakon što su te promjene izvršene, iznos koji je zapisan kao potrošen na projektu i zaostatak prihoda na projektu duže će pravdati iznose koje te stvarne vrijednosti predstavljaju.</span><span class="sxs-lookup"><span data-stu-id="90144-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]