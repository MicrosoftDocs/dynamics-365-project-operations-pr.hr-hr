---
title: Sinkroniziranje kapaciteta resursa
description: U ovoj temi nalaze se informacije o načinu sinkronizacije kapaciteta resursa u kalendarima i projektima.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997502"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="fa5b3-103">Sinkroniziranje kapaciteta resursa</span><span class="sxs-lookup"><span data-stu-id="fa5b3-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa5b3-104">Postupci sinkronizacije resursa pomažu kako bi se zajamčilo da se informacije za kalendar i osnovni kalendar slijevaju u planiranje resursa projekta.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="fa5b3-105">Ako se kalendar promijeni, postupci izvršavaju potrebna ažuriranja u planiranju projektnih resursa.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="fa5b3-106">Postupci također pomažu pri poboljšanju izvedbe jer se podaci o resursima kalendara unaprijed sinkroniziraju.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="fa5b3-107">Stoga se ažuriranja podataka o rasporedu resursa događaju brže.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="fa5b3-108">Preporučujemo da postupke planirate kao skupne, umjesto jednog po jednog.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="fa5b3-109">U suprotnom postoji opasnost da će netko zaboraviti uključene datume nakon posljednjeg sinkroniziranja podataka.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="fa5b3-110">Ako se ne upotrebljavaju uključeni datumi, može doći do praznina tijekom sinkronizacije datuma.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sinkronizacijski kalendara](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="fa5b3-112">Sinkronizacija skupnih vrijednosti kapaciteta resursa</span><span class="sxs-lookup"><span data-stu-id="fa5b3-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="fa5b3-113">Postupak sinkronizacije osmišljen je za sinkronizaciju svih podataka kalendara resursa.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="fa5b3-114">Te informacije uključuju osnovne podatke kalendara o svim promjenama u tablici kapaciteta kalendara resursa projekta.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="fa5b3-115">Ako se u projekt dodaju novi resursi, sinkronizacija pomaže zajamčiti dostupnost ažuriranih podataka kalendara.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="fa5b3-116">Ova se sinkronizacija može izvršiti u bilo kojem trenutku.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="fa5b3-117">Preporučujemo da upotrijebite skupinu.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-117">We recommend that you use a batch.</span></span> <span data-ttu-id="fa5b3-118">Tijekom sinkronizacije rezervacija kapaciteta dostupne su mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="fa5b3-119">Odaberite **Upravljanje projektima i računovodstvo** &gt; **Povremeno** &gt; **Sinkronizacija kapaciteta** &gt; **Sinkroniziraj skupnih vrijednosti kapaciteta resursa**.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="fa5b3-120">Postavite mogućnosti u sljedeću tablicu.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="fa5b3-121">Mogućnost</span><span class="sxs-lookup"><span data-stu-id="fa5b3-121">Option</span></span>      | <span data-ttu-id="fa5b3-122">Opis</span><span class="sxs-lookup"><span data-stu-id="fa5b3-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="fa5b3-123">Šifra razdoblja</span><span class="sxs-lookup"><span data-stu-id="fa5b3-123">Period code</span></span> | <span data-ttu-id="fa5b3-124">Po želji odaberite šifru intervala datuma glavne knjige kako biste postavili datume početka i završetka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="fa5b3-125">Datum početka</span><span class="sxs-lookup"><span data-stu-id="fa5b3-125">Start date</span></span>  | <span data-ttu-id="fa5b3-126">Unesite datum početka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="fa5b3-127">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="fa5b3-127">End date</span></span>    | <span data-ttu-id="fa5b3-128">Unesite datum završetka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="fa5b3-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="fa5b3-129">[![Postupak sinkronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="fa5b3-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]