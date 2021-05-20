---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 14, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 14, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d0aeb4684ae04d8774a31a51664ceb84307b10d
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949361"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="04248-103">Project Service Automation, izdanje ažuriranja 14, V3</span><span class="sxs-lookup"><span data-stu-id="04248-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="04248-104">Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="04248-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="04248-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="04248-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="04248-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="04248-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="04248-107">Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="04248-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="04248-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="04248-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="04248-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 14.</span><span class="sxs-lookup"><span data-stu-id="04248-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="04248-110">Broj izrade ove verzije jest V3.10.4.21, a ona je dostupna na sljedećem rasporedu:</span><span class="sxs-lookup"><span data-stu-id="04248-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="04248-111">**Opća dostupnost (samostalno ažuriranje):** siječanj 2020.</span><span class="sxs-lookup"><span data-stu-id="04248-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="04248-112">**Automatsko ažuriranje:** veljača 2020.</span><span class="sxs-lookup"><span data-stu-id="04248-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="04248-113">Izdanje ažuriranja 14</span><span class="sxs-lookup"><span data-stu-id="04248-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="04248-114">Poboljšanja</span><span class="sxs-lookup"><span data-stu-id="04248-114">Enhancements</span></span>

- <span data-ttu-id="04248-115">Sales</span><span class="sxs-lookup"><span data-stu-id="04248-115">Sales</span></span>

     - <span data-ttu-id="04248-116">Prilagođene vrijednosti polja iz mogućnosti **Pojedinosti retka ponude** kopiraju se u mogućnost **Pojedinosti retka ugovora o projektu** kada se ponuda ažurirala na mogućnost **Zatvorena kao ostvarena**.</span><span class="sxs-lookup"><span data-stu-id="04248-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="04248-117">Potvrđeni projekti mogu biti **Zatvoreni kao izgubljeni**.</span><span class="sxs-lookup"><span data-stu-id="04248-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="04248-118">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="04248-118">Resource Management</span></span>

     - <span data-ttu-id="04248-119">Kada produžite rezervacije, od korisnika će se zatražiti s pomoću dijaloškog okvira za potvrdu da sažmu rezultate rezervacija i osiguraju vezu do mogućnosti Održavanje rezervacija.</span><span class="sxs-lookup"><span data-stu-id="04248-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="04248-120">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="04248-120">Bug fixes</span></span>

- <span data-ttu-id="04248-121">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="04248-121">Time and Expense</span></span>

     - <span data-ttu-id="04248-122">Popravljeno: Poboljšano korisničko iskustvo kada korisnik nije odabrao nijednu stavku koju treba ispraviti.</span><span class="sxs-lookup"><span data-stu-id="04248-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="04248-123">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="04248-123">Resource Management</span></span>

     - <span data-ttu-id="04248-124">Popravljeno: Višekratna rezervacija resursa preplavljuje ime resursa koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="04248-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="04248-125">Sales</span><span class="sxs-lookup"><span data-stu-id="04248-125">Sales</span></span>

     - <span data-ttu-id="04248-126">Popravljeno: Ukupna prodajna cijena se ne izračunava sve dok korisnik također ne unese cijenu koštanja procijenjenih troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="04248-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="04248-127">Popravljano: Zatvaranje ponude kao **Ostvarena** ne uspijeva ako povezani ugovorni za projekt nije u stanju **Skice**.</span><span class="sxs-lookup"><span data-stu-id="04248-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]