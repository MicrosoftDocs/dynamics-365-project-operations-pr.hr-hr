---
title: Korištenje postojećeg polja u aplikaciji Project Service kao dimenzije određivanja cijena
description: Ova tema pruža informacije o korištenju postojećih polja u aplikaciji Project Service kao dimenzija određivanja cijena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750131"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="bfc50-103">Korištenje postojećeg polja u aplikaciji Project Service kao dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="bfc50-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="bfc50-104">Project Service Automation (PSA) ima mnogo polja u entitetu **Stvarni podaci** koja se mogu koristiti kao dimenzije određivanja cijena za određivanje cijene na temelju resursa u tvrtkama ili ustanovama projekta.</span><span class="sxs-lookup"><span data-stu-id="bfc50-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="bfc50-105">Na primjer, uobičajeno je polje **Resurs koji se može rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="bfc50-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="bfc50-106">Manje tvrtke koje imaju manje od 20 do 30 naplativih resursa mogu otkriti da je korištenje računa i stopa troškova specifičnih za svaki resurs jednostavniji pristup.</span><span class="sxs-lookup"><span data-stu-id="bfc50-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="bfc50-107">Budući da se naplativa radna snaga povećava, to bi moglo postati nerealno za održavanje jer trošak resursa i stope računa počinju varirati kako se resursi unapređuju, stječu više iskustva ili različite skupove vještina.</span><span class="sxs-lookup"><span data-stu-id="bfc50-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="bfc50-108">Budući da je taj pristup i dalje dobar za tvrtke određene veličine, pogledajte temu [Korištenje resursa koji se može rezervirati kao dimenzije određivanja cijena](bookable-resource-pricing-dimension.md) da biste razumjeli kako se postojeće polje aplikacije Project Service može koristiti kao dimenzija određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="bfc50-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="bfc50-109">Drugi je primjer kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="bfc50-109">Another example is that of transaction category.</span></span> <span data-ttu-id="bfc50-110">Klijenti i implementatori koristili su kategoriju transakcije u aplikaciji PSA da klasificiraju rad i koriste polje do cijene i troška na temelju kategorije rada.</span><span class="sxs-lookup"><span data-stu-id="bfc50-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="bfc50-111">Za dodatne informacije pogledajte članak [Korištenje kategorije transakcije kao dimenzije određivanja cijena](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="bfc50-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
