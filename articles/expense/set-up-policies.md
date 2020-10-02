---
title: Definiranje pravila koja reguliraju troškove
description: Možete definirati pravila koja reguliraju troškove kojih se vaši radnici moraju pridržavati tijekom unosa i podnošenja izvješća o troškovima i putnih naloga.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896632"
---
# <a name="define-expense-policies"></a><span data-ttu-id="e3cfd-103">Definiranje pravila koja reguliraju troškove</span><span class="sxs-lookup"><span data-stu-id="e3cfd-103">Define expense policies</span></span>

<span data-ttu-id="e3cfd-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="e3cfd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e3cfd-105">Možete definirati pravila kojih se vaši radnici moraju pridržavati tijekom unosa i podnošenja izvješća o troškovima i putnih naloga.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="e3cfd-106">Uvođenje pravila koja reguliraju troškove može vam pomoći da učinkovito upravljate troškovima.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="e3cfd-107">Na primjer, možete postaviti pravila za hotelske troškove u Zagrebu, koja navode da trošak po noćenju ne smije premašiti 1.500,00 kn.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="e3cfd-108">Ako radnik podnese izvješće o trošku ili putni nalog u kojem cijena sobe prelazi taj iznos, sustav će obavijestiti</span><span class="sxs-lookup"><span data-stu-id="e3cfd-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="e3cfd-109">radnika kako je prekoračen iznos iz pravila koja reguliraju troškove.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="e3cfd-110">Možete konfigurirati poruku koju će radnik primiti kada</span><span class="sxs-lookup"><span data-stu-id="e3cfd-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="e3cfd-111">definirate pravila.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-111">define the policy.</span></span>      
        
<span data-ttu-id="e3cfd-112">Možete definirati tri vrste pravila:</span><span class="sxs-lookup"><span data-stu-id="e3cfd-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="e3cfd-113">**Upozorenje**: Omogućuje radniku da podnese izvješće o trošku ili putni nalog, ali će trošak biti označen za sve odobravatelje i</span><span class="sxs-lookup"><span data-stu-id="e3cfd-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="e3cfd-114">za kasnije izvješćivanje.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-114">for later reporting.</span></span>        

- <span data-ttu-id="e3cfd-115">**Pogreška**: Zahtijeva od radnika da revidira trošak kako bi se uskladio s pravilima prije podnošenja izvješća o troškovima ili putnog naloga.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="e3cfd-116">**Opravdanje**: Zahtijeva od radnika ili voditelja da, prije podnošenja izvješća o troškovima ili putnog naloga, unese opravdani razlog za prekoračenje iznosa dozvoljenog pravilima.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="e3cfd-117">Savjeti za pravila</span><span class="sxs-lookup"><span data-stu-id="e3cfd-117">Policy tips</span></span>
<span data-ttu-id="e3cfd-118">Evo nekoliko prijedloga koji vam mogu pomoći pri stvaranju novih pravila za upravljanje troškovima:</span><span class="sxs-lookup"><span data-stu-id="e3cfd-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="e3cfd-119">Pravila vrijede od određenog datuma, što znači da se neće primijeniti ako su stvorena s datumom koji je nastupio nakon datuma nastanka troška.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="e3cfd-120">Na primjer, danas stvorite novo pravilo kojim se propisuje maksimalni trošak obroka od 300,00 kn.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="e3cfd-121">Svi postojeći troškovi uneseni za jučerašnji dan neće se provjeravati u skladu s ovim pravilom.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="e3cfd-122">Tijekom stvaranja pravila za kategoriju troškova koja se može specificirati, razmislite o dodavanju uvjeta za vrstu retka troška.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="e3cfd-123">Neka pravila, poput zahtijevanja računa, možda nemaju smisla za specificirane retke.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="e3cfd-124">U toj se situaciji pravilo primjenjuje samo na redak zaglavlja ili nespecificiran redak.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="e3cfd-125">Pravila upravljanja troškovima prema zadanim se postavkama vrednuju prema izvornom entitetu.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="e3cfd-126">Za scenarije među tvrtkama možete umjesto toga postaviti pravila koja će se ocjenjivati prema odredišnom entitetu (entitetu primatelju posudbe).</span><span class="sxs-lookup"><span data-stu-id="e3cfd-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="e3cfd-127">Kako biste pokrenuli pravila prema odredišnom entitetu, uključite značajku **Procijeni pravila koja reguliraju troškove u odnosu na pravnu osobu primateljicu posudbe** u radnom prostoru **Upravljanje značajkama**.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="e3cfd-128">Vrijeme za procjenu pravila</span><span class="sxs-lookup"><span data-stu-id="e3cfd-128">When to evaluate policies</span></span>

<span data-ttu-id="e3cfd-129">U parametrima upravljanja troškovima možete odabrati procjenu pravila upravljanja troškovima kada je redak spremljen ili izvješće o troškovima podneseno.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="e3cfd-130">Ako odlučite na procjenu kada se redak spremi, korisnici će imati raniji uvid u ono što trebaju učiniti kako bi odjednom dovršili svoje izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="e3cfd-131">U suprotnom, možete odgoditi procjenu pravila i uštedjeti vrijeme provjerom valjanosti na kraju, tijekom slanja u tijek rada.</span><span class="sxs-lookup"><span data-stu-id="e3cfd-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
