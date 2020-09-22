---
title: Novosti u aplikaciji Project Service Automation, izdanje ažuriranja 13, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 13, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750124"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="cd778-103">Project Service Automation V3, izdanje ažuriranja 13</span><span class="sxs-lookup"><span data-stu-id="cd778-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="cd778-104">Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="cd778-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="cd778-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="cd778-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cd778-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cd778-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cd778-107">Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="cd778-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="cd778-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cd778-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cd778-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 13.</span><span class="sxs-lookup"><span data-stu-id="cd778-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="cd778-110">Broj izrade ove verzije jest V3.10.3.18, a ona je dostupna na sljedećem rasporedu:</span><span class="sxs-lookup"><span data-stu-id="cd778-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="cd778-111">**Opća dostupnost (samostalno ažuriranje):** studeni 2019.</span><span class="sxs-lookup"><span data-stu-id="cd778-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="cd778-112">**Automatsko ažuriranje:** prosinac 2019.</span><span class="sxs-lookup"><span data-stu-id="cd778-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="cd778-113">Izdanje ažuriranja 13</span><span class="sxs-lookup"><span data-stu-id="cd778-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="cd778-114">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="cd778-114">Bug fixes</span></span>

- <span data-ttu-id="cd778-115">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="cd778-115">Time and Expense</span></span>

     - <span data-ttu-id="cd778-116">Popravljeno: Funkcionalnost pretraživanja na stranici **Odobravanje troška** ne radi tijekom pretraživanja po svrsi troška.</span><span class="sxs-lookup"><span data-stu-id="cd778-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="cd778-117">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="cd778-117">Resource Management</span></span>

     - <span data-ttu-id="cd778-118">Popravljeno: Brojevi u usklađivanju ažurirani su kako bi se ispravno poredali.</span><span class="sxs-lookup"><span data-stu-id="cd778-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="cd778-119">Popravljeno: Imenovani resursi ne mogu se dodijeliti zadacima putem kartice **Raspored**.</span><span class="sxs-lookup"><span data-stu-id="cd778-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="cd778-120">Upravljanje projektom</span><span class="sxs-lookup"><span data-stu-id="cd778-120">Project Management</span></span>

     - <span data-ttu-id="cd778-121">Popravljeno: Iznimka nulte reference tijekom dodjeljivanja člana tima kada mogućnosti **VrstaTransakcije** nedostaje podataka o postavljanju za stavke **Jedinica** i **ZadanaGrupa**.</span><span class="sxs-lookup"><span data-stu-id="cd778-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="cd778-122">Sales</span><span class="sxs-lookup"><span data-stu-id="cd778-122">Sales</span></span>

     - <span data-ttu-id="cd778-123">Popravljeno: Dvostruki zapisi vrste transakcije vraćaju pogrešku kada se stvore zapisi o cijenama uloga.</span><span class="sxs-lookup"><span data-stu-id="cd778-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="cd778-124">Popravljeno: Dodatni gumbi za mogućnosti **Nova prilika**, **Ponuda**, **Redak narudžbe** i **Dodaj proizvod** vidljivi su u naredbama za Prilike, Ponude, Naručivanje proizvoda i podrešetci redaka na temelju projekta.</span><span class="sxs-lookup"><span data-stu-id="cd778-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


