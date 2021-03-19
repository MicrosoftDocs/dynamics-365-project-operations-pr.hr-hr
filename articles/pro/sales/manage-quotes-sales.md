---
title: Upravljanje ponudama projekta
description: Ova tema pruža informacije o ponudama projekta.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272919"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="b5bf2-103">Upravljanje ponudama projekta</span><span class="sxs-lookup"><span data-stu-id="b5bf2-103">Manage project quotes</span></span>

<span data-ttu-id="b5bf2-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b5bf2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5bf2-105">U aplikaciji Dynamics 365 Project Operations, ponude projekta osmišljene su kako bi pomogle pri izradi prijedloga za rad na projektu.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="b5bf2-106">Struktura ponude projekta u aplikaciji Project Operations strukturirana je za ponude projekta sa sljedećim komponentama:</span><span class="sxs-lookup"><span data-stu-id="b5bf2-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="b5bf2-107">Redci ponude koji identificiraju određene komponente posla koje će se predstaviti kao komponente visoke razine.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="b5bf2-108">Pojedinosti retka ponude koje identificiraju i procjenjuju posao za svaku komponentu ili redak ponude visoke razine.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="b5bf2-109">Raspored ili procjene datuma i financijski aspekti posla vezani su uz redak ponude.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="b5bf2-110">Modeli ugovaranja i naplatne komponente postavljaju se za svaki redak ponude.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="b5bf2-111">Ova postavka pomaže u procjeni razvijanja prihoda, potrošnje i profitabilnosti za svaki redak ponude i ukupnu ponudu.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="b5bf2-112">Prikaz svih ponuda koje se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="b5bf2-112">View all project-based quotes</span></span>

<span data-ttu-id="b5bf2-113">Popis svih ponuda projekta mogu se vidjeti na stranici s popisom **Ponude**.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="b5bf2-114">Idite na **Prodaja** > **Ponude**.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="b5bf2-115">Prikazan je popis svih vaših ponuda projekta u sustavu.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="b5bf2-116">Upotrijebite **Preklopnik prikaza** za odabir ostalih filtriranih prikaza ponuda.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="b5bf2-117">S pomoću prilagođenih kriterija filtra možete konfigurirati vlastite prikaze i mogućnosti navigacije.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="b5bf2-118">Ponude se mogu stvoriti ili izbrisati s ove stranice s popisom ili stranica s pojedinostima.</span><span class="sxs-lookup"><span data-stu-id="b5bf2-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]