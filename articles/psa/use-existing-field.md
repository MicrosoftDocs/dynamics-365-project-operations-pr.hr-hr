---
title: Korištenje postojećeg polja u aplikaciji Project Service kao dimenzije određivanja cijena
description: Ova tema pruža informacije o korištenju postojećih polja u aplikaciji Project Service kao dimenzija određivanja cijena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281559"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="25c7d-103">Korištenje postojećeg polja u aplikaciji Project Service kao dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="25c7d-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="25c7d-104">Project Service Automation (PSA) ima mnogo polja u entitetu **Stvarni podaci** koja se mogu koristiti kao dimenzije određivanja cijena za određivanje cijene na temelju resursa u tvrtkama ili ustanovama projekta.</span><span class="sxs-lookup"><span data-stu-id="25c7d-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="25c7d-105">Na primjer, uobičajeno je polje **Resurs koji se može rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="25c7d-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="25c7d-106">Manje tvrtke koje imaju manje od 20 do 30 naplativih resursa mogu otkriti da je korištenje računa i stopa troškova specifičnih za svaki resurs jednostavniji pristup.</span><span class="sxs-lookup"><span data-stu-id="25c7d-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="25c7d-107">Budući da se naplativa radna snaga povećava, posebne bi cijene mogle postati nerealne za održavanje jer trošak resursa i cijene naplate počinju varirati kako se resursi unapređuju, stječu više iskustva ili različite skupove vještina.</span><span class="sxs-lookup"><span data-stu-id="25c7d-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="25c7d-108">Budući da je taj pristup i dalje dobar za tvrtke određene veličine, pogledajte odjeljak [Uporaba resursa koji se može rezervirati kao veličine za određivanje cijene](bookable-resource-pricing-dimension.md) kako biste razumjeli kako se postojeće polje aplikacije Project Service može upotrebljavati kao veličina za određivanje cijene.</span><span class="sxs-lookup"><span data-stu-id="25c7d-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="25c7d-109">Drugi je primjer kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="25c7d-109">Another example is that of transaction category.</span></span> <span data-ttu-id="25c7d-110">Klijenti i implementatori koristili su kategoriju transakcije u aplikaciji PSA da klasificiraju rad i koriste polje do cijene i troška na temelju kategorije rada.</span><span class="sxs-lookup"><span data-stu-id="25c7d-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="25c7d-111">Za dodatne informacije pogledajte članak [Korištenje kategorije transakcije kao dimenzije određivanja cijena](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="25c7d-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]