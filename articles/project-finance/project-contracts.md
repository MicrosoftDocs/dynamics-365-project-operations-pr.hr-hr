---
title: Ugovori o projektu
description: U ovoj temi daju se primjeri ugovora o projektu koje možete stvoriti za razne vrste projekata i izvore financiranja, kao i način na koji možete upravljati ugovorima i fakturirati klijentima projekta.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750155"
---
# <a name="project-contracts"></a><span data-ttu-id="b0eb7-103">Ugovori o projektu</span><span class="sxs-lookup"><span data-stu-id="b0eb7-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0eb7-104">U ovom članku daju se primjeri ugovora o projektu koje možete stvoriti za razne vrste projekata i izvore financiranja, kao i način na koji možete upravljati ugovorima i fakturirati klijentima projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="b0eb7-105">Vrsta projekta za koji stvarate ugovor o projektu određuje način fakturiranja projekta klijentima.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="b0eb7-106">Možete promijeniti ugovor o projektu i povezani projekt, ali ne možete promijeniti vrstu projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="b0eb7-107">Uporabom ugovora o projektu istodobno možete fakturirati jedan ili više projekata.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="b0eb7-108">Ugovor o projektu također pomaže u jamčenju dosljednog postupka fakturiranja za svaki potprojekt u strukturi projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="b0eb7-109">Svaki projekt koji će se fakturirati mora biti povezan s ugovorom o projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="b0eb7-110">Postavke za ugovor o projektu primjenjuju se na sve projekte i potprojekte koji su povezani s tim ugovorom o projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="b0eb7-111">U ugovoru o projektu može se navesti jedan ili više izvora financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="b0eb7-112">Stoga možete podijeliti naplatu između više davatelja sredstava, postaviti ograničenja financiranja tako da se izvorima financiranja ne naplaćuje više od određenog iznosa i konfigurirati pravila financiranja za naplatu izdataka.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="b0eb7-113">Financiranje ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="b0eb7-113">Funding for project contracts</span></span>
<span data-ttu-id="b0eb7-114">Neki projektni ugovori određuju da više strana dijeli odgovornost za financiranje troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="b0eb7-115">Evo nekoliko primjera:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-115">Here are some examples:</span></span>

-   <span data-ttu-id="b0eb7-116">Veliki klijent koji ima više sektora zahtijeva da se financiranje projekta podijeli po odjelima.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="b0eb7-117">Vaša tvrtka dijeli troškove velikog projekta s vanjskom tvrtkom ili ustanovom.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="b0eb7-118">Projekt ceste sufinanciraju dvije općine.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="b0eb7-119">Projekt mosta financira se iz državne potpore i privatne korporacije.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="b0eb7-120">U aplikaciji Dynamics 365 Finance možete podijeliti naplatu za jednu transakciju ili cijeli projekt između više klijenata, potpora te tvrtki ili ustanova.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="b0eb7-121">U projektima koji imaju više davatelja sredstava, sve strane koje pridonose financiranju naprednog projekta financiranja nazivaju se izvorima financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="b0eb7-122">Nakon što se klijent, tvrtka ili ustanova ili potpora definiraju kao izvor financiranja, mogu se dodijeliti jednom ili većem broju pravila financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="b0eb7-123">Pravila financiranja sadrže kriterije koji određuju način na koji se troškovi raspodjeljuju na različite izvore financiranja za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="b0eb7-124">Budući da se zalihe stavki, poput onih koje se pojavljuju u zahtjevima za kupnju i narudžbenicama, ne mogu podijeliti, iznos troškova ne može se podijeliti između više izvora financiranja u trenutku raspodjele.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="b0eb7-125">Stoga vrijednost izvora financiranja ostaje 0 (nula) dok se ne proknjiži izdavanje zaliha.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="b0eb7-126">Kada se proknjiži izdavanje zaliha, iznos troškova raspoređuje se prema pravilima raspodjele računa za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="b0eb7-127">Evo nekoliko koraka koje možete poduzeti kako biste olakšali podjelu naplate između više izvora financiranja:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="b0eb7-128">Navedite da sve transakcije koje se unose za projekt upotrebljavaju istu valutu prodaje kao i ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="b0eb7-129">Postavite ograničenja financiranja tako da se izvoru financiranja ne fakturira više od određenog iznosa za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="b0eb7-130">Konfigurirajte pravila financiranja i ograničenja financiranja za svakog radnika, stavku, kategoriju, grupu kategorija i vrstu transakcije (ili za sve vrste transakcija).</span><span class="sxs-lookup"><span data-stu-id="b0eb7-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="b0eb7-131">Odaberite neobavezne datume početka i završetka kako biste definirali razdoblje kada vrijedi svako pravilo financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="b0eb7-132">Navedite postotak za koji je odgovoran svaki izvor financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="b0eb7-133">Navedite koji je izvor financiranja odgovoran za zaokruživanje razlika uzrokovanih izračunima raspodjele sredstava.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="b0eb7-134">Postavite pravila koja određuju kako se troškovi projekta fakturiraju vanjskim klijentima, a naplaćuju internim tvrtkama ili ustanovama.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="b0eb7-135">Zabilježite transakcije na računu zadržanih sredstava dok se ne mogu dobiti dodatna sredstva ili dok ne odlučite snositi troškove interno.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="b0eb7-136">Kako bi se utvrdilo koju poreznu skupinu treba pridružiti transakciji, pretražuje se projekt radi dodjele porezne grupe.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="b0eb7-137">Ako na razini projekta nije dodijeljena porezna grupa, pretražuje se ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="b0eb7-138">Primjer: Više izvora financiranja (jednostavno)</span><span class="sxs-lookup"><span data-stu-id="b0eb7-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="b0eb7-139">Sljedeća tablica daje scenarije za upravljanje raspodjelom sredstava između više izvora financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="b0eb7-140">Ti se scenariji temelje na sljedećim pretpostavkama:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="b0eb7-141">Pri raspodjeli sredstava uzimaju se u obzir prioritetne postavke prije nego što se primijene drugi kriteriji pravila financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="b0eb7-142">Nije naveden raspon datuma koji bi definirao razdoblje kada vrijedi pravilo financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0eb7-143"><strong>Scenarij</strong></span><span class="sxs-lookup"><span data-stu-id="b0eb7-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="b0eb7-144"><strong>Izvor financiranja</strong></span><span class="sxs-lookup"><span data-stu-id="b0eb7-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="b0eb7-145"><strong>Postotak raspodjele</strong></span><span class="sxs-lookup"><span data-stu-id="b0eb7-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="b0eb7-146"><strong>Prioritet raspodjele</strong></span><span class="sxs-lookup"><span data-stu-id="b0eb7-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0eb7-147">Želite dodijeliti troškove jednom izvoru financiranja dok se njegova sredstva ne iscrpe, dodijeliti troškove drugom izvoru financiranja dok se njegova sredstva ne iscrpe i konačno dodijeliti preostale troškove trećem izvoru financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b0eb7-148">Izvor　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="b0eb7-149">Izvor　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="b0eb7-150">Izvor　financiranja　3</span><span class="sxs-lookup"><span data-stu-id="b0eb7-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-151">100 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-151">100%</span></span></li>
<li><span data-ttu-id="b0eb7-152">100 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-152">100%</span></span></li>
<li><span data-ttu-id="b0eb7-153">100 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-154">1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-154">1</span></span></li>
<li><span data-ttu-id="b0eb7-155">2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-155">2</span></span></li>
<li><span data-ttu-id="b0eb7-156">3</span><span class="sxs-lookup"><span data-stu-id="b0eb7-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0eb7-157">Želite dodijeliti 75 posto troškova jednom izvoru financiranja, a 25 posto drugom izvoru financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b0eb7-158">Kada se iscrpi bilo koji od tih izvora financiranja, preostale troškove želite platiti iz trećeg izvora financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b0eb7-159">Izvor　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="b0eb7-160">Izvor　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="b0eb7-161">Izvor　financiranja　3</span><span class="sxs-lookup"><span data-stu-id="b0eb7-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-162">75 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-162">75%</span></span></li>
<li><span data-ttu-id="b0eb7-163">25 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-163">25%</span></span></li>
<li><span data-ttu-id="b0eb7-164">100 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-165">1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-165">1</span></span></li>
<li><span data-ttu-id="b0eb7-166">1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-166">1</span></span></li>
<li><span data-ttu-id="b0eb7-167">2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0eb7-168">Želite dodijeliti 75 posto troškova jednom izvoru financiranja, a 25 posto drugom izvoru financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="b0eb7-169">Kada se iscrpi bilo koji od tih izvora financiranja, preostale troškove želite podijeliti između trećeg i četvrtog izvora financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b0eb7-170">Izvor　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="b0eb7-171">Izvor　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="b0eb7-172">Izvor　financiranja　3</span><span class="sxs-lookup"><span data-stu-id="b0eb7-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="b0eb7-173">Izvor　financiranja　4</span><span class="sxs-lookup"><span data-stu-id="b0eb7-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-174">75 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-174">75%</span></span></li>
<li><span data-ttu-id="b0eb7-175">25 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-175">25%</span></span></li>
<li><span data-ttu-id="b0eb7-176">50 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-176">50%</span></span></li>
<li><span data-ttu-id="b0eb7-177">50 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-178">1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-178">1</span></span></li>
<li><span data-ttu-id="b0eb7-179">1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-179">1</span></span></li>
<li><span data-ttu-id="b0eb7-180">2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-180">2</span></span></li>
<li><span data-ttu-id="b0eb7-181">2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0eb7-182">Želite dodijeliti prvih 25 posto troškova jednom izvoru financiranja, a ostatak drugom izvoru financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="b0eb7-183">Izvor　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="b0eb7-184">Izvor　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-185">25 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-185">25%</span></span></li>
<li><span data-ttu-id="b0eb7-186">100 %</span><span class="sxs-lookup"><span data-stu-id="b0eb7-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b0eb7-187">1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-187">1</span></span></li>
<li><span data-ttu-id="b0eb7-188">2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="b0eb7-189">Primjer: Više izvora financiranja (složeno)</span><span class="sxs-lookup"><span data-stu-id="b0eb7-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="b0eb7-190">Imate tri izvora financiranja koja želite upotrijebiti sljedećim redoslijedom:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="b0eb7-191">Upotrijebite izvor financiranja 2 i izvor financiranja 3 u jednakoj mjeri dok se izvor financiranja 2 ne iscrpi.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="b0eb7-192">Nastavite upotrebljavati izvor financiranja 3 dok se ne iscrpi.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="b0eb7-193">Upotrijebite izvor financiranja 1 nakon što se izvor financiranja 3 iscrpi.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="b0eb7-194">Kako biste ispunili ovaj cilj, najprije morate učiniti sljedeće:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="b0eb7-195">Postavite ograničenja financiranja za izvor financiranja 2 i izvor financiranja 3, za njihove odgovarajuće iznose.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="b0eb7-196">Stvorite sljedeća pravila financiranja:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="b0eb7-197">Pravilo 1 (Prioritet 1): 50 posto transakcija dodijelite izvoru financiranja 2, a 50 posto izvoru financiranja 3.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="b0eb7-198">Pravilo 2 (Prioritet 2): Dodijelite 100 posto transakcija izvoru financiranja 3.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="b0eb7-199">Pravilo 3 (Prioritet 3): Dodijelite 100 posto transakcija izvoru financiranja 1.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="b0eb7-200">Ova postavka funkcionira jer se provjeravaju transakcije u odnosu na pravila i ograničenja kako bi se utvrdilo primjenjuju li se neka od njih na transakciju.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="b0eb7-201">Ako se na transakciju ne primjenjuju posebna pravila ili ograničenja, primjenjuje se pravilo Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="b0eb7-202">Pravilo Sve transakcije podudara se sa svim transakcijama.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="b0eb7-203">Ako se pronađe pravilo koje se podudara s transakcijom, najprije se primjenjuje postotak koji je dodijeljen tom pravilu, ali tek nakon što se podudaranja provjere u odnosu na postavljena ograničenja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="b0eb7-204">Ako je dosegnuto ograničenje i ako su iscrpljena sredstva izvora financiranja, pravilo financiranja povezano s ograničenjem financiranja zanemaruje se, a program provjerava sljedeće pravilo koje se primjenjuje.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="b0eb7-205">U nekim se slučajevima prema pravilu može dodijeliti samo dio transakcije.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="b0eb7-206">To se može dogoditi jer je dosegnuto ograničenje kada se dodijelila transakcija.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="b0eb7-207">U ovom se slučaju prema tom pravilu dodjeljuje samo određeni iznos, poput 50 posto za svaki izvor financiranja.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="b0eb7-208">To je slučaj u pravilu 1, koje je opisano ranije u ovom odjeljku.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="b0eb7-209">Ostatak se dodjeljuje prema sljedećem pravilu u nizu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="b0eb7-210">U slijedećoj se tablici podrobnije ispituje ovaj scenarij.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0eb7-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="b0eb7-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="b0eb7-212"><strong>Pojedinosti</strong></span><span class="sxs-lookup"><span data-stu-id="b0eb7-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0eb7-213">Pravila financiranja</span><span class="sxs-lookup"><span data-stu-id="b0eb7-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="b0eb7-214">Pravilo 1 (Prioritet 1): Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="b0eb7-215">Dodijelite 50 % izvoru 2 i 50 % izvoru 3.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="b0eb7-216">Pravilo 2 (Prioritet 2): Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="b0eb7-217">Dodijelite 100 % izvoru financiranja 3.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="b0eb7-218">Pravilo 3 (Prioritet 2): Sve transakcije.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="b0eb7-219">Dodijelite 100 % izvoru financiranja 1.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0eb7-220">Ograničenja financiranja</span><span class="sxs-lookup"><span data-stu-id="b0eb7-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="b0eb7-221">Ograničenje izvora financiranja 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="b0eb7-222">Ograničenje izvora financiranja 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="b0eb7-223">Ograničenje izvora financiranja 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0eb7-224">Transakcija 1</span><span class="sxs-lookup"><span data-stu-id="b0eb7-224">Transaction 1</span></span></td>
<td><span data-ttu-id="b0eb7-225"><strong>Iznos transakcije:</strong> 100,00<strong>Financiranje:</strong> Transakcija se plaća samo prema pravilu 1, jer se transakcija u potpunosti plaća nakon primjene pravila 1.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="b0eb7-226">Transakcija se financira jednako između izvora financiranja 2 i 3.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="b0eb7-227">Izvor financiranja 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="b0eb7-228">Izvor financiranja 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0eb7-229">Transakcija 2</span><span class="sxs-lookup"><span data-stu-id="b0eb7-229">Transaction 2</span></span></td>
<td><span data-ttu-id="b0eb7-230"><strong>Iznos transakcije:</strong> 5.000,00<strong>Financiranje:</strong> Transakcija se plaća prema sva tri pravila.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="b0eb7-231"><strong>Pravilo 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="b0eb7-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="b0eb7-232">Izvor financiranja 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="b0eb7-233">Izvor financiranja 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="b0eb7-234">
<strong>2. pravilo</strong>
</span><span class="sxs-lookup"><span data-stu-id="b0eb7-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="b0eb7-235">Izvor financiranja 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="b0eb7-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="b0eb7-236">
<strong>Pravilo 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="b0eb7-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="b0eb7-237">Izvor financiranja 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="b0eb7-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0eb7-238">Ukupna sredstva koja se raspodjeljuju za svaki izvor financiranja</span><span class="sxs-lookup"><span data-stu-id="b0eb7-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="b0eb7-239">Izvor financiranja 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="b0eb7-240">Izvor financiranja 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="b0eb7-241">Izvor financiranja 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="b0eb7-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="b0eb7-242">Pravila naplate</span><span class="sxs-lookup"><span data-stu-id="b0eb7-242">Billing rules</span></span>
<span data-ttu-id="b0eb7-243">Kada s klijentom pregovarate o ugovoru o projektu, definirate kako i kada možete klijentu fakturirati za rad na projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="b0eb7-244">Nakon što utvrdite ugovor o projektu i projekt, možete postaviti pravila naplate za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="b0eb7-245">Pravila naplate temelje se na uvjetima projekta koji su navedeni u ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="b0eb7-246">Pravila naplate koja možete stvoriti ovise o uvjetima ugovora o projektu i vrsti projekta, kao što su Vrijeme i materijal ili Fiksna cijena, koje povezujete s pravilom naplate.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="b0eb7-247">Za ugovor o projektu možete stvoriti više pravila za naplatu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="b0eb7-248">Pravilo naplate možete dodijeliti i većem broju projekata koji su povezani s istim ugovorom o projektu i imaju slične uvjete naplate.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="b0eb7-249">Možete utvrditi sljedeće vrste pravila naplate:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="b0eb7-250">**Jedinica isporuke** – Klijentu fakturirajte kada dovršite jedinicu isporuke.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="b0eb7-251">Jedinice isporuke definirate u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="b0eb7-252">**Napredak** – Klijentu fakturirate kada dovršite određeni postotak projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="b0eb7-253">Možete postaviti pravilo naplate na automatski izračun postotka dovršenog posla ili možete ručno izračunati postotak dovršenog posla i iznos za fakturiranje klijentu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="b0eb7-254">**Kontrolna točka** – Klijentu fakturirate puni iznos do kontrolne točke projekta, kada se ona postigne.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="b0eb7-255">**Naknada** – Klijentu fakturirate svoje usluge uz naknadu za upravljanje, koja je obično postotak od troška usluge.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="b0eb7-256">**Vrijeme i materijal** – Klijentu fakturirate vrijednost vremena i materijala koji su upotrijebljeni na projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="b0eb7-257">Za sve vrste pravila naplate možete odrediti postotak zadržavanja koji se klijentu oduzima od faktura dok projekt ne dosegne dogovorenu fazu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="b0eb7-258">Postotak zadržavanja plaćanja naveden je u ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="b0eb7-259">Iznos se izračunava na temelju ukupne vrijednosti redaka na fakturi za klijenta i oduzima se od te vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="b0eb7-260">Za pravila naplate **Vrijeme i materijal** i **Napredak**, možete dodijeliti naplative kategorije.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="b0eb7-261">Naplative kategorije označavaju transakcije koje bi trebale biti uključene u fakture za klijente.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="b0eb7-262">Kada ste spremni klijentu izdati fakturu, iznos fakture za projekt izračunava se na temelju pravila naplate i generira se prijedlog fakture za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="b0eb7-263">U slijedećim odjeljcima daju se primjeri koji pokazuju kako postaviti i upravljati pravilima naplate za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="b0eb7-264">Primjer: Stvaranje pravila naplate koje se temelji na broju isporučenih jedinica</span><span class="sxs-lookup"><span data-stu-id="b0eb7-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="b0eb7-265">Vaša tvrtka ili ustanova sklapa ugovor o pružanju ukupno pet treninga zaposlenicima klijenta po cijeni od 10.000 po treningu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="b0eb7-266">Klijentu fakturirate nakon svakog treninga.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="b0eb7-267">Kada postavljate pravila naplate za ugovor, upotrijebite sljedeće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="b0eb7-268">Jedinica isporuke je jedan trening.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="b0eb7-269">Jedinična cijena je 10.000 po treningu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="b0eb7-270">Ukupan broj jedinica je pet treninga.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="b0eb7-271">Kada završite jedan trening, možete stvoriti račun na 10.000 za prvu isporučenu jedinicu i poslati račun klijentu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="b0eb7-272">Primjer: Stvaranje pravila naplate koje se temelji na određenom postotku završetka projekta (ručni izračun)</span><span class="sxs-lookup"><span data-stu-id="b0eb7-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="b0eb7-273">Vaša tvrtka ili ustanova, tvrtka za softversko savjetovanje, sklapa ugovor s klijentom o razvoju dijela proizvoda koji klijent razvija.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="b0eb7-274">Vaša se tvrtka ili ustanova slaže s isporukom softverskog koda u razdoblju od šest mjeseci.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="b0eb7-275">Klijent se slaže da će vašoj tvrtki ili ustanovi platiti ukupno 100.000 za posao.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="b0eb7-276">Stvarate pravilo naplate za fakturiranje klijentu na temelju postotka radova koji su dovršeni na projektu, kako je navedeno u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="b0eb7-277">Na kraju prvog mjeseca sastajete se s klijentom kako biste utvrdili postotak dovršenog posla.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="b0eb7-278">Nakon što s klijentom pregledate projekt, odlučujete kako je dovršeno 15 posto projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="b0eb7-279">Stvorite fakturu na 15.000 (15 posto od 100.000) i pošaljite je klijentu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="b0eb7-280">Primjer: Stvaranje pravila naplate koje se temelji na određenom postotku završetka projekta (automatski izračun)</span><span class="sxs-lookup"><span data-stu-id="b0eb7-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="b0eb7-281">Vaša tvrtka ili ustanova, tvrtka za razvoj softvera, pristaje razviti paket obračuna plaća za klijenta za iznos od 30.000.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="b0eb7-282">Klijent se slaže da će vašoj tvrtki ili ustanovi plaćati na temelju postotka dovršenosti posla.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="b0eb7-283">Procjenjujete da troškovi projekta iznose 20.000.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="b0eb7-284">Ugovor o projektu navodi kategorije posla koje upotrebljavate u postupku naplate.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="b0eb7-285">Postavljate pravila naplate koja automatski izračunavaju iznose računa za postotak dovršenosti posla za svaku kategoriju.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="b0eb7-286">Postavljate proračun za svaku kategoriju:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="b0eb7-287">**Razvoj** – Trošak od 15.000 i prihod od 20.000</span><span class="sxs-lookup"><span data-stu-id="b0eb7-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="b0eb7-288">**Instalacija** – Trošak od 5.000 i prihod od 10.000</span><span class="sxs-lookup"><span data-stu-id="b0eb7-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="b0eb7-289">Kada prvi put stvarate fakturu za klijenta, iznos fakture automatski se izračunava na temelju sljedećih podataka:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="b0eb7-290">Nakon mjesec dana, radnik na projektu predaje evidenciju radnog vremena za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="b0eb7-291">Trošak sati rada radnika iznosi 5.000 za razvoj i 1.000 za ugradnju.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="b0eb7-292">Razvojni posao završen je 33 posto (5.000 stvarnog troška / 15.000 proračunskog troška), a instalacijski posao 20 posto (1.000 stvarnog troška / 5.000 proračunskog troška).</span><span class="sxs-lookup"><span data-stu-id="b0eb7-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="b0eb7-293">Iznos fakture od 8.667 automatski se izračunava (33 posto od 20.000 + 20 posto od 10.000).</span><span class="sxs-lookup"><span data-stu-id="b0eb7-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="b0eb7-294">Stvorite fakturu na 8.667 i pošaljite je klijentu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="b0eb7-295">Primjer: Stvaranje pravila naplate koje se temelji na dogovorenim kontrolnim točkama</span><span class="sxs-lookup"><span data-stu-id="b0eb7-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="b0eb7-296">Vaša tvrtka ili ustanova, tvrtka za savjetodavno upravljanje, pristaje provesti istraživanje tržišta za potrošački proizvod koji klijent planira prodati.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="b0eb7-297">Klijent se slaže da će vaše usluge koristiti tijekom razdoblja od tri mjeseca, počevši od ožujka, i pristaje vašoj tvrtki ili ustanovi platiti 50.000.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="b0eb7-298">Projekt ima tri kontrolne točke:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-298">The project has three milestones:</span></span>

-   <span data-ttu-id="b0eb7-299">1. kontrolna točka: Prikupljanje podataka o potrošačima – 31. ožujka</span><span class="sxs-lookup"><span data-stu-id="b0eb7-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="b0eb7-300">2. kontrolna točka: Analiziranje potrošačkih podataka – 30. travnja</span><span class="sxs-lookup"><span data-stu-id="b0eb7-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="b0eb7-301">3. kontrolna točka: Predstavljanje prijedloga održivosti proizvoda – 31. svibnja</span><span class="sxs-lookup"><span data-stu-id="b0eb7-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="b0eb7-302">Klijent se slaže da će vašoj tvrtki ili ustanovi platiti 10.000 na prvoj kontrolnoj točki, 20.000 na drugoj i 20.000 na trećoj kontrolnoj točki.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="b0eb7-303">Kada postavljate ugovor o projektu, pristajete klijentu naplaćivati na temelju kontrolne točke koja je dovršena.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="b0eb7-304">Postavljanje pravila naplate uključuje sljedeće korake:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="b0eb7-305">Definiranje kontrolnih točaka projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-305">Define the project milestones.</span></span>
-   <span data-ttu-id="b0eb7-306">Definiranje iznosa za fakturiranje klijentu kada se završi svaka kontrolna točka.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="b0eb7-307">Kada se 31. ožujka dovrši prva kontrolna točka, označite je kao dovršenu, a zatim stvorite fakturu na 10.000 i pošaljite je klijentu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="b0eb7-308">Ne možete stvoriti fakturu za kontrolnu točku dok je ne označite kao završenu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="b0eb7-309">Primjer: Stvaranje pravila naplate koje se temelji na uslugama uz dodatnu naknadu za upravljanje</span><span class="sxs-lookup"><span data-stu-id="b0eb7-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="b0eb7-310">Vaša tvrtka ili ustanova, tvrtka za savjetodavno upravljanje, pristaje provesti istraživanje tržišta kako bi se procijenila održivost proizvoda koju klijent, maloprodajna tvrtka, razvija.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="b0eb7-311">Uvjeti sporazuma određuju kako ćete osigurati usluge svoja tri najbolja savjetnika za upravljanje, koji će istraživanje provoditi na temelju vremena i materijala.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="b0eb7-312">Klijent pristaje platiti 100 po satu, uz dodatnih 10 posto naknade za upravljanje savjetničkim satima rada koji se naplaćuju projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b0eb7-313">Kada postavljate ugovor o projektu, stvorite pravilo naplate za dodavanje 10 posto naknade za upravljanje savjetničkim satima rada koji se naplaćuju projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="b0eb7-314">Kada stvarate fakturu za klijenta, klijentu se naplaćuje 10-postotna naknada za upravljanje uvećana za trošak savjetničkog sata.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="b0eb7-315">Na primjer, ako su tri konzultanta na projektu radila ukupno 200 sati, faktura na 22.000 stvara se na temelju sljedećeg izračuna:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="b0eb7-316">200 sati pri 100 za sat = 20.000</span><span class="sxs-lookup"><span data-stu-id="b0eb7-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="b0eb7-317">Naknada za upravljanje od 10 posto = 2.000</span><span class="sxs-lookup"><span data-stu-id="b0eb7-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="b0eb7-318">Ukupni iznos fakture = 22.000</span><span class="sxs-lookup"><span data-stu-id="b0eb7-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="b0eb7-319">Ako su naknade koje se zaračunavaju klijentu oporezive i u ugovoru o projektu odaberete grupu PDV-a, ona se automatski unosi u pravilo naplate naknada.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="b0eb7-320">Primjer: Stvaranje pravila naplate za vrijednost vremena i materijala</span><span class="sxs-lookup"><span data-stu-id="b0eb7-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="b0eb7-321">Vaša tvrtka ili ustanova, tvrtka za softversko savjetovanje, pristaje osigurati pet tehničkih savjetnika koji će tijekom sljedećih šest mjeseci raditi na projektu razvoja softvera za klijenta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="b0eb7-322">Klijent se obvezuje platiti 150 za svaki savjetnički sat rada, uvećan za troškove uredskog materijala.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="b0eb7-323">Vaša tvrtka ili ustanova šalje klijentu fakturu na kraju svakog mjeseca.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="b0eb7-324">Kada postavljate ugovor o projektu, suglasni ste da ćete klijentu svaki mjesec fakturirati vrijeme i materijale utrošene na projektu.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="b0eb7-325">Stvorite pravilo naplate koje uključuje sljedeće podatke:</span><span class="sxs-lookup"><span data-stu-id="b0eb7-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="b0eb7-326">Razdoblje ugovora je šest mjeseci.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-326">The contract period is six months.</span></span>
-   <span data-ttu-id="b0eb7-327">Vrijeme savjetovanja izračunava se s cijenom od 150 na sat.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="b0eb7-328">Uredski materijal fakturira se prema trošku, a ukupni trošak projekta ne smije prelaziti 10.000.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="b0eb7-329">Fakturu za klijenta stvarate na kraju svakog kalendarskog mjeseca tijekom projekta.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="b0eb7-330">Tijekom prvog mjeseca, savjetnici na projektu bilježe ukupno 800 sati.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="b0eb7-331">Cijena uredskog materijala koji se naplaćuje za projekt iznosi 2.000.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="b0eb7-332">Stoga na kraju mjeseca stvarate fakturu na 122.000, što je izračunano kao 800 sati pri 150 na sat, uz dodatnih 2.000 za uredski materijal.</span><span class="sxs-lookup"><span data-stu-id="b0eb7-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



