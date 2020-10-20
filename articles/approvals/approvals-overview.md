---
title: Pregled odobrenja
description: U ovoj temi nalaze se informacije o radu s odobrenjima u aplikaciji Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961157"
---
# <a name="approvals-overview"></a><span data-ttu-id="8bd1c-103">Pregled odobrenja</span><span class="sxs-lookup"><span data-stu-id="8bd1c-103">Approvals overview</span></span>

<span data-ttu-id="8bd1c-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="8bd1c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8bd1c-105">Slanja vremena i troška kreću se kroz tijek rada odobrenja.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="8bd1c-106">Nakon odobrenja unosa, transakcije se bilježe u stvarnim podacima ili se vrijeme rezervira u rasporedu.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="8bd1c-107">Tijek rada odobrenja</span><span class="sxs-lookup"><span data-stu-id="8bd1c-107">Approvals workflow</span></span>
<span data-ttu-id="8bd1c-108">Kada stvarate i šaljete unos vremena ili troška, stvara se unos odobrenja.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="8bd1c-109">Odobravatelj projekta ili vaš upravitelj pregledava i odobrava vaš unos.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="8bd1c-110">Ako se unos odnosi na projekt, kada se odobri, stvorit će se stvarni podaci.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="8bd1c-111">To omogućuje praćenje troškova i naplate.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="8bd1c-112">Odobravanje unosa</span><span class="sxs-lookup"><span data-stu-id="8bd1c-112">Approve an entry</span></span>
<span data-ttu-id="8bd1c-113">Obrazac **Odobrenja** omogućuje vam prebacivanje između različitih prikaza kako biste mogli vidjeti različite vrste odobrenja.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="8bd1c-114">Idite na obrazac **Odobrenja** i odaberite mogućnost **Troškovi**, **Vrijeme** ili **Storniranja**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="8bd1c-115">Pregledajte svako odobrenje i odaberite ona koja želite odobriti.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="8bd1c-116">Odaberite mogućnost **Odobri** kako bite odobrili odabrane unose.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="8bd1c-117">Sustav će obraditi te unose i stvoriti stvarne podatke ili rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="8bd1c-118">Odbacivanje unosa</span><span class="sxs-lookup"><span data-stu-id="8bd1c-118">Reject an entry</span></span>
<span data-ttu-id="8bd1c-119">Kao odobravatelj projekta, možda ćete korisniku morati vratiti unos na ispravak.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="8bd1c-120">Idite na obrazac **Odobrenja** i odaberite unos koji želite odbaciti.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="8bd1c-121">Odaberite **Odbaci**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-121">Select **Reject**.</span></span>
3. <span data-ttu-id="8bd1c-122">Neobvezno – Dodajte komentar u dijaloški okvir **Komentari odbacivanja** kako biste obavijestili korisnika zašto se unos odbacuje.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="8bd1c-123">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-123">Select **OK**.</span></span> <span data-ttu-id="8bd1c-124">Unos će se vratiti korisniku.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="8bd1c-125">Storniranje unosa</span><span class="sxs-lookup"><span data-stu-id="8bd1c-125">Recall entries</span></span>
<span data-ttu-id="8bd1c-126">U jednom trenutku, možda ćete morati stornirati poslani unos.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="8bd1c-127">Ako unos nije odobren, odmah će se vratiti.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="8bd1c-128">No, odobreni unos može imati materijalni utjecaj.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="8bd1c-129">Odobravatelj projekta mora odobriti storniranje kako bi se poništila transakcija u stvarnim podacima.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="8bd1c-130">Određivanje odobravatelja projekta</span><span class="sxs-lookup"><span data-stu-id="8bd1c-130">Specify Project approvers</span></span>
<span data-ttu-id="8bd1c-131">Svaki projekt ima određeni broj članova projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-131">Each project has a number of project team members.</span></span> <span data-ttu-id="8bd1c-132">Možete odrediti koji su članovi tima ujedno i odobravatelji projekta.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="8bd1c-133">Idite na obrazac **Projekti** i otvorite projekt s popisa.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="8bd1c-134">Na kartici **Tim** odaberite člana tima koji će biti odobravatelj projekta, a zatim odaberite **Uredi**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="8bd1c-135">Postavite polje **Odobravatelj projekta** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="8bd1c-136">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-136">Select **Save**.</span></span>
5. <span data-ttu-id="8bd1c-137">Ponovite korake 2 – 4 kako biste dodali dodatne odobravatelje projekta.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="8bd1c-138">Konfiguriranje upravitelja korisnika</span><span class="sxs-lookup"><span data-stu-id="8bd1c-138">Configure the user's manager</span></span>

1. <span data-ttu-id="8bd1c-139">Otvorite **Postavke** > **Sigurnost** > **Korisnici**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="8bd1c-140">Odaberite korisnika kojem dodjeljujete upravitelja i u području **Informacije o tvrtki ili ustanovi** odaberite upravitelja s popisa.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="8bd1c-141">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="8bd1c-141">Select **Save**.</span></span>


