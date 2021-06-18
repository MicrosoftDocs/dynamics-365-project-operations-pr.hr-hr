---
title: Konfiguriranje integracije aplikacije Project Operations po pravnoj osobi
description: U ovoj temi nalaze se informacije o postavljanju integracije po pravnoj osobi u aplikaciji Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000067"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="79db5-103">Konfiguriranje integracije aplikacije Project Operations po pravnoj osobi</span><span class="sxs-lookup"><span data-stu-id="79db5-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="79db5-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="79db5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="79db5-105">U ovoj temi prolazite korake potrebne za konfiguriranje aplikacije Dynamics 365 Project Operations po pravnoj osobi.</span><span class="sxs-lookup"><span data-stu-id="79db5-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="79db5-106">Omogućivanje tipki značajki u aplikaciji Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="79db5-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="79db5-107">Poduzmite sljedeće korake kako biste omogućili potrebne značajke.</span><span class="sxs-lookup"><span data-stu-id="79db5-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="79db5-108">U aplikaciji Dynamics 365 Finance, idite na radni prostor **Upravljanje značajkama**.</span><span class="sxs-lookup"><span data-stu-id="79db5-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="79db5-109">U mogućnosti **Popis značajki** pronađite i omogućite sljedeće značajke:</span><span class="sxs-lookup"><span data-stu-id="79db5-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="79db5-110">**Omogući više redaka ugovora za projekt**</span><span class="sxs-lookup"><span data-stu-id="79db5-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="79db5-111">**Omogući aplikaciju Project Operations u sustavu Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="79db5-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="79db5-112">Ako ne vidite popis **Tipke značajki** provjerite ispunjava li vaša verzija programa Financije minimalni preduvjet (verzija aplikacije 10.0.13 sa svim primijenjenim kvalitativnim ažuriranjima ili novija).</span><span class="sxs-lookup"><span data-stu-id="79db5-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="79db5-113">Odaberite **Provjeri ima li ažuriranja** za osvježavanje popisa značajki.</span><span class="sxs-lookup"><span data-stu-id="79db5-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="79db5-114">Definirajte scenarij implementacije aplikacije Project Operations za pravnu osobu</span><span class="sxs-lookup"><span data-stu-id="79db5-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="79db5-115">Project Operations možete omogućiti u sustavu Dynamics 365 Customer Engagement na razini pravne osobe.</span><span class="sxs-lookup"><span data-stu-id="79db5-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="79db5-116">Možete imati jednu pravnu osobu koja upotrebljava aplikaciju Project Operations u sutavu Dynamics 365 Customer Engagement za scenarije temeljene na resursima / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="79db5-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="79db5-117">U istom okruženju možete imati drugu pravnu osobu koja upotrebljava aplikaciju Project Operations za scenarije na zalihi / proizvodni nalog.</span><span class="sxs-lookup"><span data-stu-id="79db5-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="79db5-118">U aplikaciji Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Parametri upravljanja projektom i računovodstva**.</span><span class="sxs-lookup"><span data-stu-id="79db5-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="79db5-119">Na popisu dostupnih pravnih osoba odaberite entitete u kojima će biti omogućeno više redaka ugovora i značajki rješenja Project Operations u aplikaciji Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="79db5-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="79db5-120">Ostavite neodabrane pravne osobe koje će upotrebljavati aplikaciju Project Operations za scenarije na zalihi / proizvodni nalog.</span><span class="sxs-lookup"><span data-stu-id="79db5-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="79db5-121">Pravna osoba može se odabrati samo ako nema postojeće projekte.</span><span class="sxs-lookup"><span data-stu-id="79db5-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="79db5-122">Parametri konfiguracije Upravljanja projektom i računovodstva</span><span class="sxs-lookup"><span data-stu-id="79db5-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="79db5-123">Svaka pravna osoba koja upotrebljava aplikaciju Project Operations u sustavu Dynamics 365 Customer Engagement treba skup zadanih parametara.</span><span class="sxs-lookup"><span data-stu-id="79db5-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="79db5-124">Ovi su parametri konfigurirani na kartici **Projektne operacije** na stranici **Parametri Upravljanja projektom i računovodstva**.</span><span class="sxs-lookup"><span data-stu-id="79db5-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="79db5-125">Parametri su sljedeći:</span><span class="sxs-lookup"><span data-stu-id="79db5-125">The parameters are:</span></span>

  - <span data-ttu-id="79db5-126">**Zadane postavke vrste naplate**: Project Operations upotrebljava fiksni skup zadanih postavki vrsta naplate koje se moraju mapirati u svojstva retka aplikacije Financije.</span><span class="sxs-lookup"><span data-stu-id="79db5-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="79db5-127">Stvorite zapis za svaku vrstu naplate: **Nije specificirano**, **Naplativo**, **Nenaplativo**, **Besplatno** i **Nedostupno**.</span><span class="sxs-lookup"><span data-stu-id="79db5-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="79db5-128">**Zadane postavke kategorije projekta** : Odaberite zadane kategorije projekata koje će se upotrebljavati za svaku vrstu transakcije.</span><span class="sxs-lookup"><span data-stu-id="79db5-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="79db5-129">Te će se zadane postavke upotrebljavati u stavci **Dnevnik integracije aplikacije Project Operations** i u procjenama kada za stvarni projekt nije navedena kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="79db5-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="79db5-130">**Predviđanja**: Odaberite model predviđanja koji će se upotrebljavati za procjenu vremena i troškova.</span><span class="sxs-lookup"><span data-stu-id="79db5-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]