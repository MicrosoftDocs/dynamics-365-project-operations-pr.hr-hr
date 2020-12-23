---
title: Pregled priznavanja prihoda
description: U ovoj temi nalaze se informacije o priznavanju prihoda u aplikaciji Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531380"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="24a12-103">Pregled priznavanja prihoda</span><span class="sxs-lookup"><span data-stu-id="24a12-103">Revenue recognition overview</span></span>

<span data-ttu-id="24a12-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="24a12-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="24a12-105">Načela priznavanja prihoda u aplikaciji Dynamics 365 Project Operations razlikuju se ovisno o odabranom načinu naplate za projekt ili dio projekta.</span><span class="sxs-lookup"><span data-stu-id="24a12-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="24a12-106">U ovoj temi nalaze se informacije o priznavanju prihoda u aplikaciji Project Operations.</span><span class="sxs-lookup"><span data-stu-id="24a12-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="24a12-107">Obračun transakcija za koje se upotrebljava način naplate vremena i materijala</span><span class="sxs-lookup"><span data-stu-id="24a12-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="24a12-108">Priznavanje troškova i prihoda povezano je.</span><span class="sxs-lookup"><span data-stu-id="24a12-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="24a12-109">Troškovi transakcije i nenaplaćene prodaje knjiže se s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="24a12-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="24a12-110">Profil troškova i prihoda projekta određuje jesu li nenaplaćene prodajne transakcije knjižene u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="24a12-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="24a12-111">Ako je odabran **Akumulirani prihod**, sustav tijekom knjiženja upotrebljava račune **WIP prodajna vrijednost** i **Prodajna vrijednost akumuliranog prihoda**.</span><span class="sxs-lookup"><span data-stu-id="24a12-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="24a12-112">Slijedi primjer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="24a12-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="24a12-113">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="24a12-113">Transaction type</span></span> | <span data-ttu-id="24a12-114">Terećenje/kredit</span><span class="sxs-lookup"><span data-stu-id="24a12-114">Debit/Credit</span></span> | <span data-ttu-id="24a12-115">Iznos</span><span class="sxs-lookup"><span data-stu-id="24a12-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="24a12-116">WIP prodajna vrijednost</span><span class="sxs-lookup"><span data-stu-id="24a12-116">WIP Sales value</span></span> | <span data-ttu-id="24a12-117">Terećenje</span><span class="sxs-lookup"><span data-stu-id="24a12-117">Debit</span></span> | <span data-ttu-id="24a12-118">100</span><span class="sxs-lookup"><span data-stu-id="24a12-118">100</span></span> |
  | <span data-ttu-id="24a12-119">Prodajna vrijednost akumuliranog prihoda</span><span class="sxs-lookup"><span data-stu-id="24a12-119">Accrued revenue sales value</span></span> | <span data-ttu-id="24a12-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="24a12-120">Credit</span></span> | <span data-ttu-id="24a12-121">100</span><span class="sxs-lookup"><span data-stu-id="24a12-121">100</span></span> |

- <span data-ttu-id="24a12-122">Prihod se priznaje tijekom fakturiranja.</span><span class="sxs-lookup"><span data-stu-id="24a12-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="24a12-123">Tijekom knjiženja sustav upotrebljava račun **Fakturirani prihod**.</span><span class="sxs-lookup"><span data-stu-id="24a12-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="24a12-124">Slijedi primjer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="24a12-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="24a12-125">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="24a12-125">Transaction type</span></span> | <span data-ttu-id="24a12-126">Terećenje/kredit</span><span class="sxs-lookup"><span data-stu-id="24a12-126">Debit/Credit</span></span> | <span data-ttu-id="24a12-127">Iznos</span><span class="sxs-lookup"><span data-stu-id="24a12-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="24a12-128">Saldo klijenta</span><span class="sxs-lookup"><span data-stu-id="24a12-128">Customer balance</span></span> | <span data-ttu-id="24a12-129">Terećenje</span><span class="sxs-lookup"><span data-stu-id="24a12-129">Debit</span></span> | <span data-ttu-id="24a12-130">120</span><span class="sxs-lookup"><span data-stu-id="24a12-130">120</span></span> |
  | <span data-ttu-id="24a12-131">Plaća se porez na promet</span><span class="sxs-lookup"><span data-stu-id="24a12-131">Sales tax payable</span></span> | <span data-ttu-id="24a12-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="24a12-132">Credit</span></span> | <span data-ttu-id="24a12-133">20</span><span class="sxs-lookup"><span data-stu-id="24a12-133">20</span></span> |
  | <span data-ttu-id="24a12-134">Fakturirani prihod</span><span class="sxs-lookup"><span data-stu-id="24a12-134">Invoiced Revenue</span></span> | <span data-ttu-id="24a12-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="24a12-135">Credit</span></span> | <span data-ttu-id="24a12-136">100</span><span class="sxs-lookup"><span data-stu-id="24a12-136">100</span></span> |

- <span data-ttu-id="24a12-137">Ako je prihod nastao pri knjiženju nenaplaćene prodaje, sustav će pri fakturiranju stornirati prihod.</span><span class="sxs-lookup"><span data-stu-id="24a12-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="24a12-138">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="24a12-138">Transaction type</span></span> | <span data-ttu-id="24a12-139">Terećenje/kredit</span><span class="sxs-lookup"><span data-stu-id="24a12-139">Debit/Credit</span></span> | <span data-ttu-id="24a12-140">Iznos</span><span class="sxs-lookup"><span data-stu-id="24a12-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="24a12-141">WIP prodajna vrijednost</span><span class="sxs-lookup"><span data-stu-id="24a12-141">WIP Sales value</span></span> | <span data-ttu-id="24a12-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="24a12-142">Credit</span></span> | <span data-ttu-id="24a12-143">100</span><span class="sxs-lookup"><span data-stu-id="24a12-143">100</span></span> |
  | <span data-ttu-id="24a12-144">Prodajna vrijednost akumuliranog prihoda</span><span class="sxs-lookup"><span data-stu-id="24a12-144">Accrued revenue sales value</span></span> | <span data-ttu-id="24a12-145">Terećenje</span><span class="sxs-lookup"><span data-stu-id="24a12-145">Debit</span></span> | <span data-ttu-id="24a12-146">100</span><span class="sxs-lookup"><span data-stu-id="24a12-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="24a12-147">Obračun transakcija za koje se upotrebljava način naplate fiksnom cijenom</span><span class="sxs-lookup"><span data-stu-id="24a12-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="24a12-148">Priznavanje troškova i prihoda odvojeno je.</span><span class="sxs-lookup"><span data-stu-id="24a12-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="24a12-149">Troškovi transakcije knjiže se s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="24a12-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="24a12-150">Nenaplaćene se prodajne transakcije ne stvaraju.</span><span class="sxs-lookup"><span data-stu-id="24a12-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="24a12-151">Prihod se može priznati tijekom fakturiranja ako profil troškova i prihoda projekta ima **Načelo upotrijebljeno za izračun završetka projekta** postavljeno na **Bez WIP-a**.</span><span class="sxs-lookup"><span data-stu-id="24a12-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="24a12-152">Ovaj način upotrebljavajte samo za kratkoročne, jednostavne projekte.</span><span class="sxs-lookup"><span data-stu-id="24a12-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="24a12-153">Prihod se može priznati s pomoću procjene prihoda od fiksne cijene, bilo načinom **Ugovor dovršen** ili **Priznavanje prihoda od postotka dovršenosti**.</span><span class="sxs-lookup"><span data-stu-id="24a12-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24a12-154">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="24a12-154">Additional resources</span></span>
[<span data-ttu-id="24a12-155">Konfiguriranje računovodstva za naplative proizvode iz projekata</span><span class="sxs-lookup"><span data-stu-id="24a12-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="24a12-156">Projekti s procjenom prihoda od fiksne cijene</span><span class="sxs-lookup"><span data-stu-id="24a12-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="24a12-157">Upravljanje procjenama prihoda</span><span class="sxs-lookup"><span data-stu-id="24a12-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="24a12-158">Načini troškova do završetka</span><span class="sxs-lookup"><span data-stu-id="24a12-158">Cost to complete methods</span></span>](cost-complete-methods.md)
