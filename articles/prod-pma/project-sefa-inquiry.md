---
title: Raspored izdataka upita za savezne nagrade
description: U ovoj temi nalaze se informacije o rasporedu izdataka upita za savezne nagrade.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073372"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d323a-103">Raspored izdataka upita za savezne nagrade</span><span class="sxs-lookup"><span data-stu-id="d323a-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d323a-104">Prema Uredu za upravljanje i proračunskoj uputi A-133, agencije koje primaju savezna sredstva podliježu zahtjevima revizije, koji su poznati i kao pojedinačne revizije.</span><span class="sxs-lookup"><span data-stu-id="d323a-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="d323a-105">Postupak revizije upotrebljava se za redovito izvješćivanje o prihodima i rashodima saveznih potpora.</span><span class="sxs-lookup"><span data-stu-id="d323a-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="d323a-106">Dio jedinstvenog revizorskog izvješća uključuje Raspored izdataka za savezne nagrade (SEFA).</span><span class="sxs-lookup"><span data-stu-id="d323a-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="d323a-107">Raspored izdataka upita za savezne nagrade uključuje naziv i broj Kataloga savezne domaće pomoći (CFDA), broj potpore, godinu dodjele, naziv savezne agencije koja osigurava sredstva i naziv prolaznog entiteta.</span><span class="sxs-lookup"><span data-stu-id="d323a-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="d323a-108">Upit se odnosi na određeno razdoblje.</span><span class="sxs-lookup"><span data-stu-id="d323a-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="d323a-109">Uobičajeno je da je to razdoblje isto kao i razdoblje financijskog izvješća, koje je poslovna godina.</span><span class="sxs-lookup"><span data-stu-id="d323a-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="d323a-110">Upit uključuje potpore koje imaju datume predviđanja u odabranom datumskom rasponu.</span><span class="sxs-lookup"><span data-stu-id="d323a-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="d323a-111">Stupac upita **Agencija za davanje potpore** prikazuje klijenta za potporu ili, za prolaznu potporu, agenciju za davanje potpore.</span><span class="sxs-lookup"><span data-stu-id="d323a-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="d323a-112">Za prolazne potpore, stupac **Prolazna agencija** prikazuje klijenta potpore.</span><span class="sxs-lookup"><span data-stu-id="d323a-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="d323a-113">Ako potpora nije prolazna potpora, stupac **Prolazna agencija** je prazan.</span><span class="sxs-lookup"><span data-stu-id="d323a-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="d323a-114">Postavljanje CFDA klastera</span><span class="sxs-lookup"><span data-stu-id="d323a-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="d323a-115">Morate postaviti CFDA klastere koji se mogu povezati s CFDA brojevima u Rasporedu izdataka upita za savezne nagrade.</span><span class="sxs-lookup"><span data-stu-id="d323a-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d323a-116">Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Katalog klastera savezne domaće pomoći**.</span><span class="sxs-lookup"><span data-stu-id="d323a-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="d323a-117">Odaberite **Novo** za stvaranje CFDA clustera.</span><span class="sxs-lookup"><span data-stu-id="d323a-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="d323a-118">Unesite naziv klastera.</span><span class="sxs-lookup"><span data-stu-id="d323a-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="d323a-119">Odaberite **Spremi** da biste spremili izmjene.</span><span class="sxs-lookup"><span data-stu-id="d323a-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="d323a-120">Postavljanje CFDA brojeva</span><span class="sxs-lookup"><span data-stu-id="d323a-120">Set up CFDA numbers</span></span>

<span data-ttu-id="d323a-121">Morate postaviti CFDA brojeve koji se mogu dodati potporama i uključiti u Rasporedu izdataka upita za savezne nagrade.</span><span class="sxs-lookup"><span data-stu-id="d323a-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d323a-122">Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Katalog brojeva savezne domaće pomoći**.</span><span class="sxs-lookup"><span data-stu-id="d323a-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="d323a-123">Odaberite **Novi** kako biste stvorili CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="d323a-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="d323a-124">U stupac **Broj** unesite CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="d323a-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="d323a-125">Pritisni tipku **Tab**.</span><span class="sxs-lookup"><span data-stu-id="d323a-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="d323a-126">U stupac **Opis** unesite CFDA naslov.</span><span class="sxs-lookup"><span data-stu-id="d323a-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="d323a-127">Pritisni tipku **Tab**.</span><span class="sxs-lookup"><span data-stu-id="d323a-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="d323a-128">Neobvezno: U polje **Programski klaster** dodajte odgovarajući CFDA klaster.</span><span class="sxs-lookup"><span data-stu-id="d323a-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="d323a-129">Odaberite **Spremi** da biste spremili izmjene.</span><span class="sxs-lookup"><span data-stu-id="d323a-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d323a-130">Postavljanje potpora na izvješće za Raspored izdataka upita za savezne nagrade</span><span class="sxs-lookup"><span data-stu-id="d323a-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d323a-131">Idite na **Upravljanje projektima i računovodstvo \> Potpore \> Potpore** i odaberite postojeću potporu.</span><span class="sxs-lookup"><span data-stu-id="d323a-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="d323a-132">Na Brzoj kartici **Postavljanje** , u polju **Katalog savezne domaće pomoći** , dodijelite CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="d323a-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="d323a-133">CFDA broj na potpori određuje CFDA klaster za izvješćivanje.</span><span class="sxs-lookup"><span data-stu-id="d323a-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="d323a-134">Na Brzoj kartici **Podaci za kontakt** unesite podatke o davatelju potpore slijedeći ove korake:</span><span class="sxs-lookup"><span data-stu-id="d323a-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="d323a-135">U polje **Klijent potpore** unesite klijenta koji je odgovoran za potporu.</span><span class="sxs-lookup"><span data-stu-id="d323a-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="d323a-136">Za postojeću potporu ovi su podaci možda već unijeti.</span><span class="sxs-lookup"><span data-stu-id="d323a-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="d323a-137">Navedite je li klijent potpore donator.</span><span class="sxs-lookup"><span data-stu-id="d323a-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="d323a-138">Ako je klijent potpore donator, potvrdni okvir **Prolazni** ostavite prazan.</span><span class="sxs-lookup"><span data-stu-id="d323a-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="d323a-139">Ako je drugi klijent donator, a klijent potpore odgovoran je za trošenje i praćenje novca, odaberite potvrdni okvir **Prolazni**.</span><span class="sxs-lookup"><span data-stu-id="d323a-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="d323a-140">Ako ste u prethodnom koraku odabrali potvrdni okvir **Prolazni** , u polju **Agencija za davanje potpore** unesite klijenta koji je dao potporu.</span><span class="sxs-lookup"><span data-stu-id="d323a-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="d323a-141">Agencija za davanje potpore i klijent ne mogu biti isti klijent.</span><span class="sxs-lookup"><span data-stu-id="d323a-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="d323a-142">Evo primjera prolazne potpore:</span><span class="sxs-lookup"><span data-stu-id="d323a-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="d323a-143">Savezna vlada financirala je infrastrukturni projekt za državu.</span><span class="sxs-lookup"><span data-stu-id="d323a-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="d323a-144">Savezna vlada dala je novac državi da ga potroši.</span><span class="sxs-lookup"><span data-stu-id="d323a-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="d323a-145">U ovom slučaju, savezna vlada je agencija davatelj potpore, a država je klijent potpore.</span><span class="sxs-lookup"><span data-stu-id="d323a-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="d323a-146">Kada prvi put uključite značajku, početni CFDA brojevi unosit će se s pomoću postojećih brojeva u potporama.</span><span class="sxs-lookup"><span data-stu-id="d323a-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="d323a-147">Isključite potpore iz SEFA izvješća koje se temelji na vrsti potpore</span><span class="sxs-lookup"><span data-stu-id="d323a-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="d323a-148">Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Vrste potpora**.</span><span class="sxs-lookup"><span data-stu-id="d323a-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="d323a-149">Na Brzoj kartici **Zadane informacije** odaberite potvrdni okvir **Izuzeti iz rasporeda izdataka za savezne nagrade**.</span><span class="sxs-lookup"><span data-stu-id="d323a-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="d323a-150">Odaberite **Spremi** da biste spremili izmjene.</span><span class="sxs-lookup"><span data-stu-id="d323a-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d323a-151">Pokretanje Rasporeda izdataka upita za savezne nagrade</span><span class="sxs-lookup"><span data-stu-id="d323a-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d323a-152">Idite na **Upravljanje projektima i računovodstvo \> Upiti i izvješća \> Upit za potporu \> Raspored izdataka za federalne nagrade**.</span><span class="sxs-lookup"><span data-stu-id="d323a-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="d323a-153">U odjeljku **Parametri** slijedite ove korake:</span><span class="sxs-lookup"><span data-stu-id="d323a-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="d323a-154">U polju **Datumski interval** odaberite kod za datumski interval.</span><span class="sxs-lookup"><span data-stu-id="d323a-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="d323a-155">Alternativno, u poljima **Od datuma** i **Do datuma** definirajte datumski interval.</span><span class="sxs-lookup"><span data-stu-id="d323a-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="d323a-156">Neobvezno: Kako biste u upit uključili samo naplaćene transakcije kao prihod, postavite mogućnost **Uključi samo naplaćene prihode** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="d323a-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="d323a-157">Stupci</span><span class="sxs-lookup"><span data-stu-id="d323a-157">Columns</span></span>

<span data-ttu-id="d323a-158">Raspored izdataka upita za savezne nagrade uključuje sljedeće stupce:</span><span class="sxs-lookup"><span data-stu-id="d323a-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="d323a-159">Katalog naziva klastera savezne domaće pomoći</span><span class="sxs-lookup"><span data-stu-id="d323a-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="d323a-160">Agencija za davanje potpora</span><span class="sxs-lookup"><span data-stu-id="d323a-160">Grantor agency</span></span>
- <span data-ttu-id="d323a-161">Prolazna agencija</span><span class="sxs-lookup"><span data-stu-id="d323a-161">Pass-through agency</span></span>
- <span data-ttu-id="d323a-162">Naziv potpore</span><span class="sxs-lookup"><span data-stu-id="d323a-162">Grant name</span></span>
- <span data-ttu-id="d323a-163">ID potpore</span><span class="sxs-lookup"><span data-stu-id="d323a-163">Grant ID</span></span>
- <span data-ttu-id="d323a-164">ID aplikacije potpore</span><span class="sxs-lookup"><span data-stu-id="d323a-164">Grant application ID</span></span>
- <span data-ttu-id="d323a-165">Katalog savezne domaće pomoći</span><span class="sxs-lookup"><span data-stu-id="d323a-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="d323a-166">Potvrde</span><span class="sxs-lookup"><span data-stu-id="d323a-166">Receipts</span></span>
- <span data-ttu-id="d323a-167">Izdaci</span><span class="sxs-lookup"><span data-stu-id="d323a-167">Expenditures</span></span>
