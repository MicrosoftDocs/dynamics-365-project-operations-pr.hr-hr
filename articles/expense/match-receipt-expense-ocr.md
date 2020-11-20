---
title: Usklađivanje računa i troška s pomoću OCR-a
description: U ovoj se temi nalaze informacije o obradi optičkog prepoznavanja znakova (OCR, optical character recognition) za račune.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124314"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="abe9d-103">Usklađivanje računa i troška s pomoću OCR-a</span><span class="sxs-lookup"><span data-stu-id="abe9d-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="abe9d-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="abe9d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abe9d-105">Unos troškova poboljšan je implementacijom optičkog prepoznavanja znakova (OCR) za obradu računa.</span><span class="sxs-lookup"><span data-stu-id="abe9d-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="abe9d-106">Ova je funkcija dizajnirana za poboljšanje korisničkog iskustva tijekom izrade izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="abe9d-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="abe9d-107">Glavne značajke</span><span class="sxs-lookup"><span data-stu-id="abe9d-107">Key features</span></span>

- <span data-ttu-id="abe9d-108">Sustav iz računa izdvaja ime trgovca, datum i ukupan iznos.</span><span class="sxs-lookup"><span data-stu-id="abe9d-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="abe9d-109">Sustav će pokušati povezati nevezane račune s nevezanim transakcijama troškova.</span><span class="sxs-lookup"><span data-stu-id="abe9d-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="abe9d-110">Iz računa možete stvoriti ručno unesene transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="abe9d-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="abe9d-111">Računi priloženi izvješću o troškovima</span><span class="sxs-lookup"><span data-stu-id="abe9d-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="abe9d-112">Kako biste tijekom stvaranja izvješća o troškovima automatski priložili račune koji obuhvaćaju transakcije kreditnom karticom, izvršite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="abe9d-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="abe9d-113">Otvorite radni prostor **Upravljanje troškovima**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="abe9d-114">Na kartici **Računi** provjerite postoje li nepovezani računi.</span><span class="sxs-lookup"><span data-stu-id="abe9d-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="abe9d-115">Račune možete prenijeti i na karticu **Računi**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="abe9d-116">Na kartici **Troškovi** provjerite postoje li nepovezani troškovi.</span><span class="sxs-lookup"><span data-stu-id="abe9d-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="abe9d-117">Administrator troškova uobičajeno uvozi te troškove od davatelja usluge kreditnih kartica.</span><span class="sxs-lookup"><span data-stu-id="abe9d-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="abe9d-118">Odaberite **Novo izvješće o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-118">Select **New expense report**.</span></span> <span data-ttu-id="abe9d-119">Primjećujete kako troškove i račune sada možete uključiti tijekom stvaranja izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="abe9d-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="abe9d-120">Ako dodate i troškove i račune, aktivirat će se automatsko podudaranje računa i troškova.</span><span class="sxs-lookup"><span data-stu-id="abe9d-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="abe9d-121">Stvaranje i podudaranje računa s izvješćem o troškovima</span><span class="sxs-lookup"><span data-stu-id="abe9d-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="abe9d-122">Kako biste stvorili trošak ili uskladili trošak s računa, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="abe9d-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="abe9d-123">Na izvješću o troškovima, na kartici **Računi**, račun priložite odabirom mogućnosti **Dodaj račune**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="abe9d-124">Ispod prenesene slike računa prikazuju se mogućnosti **Stvori** i **Uskladi**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="abe9d-125">Odaberite mogućnost **Stvori** za stvaranje ručno unesene transakcije troškova i popunjavanje vrijednosti izvučenih iz računa.</span><span class="sxs-lookup"><span data-stu-id="abe9d-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="abe9d-126">Ako odaberete **Uskladi**, sustav pokušava postojeći trošak uskladiti s računom.</span><span class="sxs-lookup"><span data-stu-id="abe9d-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="abe9d-127">Instalacija</span><span class="sxs-lookup"><span data-stu-id="abe9d-127">Installation</span></span>

<span data-ttu-id="abe9d-128">Kako biste upotrijebili ove napredne mogućnosti troškova, instalirajte dodatak Usluga upravljanja troškovima za Microsoft Dynamics 365 Finance i uključite značajke u svojoj instanci.</span><span class="sxs-lookup"><span data-stu-id="abe9d-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="abe9d-129">Dodatku možete pristupiti iz svog projekta u aplikaciji Microsoft Dynamics Lifecycle Services(LCS).</span><span class="sxs-lookup"><span data-stu-id="abe9d-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="abe9d-130">Prijavite se na LCS i otvorite željeno okruženje.</span><span class="sxs-lookup"><span data-stu-id="abe9d-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="abe9d-131">Idite na **Potpune pojedinosti**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="abe9d-132">Odaberite **Održavaj** ili se pomaknite dolje do Brze kartice **Dodaci za okruženje**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="abe9d-133">Odaberite **Instaliraj novi dodatak**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="abe9d-134">Odaberite **Usluga upravljanja troškovima**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="abe9d-135">Slijedite vodič za instalaciju i prihvatite uvjete i odredbe.</span><span class="sxs-lookup"><span data-stu-id="abe9d-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="abe9d-136">Odaberite **Instaliraj**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-136">Select **Install**.</span></span>

<span data-ttu-id="abe9d-137">U radnom prostoru **Upravljanje značajkama** uključite sljedeće značajke:</span><span class="sxs-lookup"><span data-stu-id="abe9d-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="abe9d-138">Izmijenjena izvješća o trošku</span><span class="sxs-lookup"><span data-stu-id="abe9d-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="abe9d-139">Automatsko podudaranje i stvaranje troška iz računa</span><span class="sxs-lookup"><span data-stu-id="abe9d-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="abe9d-140">Kada uključite ove značajke, događaju se sljedeće radnje:</span><span class="sxs-lookup"><span data-stu-id="abe9d-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="abe9d-141">Postojeći radni prostor **Upravljanje troškovima** zamjenjuje se novim radnim prostorom.</span><span class="sxs-lookup"><span data-stu-id="abe9d-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="abe9d-142">Dodana je nova stavka izbornika za vidljivost polja troška.</span><span class="sxs-lookup"><span data-stu-id="abe9d-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="abe9d-143">Još uvijek možete otvoriti prethodnu stranicu **Izvješća o troškovima** odlaskom na **Upravljanje troškovima > Moji troškovi > Izvješća o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="abe9d-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="abe9d-144">Tijekovi rada i sva odobrenja i dalje vas vode na postojeću stranicu izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="abe9d-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="abe9d-145">Računi će se obrađivati putem aplikacije Microsoft Azure Cognitive Services, a izdvojit će se i dodati metapodaci.</span><span class="sxs-lookup"><span data-stu-id="abe9d-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="abe9d-146">Dodana je mogućnost koja vam omogućuje stvaranje izvješća o troškovima koji obuhvaćaju podudarne nepovezane račune.</span><span class="sxs-lookup"><span data-stu-id="abe9d-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="abe9d-147">Mogućnost koja se dodaje izvješćima o troškovima omogućuje vam stvaranje retka troška iz računa ili pokušaj usklađivanja postojećeg računa s postojećim retkom troška.</span><span class="sxs-lookup"><span data-stu-id="abe9d-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="abe9d-148">Najčešća pitanja</span><span class="sxs-lookup"><span data-stu-id="abe9d-148">Frequently asked questions</span></span>

<span data-ttu-id="abe9d-149">**Koristi li Microsoft moje podatke za svoje modele?**</span><span class="sxs-lookup"><span data-stu-id="abe9d-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="abe9d-150">Ne, za svoju uslugu obrade računa Microsoft je stvorio opći model strojnog učenja.</span><span class="sxs-lookup"><span data-stu-id="abe9d-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="abe9d-151">Ovaj se model ne temelji na računima koje ste prenijeli.</span><span class="sxs-lookup"><span data-stu-id="abe9d-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="abe9d-152">**Gdje je ova značajka dostupna i obrađena?**</span><span class="sxs-lookup"><span data-stu-id="abe9d-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="abe9d-153">Trenutačno je podržan SAD.</span><span class="sxs-lookup"><span data-stu-id="abe9d-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="abe9d-154">**Kamo idu moji računi?**</span><span class="sxs-lookup"><span data-stu-id="abe9d-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="abe9d-155">Financije će kontaktirati uslugu Cognitive Services radi izdvajanja podataka s terena.</span><span class="sxs-lookup"><span data-stu-id="abe9d-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="abe9d-156">Cognitive Services zadržat će kopiju vašeg računa do 24 sata dok traje obrada.</span><span class="sxs-lookup"><span data-stu-id="abe9d-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="abe9d-157">Nakon završetka obrade, Cognitive Services uklonit će račun.</span><span class="sxs-lookup"><span data-stu-id="abe9d-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="abe9d-158">Računi se i dalje čuvaju u Financijama.</span><span class="sxs-lookup"><span data-stu-id="abe9d-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="abe9d-159">Dodatne informacije potražite u članku [Omogućivanje razumijevanja računa s novom mogućnosti prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="abe9d-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
