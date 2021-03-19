---
title: Pregled implementacije aplikacije Project Operations za scenarije koji se temelje na zalihama/proizvodnji
description: U ovoj temi nalaze se informacije o vrsti implementacije, aplikaciji Project Operations za scenarije koji se temelje na zalihama / proizvodnji.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ffbcb326e5cd86c49b3b3b27ce7d68404a6842b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289225"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="d01f4-103">Pregled implementacije aplikacije Project Operations za scenarije koji se temelje na zalihama/proizvodnji</span><span class="sxs-lookup"><span data-stu-id="d01f4-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="d01f4-104">_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_</span><span class="sxs-lookup"><span data-stu-id="d01f4-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="d01f4-105">Ova vrsta implementacije ima sljedeće mogućnosti za tvrtke koje se temelje na projektu:</span><span class="sxs-lookup"><span data-stu-id="d01f4-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="d01f4-106">Planiranje projekta s pomoću [strukturna analiza rada](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="d01f4-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="d01f4-107">Nabavka i trošenje zalihe inventara za projekte</span><span class="sxs-lookup"><span data-stu-id="d01f4-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="d01f4-108">Upravljanje prodajom koja se temelji na projektu s pomoću modula **Prodaja i marketing** u aplikacijama Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d01f4-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="d01f4-109">Cijene i troškovi projekta primjenjuju konfiguracije cijene troška i cijene naplate u aplikacijama Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d01f4-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="d01f4-110">Upravljanje resursima za projekt u aplikacijama Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d01f4-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="d01f4-111">Praćenje vremena i napretka projekta u aplikacijama Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d01f4-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="d01f4-112">Iskustva upravljanja troškovima na projektu i izvan projekta dohvaćanjem potvrde s pomoću mogućnosti OCR-a</span><span class="sxs-lookup"><span data-stu-id="d01f4-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="d01f4-113">Fakturiranje s pomoću poreza na promet klase poduzeća i sustava tečaja koji su na snazi na određeni datum</span><span class="sxs-lookup"><span data-stu-id="d01f4-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="d01f4-114">Grupe projekata koje se mogu konfigurirati za WIP računovodstvo i akumulacije</span><span class="sxs-lookup"><span data-stu-id="d01f4-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="d01f4-115">Priznavanje prihoda za projekte</span><span class="sxs-lookup"><span data-stu-id="d01f4-115">Project revenue recognition</span></span>

<span data-ttu-id="d01f4-116">Ova vrsta implementacije također omogućuje proširenje na funkcionalnost koju pružaju aplikacije Dynamics 365 Finance i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d01f4-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="d01f4-117">Odaberite ovu vrstu implementacije za uporabu aplikacije Dynamics 365 Project Operations tijekom punog životnog ciklusa projekta, uključujući sljedeće preduvjete:</span><span class="sxs-lookup"><span data-stu-id="d01f4-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="d01f4-118">Opsežni sustav upravljanja projektima koji upravlja inventariziranim stavkama i troškovima naloga / radnih naloga za interne i naplative projekte za rokove i financije.</span><span class="sxs-lookup"><span data-stu-id="d01f4-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="d01f4-119">Tvrtka ili ustanova već ima aplikaciju Dynamics 365 Finance ili Dynamics 365 Supply Chain i proizvodne aplikacije, a integriranje transakcija koje se temelje na projektu pojednostavit će pristup podacima i potrebe izvješćivanja.</span><span class="sxs-lookup"><span data-stu-id="d01f4-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="d01f4-120">Potpuno funkcionalan sustav upravljanja troškovima koji uključuje provođenje politika i naknade za praćenje troškova na projektu i izvan projekta.</span><span class="sxs-lookup"><span data-stu-id="d01f4-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="d01f4-121">Porez na promet u klasi poduzeća i modul deviznog tečaja za generiranje faktura za projekte za klijente.</span><span class="sxs-lookup"><span data-stu-id="d01f4-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="d01f4-122">Međunarodni standardi financijskog izvješćivanja (MSFI) usklađeni s računovodstvom projekta i sustavom priznavanja prihoda.</span><span class="sxs-lookup"><span data-stu-id="d01f4-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]