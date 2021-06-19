---
title: Skupovi odobrenja
description: U ovoj temi nalaze se informacije o skupu odobrenja, zahtjevima i podskupovima tih operacija.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116862"
---
# <a name="approval-sets"></a><span data-ttu-id="a3a42-103">Skupovi odobrenja</span><span class="sxs-lookup"><span data-stu-id="a3a42-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a3a42-104">Skupovi odobrenja grupiraju zahtjeve za odobrenja u manje podskupove operacija.</span><span class="sxs-lookup"><span data-stu-id="a3a42-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="a3a42-105">Ovo grupiranje omogućuje obradu odobrenja redoslijedom po projektu i omogućuje ponovni pokušaj i redoslijed.</span><span class="sxs-lookup"><span data-stu-id="a3a42-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="a3a42-106">Grupiranje poboljšava pouzdanost i sljedivost obrade odobrenja za velike količine odobrenja.</span><span class="sxs-lookup"><span data-stu-id="a3a42-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="a3a42-107">Skupovi odobrenja pokazuju cjelokupno stanje obrade njihovih povezanih zapisa.</span><span class="sxs-lookup"><span data-stu-id="a3a42-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="a3a42-108">Kada se zapis o odobrenju obrađuje s pomoću skupa odobrenja, zapis se pomiče iz stanja **Poslan** u stanje **Odobren** i prekida mu se veza iz skupa odobrenja.</span><span class="sxs-lookup"><span data-stu-id="a3a42-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="a3a42-109">Ako zapis ne uspije kad se pošalje na odobrenje, on ostaje u stanju **Poslan**, a skup odobrenja označava se kao neuspješan.</span><span class="sxs-lookup"><span data-stu-id="a3a42-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="a3a42-110">Skup odobrenja zapisuje poruku o pogrešci neuspjeha.</span><span class="sxs-lookup"><span data-stu-id="a3a42-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="a3a42-111">Obrada odobrenja i skupova odobrenja</span><span class="sxs-lookup"><span data-stu-id="a3a42-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="a3a42-112">Odobrenja koja su u redu čekanja za obradu vidljiva su u prikazu **Odobrenja za obradu**.</span><span class="sxs-lookup"><span data-stu-id="a3a42-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="a3a42-113">Sustav pokušava sinkronizirano više puta obraditi sve unose, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspjeli.</span><span class="sxs-lookup"><span data-stu-id="a3a42-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="a3a42-114">Polje **Vijek trajanja skupa odobrenja** bilježi broj preostalih pokušaja obrade skupa prije nego što se označi kao neuspješan.</span><span class="sxs-lookup"><span data-stu-id="a3a42-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="a3a42-115">Neuspjela odobrenja i skupovi odobrenja</span><span class="sxs-lookup"><span data-stu-id="a3a42-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="a3a42-116">Prikaz **Neuspjela odobrenja** navodi sva odobrenja koja zahtijevaju intervenciju korisnika.</span><span class="sxs-lookup"><span data-stu-id="a3a42-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="a3a42-117">Otvorite povezane zapisnike skupa odobrenja kako biste identificirali uzrok neuspjeha.</span><span class="sxs-lookup"><span data-stu-id="a3a42-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="a3a42-118">Odabir **Pokušaj ponovno** pridodaje broj vijeka trajanja odobrenja, vraća skup odobrenja natrag u stanje **Obrada u tijeku** i pokušava obraditi preostale zapise.</span><span class="sxs-lookup"><span data-stu-id="a3a42-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="a3a42-119">Konfiguriranje skupova odobrenja</span><span class="sxs-lookup"><span data-stu-id="a3a42-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="a3a42-120">Omogućivanje značajke Skupovi odobrenja</span><span class="sxs-lookup"><span data-stu-id="a3a42-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="a3a42-121">Prije nego što omogućite značajku Skupovi odobrenja, utvrdite da u obradi trenutačno nema odobrenja.</span><span class="sxs-lookup"><span data-stu-id="a3a42-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a3a42-122">Idite na stranicu **Parametri projekta** i odaberite **Kontrola značajke** > **Omogući nova odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="a3a42-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="a3a42-123">Isključivanje značajke Skupovi odobrenja</span><span class="sxs-lookup"><span data-stu-id="a3a42-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="a3a42-124">Prije nego što isključite značajku Skupovi odobrenja, utvrdite da u obradi trenutačno nema odobrenja.</span><span class="sxs-lookup"><span data-stu-id="a3a42-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a3a42-125">Idite na stranicu **Parametri projekta** i odaberite **Kontrola značajke** > **Onemogući nova odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="a3a42-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="a3a42-126">Konfiguriranje asinkronog praga</span><span class="sxs-lookup"><span data-stu-id="a3a42-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="a3a42-127">Kada se stvaraju skupovi odobrenja, obrada se pomiče u pozadinu nakon što odabrani broj zapisa za odobrenje premaši naznačeni prag.</span><span class="sxs-lookup"><span data-stu-id="a3a42-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="a3a42-128">Upotrijebite polje **Asinkroni prag** kako biste konfigurirali kada obradu odobrenja treba izvoditi sinkrono, a kada asinkrono.</span><span class="sxs-lookup"><span data-stu-id="a3a42-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="a3a42-129">Valjane vrijednosti su:</span><span class="sxs-lookup"><span data-stu-id="a3a42-129">Valid values are:</span></span>

  - <span data-ttu-id="a3a42-130">Nula: Svi se zahtjevi trebaju obrađivati asinkrono.</span><span class="sxs-lookup"><span data-stu-id="a3a42-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="a3a42-131">Brojevi veći od nule: Odobrenja se obrađuju asinkrono samo kada prijavljeni broj odobrenja premašuje ovu vrijednost.</span><span class="sxs-lookup"><span data-stu-id="a3a42-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
