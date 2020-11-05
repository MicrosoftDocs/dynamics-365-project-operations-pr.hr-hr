---
title: Međukompanijski troškovi
description: Radnik koji je zaposlen u jednoj pravnoj osobi u tvrtki ili ustanovi može obavljati posao za drugu pravnu osobu u istoj tvrtki ili ustanovi. U ovoj situaciji možete koristiti značajku troškova unutar tvrtke kako biste troškove radnika dodijelili pravnoj osobi za koju je posao obavljen.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073539"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="f1da6-104">Međukompanijski troškovi</span><span class="sxs-lookup"><span data-stu-id="f1da6-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1da6-105">Radnik koji je zaposlen u jednoj pravnoj osobi u tvrtki ili ustanovi može obavljati posao za drugu pravnu osobu u istoj tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="f1da6-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="f1da6-106">U ovoj situaciji možete koristiti značajku troškova unutar tvrtke kako biste troškove radnika dodijelili pravnoj osobi za koju je posao obavljen.</span><span class="sxs-lookup"><span data-stu-id="f1da6-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="f1da6-107">Pravna osoba koja zapošljava radnika naziva se pravnom osobom koja posuđuje.</span><span class="sxs-lookup"><span data-stu-id="f1da6-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="f1da6-108">Pravna osoba kojoj radnik stvara troškove naziva se pravnom osobom koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="f1da6-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="f1da6-109">Prije nego što radnik može stvoriti i poslati troškove za rad koji se obavlja za drugu pravnu osobu, u pravnoj osobi koja posuđuje, na stranici **Parametri upravljanja troškovima** odaberite mogućnost **Omogući retke troška unutar tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="f1da6-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="f1da6-110">Knjiženje poreza za troškove unutar kompanije</span><span class="sxs-lookup"><span data-stu-id="f1da6-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1da6-111">Ako želite upotrebljavati porezne grupe koje su povezane s pravnom osobom koja posuđuje (izvor) umjesto pravne osobe koja se zadužuje (odredište), u svom izvješću o troškovima morat ćete to konfigurirati u postavkama PDV-a u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="f1da6-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="f1da6-112">Kada parametar **Pravna osoba za knjiženje poreza unutar kompanije** glavne knjige postavljen na **Izvor** , a **Primijeni pravila oporezivanja PDV-om** postavljen na **Ne** , upotrijebit će se porezna kombinacija za pravnu osobu koja posuđuje.</span><span class="sxs-lookup"><span data-stu-id="f1da6-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="f1da6-113">Kada je isti parametar postavljen na **Odredište** , koristit će se porezna kombinacija za zaduženu pravnu osobu.</span><span class="sxs-lookup"><span data-stu-id="f1da6-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="f1da6-114">Za pravne osobe u SAD-u, kada je parametar postavljen na **Izvor** , polje **Potraživanje od poreza na promet** također mora biti konfigurirano na novoj stranici **Grupe za knjiženje u glavnu knjigu**.</span><span class="sxs-lookup"><span data-stu-id="f1da6-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="f1da6-115">Računovodstveni mehanizam upotrijebit će podatke iz ovog polja za računovodstveno knjiženje u vezi s porezom.</span><span class="sxs-lookup"><span data-stu-id="f1da6-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="f1da6-116">Ponašanje je u skladu s redcima troškova knjiženim s projektom ili bez njega.</span><span class="sxs-lookup"><span data-stu-id="f1da6-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
