---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 13, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 13, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: c328821064065e19938406856d327f690f577e7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000292"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="07590-103">Project Service Automation, izdanje ažuriranja 13, V3</span><span class="sxs-lookup"><span data-stu-id="07590-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="07590-104">Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="07590-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="07590-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="07590-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="07590-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="07590-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="07590-107">Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="07590-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="07590-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="07590-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="07590-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 13.</span><span class="sxs-lookup"><span data-stu-id="07590-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="07590-110">Broj izrade ove verzije jest V3.10.3.18, a ona je dostupna na sljedećem rasporedu:</span><span class="sxs-lookup"><span data-stu-id="07590-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="07590-111">**Opća dostupnost (samostalno ažuriranje):** studeni 2019.</span><span class="sxs-lookup"><span data-stu-id="07590-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="07590-112">**Automatsko ažuriranje:** prosinac 2019.</span><span class="sxs-lookup"><span data-stu-id="07590-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="07590-113">Izdanje ažuriranja 13</span><span class="sxs-lookup"><span data-stu-id="07590-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="07590-114">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="07590-114">Bug fixes</span></span>

- <span data-ttu-id="07590-115">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="07590-115">Time and Expense</span></span>

     - <span data-ttu-id="07590-116">Popravljeno: Funkcionalnost pretraživanja na stranici **Odobravanje troška** ne radi tijekom pretraživanja po svrsi troška.</span><span class="sxs-lookup"><span data-stu-id="07590-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="07590-117">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="07590-117">Resource Management</span></span>

     - <span data-ttu-id="07590-118">Popravljeno: Brojevi u usklađivanju ažurirani su kako bi se ispravno poredali.</span><span class="sxs-lookup"><span data-stu-id="07590-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="07590-119">Popravljeno: Imenovani resursi ne mogu se dodijeliti zadacima putem kartice **Raspored**.</span><span class="sxs-lookup"><span data-stu-id="07590-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="07590-120">Upravljanje projektom</span><span class="sxs-lookup"><span data-stu-id="07590-120">Project Management</span></span>

     - <span data-ttu-id="07590-121">Popravljeno: Iznimka nulte reference tijekom dodjeljivanja člana tima kada mogućnosti **VrstaTransakcije** nedostaje podataka o postavljanju za stavke **Jedinica** i **ZadanaGrupa**.</span><span class="sxs-lookup"><span data-stu-id="07590-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="07590-122">Sales</span><span class="sxs-lookup"><span data-stu-id="07590-122">Sales</span></span>

     - <span data-ttu-id="07590-123">Popravljeno: Dvostruki zapisi vrste transakcije vraćaju pogrešku kada se stvore zapisi o cijenama uloga.</span><span class="sxs-lookup"><span data-stu-id="07590-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="07590-124">Popravljeno: Dodatni gumbi za mogućnosti **Nova prilika**, **Ponuda**, **Redak narudžbe** i **Dodaj proizvod** vidljivi su u naredbama za Prilike, Ponude, Naručivanje proizvoda i podrešetki redaka koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="07590-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]