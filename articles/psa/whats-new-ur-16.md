---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 16, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006772"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="bee13-103">Project Service Automation, izdanje ažuriranja 16, V3</span><span class="sxs-lookup"><span data-stu-id="bee13-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bee13-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bee13-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bee13-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="bee13-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="bee13-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bee13-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bee13-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="bee13-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="bee13-108">Dodatne informacije potražite u članku [Instaliranje i ažuriranje željenog rješenja](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="bee13-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="bee13-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 16.</span><span class="sxs-lookup"><span data-stu-id="bee13-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="bee13-110">Broj izrade ove verzije jest V3.10.6.34, a ona je uglavnom dostupna putem samostalnog ažuriranja u siječnju 2020.</span><span class="sxs-lookup"><span data-stu-id="bee13-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="bee13-111">Izdanje ažuriranja 16</span><span class="sxs-lookup"><span data-stu-id="bee13-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bee13-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="bee13-112">Bug fixes</span></span>

-   <span data-ttu-id="bee13-113">Vrijeme i trošak</span><span class="sxs-lookup"><span data-stu-id="bee13-113">Time and Expense</span></span>

    -   <span data-ttu-id="bee13-114">Popravljeno: Korisnici koji pokušavaju poslati izbrisane unose vremena i troškova za odobrenja sada će primati odgovarajuće poruke o pogrešci.</span><span class="sxs-lookup"><span data-stu-id="bee13-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="bee13-115">Upravljanje projektom</span><span class="sxs-lookup"><span data-stu-id="bee13-115">Project Management</span></span>

    -   <span data-ttu-id="bee13-116">Popravljeno: Obrasci koji se primjenjuju na novi projekt uvažavaju jedinice za resurse koje su u predlošcima definirane za članove tima.</span><span class="sxs-lookup"><span data-stu-id="bee13-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="bee13-117">Popravljeno: Poboljšano rukovanje ponovnim dodjeljivanjem vlasništva nad zapisima.</span><span class="sxs-lookup"><span data-stu-id="bee13-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="bee13-118">Popravljeno: Projekti koji su u fazi kopiranja neće se moći kopirati dok se ne dovrše sve radnje kopiranja.</span><span class="sxs-lookup"><span data-stu-id="bee13-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="bee13-119">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="bee13-119">Resource Management</span></span>

    -   <span data-ttu-id="bee13-120">Popravljeno: Produžene rezervacije sada ispravno upravljaju kratkim periodima i više ne stvara nula sati za produžene rezervacije.</span><span class="sxs-lookup"><span data-stu-id="bee13-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="bee13-121">Popravljeno: Prikaz usklađivanja sada se prikazuje kada je vremenska zona projekta +5:30 GMT, a vremenska zona korisnika je drugačija.</span><span class="sxs-lookup"><span data-stu-id="bee13-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="bee13-122">Sales</span><span class="sxs-lookup"><span data-stu-id="bee13-122">Sales</span></span>

    -   <span data-ttu-id="bee13-123">Popravljeno: Kada se ukloni projekt mapiran na redak ugovora i mapira se novi projekt, stvarni zapisi o novom projektu nisu preispitani na temelju pravila za naplatu i cijenu definiranih u retku ugovora.</span><span class="sxs-lookup"><span data-stu-id="bee13-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="bee13-124">To je popravljeno u ovom izdanju.</span><span class="sxs-lookup"><span data-stu-id="bee13-124">This has been fixed in this release.</span></span> <span data-ttu-id="bee13-125">Cijene i stvarni zapisi novomapiranog projekta poništit će se i ponovno ispravno stvoriti na temelju pravila o cijenama i naplatama iz retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="bee13-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="bee13-126">Stvarni zapisi projekta koji nije mapiran također će se preispitati i posljedično ponovno stvoriti.</span><span class="sxs-lookup"><span data-stu-id="bee13-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="bee13-127">Popravljeno: Dodatna provjera dodana je polju **Iznos** retka procjene kako bi se osiguralo da se ne zadrže nulte vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="bee13-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="bee13-128">Popravljeno: Kada su u projektu ažurirani stvarni podaci, glavnom obrascu projekta dodaje se gumb za osvježavanje kako bi se korisnicima omogućilo da ponovno sinkroniziraju stvarne podatke.</span><span class="sxs-lookup"><span data-stu-id="bee13-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="bee13-129">Popravljeno: Kada korisnici izvrše nadogradnju s verzije 2.X na verziju 3.X, za naziv projekta dopušteni su projekti s vrijednošću NULL.</span><span class="sxs-lookup"><span data-stu-id="bee13-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]