---
title: Učinkovitost planiranja projektnih resursa
description: U ovoj temi nalaze se informacije o tome kako poboljšati učinkovitost planiranja resursa za velik broj projekata.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073371"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="7fcd4-103">Učinkovitost planiranja projektnih resursa</span><span class="sxs-lookup"><span data-stu-id="7fcd4-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="7fcd4-104">Problemi učinkovitosti koji se odnose na planiranje resursa mogu se pojaviti kada broj projekata dosegne tisuće.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="7fcd4-105">Kako biste poboljšali učinkovitost planiranja resursa, dostupna je značajka koja omogućuje korisnicima da smanje vrijeme potrebno za pokretanje obrasca dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="7fcd4-106">Točnije, ovo uklanja postupak skupnog usklađivanja kapaciteta resursa i upotrebljava tablicu **ResProjectResource** za ubrzavanje pretraživanja resursa.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="7fcd4-107">Imajte na umu kako se tablica **ResRollup** više neće upotrebljavati.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fcd4-108">Ako postoji ovisnost ili o procesu skupne sinkronizacije kapaciteta resursa ili o tablici **ResProjectResource** , nemojte upotrebljavati ovu značajku.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="7fcd4-109">Omogućivanje poboljšanje učinkovitosti planiranja resursa</span><span class="sxs-lookup"><span data-stu-id="7fcd4-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="7fcd4-110">Kako biste omogućili poboljšanje učinkovitosti planiranja resursa, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="7fcd4-111">Idite na **Upravljanje značajkama** > **Sve** i na popisu značajki pronađite **Omogući značajku poboljšanja učinkovitosti planiranja resursa projekta**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="7fcd4-112">Odaberite **Omogući odmah**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="7fcd4-113">Ako na popisu ne možete pronaći značajku, odaberite **Provjerite ima li ažuriranja** za osvježavanje popisa.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="7fcd4-114">Osvježite svoj preglednik, a zatim idite na **Upravljanje projektima i računovodstvo** > **Povremeno** > **Resursi projekta** > **Sinkroniziraj kapacitet kalendara resursa u svim tvrtkama**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="7fcd4-115">Mogućnost **Ukloni postojeće zapise o kapacitetu** postavite na **Da** za uklanjanje prethodnih podataka.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="7fcd4-116">Ako želite generirati inkrementalne podatke, postavite mogućnost na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="7fcd4-117">U polju **Kod razdoblja** odaberite razdoblje u kojem će se generirati podaci.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="7fcd4-118">Ako odaberete kod razdoblja, datumi početka i završetka ne moraju biti definirani.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="7fcd4-119">Ako polje **Kod razdoblja** ostavite prazno, odaberite određene datume početka i završetka za generiranje podataka.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="7fcd4-120">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="7fcd4-121">Ovim će se u tablicu **ResCalendarCapacity** opći podaci distribuirati u sve tvrtke vašeg okruženja, tako da skupni posao treba izvoditi samo u jednoj pravnoj osobi.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="7fcd4-122">Podaci u ovom skupnom poslu potrebni su za izračunavanje kapaciteta resursa putem povezanog kalendara.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="7fcd4-123">Idite na **Upravljanje projektima i računovodstvo** > **Povremeno** > **Resursi projekta** > **Popuni projektne resurse u svim tvrtkama** , a zatim odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="7fcd4-124">Ovo je skripta za nadogradnju podataka za opće podatke u tablicama **ResProjectResource** , **ResCalendarDateTimeRange** i **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="7fcd4-125">Vrijednosti polja **PSAPRojSchedRole.RootActivity** također se ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="7fcd4-126">Ako se ovo ne pokrene, primit ćete upozorenje kada pokušate izvršiti operacije planiranja resursa.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="7fcd4-127">Isključivanje poboljšanja učinkovitosti planiranja resursa</span><span class="sxs-lookup"><span data-stu-id="7fcd4-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="7fcd4-128">Idite na **Upravljanje značajkama** > **Sve** i potražite mogućnost **Omogući značajku poboljšanja učinkovitosti planiranja resursa projekta**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="7fcd4-129">Odaberite značajku, a zatim odaberite gumb **Onemogući**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="7fcd4-130">Osvježite preglednik.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-130">Refresh your browser.</span></span>
4. <span data-ttu-id="7fcd4-131">Idite na **Upravljanje projektima i računovodstvo** > **Povremeno** > **Sinkronizacija kapaciteta** > **Sinkroniziraj skupnih vrijednosti kapaciteta resursa**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="7fcd4-132">Na stranici **Skupna sinkronizacija kapaciteta** mogućnost **Ukloni postojeće zapise o kapacitetu** postavite na **Da** za uklanjanje prethodnih podataka.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="7fcd4-133">Ako želite generirati inkrementalne podatke, postavite mogućnost na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="7fcd4-134">U polju **Kod razdoblja** odaberite razdoblje u kojem će se generirati podaci.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="7fcd4-135">Ako odaberete kod razdoblja, datumi početka i završetka ne moraju biti definirani.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="7fcd4-136">Ako polje **Kod razdoblja** ostavite prazno, odaberite određene datume početka i završetka za generiranje podataka.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="7fcd4-137">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="7fcd4-138">Ovim će se u tablicu **ResRollup** opći podaci distribuirati u sve tvrtke vašeg okruženja, tako da skupni posao treba izvoditi samo u jednoj pravnoj osobi.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="7fcd4-139">Ovaj skupni posao potreban je svim prikazima **Dostupnost resursa**.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="7fcd4-140">Ako se ovaj skupni posao ne pokrene, podaci **ResRollup** generirat će se u hodu, što može potrajati.</span><span class="sxs-lookup"><span data-stu-id="7fcd4-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
