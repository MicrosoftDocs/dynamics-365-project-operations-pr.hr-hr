---
title: Raspored izdataka upita za savezne nagrade
description: U ovoj temi nalaze se informacije o rasporedu izdataka upita za savezne nagrade.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010057"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b45e7-103">Raspored izdataka upita za savezne nagrade</span><span class="sxs-lookup"><span data-stu-id="b45e7-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b45e7-104">Prema Uredu za upravljanje i proračunskoj uputi A-133, agencije koje primaju savezna sredstva podliježu zahtjevima revizije, koji su poznati i kao pojedinačne revizije.</span><span class="sxs-lookup"><span data-stu-id="b45e7-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="b45e7-105">Postupak revizije upotrebljava se za redovito izvješćivanje o prihodima i rashodima saveznih potpora.</span><span class="sxs-lookup"><span data-stu-id="b45e7-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="b45e7-106">Dio jedinstvenog revizorskog izvješća uključuje Raspored izdataka za savezne nagrade (SEFA).</span><span class="sxs-lookup"><span data-stu-id="b45e7-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="b45e7-107">Raspored izdataka upita za savezne nagrade uključuje naziv i broj Kataloga savezne domaće pomoći (CFDA), broj potpore, godinu dodjele, naziv savezne agencije koja osigurava sredstva i naziv prolaznog entiteta.</span><span class="sxs-lookup"><span data-stu-id="b45e7-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="b45e7-108">Upit se odnosi na određeno razdoblje.</span><span class="sxs-lookup"><span data-stu-id="b45e7-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="b45e7-109">Uobičajeno je da je to razdoblje isto kao i razdoblje financijskog izvješća, koje je poslovna godina.</span><span class="sxs-lookup"><span data-stu-id="b45e7-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="b45e7-110">Upit uključuje potpore koje imaju datume predviđanja u odabranom datumskom rasponu.</span><span class="sxs-lookup"><span data-stu-id="b45e7-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="b45e7-111">Stupac upita **Agencija za davanje potpore** prikazuje klijenta za potporu ili, za prolaznu potporu, agenciju za davanje potpore.</span><span class="sxs-lookup"><span data-stu-id="b45e7-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="b45e7-112">Za prolazne potpore, stupac **Prolazna agencija** prikazuje klijenta potpore.</span><span class="sxs-lookup"><span data-stu-id="b45e7-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="b45e7-113">Ako potpora nije prolazna potpora, stupac **Prolazna agencija** je prazan.</span><span class="sxs-lookup"><span data-stu-id="b45e7-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="b45e7-114">Postavljanje CFDA klastera</span><span class="sxs-lookup"><span data-stu-id="b45e7-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="b45e7-115">Morate postaviti CFDA klastere koji se mogu povezati s CFDA brojevima u Rasporedu izdataka upita za savezne nagrade.</span><span class="sxs-lookup"><span data-stu-id="b45e7-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b45e7-116">Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Katalog klastera savezne domaće pomoći**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="b45e7-117">Odaberite **Novo** za stvaranje CFDA clustera.</span><span class="sxs-lookup"><span data-stu-id="b45e7-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="b45e7-118">Unesite naziv klastera.</span><span class="sxs-lookup"><span data-stu-id="b45e7-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="b45e7-119">Odaberite **Spremi** da biste spremili izmjene.</span><span class="sxs-lookup"><span data-stu-id="b45e7-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="b45e7-120">Postavljanje CFDA brojeva</span><span class="sxs-lookup"><span data-stu-id="b45e7-120">Set up CFDA numbers</span></span>

<span data-ttu-id="b45e7-121">Morate postaviti CFDA brojeve koji se mogu dodati potporama i uključiti u Rasporedu izdataka upita za savezne nagrade.</span><span class="sxs-lookup"><span data-stu-id="b45e7-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b45e7-122">Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Katalog brojeva savezne domaće pomoći**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="b45e7-123">Odaberite **Novi** kako biste stvorili CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="b45e7-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="b45e7-124">U stupac **Broj** unesite CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="b45e7-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="b45e7-125">Pritisni tipku **Tab**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="b45e7-126">U stupac **Opis** unesite CFDA naslov.</span><span class="sxs-lookup"><span data-stu-id="b45e7-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="b45e7-127">Pritisni tipku **Tab**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="b45e7-128">Neobvezno: U polje **Programski klaster** dodajte odgovarajući CFDA klaster.</span><span class="sxs-lookup"><span data-stu-id="b45e7-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="b45e7-129">Odaberite **Spremi** da biste spremili izmjene.</span><span class="sxs-lookup"><span data-stu-id="b45e7-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b45e7-130">Postavljanje potpora na izvješće za Raspored izdataka upita za savezne nagrade</span><span class="sxs-lookup"><span data-stu-id="b45e7-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b45e7-131">Idite na **Upravljanje projektima i računovodstvo \> Potpore \> Potpore** i odaberite postojeću potporu.</span><span class="sxs-lookup"><span data-stu-id="b45e7-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="b45e7-132">Na Brzoj kartici **Postavljanje**, u polju **Katalog savezne domaće pomoći**, dodijelite CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="b45e7-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="b45e7-133">CFDA broj na potpori određuje CFDA klaster za izvješćivanje.</span><span class="sxs-lookup"><span data-stu-id="b45e7-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="b45e7-134">Na Brzoj kartici **Podaci za kontakt** unesite podatke o davatelju potpore slijedeći ove korake:</span><span class="sxs-lookup"><span data-stu-id="b45e7-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="b45e7-135">U polje **Klijent potpore** unesite klijenta koji je odgovoran za potporu.</span><span class="sxs-lookup"><span data-stu-id="b45e7-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="b45e7-136">Za postojeću potporu ovi su podaci možda već unijeti.</span><span class="sxs-lookup"><span data-stu-id="b45e7-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="b45e7-137">Navedite je li klijent potpore donator.</span><span class="sxs-lookup"><span data-stu-id="b45e7-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="b45e7-138">Ako je klijent potpore donator, potvrdni okvir **Prolazni** ostavite prazan.</span><span class="sxs-lookup"><span data-stu-id="b45e7-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="b45e7-139">Ako je drugi klijent donator, a klijent potpore odgovoran je za trošenje i praćenje novca, odaberite potvrdni okvir **Prolazni**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="b45e7-140">Ako ste u prethodnom koraku odabrali potvrdni okvir **Prolazni**, u polju **Agencija za davanje potpore** unesite klijenta koji je dao potporu.</span><span class="sxs-lookup"><span data-stu-id="b45e7-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="b45e7-141">Agencija za davanje potpore i klijent ne mogu biti isti klijent.</span><span class="sxs-lookup"><span data-stu-id="b45e7-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="b45e7-142">Evo primjera prolazne potpore:</span><span class="sxs-lookup"><span data-stu-id="b45e7-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="b45e7-143">Savezna vlada financirala je infrastrukturni projekt za državu.</span><span class="sxs-lookup"><span data-stu-id="b45e7-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="b45e7-144">Savezna vlada dala je novac državi da ga potroši.</span><span class="sxs-lookup"><span data-stu-id="b45e7-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="b45e7-145">U ovom slučaju, savezna vlada je agencija davatelj potpore, a država je klijent potpore.</span><span class="sxs-lookup"><span data-stu-id="b45e7-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="b45e7-146">Kada prvi put uključite značajku, početni CFDA brojevi unosit će se s pomoću postojećih brojeva u potporama.</span><span class="sxs-lookup"><span data-stu-id="b45e7-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="b45e7-147">Isključite potpore iz SEFA izvješća koje se temelji na vrsti potpore</span><span class="sxs-lookup"><span data-stu-id="b45e7-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="b45e7-148">Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Vrste potpora**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="b45e7-149">Na Brzoj kartici **Zadane informacije** odaberite potvrdni okvir **Izuzeti iz rasporeda izdataka za savezne nagrade**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="b45e7-150">Odaberite **Spremi** da biste spremili izmjene.</span><span class="sxs-lookup"><span data-stu-id="b45e7-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b45e7-151">Pokretanje Rasporeda izdataka upita za savezne nagrade</span><span class="sxs-lookup"><span data-stu-id="b45e7-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b45e7-152">Idite na **Upravljanje projektima i računovodstvo \> Upiti i izvješća \> Upit za potporu \> Raspored izdataka za federalne nagrade**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="b45e7-153">U odjeljku **Parametri** slijedite ove korake:</span><span class="sxs-lookup"><span data-stu-id="b45e7-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="b45e7-154">U polju **Datumski interval** odaberite kod za datumski interval.</span><span class="sxs-lookup"><span data-stu-id="b45e7-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="b45e7-155">Alternativno, u poljima **Od datuma** i **Do datuma** definirajte datumski interval.</span><span class="sxs-lookup"><span data-stu-id="b45e7-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="b45e7-156">Neobvezno: Kako biste u upit uključili samo naplaćene transakcije kao prihod, postavite mogućnost **Uključi samo naplaćene prihode** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="b45e7-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="b45e7-157">Stupci</span><span class="sxs-lookup"><span data-stu-id="b45e7-157">Columns</span></span>

<span data-ttu-id="b45e7-158">Raspored izdataka upita za savezne nagrade uključuje sljedeće stupce:</span><span class="sxs-lookup"><span data-stu-id="b45e7-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="b45e7-159">Katalog naziva klastera savezne domaće pomoći</span><span class="sxs-lookup"><span data-stu-id="b45e7-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="b45e7-160">Agencija za davanje potpora</span><span class="sxs-lookup"><span data-stu-id="b45e7-160">Grantor agency</span></span>
- <span data-ttu-id="b45e7-161">Prolazna agencija</span><span class="sxs-lookup"><span data-stu-id="b45e7-161">Pass-through agency</span></span>
- <span data-ttu-id="b45e7-162">Naziv potpore</span><span class="sxs-lookup"><span data-stu-id="b45e7-162">Grant name</span></span>
- <span data-ttu-id="b45e7-163">ID potpore</span><span class="sxs-lookup"><span data-stu-id="b45e7-163">Grant ID</span></span>
- <span data-ttu-id="b45e7-164">ID aplikacije potpore</span><span class="sxs-lookup"><span data-stu-id="b45e7-164">Grant application ID</span></span>
- <span data-ttu-id="b45e7-165">Katalog savezne domaće pomoći</span><span class="sxs-lookup"><span data-stu-id="b45e7-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="b45e7-166">Potvrde</span><span class="sxs-lookup"><span data-stu-id="b45e7-166">Receipts</span></span>
- <span data-ttu-id="b45e7-167">Izdaci</span><span class="sxs-lookup"><span data-stu-id="b45e7-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]