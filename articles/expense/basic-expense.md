---
title: Unos izdatka (jednostavno)
description: U ovoj temi nalaze se informacije o načinu unosa troška u jednostavnoj implementaciji.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e75a61c25be06a9db121e8165e8ccd25d4719d08
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002182"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="8e12e-103">Unos izdatka (jednostavno)</span><span class="sxs-lookup"><span data-stu-id="8e12e-103">Expense entry (lite)</span></span>

<span data-ttu-id="8e12e-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="8e12e-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8e12e-105">Osnovno ili jednostavno upravljanje troškovima mogućnost je evidentiranja jednostavnih troškova.</span><span class="sxs-lookup"><span data-stu-id="8e12e-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="8e12e-106">Možete evidentirati troškove na projektu, a zatim će ih odobravatelj projekta pregledati i odobriti.</span><span class="sxs-lookup"><span data-stu-id="8e12e-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="8e12e-107">Dodatne informacija o mogućnostima troškova u rješenju Dynamics 365 Project Operations potražite u odjeljku [Pregled troškova](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e12e-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="8e12e-108">Bilježenje osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="8e12e-108">Capture a basic expense</span></span>

<span data-ttu-id="8e12e-109">Možete zabilježiti svoje troškove kako biste ih mogli poslati odobravatelju.</span><span class="sxs-lookup"><span data-stu-id="8e12e-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="8e12e-110">Idite na stavku **Troškovi** i odaberite mogućnost **Novi**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="8e12e-111">Na stranici **Novi trošak** unesite potrebne podatke o trošku, a zatim odaberite mogućnost **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="8e12e-112">Slanje osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="8e12e-112">Submit a basic expense</span></span>

<span data-ttu-id="8e12e-113">Nakon što završite s bilježenjem svih troškova i spremni ste ih dati na odobrenje, morate ih poslati.</span><span class="sxs-lookup"><span data-stu-id="8e12e-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="8e12e-114">Idite na stavku **Troškovi** i odaberite trošak.</span><span class="sxs-lookup"><span data-stu-id="8e12e-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="8e12e-115">Ili odaberite sve troškove s pomoću potvrdnog okvira u zaglavlju.</span><span class="sxs-lookup"><span data-stu-id="8e12e-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="8e12e-116">Odaberite **Šalji**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-116">Select **Submit**.</span></span> <span data-ttu-id="8e12e-117">Sustav obrađuje odabrane unose, a zatim stvara zahtjeve za odobrenje troškova.</span><span class="sxs-lookup"><span data-stu-id="8e12e-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="8e12e-118">Dodaj privitak</span><span class="sxs-lookup"><span data-stu-id="8e12e-118">Add an attachment</span></span>

<span data-ttu-id="8e12e-119">Možda ćete odobravatelju morati dostaviti dodatnu dokumentaciju o trošku.</span><span class="sxs-lookup"><span data-stu-id="8e12e-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="8e12e-120">Potvrdu možete priložiti vremenskoj traci unosa troškova.</span><span class="sxs-lookup"><span data-stu-id="8e12e-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="8e12e-121">Izaberite **Uredi** i u odjeljku **Vremenska traka**, a zatim odaberite ikonu spajalice kako biste priložili potvrdu.</span><span class="sxs-lookup"><span data-stu-id="8e12e-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="8e12e-122">Opoziv osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="8e12e-122">Recall a basic expense</span></span>

<span data-ttu-id="8e12e-123">Kada greškom pošaljete trošak, možete ga stornirati.</span><span class="sxs-lookup"><span data-stu-id="8e12e-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="8e12e-124">Vrijeme potrebno za storniranje unosa troška ovisi o fazi odobrenja u kojoj se nalazi.</span><span class="sxs-lookup"><span data-stu-id="8e12e-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="8e12e-125">Ako odobravatelj još nije odobrio unos, storniranje se može izvršiti odmah.</span><span class="sxs-lookup"><span data-stu-id="8e12e-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="8e12e-126">Međutim, ako je unos već odobren, od odobravatelja se treba zatražiti odobrenje opoziva i storniranja transakcija.</span><span class="sxs-lookup"><span data-stu-id="8e12e-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="8e12e-127">Idite na stavku **Troškovi**, a zatim na popisu troškova odaberite trošak koji želite stornirati.</span><span class="sxs-lookup"><span data-stu-id="8e12e-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="8e12e-128">Odaberite **Storniraj**.</span><span class="sxs-lookup"><span data-stu-id="8e12e-128">Select **Recall**.</span></span> <span data-ttu-id="8e12e-129">Ako unos troška još nije odobren, sustav ga odmah stornira.</span><span class="sxs-lookup"><span data-stu-id="8e12e-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="8e12e-130">Ako je unos troška već odobren, stvara se zahtjev za storniranje kako bi se obavijestio odobravatelj da želite stornirati trošak.</span><span class="sxs-lookup"><span data-stu-id="8e12e-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="8e12e-131">Odobravatelj će tada potvrditi da se storniranje može izvršiti i unos će biti vraćen.</span><span class="sxs-lookup"><span data-stu-id="8e12e-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="8e12e-132">Brisanje osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="8e12e-132">Delete a basic expense</span></span>

<span data-ttu-id="8e12e-133">Troškovi koji još nisu poslani mogu se izbrisati.</span><span class="sxs-lookup"><span data-stu-id="8e12e-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="8e12e-134">Kako biste izbrisali trošak koji je već poslan, prvo ga morate stornirati.</span><span class="sxs-lookup"><span data-stu-id="8e12e-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e12e-135">Pogledajte također</span><span class="sxs-lookup"><span data-stu-id="8e12e-135">See also</span></span>

- [<span data-ttu-id="8e12e-136">Pregled odobrenja</span><span class="sxs-lookup"><span data-stu-id="8e12e-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]