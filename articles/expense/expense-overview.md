---
title: Pregled izdatka
description: U ovoj temi nalaze se informacije o funkcioniranju troška u aplikaciji Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 921df6fa8f1eb33bd01792c0b7c787fc74604adf
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368557"
---
# <a name="expense-home-page"></a><span data-ttu-id="7dfc7-103">Početna stranica troška</span><span class="sxs-lookup"><span data-stu-id="7dfc7-103">Expense home page</span></span>

<span data-ttu-id="7dfc7-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="7dfc7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7dfc7-105">Dynamics 365 Project Operations podržava mogućnost obrade troškova.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="7dfc7-106">Obrada troškova događa se s projektima ili bez njih uporabom prilagodljivog tijeka rada pravila, kategorija transakcija i odobrenja.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="7dfc7-107">U aplikaciji Project Operations postoje dva podržana modela implementacije troška:</span><span class="sxs-lookup"><span data-stu-id="7dfc7-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="7dfc7-108">**Potpuno**: Dostupno je potpuno raspoređivanje za **Project Operations za scenarije koji se temelje na resursima / bez zaliha** ili **Project Operations za scenarije koji se temelje na proizvodnim nalozima**.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="7dfc7-109">**Osnovno**: Osnovna implementacija dostupna je za **Project Operations za scenarije koji se temelje na resursima / bez zaliha** i **Jednostavna implementacija – od sklapanja posla do predračuna**.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="7dfc7-110">Potpuni</span><span class="sxs-lookup"><span data-stu-id="7dfc7-110">Full</span></span> 
<span data-ttu-id="7dfc7-111">Potpuna implementacija troška omogućuje cjelovitu provedbu pravila koja obuhvaća i mogućnost stvaranja pravila, kao što su:</span><span class="sxs-lookup"><span data-stu-id="7dfc7-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="7dfc7-112">Ograničenja kategorija troška</span><span class="sxs-lookup"><span data-stu-id="7dfc7-112">Expense category limits</span></span>
  - <span data-ttu-id="7dfc7-113">Putovanja</span><span class="sxs-lookup"><span data-stu-id="7dfc7-113">Travel</span></span>
  - <span data-ttu-id="7dfc7-114">Po danu</span><span class="sxs-lookup"><span data-stu-id="7dfc7-114">Per diem</span></span>
  - <span data-ttu-id="7dfc7-115">Uvoze kreditnih kartica</span><span class="sxs-lookup"><span data-stu-id="7dfc7-115">Credit card imports</span></span>
  - <span data-ttu-id="7dfc7-116">Primitak optičkog prepoznavanja znakova</span><span class="sxs-lookup"><span data-stu-id="7dfc7-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="7dfc7-117">Osnovno</span><span class="sxs-lookup"><span data-stu-id="7dfc7-117">Basic</span></span> 
<span data-ttu-id="7dfc7-118">Scenarij implementacije osnovnih troškova omogućuje vam samo bilježenje osnovnih troškova u odnosu na projekt.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="7dfc7-119">Dodatne informacije potražite u odjeljku [Unos troška (jednostavno)](basic-expense.md).</span><span class="sxs-lookup"><span data-stu-id="7dfc7-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="7dfc7-120">Određivanje implementacije troška</span><span class="sxs-lookup"><span data-stu-id="7dfc7-120">Determine your Expense deployment</span></span>
<span data-ttu-id="7dfc7-121">Kako biste utvrdili upotrebljavate li implementaciju upravljanja osnovnim troškovima, provjerite završava li URL adresa sljedećim izrazom **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="7dfc7-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]