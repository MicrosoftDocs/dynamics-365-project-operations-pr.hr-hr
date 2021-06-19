---
title: Polja aplikacije Project Operations kao cjenovne veličine
description: U ovoj temi nalaze se informacije o uporabi polja kao veličinama za određivanje cijena u aplikaciji Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004477"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="eb1c6-103">Polja aplikacije Project Operations kao veličine za određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="eb1c6-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="eb1c6-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="eb1c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb1c6-105">Entitet **Stvarni podaci** ima mnoga polja koja se mogu upotrijebiti kao cjenovne veličine za cijene utemeljene na resursima.</span><span class="sxs-lookup"><span data-stu-id="eb1c6-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="eb1c6-106">Na primjer, uobičajeno je polje **Resurs koji se može rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="eb1c6-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="eb1c6-107">Manje tvrtke koje imaju manje od 20 do 30 naplativih resursa mogu otkriti da je korištenje računa i stopa troškova specifičnih za svaki resurs jednostavniji pristup.</span><span class="sxs-lookup"><span data-stu-id="eb1c6-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="eb1c6-108">Međutim, kako raste naplativa radna snaga, održavanje cijena specifičnih za resurse može postati nerealno.</span><span class="sxs-lookup"><span data-stu-id="eb1c6-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="eb1c6-109">Trošak resursa i cijene računa počinju se mijenjati kako se resursi unaprjeđuju, stječu više iskustva ili drugačiji skup vještina.</span><span class="sxs-lookup"><span data-stu-id="eb1c6-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="eb1c6-110">Drugi je primjer kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="eb1c6-110">Another example is that of transaction category.</span></span> <span data-ttu-id="eb1c6-111">Klijenti i implementatori upotrebljavali su kategoriju transakcije kako bi klasificirali rad i upotrijebili polje za cijenu i trošak na temelju kategorije rada.</span><span class="sxs-lookup"><span data-stu-id="eb1c6-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]