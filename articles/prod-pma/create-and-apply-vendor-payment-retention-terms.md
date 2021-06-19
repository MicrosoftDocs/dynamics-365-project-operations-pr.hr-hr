---
title: Stvaranje i primjena uvjeta zadržanog plaćanja dobavljaču
description: U ovoj temi nalaze se informacije o načinu postavljanja i održavanja uvjeta zadržanog plaćanja dobavljaču.
author: Yowelle
ms.date: 05/26/2020
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
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006308"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="7c7f7-103">Stvaranje i primjena uvjeta zadržanog plaćanja dobavljaču</span><span class="sxs-lookup"><span data-stu-id="7c7f7-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="7c7f7-104">Postavljanje uvjeta zadržavanja plaćanja dobavljaču za projekt korisno je kada vaša tvrtka ili ustanova želi zadržati dio od ukupnog iznosa koji je dužna dobavljaču.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="7c7f7-105">Na primjer, kada želite zadržati plaćanje dobavljaču dok isporučeni proizvodi ne ispune vaša očekivanja.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="7c7f7-106">Uvjeti zadržavanja plaćanja dobavljaču mogu se odrediti kada pregovarate o ugovoru o nabavi.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="7c7f7-107">Stvaranje uvjeta zadržavanja plaćanja dobavljaču</span><span class="sxs-lookup"><span data-stu-id="7c7f7-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="7c7f7-108">Možete unijeti postotak zadržavanja od ukupnog plaćanja dobavljaču i postotak prethodno zadržanih iznosa koji će se osloboditi.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="7c7f7-109">Iznosi se automatski zadržavaju od faktura dobavljača sve dok ugovor ne dosegne određeno stanje završenosti.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="7c7f7-110">Nakon što postavite uvjete zadržavanja, možete ih primijeniti na svaki projekt tog dobavljača.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="7c7f7-111">Upotrijebite sljedeće korake za postavljanje i održavanje uvjeta zadržavanja plaćanja dobavljaču.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="7c7f7-112">Idite na **Upravljanje projektima i računovodstvo** > **Zadržavanje** > **Uvjeti zadržavanja plaćanja dobavljaču**.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="7c7f7-113">Odaberite **Novo** kako biste dodali novi uvjet za zadržavanje plaćanja dobavljaču.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="7c7f7-114">Vrijednost **ID pravila** za novi uvjet unosi se automatski.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="7c7f7-115">U polje **Opis** unesite kratki opis i na Brzoj kartici **Uvjeti** odaberite **Dodaj redak** za unos vrijednosti uvjeta za sljedeće:</span><span class="sxs-lookup"><span data-stu-id="7c7f7-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="7c7f7-116">**Postotak isporučenih jedinica**: Unesite postotak završetka za uvjet.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="7c7f7-117">Iznosi se automatski zadržavaju od faktura dobavljača sve dok se stanje završenosti ne izjednači s navedenim postotkom.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="7c7f7-118">Na primjer, ako unesete 50,00, iznosi se zadržavaju sve dok projekt ne bude završen 50 posto.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="7c7f7-119">**Postotak zadržavanja**: Unesite postotak iznosa fakture dobavljača koji će se zadržati.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="7c7f7-120">Na primjer, ako unesete 10,00, tada se zadržava 10 posto iznosa od fakture dobavljača dok projekt ne dosegne postotak dovršenosti kako je postavljeno u polju **Postotak isporučenih jedinica**.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="7c7f7-121">**Postotak za oslobađanje**: Odaberite **Dodaj redak** za unos postotka svih prethodno zadržanih iznosa koji se oslobađaju na odabranoj razini dovršenosti projekta.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="7c7f7-122">Ako imate više od jedne kontrolne točke za različite razine dovršenosti projekta, unesite zasebni redak zadržavanja plaćanja dobavljaču za svako pravilo zadržavanja.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="7c7f7-123">Svaki redak može odrediti različiti postotak zadržavanja i različiti postotak oslobađanja za svaku naznačenu razinu dovršenosti projekta.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="7c7f7-124">Nakon što stvorite uvjete zadržavanja plaćanja dobavljaču, možete ih primijeniti na projekt.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="7c7f7-125">Primjena uvjeta zadržavanja dobavljača na projekt</span><span class="sxs-lookup"><span data-stu-id="7c7f7-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="7c7f7-126">Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti** i otvorite projekt sa stranice s popisom projekata.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="7c7f7-127">Na Brzoj kartici **Ugovori s dobavljačima** odaberite **Dodaj redak**.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="7c7f7-128">U polju **koda računa** odaberite jednu od sljedećih mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="7c7f7-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="7c7f7-129">**Tablica**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na pojedinog dobavljača.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="7c7f7-130">**Grupa**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na sve dobavljače u grupi dobavljača.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="7c7f7-131">**Svi**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na sve dobavljače.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="7c7f7-132">U polju **Dobavljač /grupa dobavljača** odaberite dobavljača ili grupu dobavljača na koje se primjenjuju uvjeti zadržavanja plaćanja.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="7c7f7-133">Ako ste u prethodnom koraku odabrali **Svi**, ovo polje nije dostupno.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="7c7f7-134">U polju **Uvjeti zadržavanja plaćanja dobavljaču** odaberite uvjete zadržavanja koje ste stvorili u prethodnom postupku.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="7c7f7-135">Ako projekt za dobavljača ima postavljene i uvjete „plati kad bude plaćeno” (PWP, pay-when-paid), unesite postotak praga za projekt u polje **Postotak praga PWP-a**.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="7c7f7-136">Uvjeti zadržavanja plaćanja dobavljaču prikazuju se i na narudžbenicama koje stvarate za dobavljača.</span><span class="sxs-lookup"><span data-stu-id="7c7f7-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]