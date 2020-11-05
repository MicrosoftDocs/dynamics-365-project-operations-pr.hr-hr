---
title: Postavljanje tijekova rada za upravljanje troškovima
description: Možete postaviti postupak tijeka rada koji se upotrebljava za pregled i odobravanje dokumenata o putovanju i troškovima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073415"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="11608-103">Postavljanje tijekova rada za upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="11608-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="11608-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="11608-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="11608-105">Možete postaviti postupak tijeka rada za pregled i odobravanje dokumenata o putovanju i troškovima.</span><span class="sxs-lookup"><span data-stu-id="11608-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="11608-106">Možete definirati tijekove rada za izvješća o troškovima, putne naloge i zahtjeve za predujmom gotovine.</span><span class="sxs-lookup"><span data-stu-id="11608-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="11608-107">Tijek rada predstavlja poslovni proces i definira način prolaska dokumenta kroz sustav.</span><span class="sxs-lookup"><span data-stu-id="11608-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="11608-108">Tijek rada također ukazuje na to tko mora izvršiti zadatak ili odobriti dokument.</span><span class="sxs-lookup"><span data-stu-id="11608-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="11608-109">Nekoliko je blagodati uporabe sustava tijeka rada u vašoj tvrtki ili ustanovi:</span><span class="sxs-lookup"><span data-stu-id="11608-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="11608-110">**Dosljedni procesi** : Možete definirati postupak odobrenja za određene dokumente, poput zahtjeva za kupnju i izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="11608-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="11608-111">Uporaba sustava tijeka rada osigurava da se dokumenti obrađuju i odobravaju na dosljedan i učinkovit način.</span><span class="sxs-lookup"><span data-stu-id="11608-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="11608-112">**Vidljivost procesa** : Možete pratiti mjerne podatke statusa, povijesti i učinkovitosti određene instance tijeka rada.</span><span class="sxs-lookup"><span data-stu-id="11608-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="11608-113">To vam pomaže utvrditi trebaju li se unijeti promjene u tijek rada kako bi se poboljšala učinkovitost.</span><span class="sxs-lookup"><span data-stu-id="11608-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="11608-114">**Centralizirani popis posla** : Korisnici mogu pregledavati centralizirani popis posla kako bi vidjeli zadatke tijeka rada i odobrenja koja su im dodijeljena.</span><span class="sxs-lookup"><span data-stu-id="11608-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="11608-115">Vrste tijekova rada</span><span class="sxs-lookup"><span data-stu-id="11608-115">Workflow types</span></span>

<span data-ttu-id="11608-116">Sljedeća tablica navodi vrste tijekova rada u kojima možete stvoriti u mogućnosti **Upravljanje troškovima**.</span><span class="sxs-lookup"><span data-stu-id="11608-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="11608-117"><strong>Vrsta</strong></span><span class="sxs-lookup"><span data-stu-id="11608-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="11608-118"><strong>Ovu vrstu upotrijebite za</strong></span><span class="sxs-lookup"><span data-stu-id="11608-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="11608-119"><strong>Automatsko odobrenje izvješća o trošku</strong></span><span class="sxs-lookup"><span data-stu-id="11608-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="11608-120">Stvorite tijekove rada odobrenja za izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="11608-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="11608-121"><strong>Automatsko objavljivanje izvješća o trošku</strong></span><span class="sxs-lookup"><span data-stu-id="11608-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="11608-122">Stvorite tijekove rada za automatsko objavljivanje izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="11608-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="11608-123"><strong>Stavka retka troška</strong></span><span class="sxs-lookup"><span data-stu-id="11608-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="11608-124">Stvorite tijekove rada odobrenja za stavke retka izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="11608-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="11608-125"><strong>Automatsko knjiženje stavke retka troška</strong></span><span class="sxs-lookup"><span data-stu-id="11608-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="11608-126">Stvorite tijekove rada za automatsko objavljivanja stavki retka izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="11608-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="11608-127"><strong>Putni nalog</strong></span><span class="sxs-lookup"><span data-stu-id="11608-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="11608-128">Stvorite tijekove rada odobrenja za putne naloge.</span><span class="sxs-lookup"><span data-stu-id="11608-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="11608-129"><strong>Zahtjev za gotovinski predujam</strong></span><span class="sxs-lookup"><span data-stu-id="11608-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="11608-130">Stvorite tijekove rada odobrenja zahtjeva za gotovinski predujam.</span><span class="sxs-lookup"><span data-stu-id="11608-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="11608-131"><strong>Povrat PDV-a</strong></span><span class="sxs-lookup"><span data-stu-id="11608-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="11608-132">Stvorite tijekove rada odobrenja za povrat poreza na dodanu vrijednost (PDV).</span><span class="sxs-lookup"><span data-stu-id="11608-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
