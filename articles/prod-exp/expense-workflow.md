---
title: Tijek rada upravljanja troškovima
description: U ovoj temi objašnjava se način uporabe sustava tijeka rada u aplikaciji Microsoft Dynamics 365 Finance za postavljanje postupka pregleda izvješća o troškovima u Upravljanju troškovima.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005197"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="58ea4-103">Tijek rada upravljanja troškovima</span><span class="sxs-lookup"><span data-stu-id="58ea4-103">Expense management workflow</span></span>

<span data-ttu-id="58ea4-104">Možete upotrebljavati sustav tijeka rada za postavljanje postupka pregleda izvješća o troškovima u Upravljanju troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="58ea4-105">Možete postaviti tijek rada koji upotrebljava sljedeće kriterije za određivanje osobe koja odobrava izvješća o troškovima:</span><span class="sxs-lookup"><span data-stu-id="58ea4-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="58ea4-106">Hijerarhija izvješćivanja zaposlenika i unaprijed definirana ograničenja odobrenja</span><span class="sxs-lookup"><span data-stu-id="58ea4-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="58ea4-107">Odobravanje na više razina koje podržava privremene odobravatelje i konačnog odobravatelja</span><span class="sxs-lookup"><span data-stu-id="58ea4-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="58ea4-108">Financijske dimenzije i odgovornost projekta</span><span class="sxs-lookup"><span data-stu-id="58ea4-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="58ea4-109">Dodjela određenim korisnicima ili grupama korisnika</span><span class="sxs-lookup"><span data-stu-id="58ea4-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="58ea4-110">Odobrenja tijeka rada mogu se stvoriti za izvješća o troškovima, putne naloge, gotovinske predujmove i povrat poreza na dodanu vrijednost (PDV).</span><span class="sxs-lookup"><span data-stu-id="58ea4-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="58ea4-111">**Primjer**</span><span class="sxs-lookup"><span data-stu-id="58ea4-111">**Example**</span></span>

<span data-ttu-id="58ea4-112">Sljedeći je postupak primjer tijeka rada upravljanja troškovima za izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="58ea4-113">Zaposlenik stvara i sprema izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="58ea4-114">Zaposlenik šalje izvješće o troškovima na odobrenje.</span><span class="sxs-lookup"><span data-stu-id="58ea4-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="58ea4-115">Odobravatelj se identificira na temelju pravila koja su definirana kada je postavljen tijeka rada.</span><span class="sxs-lookup"><span data-stu-id="58ea4-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="58ea4-116">Odobravatelj prima obavijest da je izvješće o troškovima spremno za odobrenje.</span><span class="sxs-lookup"><span data-stu-id="58ea4-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="58ea4-117">Odobravatelj pregledava izvješće o troškovima i provjerava jesu li ispunjeni sljedeći uvjeti:</span><span class="sxs-lookup"><span data-stu-id="58ea4-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="58ea4-118">Troškovi ne krše nikakva pravila o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="58ea4-119">Ako trošak krši pravila, odobravatelj provjerava uključuje li izvješće o troškovima valjano poslovno opravdanje.</span><span class="sxs-lookup"><span data-stu-id="58ea4-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="58ea4-120">Elektronički računi priloženi su izvješću o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="58ea4-121">Odobravatelj odobrava izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="58ea4-122">Izvješće o troškovima dodjeljuje se koordinatoru za knjiženje Dugovanja.</span><span class="sxs-lookup"><span data-stu-id="58ea4-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="58ea4-123">Događa se jedan od sljedećih koraka, ovisno o tome je li konfigurirano automatsko knjiženje:</span><span class="sxs-lookup"><span data-stu-id="58ea4-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="58ea4-124">Ako je konfigurirano automatsko knjiženje, izvješće o trošku obrađuje se za plaćanje i ažurira se status izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="58ea4-125">Ako automatsko knjiženje nije konfigurirano, koordinator Dugovanja provjerava jesu li predani svi izvorni računi te jesu li računi usklađeni s troškovima u izvješću o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="58ea4-126">Ispravnost svih poreznih kodova koji se unose u izvješće o troškovima također mora biti provjerena.</span><span class="sxs-lookup"><span data-stu-id="58ea4-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="58ea4-127">Nakon provjere ovih preduvjeta knjiži se izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="58ea4-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="58ea4-128">Nakon što se proknjiži izvješće o troškovima, autorizira se plaćanje izvješća o troškovima, a zaposleniku se vraća naknada.</span><span class="sxs-lookup"><span data-stu-id="58ea4-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]