---
title: Konfiguracija kategorija projekta
description: U ovoj temi nalaze se informacije o postavljanju kategorija projekta.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131919"
---
# <a name="configure-project-categories"></a><span data-ttu-id="ed563-103">Konfiguracija kategorija projekta</span><span class="sxs-lookup"><span data-stu-id="ed563-103">Configure project categories</span></span>

<span data-ttu-id="ed563-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ed563-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ed563-105">Project Operations pruža snažne mogućnosti za kategorizaciju prihoda i troškova na projektima.</span><span class="sxs-lookup"><span data-stu-id="ed563-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="ed563-106">Kategorije pružaju mogućnost izvješćivanja i analize projektnih transakcija te obavljanje knjiženja u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="ed563-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="ed563-107">Dijagram u nastavku prikazuje povezanost između kategorija transakcija, dijeljenih kategorija i kategorija projekta.</span><span class="sxs-lookup"><span data-stu-id="ed563-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="ed563-108">Kategorije transakcija osnovno su grupiranje za projektne transakcije.</span><span class="sxs-lookup"><span data-stu-id="ed563-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="ed563-109">Unutar tog grupiranja postoji skup dijeljenih kategorija koje se mogu dijeliti između aplikacija i modula.</span><span class="sxs-lookup"><span data-stu-id="ed563-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="ed563-110">Ulazeći još dublje u pojedinosti, kategorije projekta najpodrobnija su razina kategorija.</span><span class="sxs-lookup"><span data-stu-id="ed563-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="ed563-111">Kategorije projekta specifične su za pravnu osobu, modul i aplikaciju.</span><span class="sxs-lookup"><span data-stu-id="ed563-111">Project categories are specific to legal entity, module, and application.</span></span>

![Povezanost između kategorija transakcija, dijeljenih kategorija i kategorija projekta.](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="ed563-113">Kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="ed563-113">Transaction categories</span></span>

<span data-ttu-id="ed563-114">Kategorije transakcija predstavljaju osnovno grupiranje za projektne transakcije i nisu specifične za tvrtku ili vrstu transakcije.</span><span class="sxs-lookup"><span data-stu-id="ed563-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="ed563-115">Na primjer, Contoso Robotics upotrebljava kategorije Dizajn, Putovanje, Instalacija i Uslužne transakcije za grupiranje projektnih transakcija.</span><span class="sxs-lookup"><span data-stu-id="ed563-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="ed563-116">Kategorije transakcija definirane su u modulu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ed563-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="ed563-117">Idite na **Postavke** \> **Kategorije transakcija** kako biste otvorili postavke.</span><span class="sxs-lookup"><span data-stu-id="ed563-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="ed563-118">Stvorite novu kategoriju transakcija bilo odabirom mogućnosti **Nova** ili **Uvoz iz programa Excel**.</span><span class="sxs-lookup"><span data-stu-id="ed563-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="ed563-119">Dijeljene kategorije</span><span class="sxs-lookup"><span data-stu-id="ed563-119">Shared categories</span></span>

<span data-ttu-id="ed563-120">Dynamics 365 upotrebljava koncept dijeljenih kategorija za kategorizaciju troškova u različitim aplikacijama, kao što su Dynamics 365 Finance, Dynamics 365 Supply Chain i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ed563-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="ed563-121">Za svaku stvorenu kategoriju transakcija, Project Operations automatski stvara četiri povezane dijeljene kategorije: Sati, Trošak, Naknade i Stavka.</span><span class="sxs-lookup"><span data-stu-id="ed563-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="ed563-122">Dijeljene kategorije možete pregledati i prilagoditi odlaskom na stavku **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Kategorije** \> **Dijeljene kategorije**.</span><span class="sxs-lookup"><span data-stu-id="ed563-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="ed563-123">Kategorije projekata</span><span class="sxs-lookup"><span data-stu-id="ed563-123">Project categories</span></span>

<span data-ttu-id="ed563-124">Kategorije projekata predstavljaju najpodrobniju razinu konfiguracije kategorija i računovođa projekta mora ih konfigurirati odvojeno i za svaku tvrtku.</span><span class="sxs-lookup"><span data-stu-id="ed563-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="ed563-125">Idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Kategorije** \> **Kategorije projekta**.</span><span class="sxs-lookup"><span data-stu-id="ed563-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="ed563-126">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ed563-126">Select **New**.</span></span>
3. <span data-ttu-id="ed563-127">Odaberite **ID kategorije** dijeljene kategorije koju ste stvorili u prethodnom odjeljku.</span><span class="sxs-lookup"><span data-stu-id="ed563-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="ed563-128">Project Operations omogućuje uporabu samo onih dijeljenih kategorija koje su povezane s kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="ed563-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="ed563-129">Odabir grupe kategorije.</span><span class="sxs-lookup"><span data-stu-id="ed563-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="ed563-130">Grupe kategorije</span><span class="sxs-lookup"><span data-stu-id="ed563-130">Category groups</span></span>

<span data-ttu-id="ed563-131">Grupe kategorija upotrebljavaju se za dijeljenje svojstava, prvenstveno profila knjiženja, između povezanih kategorija projekta.</span><span class="sxs-lookup"><span data-stu-id="ed563-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="ed563-132">Za svaku vrstu transakcije mora postojati najmanje jedna grupa kategorija, a svakoj kategoriji projekta dodjeljuje se grupa.</span><span class="sxs-lookup"><span data-stu-id="ed563-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="ed563-133">Specifikacije knjiženja u aplikaciji Project Operations određene su pravilima profila troškova i prihoda projekta, kategorijama projekata i grupama kategorija.</span><span class="sxs-lookup"><span data-stu-id="ed563-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="ed563-134">Grupe kategorija možete postaviti tako da odete na postavku **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Kategorije** \> **Grupe kategorija**.</span><span class="sxs-lookup"><span data-stu-id="ed563-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
