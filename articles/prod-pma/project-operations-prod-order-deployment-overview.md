---
title: Pregled implementacije aplikacije Project Operations za scenarije koji se temelje na zalihama/proizvodnji
description: U ovoj temi nalaze se informacije o vrsti implementacije, aplikaciji Project Operations za scenarije koji se temelje na zalihama / proizvodnji.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b2a606bc587b99c16d45b19689ba90b422c3c62
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999392"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="c1f9b-103">Pregled implementacije aplikacije Project Operations za scenarije koji se temelje na zalihama/proizvodnji</span><span class="sxs-lookup"><span data-stu-id="c1f9b-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="c1f9b-104">_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_</span><span class="sxs-lookup"><span data-stu-id="c1f9b-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="c1f9b-105">Ova vrsta implementacije ima sljedeće mogućnosti za tvrtke koje se temelje na projektu:</span><span class="sxs-lookup"><span data-stu-id="c1f9b-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="c1f9b-106">Planiranje projekta s pomoću [strukturna analiza rada](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="c1f9b-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="c1f9b-107">Nabavka i trošenje zalihe inventara za projekte</span><span class="sxs-lookup"><span data-stu-id="c1f9b-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="c1f9b-108">Upravljanje prodajom koja se temelji na projektu s pomoću modula **Prodaja i marketing** u aplikacijama Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1f9b-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="c1f9b-109">Cijene i troškovi projekta primjenjuju konfiguracije cijene troška i cijene naplate u aplikacijama Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1f9b-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="c1f9b-110">Upravljanje resursima za projekt u aplikacijama Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1f9b-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="c1f9b-111">Praćenje vremena i napretka projekta u aplikacijama Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1f9b-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="c1f9b-112">Iskustva upravljanja troškovima na projektu i izvan projekta dohvaćanjem potvrde s pomoću mogućnosti OCR-a</span><span class="sxs-lookup"><span data-stu-id="c1f9b-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="c1f9b-113">Fakturiranje s pomoću poreza na promet klase poduzeća i sustava tečaja koji su na snazi na određeni datum</span><span class="sxs-lookup"><span data-stu-id="c1f9b-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="c1f9b-114">Grupe projekata koje se mogu konfigurirati za WIP računovodstvo i akumulacije</span><span class="sxs-lookup"><span data-stu-id="c1f9b-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="c1f9b-115">Priznavanje prihoda za projekte</span><span class="sxs-lookup"><span data-stu-id="c1f9b-115">Project revenue recognition</span></span>

<span data-ttu-id="c1f9b-116">Ova vrsta implementacije također omogućuje proširenje na funkcionalnost koju pružaju aplikacije Dynamics 365 Finance i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c1f9b-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="c1f9b-117">Odaberite ovu vrstu implementacije za uporabu aplikacije Dynamics 365 Project Operations tijekom punog životnog ciklusa projekta, uključujući sljedeće preduvjete:</span><span class="sxs-lookup"><span data-stu-id="c1f9b-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="c1f9b-118">Opsežni sustav upravljanja projektima koji upravlja inventariziranim stavkama i troškovima naloga / radnih naloga za interne i naplative projekte za rokove i financije.</span><span class="sxs-lookup"><span data-stu-id="c1f9b-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="c1f9b-119">Tvrtka ili ustanova već ima aplikaciju Dynamics 365 Finance ili Dynamics 365 Supply Chain i proizvodne aplikacije, a integriranje transakcija koje se temelje na projektu pojednostavit će pristup podacima i potrebe izvješćivanja.</span><span class="sxs-lookup"><span data-stu-id="c1f9b-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="c1f9b-120">Potpuno funkcionalan sustav upravljanja troškovima koji uključuje provođenje politika i naknade za praćenje troškova na projektu i izvan projekta.</span><span class="sxs-lookup"><span data-stu-id="c1f9b-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="c1f9b-121">Porez na promet u klasi poduzeća i modul deviznog tečaja za generiranje faktura za projekte za klijente.</span><span class="sxs-lookup"><span data-stu-id="c1f9b-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="c1f9b-122">Međunarodni standardi financijskog izvješćivanja (MSFI) usklađeni s računovodstvom projekta i sustavom priznavanja prihoda.</span><span class="sxs-lookup"><span data-stu-id="c1f9b-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]