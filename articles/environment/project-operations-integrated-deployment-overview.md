---
title: Pregled implementacije aplikacije Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovoj temi nalaze se informacije o vrsti implementacije, aplikaciji Project Operations za scenarije koji se temelje na resursu / bez zaliha.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 770947835af41bd06c02ca08b6ed8e810b9bdcf8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289945"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="67544-103">Pregled implementacije aplikacije Project Operations za scenarije temeljene na resursima / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="67544-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="67544-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="67544-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="67544-105">Vrsta implementacije Dynamics 365 Project Operations za scenarije koji se temelje na resursima / bez zaliha ima sljedeće mogućnosti za tvrtke koje se temelje na projektu:</span><span class="sxs-lookup"><span data-stu-id="67544-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="67544-106">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="67544-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="67544-107">Višedimenzionalno određivanje cijena i troškova za radne resurse</span><span class="sxs-lookup"><span data-stu-id="67544-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="67544-108">Određivanje cijena kategorija troškova na temelju kategorije</span><span class="sxs-lookup"><span data-stu-id="67544-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="67544-109">Upravljanje prodajom na temelju projekta s pomoću mogućnosti aplikacije Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="67544-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="67544-110">Universal resource scheduling koji se integrira s drugim aplikacijama poput aplikacija Dynamics 365 Field Service i Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="67544-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="67544-111">Praćenje vremena i napretka projekta</span><span class="sxs-lookup"><span data-stu-id="67544-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="67544-112">Osnovno i potpuno iskustvo upravljanja troškovima na projektu i izvan projekta uključuje dohvaćanje potvrde s pomoću mogućnosti OCR-a</span><span class="sxs-lookup"><span data-stu-id="67544-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="67544-113">Fakturiranje koje se proteže od predračuna do fakture za klijenta, a podržano je porezom na promet klase poduzeća i sustavom deviznog tečaja koji djeluje na datum.</span><span class="sxs-lookup"><span data-stu-id="67544-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="67544-114">Troškovi projekta, profili prihoda i pravila za rad u tijeku (WIP, work in progress) računovodstvo i akumulacija</span><span class="sxs-lookup"><span data-stu-id="67544-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="67544-115">Priznavanje prihoda za projekte</span><span class="sxs-lookup"><span data-stu-id="67544-115">Project revenue recognition</span></span>
- <span data-ttu-id="67544-116">Proširivost kroz aplikaciju Power Platform</span><span class="sxs-lookup"><span data-stu-id="67544-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="67544-117">Ova vrsta implementacije omogućuje proširenje na funkcionalnost koju pružaju aplikacije Dynamics 365 Finance i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="67544-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="67544-118">Trebalo bi odabrati ovu implementaciju ako se od aplikacije Project Operations očekuje da upotrijebi puni životni ciklus projekta, koji uključuje sljedeće preduvjete:</span><span class="sxs-lookup"><span data-stu-id="67544-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="67544-119">Mogućnost upravljanja prodajom koja se temelji na projektu s drugim vrstama prodaje uporabom mogućnosti u aplikaciji Prodaja.</span><span class="sxs-lookup"><span data-stu-id="67544-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="67544-120">Integrirani sustav upravljanja projektom koji upravlja internim i naplativim projektima za rasporede i financijska sredstva od prodaje projekata do računovodstva.</span><span class="sxs-lookup"><span data-stu-id="67544-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="67544-121">Sustav upravljanja troškovima koji uključuje provođenje politika i naknade za praćenje troškova na projektu i izvan projekta.</span><span class="sxs-lookup"><span data-stu-id="67544-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="67544-122">Zahtijevajte sveobuhvatni poreza na promet u klasi poduzeća i modul deviznog tečaja za generiranje faktura za projekte za klijente.</span><span class="sxs-lookup"><span data-stu-id="67544-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="67544-123">Međunarodni standardi financijskog izvješćivanja (MSFI) usklađeni s računovodstvom projekta i sustavom priznavanja prihoda.</span><span class="sxs-lookup"><span data-stu-id="67544-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="67544-124">Aplikaciju Financije ili Supply Chain Management i integraciju transakcija koje se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="67544-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]