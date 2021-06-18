---
title: Stvaranje predugovora za naplatu na temelju napretka
description: U ovoj se temi objašnjava način stvaranja ugovora o projektima tako da klijentima možete generirati račune na temelju postotka dovršenog posla.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999662"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="ac1eb-103">Stvaranje predugovora za naplatu na temelju napretka</span><span class="sxs-lookup"><span data-stu-id="ac1eb-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac1eb-104">U ovoj se temi objašnjava način stvaranja ugovora o projektima tako da klijentima možete stvoriti račune na temelju postotka dovršenog posla.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="ac1eb-105">Iznosi faktura automatski se izračunavaju za proračunske kategorije posla koje ste postavili za projekt.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="ac1eb-106">Vrijeme računa postavlja se kada pregovarate s klijentom o ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="ac1eb-107">Upotrijebite postupke navedene u ovoj temi za postavljanje ugovora, povezanog projekta i pravila naplate koja izračunavaju iznose fakture za proračunske kategorije posla koje ste postavili za projekt.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="ac1eb-108">Nakon što stvorite ugovor i projekt, možete postaviti pojedinosti projekta.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="ac1eb-109">Na primjer, možete definirati aktivnosti i dodijeliti radnike projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="ac1eb-110">Primjer</span><span class="sxs-lookup"><span data-stu-id="ac1eb-110">Example</span></span>

<span data-ttu-id="ac1eb-111">Vaša je tvrtka ili ustanova tvrtka za razvoj softvera.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-111">Your organization is a software development firm.</span></span> <span data-ttu-id="ac1eb-112">Pristajete razviti paket obračuna plaća za klijenta za ukupnu naknadu od 20.000 USD.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="ac1eb-113">Vaša tvrtka ili ustanova pristaje fakturirati klijentu kako dovršavate određene postotke projekta.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="ac1eb-114">Za posao postavljate sljedeće kategorije projekta kako biste ih mogli upotrebljavati u postupku naplate:</span><span class="sxs-lookup"><span data-stu-id="ac1eb-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="ac1eb-115">Savjetovanje</span><span class="sxs-lookup"><span data-stu-id="ac1eb-115">Consulting</span></span>
- <span data-ttu-id="ac1eb-116">Izrađujte</span><span class="sxs-lookup"><span data-stu-id="ac1eb-116">Design</span></span>
- <span data-ttu-id="ac1eb-117">Instalacija</span><span class="sxs-lookup"><span data-stu-id="ac1eb-117">Installation</span></span>

<span data-ttu-id="ac1eb-118">Postavljate i pravila naplate koja automatski izračunavaju iznose faktura za postotak dovršenosti posla na projektu za svaku kategoriju.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="ac1eb-119">Upravitelj proračuna stvara proračun za kategorije projekta.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="ac1eb-120">Količina dovršenosti posla automatski se izračunava kao postotak stvarnog posla u odnosu na proračunske iznose.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ac1eb-121">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="ac1eb-121">Prerequisites</span></span>

<span data-ttu-id="ac1eb-122">Prije stvaranja projekta koji upotrebljava pravila naplate, morate postaviti brojčane nizove za pravila naplate i dnevnik naknada koji se upotrebljava za knjiženje naplate napretka.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="ac1eb-123">Idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Parametri upravljanja projektom i računovodstva**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="ac1eb-124">Na stranici **Parametri upravljanja projektom i računovodstva**, na kartici **Brojčani nizovi**, postavite brojčani niz koji želite upotrebljavati tijekom izrade pravila naplate.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="ac1eb-125">Idite na **Upravljanje projektima i računovodstvo** \> **Dnevnici** \> **Naknada**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="ac1eb-126">Na stranici **Dnevnik naknada** odaberite **Novi** i unesite naziv dnevnika.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="ac1eb-127">Stvaranje ugovora za naplatu napretka</span><span class="sxs-lookup"><span data-stu-id="ac1eb-127">Create a contract for progress billings</span></span>

<span data-ttu-id="ac1eb-128">Ovaj postupak upotrebljavajte za izradu ugovora o projektu za projekt s fiksnom cijenom.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="ac1eb-129">Fakturu za projekt stvarate kada posao koji je dovršen na projektu dosegne određeni postotak.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="ac1eb-130">Idite na **Upravljanje projektom i računovodstvo** \> **Projekti** \> **Ugovori o projektu**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="ac1eb-131">Na stranici **Ugovori o projektu** odaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="ac1eb-132">U dijaloškom okviru **Novi ugovor o projektu** postavite sljedeća polja:</span><span class="sxs-lookup"><span data-stu-id="ac1eb-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="ac1eb-133">**Ime**</span><span class="sxs-lookup"><span data-stu-id="ac1eb-133">**Name**</span></span>
    - <span data-ttu-id="ac1eb-134">**Vrsta financiranja**</span><span class="sxs-lookup"><span data-stu-id="ac1eb-134">**Funding type**</span></span>
    - <span data-ttu-id="ac1eb-135">**Izvor financiranja**</span><span class="sxs-lookup"><span data-stu-id="ac1eb-135">**Funding source**</span></span>
    - <span data-ttu-id="ac1eb-136">**Valuta prodaje** – Prema zadanim postavkama, ova se valuta upotrebljava za fakture klijenta koji su povezani s ugovorom o projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="ac1eb-137">Međutim, valutu prodaje možete promijeniti na određenoj fakturi za klijenta.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="ac1eb-138">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-138">Select **OK**.</span></span> <span data-ttu-id="ac1eb-139">Podaci se kopiraju u zaglavlje stranice **Ugovori o projektu**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="ac1eb-140">Na stranici **Ugovori o projektu** ispunite ostatak potrebnih podataka za projekt.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="ac1eb-141">Stvaranje projekta za naplatu napretka</span><span class="sxs-lookup"><span data-stu-id="ac1eb-141">Create a project for progress billings</span></span>

<span data-ttu-id="ac1eb-142">Slijedite ove korake za stvaranje projekta i svih potprojekata koji su povezani s ugovorom o projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="ac1eb-143">Idite na mogućnost **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="ac1eb-144">Na stranici **Svi projekti** odaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="ac1eb-145">U dijaloškom okviru **Novi projekt**, u polju **Vrsta projekta**, odaberite **Vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="ac1eb-146">Odaberite projektnu grupu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-146">Select a project group.</span></span> <span data-ttu-id="ac1eb-147">Projektna grupa definira podatke o knjiženju za projekte koji su dodijeljeni grupi.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="ac1eb-148">Odaberite **Stvori projekt**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-148">Select **Create project**.</span></span>
6. <span data-ttu-id="ac1eb-149">Nakon stvaranja projekta, postavite fazu projekta na **U postupku**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="ac1eb-150">Stvaranje proračuna projekta</span><span class="sxs-lookup"><span data-stu-id="ac1eb-150">Create a budget for a project</span></span>

<span data-ttu-id="ac1eb-151">Proračunske kategorije upotrebljavaju se za automatski izračun iznosa računa za postotak dovršenosti posla za svaku kategoriju.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="ac1eb-152">Slijedite ove korake kako biste stvorili proračunske kategorije za procijenjene troškove.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="ac1eb-153">Idite na mogućnost **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="ac1eb-154">Na stranici **Svi projekti** odaberite i otvorite projekt koji želite.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="ac1eb-155">Na stranici **Projekti**, u oknu Radnje, na kartici **Planiranje**, u grupi **Proračun**, odaberite **Proračun projekta**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="ac1eb-156">Na stranici **Proračun projekta** unesite procijenjeni trošak za svaku kategoriju projekta.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="ac1eb-157">Stvorite pravila naplate za napredovanje naplate</span><span class="sxs-lookup"><span data-stu-id="ac1eb-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="ac1eb-158">Idite na **Upravljanje projektom i računovodstvo** \> **Projekti** \> **Ugovori o projektu**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="ac1eb-159">Na stranici **Ugovori o projektima** odaberite i otvorite ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="ac1eb-160">Na stranici ugovora o projektu, na Brzoj kartici **Pravila naplate**, odaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="ac1eb-161">Na stranici **Pravilo naplate**, u polju **Vrsta retka**, odaberite **Napredak**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="ac1eb-162">Na Brzoj kartici **Pojedinosti retka pravila naplate**, u polju **Vrijednost ugovora**, unesite ukupnu vrijednost ugovora.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="ac1eb-163">U polju **Kategorija** odaberite kategoriju u koju ćete knjižiti transakciju naknade.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="ac1eb-164">U polju **Projekt** odaberite projekt koji upotrebljava ovo pravilo naplate.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="ac1eb-165">Izborno: Dodijelite pravilo naplate dodatnim projektima.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="ac1eb-166">Na Brzoj kartici **Projekt**, u odjeljku **Dostupni projekti**, odaberite projekt, a zatim odaberite gumb sa strelicom udesno kako biste projekt dodali odjeljku **Odabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="ac1eb-167">Neobvezno: Izračunajte postotni iznos koji kupac usteže kada plaća fakturu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="ac1eb-168">Na Brzoj kartici **Uvjeti ustezanja plaćanja** odaberite izvor financiranja, a zatim u polju **Postotak ustezanja** unesite postotak ustezanja.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="ac1eb-169">Ponovite ove korake za stvaranje dodatnih pravila naplate za ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1eb-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]