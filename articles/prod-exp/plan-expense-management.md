---
title: Konfiguriranje upravljanja troškovima
description: U ovom se članku opisuju razmatranja i odluke koje morate donijeti tijekom postupka planiranja, prije nego što konfigurirate upravljanje troškovima u aplikaciji Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960328"
---
# <a name="configure-expense-management"></a><span data-ttu-id="aa2b6-103">Konfiguriranje upravljanja troškovima</span><span class="sxs-lookup"><span data-stu-id="aa2b6-103">Configure expense management</span></span>

<span data-ttu-id="aa2b6-104">U ovoj se temi opisuju razmatranja i odluke koje morate donijeti tijekom postupka planiranja, prije nego što konfigurirate upravljanje troškovima.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="aa2b6-105">U modul Upravljanje troškovima možete pohranjivati informacije o načinima plaćanja, putnim nalozima, izvješćima o troškovima, pravilima itd.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="aa2b6-106">Budući da se mnoge odluke koje donosite kada planirate svoju konfiguraciju modula Upravljanje troškovima temelje na hijerarhiji i financijskoj strukturi vaše tvrtke ili ustanove, morate pogledati dokumente za planiranje tih područja.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="aa2b6-107">Međukompanijski troškovi</span><span class="sxs-lookup"><span data-stu-id="aa2b6-107">Intercompany expenses</span></span>

<span data-ttu-id="aa2b6-108">Kada omogućite troškove unutar tvrtke, dopuštate pravnim osobama i zaposlenicima da prave troškove u ime druge pravne osobe i prikupljaju uplate od pravne osobe koja radi unutar vaše tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="aa2b6-109">Na primjer, zaposlenik u pravnoj osobi A dovršava projekt za pravnu osobu B, a projekt snosi povezane troškove putovanja.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="aa2b6-110">Ako su omogućeni troškovi unutar tvrtke, zaposlenik tada može podnijeti izvješće o troškovima koje će se knjižiti na pravnu osobu B, a trošak tada mora platiti pravna osoba A. Ako vaša tvrtka ili ustanova nema više pravnih osoba, ne morate omogućiti troškove unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="aa2b6-111">**Odluka:** Želite li omogućiti troškove unutar tvrtke?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="aa2b6-112">Financijsko upravljanje</span><span class="sxs-lookup"><span data-stu-id="aa2b6-112">Financial management</span></span>

<span data-ttu-id="aa2b6-113">Upravljanje troškovima čvrsto je integrirano s upravljanjem financijama vaše tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="aa2b6-114">Dosta od vaše konfiguracije za upravljanje troškovima temeljit će se na odlukama koje ste donijeli o financijama vaše tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="aa2b6-115">Sljedeći odjeljci opisuju različita područja koja zahtijevaju planiranje i donošenje odluka, na temelju financijskih odluka vaše tvrtke ili ustanove i smjernica vašeg upravljačkog tima.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="aa2b6-116">Po danima</span><span class="sxs-lookup"><span data-stu-id="aa2b6-116">Per diems</span></span>

<span data-ttu-id="aa2b6-117">Morate definirati zaposlenike po dnevnicama koje osigurava vaša tvrtka ili ustanova.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="aa2b6-118">Budući da se dnevnice obično upotrebljavaju za pokrivanje troškova poput prehrane, smještaja i ostalih sporednih troškova, možete stvoriti pravila za dnevnice koje daje vaša tvrtka ili ustanova.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="aa2b6-119">Cijene dnevnica mogu se temeljiti na dobu godine, mjestu putovanja ili oboje.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="aa2b6-120">Kada definirate pravilo za dnevnice, možete odrediti da se od dnevnice odbija postotak ako radnik prima besplatne obroke ili usluge.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="aa2b6-121">Također, možete definirati razine cijena dnevnica koje se postavljaju za minimalni i maksimalni broj sati za koji se dnevnica može primijeniti kada je radnik na putu.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="aa2b6-122">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="aa2b6-122">**Decisions:**</span></span>

- <span data-ttu-id="aa2b6-123">Zadana pravila za dnevnice za prvi i zadnji dan:</span><span class="sxs-lookup"><span data-stu-id="aa2b6-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="aa2b6-124">Koji je minimalan broj sati koje zaposlenik može prijaviti u danu kako bi dobio dnevnicu?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="aa2b6-125">Postoji li smanjenje iznosa koji se daje za obroke za prvi dan i zadnji dan?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="aa2b6-126">Ako postoji smanjenje, koliki je postotak smanjenja?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="aa2b6-127">Postoji li smanjenje iznosa koji se daje za hotel za prvi dan i zadnji dan?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="aa2b6-128">Ako postoji smanjenje, koliki je postotak smanjenja?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="aa2b6-129">Postoji li smanjenje iznosa koji se daje za ostale troškove koji nastaju prvi dan i zadnji dan?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="aa2b6-130">Ako postoji smanjenje, koliki je postotak smanjenja?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="aa2b6-131">Zadana pravila za dnevnicu:</span><span class="sxs-lookup"><span data-stu-id="aa2b6-131">Default per diem rules:</span></span>

    - <span data-ttu-id="aa2b6-132">Postoji li postotno smanjenje dnevnice za svaki obrok ako je, na primjer, obrok besplatan?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="aa2b6-133">Ako postoji smanjenje, koliki je postotak smanjenja za svaki obrok?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="aa2b6-134">Izračunava li se smanjenje za obrok po danu, po putovanju ili po broju dnevnih obroka?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="aa2b6-135">Treba li iznose dnevnica redovito popunjavati ili ih treba prikupljati?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="aa2b6-136">Izračunavaju li se dnevnice na 24-satno razdoblje ili na kalendarski dan?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="aa2b6-137">Pravila za dnevnice koja se temelje na lokaciji:</span><span class="sxs-lookup"><span data-stu-id="aa2b6-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="aa2b6-138">Razlikuju li se dnevnice ovisno o lokaciji?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="aa2b6-139">Koje su lokacije uključene?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-139">What locations are included?</span></span>
    - <span data-ttu-id="aa2b6-140">Ako se dnevnice razlikuju ovisno o mjestu, koliki se postotni iznos daje za sljedeće vrste troškova:</span><span class="sxs-lookup"><span data-stu-id="aa2b6-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="aa2b6-141">Obroci</span><span class="sxs-lookup"><span data-stu-id="aa2b6-141">Meals</span></span>
        - <span data-ttu-id="aa2b6-142">Hoteli</span><span class="sxs-lookup"><span data-stu-id="aa2b6-142">Hotel</span></span>
        - <span data-ttu-id="aa2b6-143">Ostali troškovi</span><span class="sxs-lookup"><span data-stu-id="aa2b6-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="aa2b6-144">Dnevnici i računi za upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="aa2b6-144">Expense management journals and accounts</span></span>

<span data-ttu-id="aa2b6-145">Upravljanje troškovima zahtijeva uporabu više dnevnika i računa.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="aa2b6-146">Morate odlučiti, na primjer, hoće li se isti račun upotrebljavati za gotovinske predujmove i povrate po kreditnim karticama.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="aa2b6-147">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="aa2b6-147">**Decisions:**</span></span>

- <span data-ttu-id="aa2b6-148">U koji se dnevnik glavne knjige knjiže odobrena izvješća o troškovima?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="aa2b6-149">Koji se račun upotrebljava za gotovinske predujmove?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="aa2b6-150">Treba li odmah knjižiti gotovinske predujmove?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="aa2b6-151">Načini plaćanja</span><span class="sxs-lookup"><span data-stu-id="aa2b6-151">Payment methods</span></span>

<span data-ttu-id="aa2b6-152">Kad zaposlenicima dopuštate da prave troškove u ime vaše tvrtke, morate definirati načine plaćanja koje zaposlenici smiju upotrebljavati.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="aa2b6-153">Na primjer, zaposlenicima možete dopustiti uporabu gotovine ili korporativne kreditne kartice.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="aa2b6-154">Također zaposlenicima možete dopustiti da se koriste osobnom kreditnom karticom, nakon čega im nadoknađujete novac.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="aa2b6-155">Morate donijeti sljedeće odluke za svaki način plaćanja koji dopustite.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="aa2b6-156">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="aa2b6-156">**Decisions:**</span></span>

- <span data-ttu-id="aa2b6-157">Koji su načini plaćanja dopušteni?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="aa2b6-158">Tko podmiruje troškove načina plaćanja?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="aa2b6-159">Postoji li vrsta računa za prijeboj?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-159">Is there an offset account type?</span></span> <span data-ttu-id="aa2b6-160">Ako postoji vrsta računa za prijeboj, što je to?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="aa2b6-161">Ako postoji vrsta računa za prijeboj, što je račun?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="aa2b6-162">Ako je način plaćanja kreditna kartica, treba li se način plaćanja upotrebljavati samo s uvoznim transakcijama?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="aa2b6-163">Kategorije troškova i dijeljene kategorije</span><span class="sxs-lookup"><span data-stu-id="aa2b6-163">Expense categories and shared categories</span></span>

<span data-ttu-id="aa2b6-164">Kad zaposlenici stvaraju izvješće o troškovima, svaki trošak koji evidentiraju mora biti povezan s kategorijom troška.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="aa2b6-165">Kategorije troškova izvedene su iz dijeljenih kategorija koje se mogu dijeliti između pravnih osoba u vašoj tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="aa2b6-166">Te se kategorije također mogu dijeliti u Upravljanju projektima i računovodstvu, ovisno o načinu na koji je definirana vaša tvrtka ili ustanova.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="aa2b6-167">Na temelju definicije vaše tvrtke ili ustanove i smjernica implementacijskog tima, morate odrediti hoće li se kategorije koje se upotrebljavaju u Upravljanju troškovima upotrebljavati samo u Upravljanju troškovima ili bi ih se trebalo dijeliti između Upravljanja projektom i računovodstvom i Upravljanja troškovima.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="aa2b6-168">Imajte na umu kako se te kategorije mogu dijeliti između Projekta i Troška ili Projekta i Proizvodnje, ali ne i između Troška i Proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="aa2b6-169">Morate donijeti sljedeće odluke za svaku kategoriju troškova.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="aa2b6-170">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="aa2b6-170">**Decisions:**</span></span>

- <span data-ttu-id="aa2b6-171">Što je kategorija troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-171">What is the expense category?</span></span> <span data-ttu-id="aa2b6-172">Primjeri uključuju kategorije za letove, hotele ili kilometražu.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="aa2b6-173">Može li se kategorija troškova upotrebljavati i za Upravljanje projektima i računovodstvo?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="aa2b6-174">Što je vrsta troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-174">What is the expense type?</span></span>
- <span data-ttu-id="aa2b6-175">Koji je zadani način plaćanja za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="aa2b6-176">Moraju li se specificirati troškovi iz kategorije troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="aa2b6-177">Koji je glavni zadani račun za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="aa2b6-178">Koja je zadana stavka grupe poreza na promet za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="aa2b6-179">Jesu li dodatni načini plaćanja dozvoljeni za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="aa2b6-180">Ako su dopušteni dodatni načini plaćanja, koji su to načini?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="aa2b6-181">Postoje li potkategorije u ovoj kategoriji troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="aa2b6-182">Ako postoje potkategorije, morate također donijeti sljedeće odluke:</span><span class="sxs-lookup"><span data-stu-id="aa2b6-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="aa2b6-183">Je li neka od potkategorija izuzeta iz povrata poreza?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="aa2b6-184">Koja je stavka grupe poreza na promet potkategorija?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="aa2b6-185">Ako se kategorija troškova upotrebljava i u Upravljanju projektom i računovodstvu, odgovorite na preostala pitanja.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="aa2b6-186">U suprotnom, prijeđite na sljedeći odjeljak.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="aa2b6-187">Koji će se računi za troškove upotrebljavati za sljedeće troškove?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="aa2b6-188">Cijena</span><span class="sxs-lookup"><span data-stu-id="aa2b6-188">Cost</span></span>
    - <span data-ttu-id="aa2b6-189">Raspodjela plaća</span><span class="sxs-lookup"><span data-stu-id="aa2b6-189">Payroll allocation</span></span>
    - <span data-ttu-id="aa2b6-190">Vrijednost troškova WIP-a</span><span class="sxs-lookup"><span data-stu-id="aa2b6-190">WIP-cost value</span></span>
    - <span data-ttu-id="aa2b6-191">Troškovna stavka</span><span class="sxs-lookup"><span data-stu-id="aa2b6-191">Cost-item</span></span>
    - <span data-ttu-id="aa2b6-192">Vrijednosna stavka troškova WIP-a</span><span class="sxs-lookup"><span data-stu-id="aa2b6-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="aa2b6-193">Obračunani gubitak</span><span class="sxs-lookup"><span data-stu-id="aa2b6-193">Accrued loss</span></span>
    - <span data-ttu-id="aa2b6-194">Obračunani gubitak WIP-a</span><span class="sxs-lookup"><span data-stu-id="aa2b6-194">WIP-accrued loss</span></span>

- <span data-ttu-id="aa2b6-195">Koji će se računi za prihod upotrebljavati za sljedeće?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="aa2b6-196">Fakturirani prihod</span><span class="sxs-lookup"><span data-stu-id="aa2b6-196">Invoiced revenue</span></span>
    - <span data-ttu-id="aa2b6-197">Obračunani prihod – vrijednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aa2b6-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="aa2b6-198">Prodajna vrijednost WIP-a</span><span class="sxs-lookup"><span data-stu-id="aa2b6-198">WIP-sales value</span></span>
    - <span data-ttu-id="aa2b6-199">Obračunani prihod proizvodnje</span><span class="sxs-lookup"><span data-stu-id="aa2b6-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="aa2b6-200">Proizvodnja WIP-a</span><span class="sxs-lookup"><span data-stu-id="aa2b6-200">WIP-production</span></span>
    - <span data-ttu-id="aa2b6-201">Obračunani prihod – dobit</span><span class="sxs-lookup"><span data-stu-id="aa2b6-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="aa2b6-202">Dobit WIP-a</span><span class="sxs-lookup"><span data-stu-id="aa2b6-202">WIP-profit</span></span>
    - <span data-ttu-id="aa2b6-203">Obračunani prihod – pretplata</span><span class="sxs-lookup"><span data-stu-id="aa2b6-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="aa2b6-204">Pretplata WIP-a</span><span class="sxs-lookup"><span data-stu-id="aa2b6-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="aa2b6-205">Porezi</span><span class="sxs-lookup"><span data-stu-id="aa2b6-205">Taxes</span></span>

<span data-ttu-id="aa2b6-206">Za poreze povezane s troškovima morate odrediti što je uključeno ili omogućeno u izvješćima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="aa2b6-207">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="aa2b6-207">**Decisions:**</span></span>

- <span data-ttu-id="aa2b6-208">Je li porez na promet uključen u iznose troškova?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="aa2b6-209">Treba li omogućiti povrat poreza na troškove?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa2b6-210">Kada ste planirali glavnu knjigu, ako ste odlučili primijeniti porez na promet SAD-a i upotrebljavati odgovarajuće porezne propise, ne možete omogućiti povrat poreza na troškove.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="aa2b6-211">(Kako biste primijenili porez na promet SAD-a i upotrebljavali odgovarajuće porezne propise, mogućnost **Primijeni pravila oporezivanja poreza na promet** postavite na **Da**.)</span><span class="sxs-lookup"><span data-stu-id="aa2b6-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="aa2b6-212">Pravilnici</span><span class="sxs-lookup"><span data-stu-id="aa2b6-212">Policies</span></span>

<span data-ttu-id="aa2b6-213">Stvaranjem pravila za izvješćivanje o troškovima možete pomoći svojoj tvrtki ili ustanovi da uštedi vrijeme i novac kada zaposlenici naprave troškove u njezino ime.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="aa2b6-214">Pravila jamče da zaposlenici ostanu unutar proračuna, pruže sve potrebne podatke i troše novac samo onako kako im je potrebno.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="aa2b6-215">Morate donijeti sljedeće odluke za svaki pravilnik za izvješća o troškovima i za odobravanje izvješća o troškovima koje stvarate.</span><span class="sxs-lookup"><span data-stu-id="aa2b6-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="aa2b6-216">**Odluke:**</span><span class="sxs-lookup"><span data-stu-id="aa2b6-216">**Decisions:**</span></span>

- <span data-ttu-id="aa2b6-217">Koji je naziv pravilnika?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-217">What is the name of the policy?</span></span>
- <span data-ttu-id="aa2b6-218">Čemu služi pravilnik o trošku?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-218">What is the expense policy for?</span></span>
- <span data-ttu-id="aa2b6-219">Ako ste prethodno odlučili omogućiti troškove među tvrtkama, na koje će se tvrtke u vašoj tvrtki ili ustanovi primjenjivati ovaj pravilnik?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="aa2b6-220">Kada pravilnik stupa na snagu?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-220">When does the policy become effective?</span></span>
- <span data-ttu-id="aa2b6-221">Kada pravilnik prestaje vrijediti?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-221">When does the policy expire?</span></span>
- <span data-ttu-id="aa2b6-222">Što je pravilo iz pravilnika?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-222">What is the policy rule?</span></span>
- <span data-ttu-id="aa2b6-223">Koji je ishod pravila iz pravilnika?</span><span class="sxs-lookup"><span data-stu-id="aa2b6-223">What is the outcome of the policy rule?</span></span>
