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
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278859"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="418b4-103">Pregled priznavanja prihoda</span><span class="sxs-lookup"><span data-stu-id="418b4-103">Revenue recognition overview</span></span>

<span data-ttu-id="418b4-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="418b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="418b4-105">Načela priznavanja prihoda u aplikaciji Dynamics 365 Project Operations razlikuju se ovisno o odabranom načinu naplate za projekt ili dio projekta.</span><span class="sxs-lookup"><span data-stu-id="418b4-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="418b4-106">U ovoj temi nalaze se informacije o priznavanju prihoda u aplikaciji Project Operations.</span><span class="sxs-lookup"><span data-stu-id="418b4-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="418b4-107">Obračun transakcija za koje se upotrebljava način naplate vremena i materijala</span><span class="sxs-lookup"><span data-stu-id="418b4-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="418b4-108">Priznavanje troškova i prihoda povezano je.</span><span class="sxs-lookup"><span data-stu-id="418b4-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="418b4-109">Troškovi transakcije i nenaplaćene prodaje knjiže se s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="418b4-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="418b4-110">Profil troškova i prihoda projekta određuje jesu li nenaplaćene prodajne transakcije knjižene u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="418b4-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="418b4-111">Ako je odabran **Akumulirani prihod**, sustav tijekom knjiženja upotrebljava račune **WIP prodajna vrijednost** i **Prodajna vrijednost akumuliranog prihoda**.</span><span class="sxs-lookup"><span data-stu-id="418b4-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="418b4-112">Slijedi primjer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="418b4-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="418b4-113">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="418b4-113">Transaction type</span></span> | <span data-ttu-id="418b4-114">Terećenje/kredit</span><span class="sxs-lookup"><span data-stu-id="418b4-114">Debit/Credit</span></span> | <span data-ttu-id="418b4-115">Iznos</span><span class="sxs-lookup"><span data-stu-id="418b4-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="418b4-116">WIP prodajna vrijednost</span><span class="sxs-lookup"><span data-stu-id="418b4-116">WIP Sales value</span></span> | <span data-ttu-id="418b4-117">Terećenje</span><span class="sxs-lookup"><span data-stu-id="418b4-117">Debit</span></span> | <span data-ttu-id="418b4-118">100</span><span class="sxs-lookup"><span data-stu-id="418b4-118">100</span></span> |
  | <span data-ttu-id="418b4-119">Prodajna vrijednost akumuliranog prihoda</span><span class="sxs-lookup"><span data-stu-id="418b4-119">Accrued revenue sales value</span></span> | <span data-ttu-id="418b4-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="418b4-120">Credit</span></span> | <span data-ttu-id="418b4-121">100</span><span class="sxs-lookup"><span data-stu-id="418b4-121">100</span></span> |

- <span data-ttu-id="418b4-122">Prihod se priznaje tijekom fakturiranja.</span><span class="sxs-lookup"><span data-stu-id="418b4-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="418b4-123">Tijekom knjiženja sustav upotrebljava račun **Fakturirani prihod**.</span><span class="sxs-lookup"><span data-stu-id="418b4-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="418b4-124">Slijedi primjer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="418b4-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="418b4-125">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="418b4-125">Transaction type</span></span> | <span data-ttu-id="418b4-126">Terećenje/kredit</span><span class="sxs-lookup"><span data-stu-id="418b4-126">Debit/Credit</span></span> | <span data-ttu-id="418b4-127">Iznos</span><span class="sxs-lookup"><span data-stu-id="418b4-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="418b4-128">Saldo klijenta</span><span class="sxs-lookup"><span data-stu-id="418b4-128">Customer balance</span></span> | <span data-ttu-id="418b4-129">Terećenje</span><span class="sxs-lookup"><span data-stu-id="418b4-129">Debit</span></span> | <span data-ttu-id="418b4-130">120</span><span class="sxs-lookup"><span data-stu-id="418b4-130">120</span></span> |
  | <span data-ttu-id="418b4-131">Plaća se porez na promet</span><span class="sxs-lookup"><span data-stu-id="418b4-131">Sales tax payable</span></span> | <span data-ttu-id="418b4-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="418b4-132">Credit</span></span> | <span data-ttu-id="418b4-133">20</span><span class="sxs-lookup"><span data-stu-id="418b4-133">20</span></span> |
  | <span data-ttu-id="418b4-134">Fakturirani prihod</span><span class="sxs-lookup"><span data-stu-id="418b4-134">Invoiced Revenue</span></span> | <span data-ttu-id="418b4-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="418b4-135">Credit</span></span> | <span data-ttu-id="418b4-136">100</span><span class="sxs-lookup"><span data-stu-id="418b4-136">100</span></span> |

- <span data-ttu-id="418b4-137">Ako je prihod nastao pri knjiženju nenaplaćene prodaje, sustav će pri fakturiranju stornirati prihod.</span><span class="sxs-lookup"><span data-stu-id="418b4-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="418b4-138">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="418b4-138">Transaction type</span></span> | <span data-ttu-id="418b4-139">Terećenje/kredit</span><span class="sxs-lookup"><span data-stu-id="418b4-139">Debit/Credit</span></span> | <span data-ttu-id="418b4-140">Iznos</span><span class="sxs-lookup"><span data-stu-id="418b4-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="418b4-141">WIP prodajna vrijednost</span><span class="sxs-lookup"><span data-stu-id="418b4-141">WIP Sales value</span></span> | <span data-ttu-id="418b4-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="418b4-142">Credit</span></span> | <span data-ttu-id="418b4-143">100</span><span class="sxs-lookup"><span data-stu-id="418b4-143">100</span></span> |
  | <span data-ttu-id="418b4-144">Prodajna vrijednost akumuliranog prihoda</span><span class="sxs-lookup"><span data-stu-id="418b4-144">Accrued revenue sales value</span></span> | <span data-ttu-id="418b4-145">Terećenje</span><span class="sxs-lookup"><span data-stu-id="418b4-145">Debit</span></span> | <span data-ttu-id="418b4-146">100</span><span class="sxs-lookup"><span data-stu-id="418b4-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="418b4-147">Obračun transakcija za koje se upotrebljava način naplate fiksnom cijenom</span><span class="sxs-lookup"><span data-stu-id="418b4-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="418b4-148">Priznavanje troškova i prihoda odvojeno je.</span><span class="sxs-lookup"><span data-stu-id="418b4-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="418b4-149">Troškovi transakcije knjiže se s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="418b4-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="418b4-150">Nenaplaćene se prodajne transakcije ne stvaraju.</span><span class="sxs-lookup"><span data-stu-id="418b4-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="418b4-151">Prihod se može priznati tijekom fakturiranja ako profil troškova i prihoda projekta ima **Načelo upotrijebljeno za izračun završetka projekta** postavljeno na **Bez WIP-a**.</span><span class="sxs-lookup"><span data-stu-id="418b4-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="418b4-152">Ovaj način upotrebljavajte samo za kratkoročne, jednostavne projekte.</span><span class="sxs-lookup"><span data-stu-id="418b4-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="418b4-153">Prihod se može priznati s pomoću procjene prihoda od fiksne cijene, bilo načinom **Ugovor dovršen** ili **Priznavanje prihoda od postotka dovršenosti**.</span><span class="sxs-lookup"><span data-stu-id="418b4-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="418b4-154">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="418b4-154">Additional resources</span></span>
[<span data-ttu-id="418b4-155">Konfiguriranje računovodstva za naplative proizvode iz projekata</span><span class="sxs-lookup"><span data-stu-id="418b4-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="418b4-156">Projekti s procjenom prihoda od fiksne cijene</span><span class="sxs-lookup"><span data-stu-id="418b4-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="418b4-157">Upravljanje procjenama prihoda</span><span class="sxs-lookup"><span data-stu-id="418b4-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="418b4-158">Načini troškova do završetka</span><span class="sxs-lookup"><span data-stu-id="418b4-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]