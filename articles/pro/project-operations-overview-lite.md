---
title: Pregled osnovne implementacije
description: U ovoj temi nalaze se informacije o jednostavnoj implementaciji aplikacije Dynamics 365 Project Operations.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 9bd20d0bccb51e3afc0ad2d4a5409723c6fdcd92
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369952"
---
# <a name="lite-deployment-overview"></a><span data-ttu-id="04750-103">Pregled osnovne implementacije</span><span class="sxs-lookup"><span data-stu-id="04750-103">Lite deployment overview</span></span>

<span data-ttu-id="04750-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="04750-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="04750-105">Vrsta osnovne implementacije aplikacije Dynamics 365 Project Operations ima sljedeće mogućnosti za tvrtke koje se temelje na projektu:</span><span class="sxs-lookup"><span data-stu-id="04750-105">The Lite deployment type of Dynamics 365 Project Operations has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="04750-106">Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu</span><span class="sxs-lookup"><span data-stu-id="04750-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="04750-107">Višedimenzionalno određivanje cijena i troškova za radne resurse</span><span class="sxs-lookup"><span data-stu-id="04750-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="04750-108">Određivanje cijena kategorija troškova na temelju kategorije</span><span class="sxs-lookup"><span data-stu-id="04750-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="04750-109">Upravljanje prodajom na temelju projekta s pomoću mogućnosti aplikacije Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="04750-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="04750-110">Universal resource scheduling koji se integrira s drugim aplikacijama poput aplikacija Dynamics 365 Field Service i Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="04750-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="04750-111">Praćenje vremena i napretka projekta</span><span class="sxs-lookup"><span data-stu-id="04750-111">Project progress and time tracking</span></span>
- <span data-ttu-id="04750-112">Praćenje osnovnih troškova za troškove koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="04750-112">Basic expense tracking for project-based expenses</span></span>
- <span data-ttu-id="04750-113">Izrada predračuna koji se može pregledati i poslati financijskom sustavu na obradu</span><span class="sxs-lookup"><span data-stu-id="04750-113">Proforma invoicing that can be reviewed and sent to a financial system for processing</span></span>
- <span data-ttu-id="04750-114">Proširivost kroz aplikaciju Power Platform</span><span class="sxs-lookup"><span data-stu-id="04750-114">Extensibility through the Power Platform</span></span>

<span data-ttu-id="04750-115">Upotrijebite ovu vrstu implementacije ako od aplikacije Project Operations očekujete da upotrijebi puni životni ciklus projekta, uključujući sljedeće preduvjete:</span><span class="sxs-lookup"><span data-stu-id="04750-115">Use this deployment type if your expectation from Project Operations is to use the full project lifecycle, including the following requirements:</span></span>

- <span data-ttu-id="04750-116">Mogućnost upravljanja prodajom koja se temelji na projektu s drugim vrstama prodaje uporabom mogućnosti u aplikaciji Prodaja.</span><span class="sxs-lookup"><span data-stu-id="04750-116">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="04750-117">Integrirani sustav koji upravlja internim i naplativim projektima za rasporede i financijska sredstva od prodaje projekata do fakturiranja.</span><span class="sxs-lookup"><span data-stu-id="04750-117">An integrated system that manages internal and billable projects for schedules and financials from project sales to invoicing.</span></span>
- <span data-ttu-id="04750-118">Planiranje resursa poduzeća od strane trećih (ERP / sustav financijskog računovodstva za integraciju s aplikacijom Project Operations.</span><span class="sxs-lookup"><span data-stu-id="04750-118">A third-party Enterprise resource planning (ERP/Financial accounting system to integrate with Project Operations.</span></span>
- <span data-ttu-id="04750-119">Sustav treće strane za rad s porezima na promet, tečajevima, naknadama troškova i troškovima koji se ne odnose na projekt.</span><span class="sxs-lookup"><span data-stu-id="04750-119">A third-party system to work with sales taxes, exchange rates, expense reimbursements, and non-project expenses.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]