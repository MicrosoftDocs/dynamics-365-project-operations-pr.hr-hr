---
title: Pregled odobrenja
description: U ovoj temi nalaze se informacije o radu s odobrenjima u aplikaciji Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368647"
---
# <a name="approvals-overview"></a><span data-ttu-id="f1f61-103">Pregled odobrenja</span><span class="sxs-lookup"><span data-stu-id="f1f61-103">Approvals overview</span></span>

<span data-ttu-id="f1f61-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="f1f61-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1f61-105">Prijave vremena, troškova i utrošenog materijala kreću se kroz radni tijek odobrenja.</span><span class="sxs-lookup"><span data-stu-id="f1f61-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="f1f61-106">Nakon odobrenja unosa, transakcije se bilježe u stvarnim podacima ili se vrijeme rezervira u rasporedu.</span><span class="sxs-lookup"><span data-stu-id="f1f61-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="f1f61-107">Tijek rada odobrenja</span><span class="sxs-lookup"><span data-stu-id="f1f61-107">Approvals workflow</span></span>
<span data-ttu-id="f1f61-108">Kada stvorite i pošaljete unos vremena, troška ili utrošenog materijala, stvara se zapis o odobrenju.</span><span class="sxs-lookup"><span data-stu-id="f1f61-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="f1f61-109">Odobravatelji ili voditelj projekta pregledava i odobrava unos.</span><span class="sxs-lookup"><span data-stu-id="f1f61-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="f1f61-110">Ako je unos povezan s projektom, stvarni podaci stvorit će se kada bude odobren.</span><span class="sxs-lookup"><span data-stu-id="f1f61-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="f1f61-111">To omogućuje praćenje troškova i naplate.</span><span class="sxs-lookup"><span data-stu-id="f1f61-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="f1f61-112">Odobravanje unosa</span><span class="sxs-lookup"><span data-stu-id="f1f61-112">Approve an entry</span></span>
<span data-ttu-id="f1f61-113">Stranica **Odobrenja** omogućuje vam prebacivanje između različitih prikaza kako biste mogli pregledavati različite vrste odobrenja.</span><span class="sxs-lookup"><span data-stu-id="f1f61-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="f1f61-114">Idite na stranicu **Odobrenja** i odaberite **Troškovi**, **Vrijeme**, **Utrošeni materijal** ili **Opozivi**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="f1f61-115">Pregledajte svako odobrenje i odaberite ona koja želite odobriti.</span><span class="sxs-lookup"><span data-stu-id="f1f61-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="f1f61-116">Odaberite mogućnost **Odobri** kako bite odobrili odabrane unose.</span><span class="sxs-lookup"><span data-stu-id="f1f61-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="f1f61-117">Sustav obrađuje ove unose i stvara stvarne podatke.</span><span class="sxs-lookup"><span data-stu-id="f1f61-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="f1f61-118">Odbacivanje unosa</span><span class="sxs-lookup"><span data-stu-id="f1f61-118">Reject an entry</span></span>
<span data-ttu-id="f1f61-119">Kao odobravatelj projekta, možda ćete korisniku morati vratiti unos na ispravak.</span><span class="sxs-lookup"><span data-stu-id="f1f61-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="f1f61-120">Idite na stranicu **Odobrenja** i odaberite unos koji želite odbiti.</span><span class="sxs-lookup"><span data-stu-id="f1f61-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="f1f61-121">Odaberite **Odbaci**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-121">Select **Reject**.</span></span>
3. <span data-ttu-id="f1f61-122">Neobvezno, dodajte komentar u dijaloški okvir **Komentari odbijanja** za obavještavanje korisnika zašto se unos odbija.</span><span class="sxs-lookup"><span data-stu-id="f1f61-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="f1f61-123">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-123">Select **OK**.</span></span> <span data-ttu-id="f1f61-124">Unos će se vratiti korisniku.</span><span class="sxs-lookup"><span data-stu-id="f1f61-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="f1f61-125">Otkazivanje odobrenja</span><span class="sxs-lookup"><span data-stu-id="f1f61-125">Cancel approval</span></span>
<span data-ttu-id="f1f61-126">U nekim slučajevima možda ćete trebati otkazati prethodno odobreni unos.</span><span class="sxs-lookup"><span data-stu-id="f1f61-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="f1f61-127">Otkazivanje prethodno odobrenog unosa imat će financijski učinak.</span><span class="sxs-lookup"><span data-stu-id="f1f61-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="f1f61-128">Zahtjevi za opoziv odobrenja</span><span class="sxs-lookup"><span data-stu-id="f1f61-128">Approving recall requests</span></span>
<span data-ttu-id="f1f61-129">U nekim slučajevima savjetnik će možda morati opozvati prethodno odobreni unos.</span><span class="sxs-lookup"><span data-stu-id="f1f61-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="f1f61-130">Otkazivanje prethodno odobrenog unosa imat će financijski učinak.</span><span class="sxs-lookup"><span data-stu-id="f1f61-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="f1f61-131">Odobritelj projekta mora odobriti opoziv radi poništavanja transakcije u Stvarnim podacima.</span><span class="sxs-lookup"><span data-stu-id="f1f61-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="f1f61-132">Određivanje odobravatelja projekta</span><span class="sxs-lookup"><span data-stu-id="f1f61-132">Specify Project approvers</span></span>
<span data-ttu-id="f1f61-133">Svaki projekt ima određeni broj članova projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="f1f61-133">Each project has a number of project team members.</span></span> <span data-ttu-id="f1f61-134">Možete odrediti koji su članovi tima ujedno i odobravatelji projekta.</span><span class="sxs-lookup"><span data-stu-id="f1f61-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="f1f61-135">Idite na stranicu **Projekti** i s popisa otvorite projekt.</span><span class="sxs-lookup"><span data-stu-id="f1f61-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="f1f61-136">Na kartici **Tim** odaberite člana tima koji će biti odobravatelj projekta, a zatim odaberite **Uredi**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="f1f61-137">Postavite polje **Odobravatelj projekta** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="f1f61-138">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-138">Select **Save**.</span></span>
5. <span data-ttu-id="f1f61-139">Ponovite korake 2 – 4 kako biste dodali dodatne odobravatelje projekta.</span><span class="sxs-lookup"><span data-stu-id="f1f61-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="f1f61-140">Konfiguriranje upravitelja korisnika</span><span class="sxs-lookup"><span data-stu-id="f1f61-140">Configure the user's manager</span></span>

1. <span data-ttu-id="f1f61-141">Otvorite **Postavke** > **Sigurnost** > **Korisnici**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="f1f61-142">Odaberite korisnika kojem dodjeljujete upravitelja i u području **Informacije o tvrtki ili ustanovi** odaberite upravitelja s popisa.</span><span class="sxs-lookup"><span data-stu-id="f1f61-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="f1f61-143">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="f1f61-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
