---
title: Troškovi unutar tvrtke
description: U ovoj temi nalaze se informacije o načinu uporabe troškova unutar tvrtke za dodjelu troškova radnika pravnoj osobi za koju je posao obavljen.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271524"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="9592c-103">Međukompanijski troškovi</span><span class="sxs-lookup"><span data-stu-id="9592c-103">Intercompany expenses</span></span>

<span data-ttu-id="9592c-104">Radnik koji je zaposlen u jednoj pravnoj osobi u tvrtki ili ustanovi može obavljati posao za drugu pravnu osobu u istoj tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="9592c-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="9592c-105">Možete upotrijebiti troškove unutar tvrtke za dodjelu troškova radnika pravnoj osobi za koju je posao obavljen.</span><span class="sxs-lookup"><span data-stu-id="9592c-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="9592c-106">Pravna osoba koja zapošljava radnika naziva se pravnom osobom koja posuđuje.</span><span class="sxs-lookup"><span data-stu-id="9592c-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="9592c-107">Pravna osoba kojoj radnik stvara troškove naziva se pravnom osobom koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="9592c-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="9592c-108">Prije nego što radnik može stvoriti i poslati troškove unutar tvrtke, morate omogućiti retke za troškove unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="9592c-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="9592c-109">U pravnoj osobi koja posuđuje, na stranici **Parametri za upravljanje troškovima**, odaberite mogućnost **Omogući redak troškova unutar tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="9592c-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="9592c-110">Knjiženje poreza za troškove unutar kompanije</span><span class="sxs-lookup"><span data-stu-id="9592c-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9592c-111">Prije nego što u svom izvješću o troškovima možete upotrijebiti porezne grupe povezane s pravnom osobom koja posuđuje (izvor) umjesto pravne osobe koja se zadužuje (odredište), morate omogućiti funkciju u postavci poreza na promet Glavne knjige.</span><span class="sxs-lookup"><span data-stu-id="9592c-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="9592c-112">Kada je parametar **Pravna osoba za knjiženje poreza unutar tvrtke** postavljen na **Izvor**, a stavka **Primijeni pravilo oporezivanja poreza na promet** postavljena na **Ne**, upotrebljava se porezna kombinacija za pravnu osobu koja posuđuje.</span><span class="sxs-lookup"><span data-stu-id="9592c-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="9592c-113">Kada je isti parametar postavljen na **Odredište**, koristit će se porezna kombinacija za zaduženu pravnu osobu.</span><span class="sxs-lookup"><span data-stu-id="9592c-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="9592c-114">Za pravne osobe u SAD-u, kada je parametar postavljen na **Izvor**, polje **Potraživanje od poreza na promet** također mora biti konfigurirano na novoj stranici **Grupe za knjiženje u glavnu knjigu**.</span><span class="sxs-lookup"><span data-stu-id="9592c-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="9592c-115">Računovodstveni mehanizam upotrijebit će podatke iz ovog polja za računovodstveno knjiženje u vezi s porezom.</span><span class="sxs-lookup"><span data-stu-id="9592c-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="9592c-116">Ponašanje je u skladu s redcima troškova knjiženim s projektom ili bez njega.</span><span class="sxs-lookup"><span data-stu-id="9592c-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]