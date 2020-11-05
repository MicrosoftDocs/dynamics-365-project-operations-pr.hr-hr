---
title: Obrada računa za troškove
description: U ovoj se temi nalaze informacije o obradi optičkog prepoznavanja znakova (OCR, optical character recognition) za račune. Ova je funkcija dizajnirana za poboljšanje korisničkog iskustva kada je izvješće o troškovima stvoreno u aplikaciji Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073546"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="9d502-104">Obrada računa za troškove</span><span class="sxs-lookup"><span data-stu-id="9d502-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d502-105">Unos troškova poboljšan je uvođenjem optičkog prepoznavanja znakova (OCR) za obradu računa.</span><span class="sxs-lookup"><span data-stu-id="9d502-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="9d502-106">Ova je funkcija dizajnirana za poboljšanje korisničkog iskustva kada je stvoreno izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="9d502-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="9d502-107">Glavne značajke</span><span class="sxs-lookup"><span data-stu-id="9d502-107">Key features</span></span>

- <span data-ttu-id="9d502-108">Ime trgovca, datum i ukupan iznos izdvojeni su iz računa.</span><span class="sxs-lookup"><span data-stu-id="9d502-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="9d502-109">Značajka će pokušati povezati nevezane račune s nevezanim transakcijama troškova.</span><span class="sxs-lookup"><span data-stu-id="9d502-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="9d502-110">Iz računa korisnici mogu stvoriti ručno unesene transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="9d502-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="9d502-111">Primjeri uporabe</span><span class="sxs-lookup"><span data-stu-id="9d502-111">Usage examples</span></span>

<span data-ttu-id="9d502-112">Kako biste tijekom stvaranja izvješća o troškovima automatski priložili račune koji obuhvaćaju transakcije kreditnom karticom, napravite sljedeće:</span><span class="sxs-lookup"><span data-stu-id="9d502-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="9d502-113">Otvorite radni prostor **Upravljanje troškovima**.</span><span class="sxs-lookup"><span data-stu-id="9d502-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="9d502-114">Na kartici **Računi** provjerite postoje li nepovezani računi.</span><span class="sxs-lookup"><span data-stu-id="9d502-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="9d502-115">Račune možete prenijeti i na karticu **Računi**.</span><span class="sxs-lookup"><span data-stu-id="9d502-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="9d502-116">Na kartici **Troškovi** provjerite postoje li nepovezani troškovi.</span><span class="sxs-lookup"><span data-stu-id="9d502-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="9d502-117">Administrator troškova uobičajeno uvozi te troškove od davatelja usluge kreditnih kartica.</span><span class="sxs-lookup"><span data-stu-id="9d502-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="9d502-118">Odaberite **Novo izvješće o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="9d502-118">Select **New expense report**.</span></span> <span data-ttu-id="9d502-119">Primjećujete kako troškove i račune sada možete uključiti tijekom stvaranja izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="9d502-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="9d502-120">Ako dodate i troškove i račune, aktivirat će se automatsko podudaranje računa i troškova.</span><span class="sxs-lookup"><span data-stu-id="9d502-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="9d502-121">Kako biste stvorili trošak ili uskladili trošak s računa, napravite sljedeće:</span><span class="sxs-lookup"><span data-stu-id="9d502-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="9d502-122">Na izvješću o troškovima, na kartici **Računi** , račun priložite odabirom mogućnosti **Dodaj račune**.</span><span class="sxs-lookup"><span data-stu-id="9d502-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="9d502-123">Ispod prenesene slike računa prikazuju se mogućnosti **Stvori** i **Uskladi**.</span><span class="sxs-lookup"><span data-stu-id="9d502-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="9d502-124">Odaberite mogućnost **Stvori** za stvaranje ručno unesene transakcije troškova i popunjavanje vrijednosti izvučenih iz računa.</span><span class="sxs-lookup"><span data-stu-id="9d502-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="9d502-125">Ako odaberete **Uskladi** , sustav pokušava postojeći trošak uskladiti s računom.</span><span class="sxs-lookup"><span data-stu-id="9d502-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="9d502-126">Instalacija</span><span class="sxs-lookup"><span data-stu-id="9d502-126">Installation</span></span>

<span data-ttu-id="9d502-127">Ova značajka radi u kombinaciji sa značajkom **Izmijenjena izvješća o trošku** za pojednostavljivanje iskustva s troškom.</span><span class="sxs-lookup"><span data-stu-id="9d502-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="9d502-128">Ova je značajka dostupna samo za Razinu 2+ okruženja, a to su Sigurnosna ograda i Proizvodnja.</span><span class="sxs-lookup"><span data-stu-id="9d502-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="9d502-129">Kako biste upotrijebili ove napredne mogućnosti troškova, instalirajte dodatak Usluga upravljanja troškovima za Microsoft Dynamics 365 Finance i uključite značajke u svojoj instanci.</span><span class="sxs-lookup"><span data-stu-id="9d502-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="9d502-130">Dodatku možete pristupiti iz svog projekta u aplikaciji Microsoft Dynamics Lifecycle Services(LCS).</span><span class="sxs-lookup"><span data-stu-id="9d502-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="9d502-131">Prijavite se na LCS i otvorite željeno okruženje.</span><span class="sxs-lookup"><span data-stu-id="9d502-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="9d502-132">Idite na **Potpune pojedinosti**.</span><span class="sxs-lookup"><span data-stu-id="9d502-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="9d502-133">Odaberite **Održavaj** ili se pomaknite dolje do Brze kartice **Dodaci za okruženje**.</span><span class="sxs-lookup"><span data-stu-id="9d502-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="9d502-134">Odaberite **Instaliraj novi dodatak**.</span><span class="sxs-lookup"><span data-stu-id="9d502-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="9d502-135">Odaberite **Usluga upravljanja troškovima**.</span><span class="sxs-lookup"><span data-stu-id="9d502-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="9d502-136">Slijedite vodič za instalaciju i prihvatite uvjete i odredbe.</span><span class="sxs-lookup"><span data-stu-id="9d502-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="9d502-137">Odaberite **Instaliraj**.</span><span class="sxs-lookup"><span data-stu-id="9d502-137">Select **Install**.</span></span>

<span data-ttu-id="9d502-138">U radnom prostoru **Upravljanje značajkama** uključite sljedeće značajke:</span><span class="sxs-lookup"><span data-stu-id="9d502-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="9d502-139">Izmijenjena izvješća o trošku</span><span class="sxs-lookup"><span data-stu-id="9d502-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="9d502-140">Automatsko podudaranje i stvaranje troška iz računa</span><span class="sxs-lookup"><span data-stu-id="9d502-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="9d502-141">Kada uključite ove značajke, događaju se sljedeće radnje:</span><span class="sxs-lookup"><span data-stu-id="9d502-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="9d502-142">Postojeći radni prostor **Upravljanje troškovima** zamjenjuje se novim radnim prostorom.</span><span class="sxs-lookup"><span data-stu-id="9d502-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="9d502-143">Dodana je nova stavka izbornika za vidljivost polja troška.</span><span class="sxs-lookup"><span data-stu-id="9d502-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="9d502-144">Još uvijek možete otvoriti prethodnu stranicu **Izvješća o troškovima** odlaskom na **Upravljanje troškovima > Moji troškovi > Izvješća o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="9d502-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="9d502-145">Tijekovi rada i sva odobrenja i dalje vas vode na postojeću stranicu izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="9d502-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="9d502-146">Računi će se obrađivati putem aplikacije Microsoft Azure Cognitive Services, a izdvojit će se i dodati metapodaci.</span><span class="sxs-lookup"><span data-stu-id="9d502-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="9d502-147">Dodana je mogućnost koja vam omogućuje stvaranje izvješća o troškovima koji obuhvaćaju podudarne nepovezane račune.</span><span class="sxs-lookup"><span data-stu-id="9d502-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="9d502-148">Mogućnost koja se dodaje izvješćima o troškovima omogućuje vam stvaranje retka troška iz računa ili pokušaj usklađivanja postojećeg računa s postojećim retkom troška.</span><span class="sxs-lookup"><span data-stu-id="9d502-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="9d502-149">Dodatne informacija o izmijenjenoj značajci izvješća o troškovima potražite u odjeljku [Izmijenjena izvješća o troškovima](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="9d502-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9d502-150">Najčešća pitanja</span><span class="sxs-lookup"><span data-stu-id="9d502-150">Frequently asked questions</span></span>

<span data-ttu-id="9d502-151">**Koristi li Microsoft moje podatke za svoje modele?**</span><span class="sxs-lookup"><span data-stu-id="9d502-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="9d502-152">Ne, za svoju uslugu obrade računa Microsoft je stvorio opći model strojnog učenja.</span><span class="sxs-lookup"><span data-stu-id="9d502-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="9d502-153">Ovaj se model ne temelji na računima koje ste prenijeli.</span><span class="sxs-lookup"><span data-stu-id="9d502-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="9d502-154">**Gdje je ova značajka dostupna i obrađena?**</span><span class="sxs-lookup"><span data-stu-id="9d502-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="9d502-155">Trenutačno je podržan SAD.</span><span class="sxs-lookup"><span data-stu-id="9d502-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="9d502-156">**Kamo idu moji računi?**</span><span class="sxs-lookup"><span data-stu-id="9d502-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="9d502-157">Financije će kontaktirati uslugu Cognitive Services radi izdvajanja podataka s terena.</span><span class="sxs-lookup"><span data-stu-id="9d502-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="9d502-158">Cognitive Services zadržat će kopiju vašeg računa do 24 sata dok traje obrada.</span><span class="sxs-lookup"><span data-stu-id="9d502-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="9d502-159">Nakon završetka obrade, Cognitive Services uklonit će račun.</span><span class="sxs-lookup"><span data-stu-id="9d502-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="9d502-160">Računi se i dalje čuvaju u Financijama.</span><span class="sxs-lookup"><span data-stu-id="9d502-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="9d502-161">Dodatne informacije potražite u članku [Omogućivanje razumijevanja računa s novom mogućnosti prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="9d502-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
