---
title: Upravljanje ugovorima o projektu
description: U ovoj temi nalaze se informacije o načinu prikazivanja ugovora koji se temelje na projektu.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e2f182f66bd1f4fe57d19e4bf82525ac8b84c29
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003082"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="c81ef-103">Upravljanje ugovorima o projektu</span><span class="sxs-lookup"><span data-stu-id="c81ef-103">Manage project contracts</span></span>

<span data-ttu-id="c81ef-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="c81ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c81ef-105">Ugovori o projektu u aplikaciji Dynamics 365 Project Operations dohvaćaju i upravljaju ugovorno dogovorenim obvezama i pojedinostima o naplati projekta.</span><span class="sxs-lookup"><span data-stu-id="c81ef-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="c81ef-106">Struktura ugovora o projektu u aplikaciji Project Operations prilagođena je poslu koji se temelji na projektu sa sljedećim komponentama:</span><span class="sxs-lookup"><span data-stu-id="c81ef-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="c81ef-107">Redci ugovora koji identificiraju određene komponente posla koje će se na fakturi za projekt predstaviti kao komponente visoke razine.</span><span class="sxs-lookup"><span data-stu-id="c81ef-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="c81ef-108">Pojedinosti retka ugovora koje identificiraju i procjenjuju posao za svaku komponentu ili redak ugovora visoke razine.</span><span class="sxs-lookup"><span data-stu-id="c81ef-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="c81ef-109">Procjena uključuje raspored i financijske aspekte posla vezanog uz redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="c81ef-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="c81ef-110">Modeli ugovaranja i naplative komponente postavljaju se za svaki redak ugovora koji sadrži način naplate za svaki redak ugovora i cjelokupni ugovor.</span><span class="sxs-lookup"><span data-stu-id="c81ef-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="c81ef-111">Prikaz ugovora koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="c81ef-111">View all project-based contracts</span></span>

<span data-ttu-id="c81ef-112">Popis svih ugovora o projektu koji se mogu vidjeti na stranici s popisom **Ugovori**.</span><span class="sxs-lookup"><span data-stu-id="c81ef-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="c81ef-113">Idite na **Prodaja** > **Ugovori**.</span><span class="sxs-lookup"><span data-stu-id="c81ef-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="c81ef-114">Prikazan je popis svih vaših ugovora o projektu u sustavu.</span><span class="sxs-lookup"><span data-stu-id="c81ef-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="c81ef-115">Odaberite **Preklopnik prikaza** (strelica padajućeg izbornika pokraj naziva prikaza) za odabir ostalih filtriranih prikaza.</span><span class="sxs-lookup"><span data-stu-id="c81ef-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="c81ef-116">Možete stvoriti vlastite prikaze s prilagođenim kriterijima filtra.</span><span class="sxs-lookup"><span data-stu-id="c81ef-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="c81ef-117">Ugovori se mogu stvoriti ili izbrisati s ove stranice s popisom ili stranica s pojedinostima.</span><span class="sxs-lookup"><span data-stu-id="c81ef-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]