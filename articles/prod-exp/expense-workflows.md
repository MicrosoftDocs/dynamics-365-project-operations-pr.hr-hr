---
title: Postavljanje tijekova rada za upravljanje troškovima
description: Možete postaviti postupak tijeka rada za pregled i odobravanje dokumenata o putovanju i troškovima.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073542"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="16827-103">Postavljanje tijekova rada za upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="16827-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16827-104">Možete postaviti postupak tijeka rada koji se upotrebljava za pregled i odobravanje dokumenata o putovanju i troškovima.</span><span class="sxs-lookup"><span data-stu-id="16827-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="16827-105">Dokumenti za koje se mogu definirati tijekovi rada uključuju izvješća o troškovima, putne naloge i zahtjeve za predujmom gotovine.</span><span class="sxs-lookup"><span data-stu-id="16827-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="16827-106">Tijek rada predstavlja poslovni proces.</span><span class="sxs-lookup"><span data-stu-id="16827-106">A workflow represents a business process.</span></span> <span data-ttu-id="16827-107">Definira kako dokument prolazi kroz sustav i ukazuje na to tko mora izvršiti zadatak ili odobriti dokument.</span><span class="sxs-lookup"><span data-stu-id="16827-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="16827-108">Nekoliko je blagodati uporabe sustava tijeka rada u vašoj tvrtki ili ustanovi:</span><span class="sxs-lookup"><span data-stu-id="16827-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="16827-109">**Dosljedni procesi** –– Možete definirati postupak odobrenja za određene dokumente, poput zahtjeva za kupnju i izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="16827-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="16827-110">Uporaba sustava tijeka rada pomaže osigurati da se dokumenti obrađuju i odobravaju na dosljedan i učinkovit način.</span><span class="sxs-lookup"><span data-stu-id="16827-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="16827-111">Vidljivost procesa –– Možete pratiti mjerne podatke statusa, povijesti i učinkovitosti određene instance tijeka rada.</span><span class="sxs-lookup"><span data-stu-id="16827-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="16827-112">To vam pomaže utvrditi trebaju li se unijeti promjene u tijek rada kako bi se poboljšala učinkovitost.</span><span class="sxs-lookup"><span data-stu-id="16827-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="16827-113">Centralizirani popis posla –– Korisnici mogu pregledavati centralizirani popis posla kako bi vidjeli zadatke tijeka rada i odobrenja koja su im dodijeljena.</span><span class="sxs-lookup"><span data-stu-id="16827-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="16827-114">**Vrste tijekova rada koje možete stvoriti**</span><span class="sxs-lookup"><span data-stu-id="16827-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="16827-115">Sljedeća tablica navodi vrste tijekova rada koje možete stvoriti u mogućnosti **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="16827-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="16827-116"><strong>Vrsta</strong></span><span class="sxs-lookup"><span data-stu-id="16827-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="16827-117"><strong>Ovu vrstu upotrijebite za</strong></span><span class="sxs-lookup"><span data-stu-id="16827-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="16827-118"><strong>Izvještaj o troškovima</strong></span><span class="sxs-lookup"><span data-stu-id="16827-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="16827-119">Stvorite tijekove rada odobrenja za izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="16827-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="16827-120"><strong>Automatsko objavljivanje izvješća o trošku</strong></span><span class="sxs-lookup"><span data-stu-id="16827-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="16827-121">Stvorite tijekove rada za automatsko objavljivanje izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="16827-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="16827-122"><strong>Stavka retka troška</strong></span><span class="sxs-lookup"><span data-stu-id="16827-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="16827-123">Stvorite tijekove rada odobrenja za stavke retka izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="16827-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="16827-124"><strong>Automatsko knjiženje stavke retka troška</strong></span><span class="sxs-lookup"><span data-stu-id="16827-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="16827-125">Stvorite tijekove rada za automatsko objavljivanja stavki retka izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="16827-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="16827-126"><strong>Putni nalog</strong></span><span class="sxs-lookup"><span data-stu-id="16827-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="16827-127">Stvorite tijekove rada odobrenja za putne naloge.</span><span class="sxs-lookup"><span data-stu-id="16827-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="16827-128"><strong>Zahtjev za gotovinski predujam</strong></span><span class="sxs-lookup"><span data-stu-id="16827-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="16827-129">Stvorite tijekove rada odobrenja zahtjeva za gotovinski predujam.</span><span class="sxs-lookup"><span data-stu-id="16827-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="16827-130"><strong>Povrat PDV-a</strong></span><span class="sxs-lookup"><span data-stu-id="16827-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="16827-131">Stvorite tijekove rada odobrenja za povrat poreza na dodanu vrijednost (PDV).</span><span class="sxs-lookup"><span data-stu-id="16827-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

