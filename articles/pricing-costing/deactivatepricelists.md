---
title: Deaktiviranje cjenika
description: U ovoj se temi objašnjava kako deaktivirati ili ukloniti neupotrijebljene ili stare cjenike.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701916"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="8eedd-103">Deaktiviranje cjenika</span><span class="sxs-lookup"><span data-stu-id="8eedd-103">Deactivate price lists</span></span> 

<span data-ttu-id="8eedd-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="8eedd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8eedd-105">Za uklanjanje starih ili neupotrijebljenih cjenika iz aplikacije Dynamics 365 Project Operations, morate poduzeti dva koraka.</span><span class="sxs-lookup"><span data-stu-id="8eedd-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="8eedd-106">Uklonite ili izbrišite cjenik s određenih stranica.</span><span class="sxs-lookup"><span data-stu-id="8eedd-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="8eedd-107">Deaktivirajte ili izbrišite cjenik iz Aktivnih cjenika na stranici **Cjenici**.</span><span class="sxs-lookup"><span data-stu-id="8eedd-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="8eedd-108">Morate izvršiti oba koraka kako biste u potpunosti uklonili cjenik.</span><span class="sxs-lookup"><span data-stu-id="8eedd-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="8eedd-109">Nije dovoljno samo izvođenje 2. koraka tj. izravnog brisanja ili deaktiviranja cjenika iz prikaza Aktivni cjenici.</span><span class="sxs-lookup"><span data-stu-id="8eedd-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="8eedd-110">Morate izbrisati i povezanost ovog cjenika sa svim mjestima spomenutim u 1. koraku.</span><span class="sxs-lookup"><span data-stu-id="8eedd-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="8eedd-111">Brisanje cjenika s određenih stranica</span><span class="sxs-lookup"><span data-stu-id="8eedd-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="8eedd-112">Kako biste izbrisali cjenik iz aplikacije Project Operations, idite na sljedeće stranice:</span><span class="sxs-lookup"><span data-stu-id="8eedd-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="8eedd-113">Stranica **Parametri projekta** > kartica **Cjenici**</span><span class="sxs-lookup"><span data-stu-id="8eedd-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="8eedd-114">Stranica **Organizacijska jedinica** > rešetka **Cjenici**</span><span class="sxs-lookup"><span data-stu-id="8eedd-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="8eedd-115">Stranica **Račun** > rešetka **Cjenici projekta**</span><span class="sxs-lookup"><span data-stu-id="8eedd-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="8eedd-116">Stranica **Ponude projekta** > rešetka **Cjenici projekta**: Ovo se primjenjuje na sve aktivne ponude projekta.</span><span class="sxs-lookup"><span data-stu-id="8eedd-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="8eedd-117">Stranica **Ugovori o projektu** > rešetka **Cjenici projekta**: Ovo se primjenjuje na sve aktivne ugovore o projektu.</span><span class="sxs-lookup"><span data-stu-id="8eedd-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="8eedd-118">Za svaku stranicu morate odabrati cjenik koji želite izbrisati, a zatim odaberite **Briši**.</span><span class="sxs-lookup"><span data-stu-id="8eedd-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="8eedd-119">Brisanje ili deaktiviranje cjenika sa stranice Cjenici</span><span class="sxs-lookup"><span data-stu-id="8eedd-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="8eedd-120">Kako biste izbrisali cjenik iz aktivnih cjenika, idite na **Prodajni** > **Klijenti** > **Cjenici**.</span><span class="sxs-lookup"><span data-stu-id="8eedd-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="8eedd-121">Odaberite cjenik koji želite izbrisati i zatim odaberite **Briši**.</span><span class="sxs-lookup"><span data-stu-id="8eedd-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="8eedd-122">Ako se cjenik navodi na nekoj postojećoj transakciji, nećete ga moći izbrisati.</span><span class="sxs-lookup"><span data-stu-id="8eedd-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="8eedd-123">Ako se to dogodi, možete deaktivirati cjenik tako da se ne prikazuje ni u jednom prikazu.</span><span class="sxs-lookup"><span data-stu-id="8eedd-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="8eedd-124">Kako biste deaktivirali cjenik, ponovno odaberite cjenik, a zatim odaberite **Deaktiviraj**.</span><span class="sxs-lookup"><span data-stu-id="8eedd-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
