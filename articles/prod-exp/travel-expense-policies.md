---
title: Postavljanje pravila o troškovima
description: Možete postaviti pravila koja se odnose na troškove kojih se vaši radnici moraju pridržavati tijekom unosa i slanja izvješća o troškovima i putnih naloga u aplikaciji Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073535"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="7377e-103">Postavljanje pravila o troškovima</span><span class="sxs-lookup"><span data-stu-id="7377e-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7377e-104">Možete definirati pravila kojih se vaši radnici moraju pridržavati tijekom unosa i podnošenja izvješća o troškovima i putnih naloga.</span><span class="sxs-lookup"><span data-stu-id="7377e-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="7377e-105">Uvođenje pravila koja reguliraju troškove može vam pomoći da učinkovito upravljate troškovima.</span><span class="sxs-lookup"><span data-stu-id="7377e-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="7377e-106">Na primjer, možete postaviti pravila za hotelske troškove u Zagrebu, koja navode da trošak po noćenju ne smije premašiti 1.500,00 kn.</span><span class="sxs-lookup"><span data-stu-id="7377e-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="7377e-107">Ako radnik podnese izvješće o trošku ili putni nalog u kojem cijena sobe prelazi taj iznos, sustav će obavijestiti</span><span class="sxs-lookup"><span data-stu-id="7377e-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="7377e-108">radnika kako je prekoračen iznos iz pravila koja reguliraju troškove.</span><span class="sxs-lookup"><span data-stu-id="7377e-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="7377e-109">Možete konfigurirati poruku koju će radnik primiti kada</span><span class="sxs-lookup"><span data-stu-id="7377e-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="7377e-110">definirate pravila.</span><span class="sxs-lookup"><span data-stu-id="7377e-110">define the policy.</span></span>      
        
<span data-ttu-id="7377e-111">Možete definirati tri vrste pravila:</span><span class="sxs-lookup"><span data-stu-id="7377e-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="7377e-112">Upozorenje – Omogućuje radniku da podnese izvješće o trošku ili putni nalog, ali će trošak biti označen za sve odobravatelje i</span><span class="sxs-lookup"><span data-stu-id="7377e-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="7377e-113">za kasnije izvješćivanje.</span><span class="sxs-lookup"><span data-stu-id="7377e-113">for later reporting.</span></span>        

- <span data-ttu-id="7377e-114">Pogreška – Zahtijeva od radnika da revidira trošak kako bi se uskladio s pravilima prije podnošenja izvješća o troškovima ili putnog naloga.</span><span class="sxs-lookup"><span data-stu-id="7377e-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="7377e-115">Opravdanje – Zahtijeva od radnika ili voditelja da, prije podnošenja izvješća o troškovima ili putnog naloga, unese opravdani razlog za prekoračenje iznosa dozvoljenog pravilima.</span><span class="sxs-lookup"><span data-stu-id="7377e-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="7377e-116">Savjeti za pravila</span><span class="sxs-lookup"><span data-stu-id="7377e-116">Policy tips</span></span>
<span data-ttu-id="7377e-117">Evo nekoliko prijedloga koji vam mogu pomoći pri stvaranju novih pravila za upravljanje troškovima.</span><span class="sxs-lookup"><span data-stu-id="7377e-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="7377e-118">Pravila vrijede od određenog datuma i neće se primijeniti ako su stvorena s datumom koji je nastupio nakon datuma nastanka troška.</span><span class="sxs-lookup"><span data-stu-id="7377e-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="7377e-119">Na primjer, ako danas stvorite novo pravilo kako biste uveli maksimalni trošak obroka od 50 USD, tada se svi postojeći troškovi uneseni od jučer neće provjeriti u skladu s ovim pravilom.</span><span class="sxs-lookup"><span data-stu-id="7377e-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="7377e-120">Tijekom stvaranja pravila za kategoriju troškova koja se može specificirati, razmislite o dodavanju uvjeta za vrstu retka troška.</span><span class="sxs-lookup"><span data-stu-id="7377e-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="7377e-121">Neka pravila, poput zahtjeva za računom, možda neće imati smisla za specificirane retke i trebala bi se primijeniti samo na zaglavlje ili nespecificirani redak.</span><span class="sxs-lookup"><span data-stu-id="7377e-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="7377e-122">Pravila upravljanja troškovima prema zadanim se postavkama vrednuju prema izvornom entitetu.</span><span class="sxs-lookup"><span data-stu-id="7377e-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="7377e-123">Za scenarije među tvrtkama možete umjesto toga postaviti pravila koja će se ocjenjivati prema odredišnom entitetu (entitetu primatelju posudbe).</span><span class="sxs-lookup"><span data-stu-id="7377e-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="7377e-124">Kako biste pokrenuli pravila prema odredišnom entitetu, uključite značajku „Procijeni pravila koja reguliraju troškove u odnosu na pravnu osobu primateljicu posudbe” u radnom prostoru **Upravljanje značajkama**.</span><span class="sxs-lookup"><span data-stu-id="7377e-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="7377e-125">Vrijeme za procjenu pravila</span><span class="sxs-lookup"><span data-stu-id="7377e-125">When to evaluate policies</span></span>

<span data-ttu-id="7377e-126">U parametrima upravljanja troškovima postoji mogućnost procjene pravila upravljanja troškovima ili kada se spremi redak ili kada se pošalje izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="7377e-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="7377e-127">Ako se odlučite na procjenu kada se spremi redak to će korisnicima omogućiti da imaju raniji uvid u ono što trebaju učiniti kako bi odjednom dovršili svoje izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="7377e-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="7377e-128">U suprotnom, možete odgoditi procjenu pravila i uštedjeti vrijeme ako do provjere valjanosti dolazi na kraju, tijekom slanja u tijek rada.</span><span class="sxs-lookup"><span data-stu-id="7377e-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
