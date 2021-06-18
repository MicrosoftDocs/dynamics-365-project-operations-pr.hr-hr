---
title: Zašto je zadana cijena u stvarnim podacima vrijeme – trošak nula?
description: Pronalaženje problema zbog kojeg je zadana cijena u stvarnim podacima vrijeme – trošak 0.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: ffe915a48f088bde457121a323325ba490c24e45
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993047"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="f4dc4-103">Zašto je zadana cijena u stvarnim podacima vrijeme – trošak nula?</span><span class="sxs-lookup"><span data-stu-id="f4dc4-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f4dc4-104">Ova se najčešća pitanja primjenjuju na stvarne vrijednosti u slučajevima u kojima je klasa transakcije postavljena na Vrijeme, a vrsta transakcije je Trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="f4dc4-105">Sljedeće tri provjere pomoći će vam utvrditi zašto je zadana cijena u stvarnim podacima vrijeme – trošak 0.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="f4dc4-106">Provjera 1: identifikacija cjenika s cijenama koštanja za projekt</span><span class="sxs-lookup"><span data-stu-id="f4dc4-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="f4dc4-107">Pronađite projekt iz polja Projekt stvarnih podataka pa otvorite stranicu projekta.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="f4dc4-108">Kliknite vezu ugovorene jedinice u polju.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="f4dc4-109">Na stranici Ugovorena jedinica provjerite ima li ta ugovorena jedinica cjenik na rešetki Cjenici s cijenama koštanja.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="f4dc4-110">Ako postoji više od jednog cjenika, utvrdili ste problem.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="f4dc4-111">Project Service podržava samo jedan cjenik po organizacijskoj jedinici.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="f4dc4-112">Uklonite sve cjenike iz tog entiteta dok rešetki Cjenici s cijenama koštanja organizacijske jedinice ne bude priložen samo jedan cjenik.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="f4dc4-113">Ako toj organizacijskoj jedinici nije priložen nijedan cjenik, zabilježite koja je valuta te organizacijske jedinice.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="f4dc4-114">Idite na Project Service pa stavku Parametri pa otvorite karticu Cjenici. Provjerite nema li možda nijednog cjenika čiji je kontekst postavljen na Trošak, a valuta se podudara s valutom organizacijske jedinice.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="f4dc4-115">Ako nijedan cjenik ne ispunjava te kriterije, utvrdili ste problem.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="f4dc4-116">Provjerite postoji li barem jedan cjenik čiji je kontekst postavljen na Trošak, a valuta se podudara s valutom ogranizacijske jedinice.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="f4dc4-117">Ako više od jednog cjenika ispunjava te kriterije, nastavite čitati ovaj dokument da biste izvršili dodatne provjere.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="f4dc4-118">Provjera 2: Je li ijedan od cjenika utvrđenih gore valjan za određeni datum u stvarnim podacima vrijeme – trošak?</span><span class="sxs-lookup"><span data-stu-id="f4dc4-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="f4dc4-119">Da bi servis Project Service pri postavljanju zadane cijene uzeo u obzir neki cjenik, taj cjenik mora biti primjenjiv za datum u stvarnim podacima vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="f4dc4-120">Provjerite sljedeće da biste utvrdili jesu li cjenici utvrđeni gore primjenjivi:</span><span class="sxs-lookup"><span data-stu-id="f4dc4-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="f4dc4-121">Uvjerite se da polja datuma početka i završetka na kartici Općenito za priložene cjenike nisu prazna.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="f4dc4-122">Ako su polja datuma početka i završetka na cjenicima utvrđenima gore prazna, utvrdili ste problem.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="f4dc4-123">Zabilježite polje datuma početka u stvarnim podacima vrijeme – trošak i provjerite je li ijedan od utvrđenih cjenika primjenjiv za taj datum.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="f4dc4-124">Na primjer, datum u stvarnim podacima vrijeme – trošak mora biti između datuma početka i datuma završetka na cjeniku.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="f4dc4-125">Ako nijedan cjenik ne pokriva taj datum u stvarnim podacima vrijeme – trošak, utvrdili ste problem.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="f4dc4-126">Izmijenite datume početka i završetka cjenika da biste osigurali da cjenik pokriva datum iz stvarnih podataka vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="f4dc4-127">Ako više od jednog cjenika pokriva datum iz stvarnih podataka vrijeme – trošak, utvrdili ste problem.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="f4dc4-128">Taj problem možete otkloniti tako da uredite datume početka i završetka cjenika tako da samo jedan cjenik pokriva datum iz stvarnih podataka vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="f4dc4-129">Ako samo jedan cjenik pokriva taj datum iz stvarnh podataka vrijeme – trošak, prijeđite na sljedeću provjeru u dokumentu.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="f4dc4-130">Nakon što dovršite potrebne popravke, ponovno stvorite Unos vremena, odobrite ga pa provjerite prikazuje li se valjana cijena u stvarnim podacima vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="f4dc4-131">Provjera 3: Postoji li cijena na cjeniku za dimenzije cijena u stvarnim podacima vrijeme – trošak?</span><span class="sxs-lookup"><span data-stu-id="f4dc4-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="f4dc4-132">Ako ste uspješno dovršili provjere 1 i 2, sada bi vam samo jedan cjenik trebao biti primjenjiv za taj datum u stvarnim podacima vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="f4dc4-133">Otvorite ovaj Cjenik i otvorite karticu Cijene uloga. Uvjerite se da rešetka sadrži redak za dimenzije cijena u stvarnim podacima vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="f4dc4-134">Ako rešetka cijena uloga ne sadrži redak za dimenzije cijena u stvarnim podacima vrijeme – trošak, utvrdili ste problem.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="f4dc4-135">Na rešetki Cijene uloga stvorite redak za dimenzije cijena u stvarnim podacima vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="f4dc4-136">Nakon što to dovršite, ponovno stvorite Unos vremena, odobrite ga pa provjerite prikazuje li se valjana cijena za stvarne podatke vrijeme – trošak.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="f4dc4-137">Ako nakon tri gornje provjere u stvarnim podacima vrijeme – trošak i dalje nije prikazana valjana cijena, prijavite problem službi za podršku.</span><span class="sxs-lookup"><span data-stu-id="f4dc4-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]