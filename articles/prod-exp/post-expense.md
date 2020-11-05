---
title: Knjiženje izvješća o troškovima
description: U ovoj se temi objašnjava način knjiženja izvješća o troškovima u glavnu knjigu.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073534"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="92d9a-103">Knjiženje izvješća o troškovima</span><span class="sxs-lookup"><span data-stu-id="92d9a-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92d9a-104">Nakon što se odobri izvješće o troškovima i prenese u opću temeljnicu, može se knjižiti u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="92d9a-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="92d9a-105">Kada objavite izvješće o troškovima, identificiraju se troškovi koji ispunjavaju uvjete za povrat poreza na dodanu vrijednost (PDV).</span><span class="sxs-lookup"><span data-stu-id="92d9a-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="92d9a-106">Zadatak provjere i povrata plaćenog PDV-a dodjeljuje se zaposleniku koji je odgovoran za provjeru valjanosti izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="92d9a-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="92d9a-107">Ako se troškovima iz izvješća o troškovima tereti tvrtka koja nije tvrtka koja zapošljava zaposlenika, morate provjeriti valjanost tvrtke koja duguje za te troškove i tvrtke kojoj se za troškove duguje.</span><span class="sxs-lookup"><span data-stu-id="92d9a-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="92d9a-108">Na primjer, zaposlenik koji je predao izvješće o trošku radi za tvrtku DAT, ali je tvrtki DIR naplatio trošak.</span><span class="sxs-lookup"><span data-stu-id="92d9a-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="92d9a-109">U ovom je slučaju DAT tvrtka kojoj se duguje trošak, a DIR tvrtka koja duguje za trošak.</span><span class="sxs-lookup"><span data-stu-id="92d9a-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="92d9a-110">Nakon što provjerite valjanost ovih redaka temeljnice, retke troškova možete knjižiti u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="92d9a-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="92d9a-111">Kako biste knjižili izvješće o troškovima, na stranici **Odobrena izvješća o troškovima** odaberite izvješće o troškovima, a zatim na oknu radnji odaberite **Knjiži**.</span><span class="sxs-lookup"><span data-stu-id="92d9a-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="92d9a-112">Također možete istodobno knjižiti sva izvješća o troškovima na popisu.</span><span class="sxs-lookup"><span data-stu-id="92d9a-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="92d9a-113">Odaberite sva izvješća o troškovima, a zatim odaberite **Knjiži**.</span><span class="sxs-lookup"><span data-stu-id="92d9a-113">Select all the expense reports, and then select **Post**.</span></span>
