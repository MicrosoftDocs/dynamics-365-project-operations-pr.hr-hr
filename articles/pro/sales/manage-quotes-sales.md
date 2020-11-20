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
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177817"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="a4dd9-103">Upravljanje ponudama projekta</span><span class="sxs-lookup"><span data-stu-id="a4dd9-103">Manage project quotes</span></span>

<span data-ttu-id="a4dd9-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="a4dd9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a4dd9-105">U aplikaciji Dynamics 365 Project Operations, ponude projekta osmišljene su kako bi pomogle pri izradi prijedloga za rad na projektu.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="a4dd9-106">Struktura ponude projekta u aplikaciji Project Operations strukturirana je za ponude projekta sa sljedećim komponentama:</span><span class="sxs-lookup"><span data-stu-id="a4dd9-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="a4dd9-107">Redci ponude koji identificiraju određene komponente posla koje će se predstaviti kao komponente visoke razine.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="a4dd9-108">Pojedinosti retka ponude koje identificiraju i procjenjuju posao za svaku komponentu ili redak ponude visoke razine.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="a4dd9-109">Raspored ili procjene datuma i financijski aspekti posla vezani su uz redak ponude.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="a4dd9-110">Modeli ugovaranja i naplatne komponente postavljaju se za svaki redak ponude.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="a4dd9-111">Ova postavka pomaže u procjeni razvijanja prihoda, potrošnje i profitabilnosti za svaki redak ponude i ukupnu ponudu.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="a4dd9-112">Prikaz svih ponuda koje se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="a4dd9-112">View all project-based quotes</span></span>

<span data-ttu-id="a4dd9-113">Popis svih ponuda projekta mogu se vidjeti na stranici s popisom **Ponude**.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="a4dd9-114">Idite na **Prodaja** > **Ponude**.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="a4dd9-115">Prikazan je popis svih vaših ponuda projekta u sustavu.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="a4dd9-116">Upotrijebite **Preklopnik prikaza** za odabir ostalih filtriranih prikaza ponuda.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="a4dd9-117">S pomoću prilagođenih kriterija filtra možete konfigurirati vlastite prikaze i mogućnosti navigacije.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="a4dd9-118">Ponude se mogu stvoriti ili izbrisati s ove stranice s popisom ili stranica s pojedinostima.</span><span class="sxs-lookup"><span data-stu-id="a4dd9-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
