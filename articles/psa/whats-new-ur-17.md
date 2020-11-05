---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 17, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073344"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="f80bd-103">Project Service Automation, izdanje ažuriranja 17, V3</span><span class="sxs-lookup"><span data-stu-id="f80bd-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="f80bd-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f80bd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f80bd-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="f80bd-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="f80bd-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f80bd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f80bd-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="f80bd-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="f80bd-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f80bd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f80bd-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 17.</span><span class="sxs-lookup"><span data-stu-id="f80bd-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="f80bd-110">Ova verzija ima broj međuverzije V3.10.6.34 i općenito je dostupna putem samostalnog ažuriranja iz ožujka 2020.</span><span class="sxs-lookup"><span data-stu-id="f80bd-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="f80bd-111">Izdanje ažuriranja 17</span><span class="sxs-lookup"><span data-stu-id="f80bd-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f80bd-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="f80bd-112">Bug fixes</span></span>

<span data-ttu-id="f80bd-113">**Općenito**</span><span class="sxs-lookup"><span data-stu-id="f80bd-113">**General**</span></span>

- <span data-ttu-id="f80bd-114">Popravljeno: Ažurirajte rješenje Project Service Automation kako biste primijenili licence za članove tima (Središte resursa projekta uključuje metapodatke 3.x plana usluge za člana tima)</span><span class="sxs-lookup"><span data-stu-id="f80bd-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="f80bd-115">**Vrijeme i trošak**</span><span class="sxs-lookup"><span data-stu-id="f80bd-115">**Time and Expense**</span></span>

- <span data-ttu-id="f80bd-116">Popravljeno: Procjenu rashoda nije moguće promijeniti s vrijednosti koja nije jednaka nuli na nulu (0).</span><span class="sxs-lookup"><span data-stu-id="f80bd-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="f80bd-117">Promjena se zanemaruje.</span><span class="sxs-lookup"><span data-stu-id="f80bd-117">The change is ignored.</span></span>

<span data-ttu-id="f80bd-118">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="f80bd-118">**Project Management**</span></span>

- <span data-ttu-id="f80bd-119">Popravljeno: U naziv položaja člana tima dodana je provjera za nulte vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="f80bd-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="f80bd-120">Popravljeno: Polje **msdyn_userresourceid** entiteta **msdyn_resourceassignment** je zastarjelo.</span><span class="sxs-lookup"><span data-stu-id="f80bd-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="f80bd-121">Popravljeno: Nadogradnja s verzije 2.x na verziju 3.x sada obrađuje prazne konture rada na dodijeljenim zadacima.</span><span class="sxs-lookup"><span data-stu-id="f80bd-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="f80bd-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f80bd-122">**Sales**</span></span>

- <span data-ttu-id="f80bd-123">Popravljeno: **Invoice.PreValidateInvoiceUpdate** sada obrađuje scenarij pravilne preraspodjele vlasnicima zapisa.</span><span class="sxs-lookup"><span data-stu-id="f80bd-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="f80bd-124">Popravljeno: Kad je klasa transakcije **Vrijeme** , stavka **UnitGroup** ne može se uređivati za sve subjekte, uključujući stavke **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** i **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="f80bd-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="f80bd-125">Međutim, **Unit** ne može se uređivati samo za stavke **JournalLine** i **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="f80bd-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


