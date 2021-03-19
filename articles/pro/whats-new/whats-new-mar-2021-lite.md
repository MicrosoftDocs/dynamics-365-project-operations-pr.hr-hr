---
title: Novosti u ožujku 2021. – osnovna implementacija aplikacije Project Operations
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju osnovne implementacije aplikacije Project Operations za ožujak 2021.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499984"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="66ad1-103">Novosti u ožujku 2021. – osnovna implementacija aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="66ad1-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="66ad1-104">_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="66ad1-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="66ad1-105">Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="66ad1-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="66ad1-106">Project Operations na verziji 4.8.0.91 okruženja platforme Dataverse</span><span class="sxs-lookup"><span data-stu-id="66ad1-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="66ad1-107">Ažuriranja kvalitete</span><span class="sxs-lookup"><span data-stu-id="66ad1-107">Quality updates</span></span>

| <span data-ttu-id="66ad1-108">**Područje značajke**</span><span class="sxs-lookup"><span data-stu-id="66ad1-108">**Feature area**</span></span> | <span data-ttu-id="66ad1-109">**Broj reference**</span><span class="sxs-lookup"><span data-stu-id="66ad1-109">**Reference number**</span></span> | <span data-ttu-id="66ad1-110">**Ažuriranja kvalitete**</span><span class="sxs-lookup"><span data-stu-id="66ad1-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="66ad1-111">Naplata i određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="66ad1-111">Billing and pricing</span></span> | <span data-ttu-id="66ad1-112">2133873</span><span class="sxs-lookup"><span data-stu-id="66ad1-112">2133873</span></span> | <span data-ttu-id="66ad1-113">Popravljen je prikaz simbola valute **Jedinična prodajna cijena** u rešetki **Procjene troškova**.</span><span class="sxs-lookup"><span data-stu-id="66ad1-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="66ad1-114">Naplata i određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="66ad1-114">Billing and pricing</span></span> | <span data-ttu-id="66ad1-115">2174616</span><span class="sxs-lookup"><span data-stu-id="66ad1-115">2174616</span></span> | <span data-ttu-id="66ad1-116">Kada se prihvati ponuda, prilagođeni cjenik iz ugovora navodi se u pojedinostima retka ugovora koje se kopiraju iz ponude.</span><span class="sxs-lookup"><span data-stu-id="66ad1-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="66ad1-117">Upravljanje prilikama</span><span class="sxs-lookup"><span data-stu-id="66ad1-117">Opportunity Management</span></span> | <span data-ttu-id="66ad1-118">2167475</span><span class="sxs-lookup"><span data-stu-id="66ad1-118">2167475</span></span> | <span data-ttu-id="66ad1-119">Popravljen je iznos poreza na računu za ispravak koji je pokrenuo nefakturirani stvarni unos.</span><span class="sxs-lookup"><span data-stu-id="66ad1-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="66ad1-120">Upravljanje prilikama</span><span class="sxs-lookup"><span data-stu-id="66ad1-120">Opportunity Management</span></span> | <span data-ttu-id="66ad1-121">2176285</span><span class="sxs-lookup"><span data-stu-id="66ad1-121">2176285</span></span> | <span data-ttu-id="66ad1-122">Iznos poreza ne smije se kopirati iz pojedinosti retka ugovora o prodaji / ponude u pojedinosti retka ugovora o cijeni / ponudi.</span><span class="sxs-lookup"><span data-stu-id="66ad1-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="66ad1-123">Upravljanje prilikama</span><span class="sxs-lookup"><span data-stu-id="66ad1-123">Opportunity Management</span></span> | <span data-ttu-id="66ad1-124">2188079</span><span class="sxs-lookup"><span data-stu-id="66ad1-124">2188079</span></span> | <span data-ttu-id="66ad1-125">Pravilo za dijeljenu naplatu ne smije se stvarati za ugovore koji se ne temelje na radu.</span><span class="sxs-lookup"><span data-stu-id="66ad1-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="66ad1-126">Planiranje i praćenje</span><span class="sxs-lookup"><span data-stu-id="66ad1-126">Planning and Tracking</span></span> | <span data-ttu-id="66ad1-127">2138853</span><span class="sxs-lookup"><span data-stu-id="66ad1-127">2138853</span></span> | <span data-ttu-id="66ad1-128">Ažurirana je funkcija kopiranja projekta kako bi se osiguralo da redci procjene troškova referentne zadatke kopiraju u odredišni projekt.</span><span class="sxs-lookup"><span data-stu-id="66ad1-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="66ad1-129">Planiranje i praćenje</span><span class="sxs-lookup"><span data-stu-id="66ad1-129">Planning and Tracking</span></span> | <span data-ttu-id="66ad1-130">2173259</span><span class="sxs-lookup"><span data-stu-id="66ad1-130">2173259</span></span> | <span data-ttu-id="66ad1-131">Ažurirana je funkcija kopiranja projekta kako bi se osiguralo da se u određenim scenarijima ne prikazuje poruka o pogrešci **Kopiranje WBS-a**.</span><span class="sxs-lookup"><span data-stu-id="66ad1-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="66ad1-132">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="66ad1-132">Time and Expense</span></span> | <span data-ttu-id="66ad1-133">2148910</span><span class="sxs-lookup"><span data-stu-id="66ad1-133">2148910</span></span> | <span data-ttu-id="66ad1-134">Ispravljen je problem s prikazom stranice **Uredi unos** u rešetki **Vremenski unos**.</span><span class="sxs-lookup"><span data-stu-id="66ad1-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="66ad1-135">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="66ad1-135">Time and Expense</span></span> | <span data-ttu-id="66ad1-136">2159798</span><span class="sxs-lookup"><span data-stu-id="66ad1-136">2159798</span></span> | <span data-ttu-id="66ad1-137">Postrožene su kontrole kako bi se osiguralo da se odobreni unosi troškova ne mogu uređivati.</span><span class="sxs-lookup"><span data-stu-id="66ad1-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


