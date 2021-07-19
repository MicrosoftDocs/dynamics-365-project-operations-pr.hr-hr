---
title: Izvedba prijedloga fakture za projekt
description: U ovoj temi nalaze se informacije o poboljšanjima izvedbe prijedloga faktura za projekt.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269781"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="fc68f-103">Izvedba prijedloga fakture za projekt</span><span class="sxs-lookup"><span data-stu-id="fc68f-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc68f-104">Kada izrađujete novi prijedlog fakture, mogli biste naići na probleme s izvedbom kako se povećava broj projekata i potprojekata.</span><span class="sxs-lookup"><span data-stu-id="fc68f-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="fc68f-105">Kako bi se poboljšala izvedba, dostupna je značajka koja smanjuje vrijeme potrebno za stvaranje novog prijedloga fakture za knjižene projektnih transakcija.</span><span class="sxs-lookup"><span data-stu-id="fc68f-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="fc68f-106">Omogućivanje poboljšanja izvedbe prijedloga fakture za projekt</span><span class="sxs-lookup"><span data-stu-id="fc68f-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="fc68f-107">Kako biste omogućili značajku poboljšanja izvedbe prijedloga fakture za projekt, poduzmite korake u nastavku.</span><span class="sxs-lookup"><span data-stu-id="fc68f-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="fc68f-108">Idite na **Upravljanje značajkama** > **Sve**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="fc68f-109">Na popisu značajki pronađite **Poboljšanje izvedbe prijedloga fakture za projekt**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="fc68f-110">Odaberite **Omogući odmah**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="fc68f-111">Osvježite svoj preglednik, a zatim stvorite novi prijedlog fakture.</span><span class="sxs-lookup"><span data-stu-id="fc68f-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="fc68f-112">Isključivanje poboljšanja izvedbe prijedloga fakture za projekt</span><span class="sxs-lookup"><span data-stu-id="fc68f-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="fc68f-113">Kako biste isključili značajku poboljšanja izvedbe prijedloga fakture za projekt, poduzmite korake u nastavku.</span><span class="sxs-lookup"><span data-stu-id="fc68f-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="fc68f-114">Idite na **Upravljanje značajkama** > **Sve**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="fc68f-115">Na popisu značajki pronađite **Poboljšanje izvedbe prijedloga fakture za projekt**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="fc68f-116">Odaberite **Onemogući**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="fc68f-117">Osvježite preglednik.</span><span class="sxs-lookup"><span data-stu-id="fc68f-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="fc68f-118">Izvedba prijedloga fakture ne može se primijeniti kada su omogućena pravila naplate.</span><span class="sxs-lookup"><span data-stu-id="fc68f-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="fc68f-119">Tijekom skupnog postupka izrade prijedloga faktura, broj podzadataka podijelit će zadatke na maksimalni broj na temelju broja ugovora s transakcijama koje je moguće fakturirati, bez obzira na to što ste unijeli.</span><span class="sxs-lookup"><span data-stu-id="fc68f-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="fc68f-120">Na primjer, ako unesete **3** za broj podzadataka za stvaranje prijedloga fakture u skupu, a postoje samo dva ugovora s transakcijama koje je moguće fakturirati, stvaraju se samo dva podzadatka.</span><span class="sxs-lookup"><span data-stu-id="fc68f-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
