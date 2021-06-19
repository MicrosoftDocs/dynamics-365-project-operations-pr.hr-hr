---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 20, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 5562b1de1d655328cfbb22e46c7fed53525507b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006502"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="cce0a-103">Project Service Automation, izdanje ažuriranja 20, V3</span><span class="sxs-lookup"><span data-stu-id="cce0a-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cce0a-104">Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cce0a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cce0a-105">Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="cce0a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cce0a-106">Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cce0a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cce0a-107">Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="cce0a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cce0a-108">Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cce0a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cce0a-109">Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 20.</span><span class="sxs-lookup"><span data-stu-id="cce0a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="cce0a-110">Ova verzija ima broj međuverzije V 3.10.31.37 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="cce0a-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="cce0a-111">Izdanje ažuriranja 20</span><span class="sxs-lookup"><span data-stu-id="cce0a-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cce0a-112">Ispravke pogrešaka</span><span class="sxs-lookup"><span data-stu-id="cce0a-112">Bug fixes</span></span>

<span data-ttu-id="cce0a-113">**Upravljanje projektom**</span><span class="sxs-lookup"><span data-stu-id="cce0a-113">**Project Management**</span></span>

<span data-ttu-id="cce0a-114">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="cce0a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cce0a-115">Uvoz članova projektnog tima metodom raspodjele koja zahtijeva sate rezultira nejasnom porukom o pogrešci kada je navedeno nula sati.</span><span class="sxs-lookup"><span data-stu-id="cce0a-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="cce0a-116">Korisnici primaju neispravnu pogrešku kada je u polje **Opis** unesen maksimalni broj znakova za projektni zadatak.</span><span class="sxs-lookup"><span data-stu-id="cce0a-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="cce0a-117">Stranica **Preuzimanje dodatka za aplikaciju Microsoft Dynamics 365 Project Service Automation** preusmjerava na englesku stranicu za preuzimanje kada su postavke jezika korisnika postavljene na japanski.</span><span class="sxs-lookup"><span data-stu-id="cce0a-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="cce0a-118">Kada se dogodi pogreška na poslužitelju, oznaka za sinkronizaciju na kartici **Raspored** obrasca **Projekti** ponekad nedostaje.</span><span class="sxs-lookup"><span data-stu-id="cce0a-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="cce0a-119">Suvišna ažuriranja zadatka šalju se poslužitelju kada je zadatak izmijenjen.</span><span class="sxs-lookup"><span data-stu-id="cce0a-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="cce0a-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cce0a-120">**Sales**</span></span>

<span data-ttu-id="cce0a-121">Popravljeni su sljedeći problemi:</span><span class="sxs-lookup"><span data-stu-id="cce0a-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="cce0a-122">Ako na obrascu **Ugovor** dvaput kliknite mogućnost **Stvori fakturu**, stvaraju se dvije fakture za jedan zapis o stvarnim podacima.</span><span class="sxs-lookup"><span data-stu-id="cce0a-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="cce0a-123">U programu Internet Explorer 11 korisnici ne mogu stvoriti unose troškova.</span><span class="sxs-lookup"><span data-stu-id="cce0a-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="cce0a-124">Poništavanje troška i nenaplaćenih stvarnih podataka o prodaji nisu povezani.</span><span class="sxs-lookup"><span data-stu-id="cce0a-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="cce0a-125">Gumb **Osvježi stvarne podatke** na obrascu **Projekt** ne osvježava **Stvarne sate zadatka**.</span><span class="sxs-lookup"><span data-stu-id="cce0a-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="cce0a-126">Dodatak **PreValidateProjectTeamMemberCreate** može stvoriti duplicirane generičke resurse koji se mogu rezervirati kad je atribut **msdyn_isgenericresourceprojectscoped** postavljen na **netočno**.</span><span class="sxs-lookup"><span data-stu-id="cce0a-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="cce0a-127">**Ponovni izračun** briše zaračunate troškove pojedinosti retka ponude koji se temelje na proizvodima i retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="cce0a-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="cce0a-128">U specifičnim scenarijima, dodatak **PostEstimateLineUpdate** prikazuje pogrešku iznimke prazne reference.</span><span class="sxs-lookup"><span data-stu-id="cce0a-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="cce0a-129">Trajanje vremenske faze na **Grafikonu analize profitabilnosti** ne odgovara trajanju troškova u pojedinostima retka ponude s fiksnom cijenom.</span><span class="sxs-lookup"><span data-stu-id="cce0a-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="cce0a-130">Vrijednosti jedinica i grupe jedinica ne postavljaju se ispravno za kategorije troškova na obrascima **Pojedinosti retka ugovora** i **Pojedinosti retka ponude**.</span><span class="sxs-lookup"><span data-stu-id="cce0a-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="cce0a-131">Popisi **Cijena koštanja OrgUnit** dopuštaju preklapanje u efektivnosti datuma.</span><span class="sxs-lookup"><span data-stu-id="cce0a-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="cce0a-132">Korisnicima nije dopušteno mijenjati **OrgUnit** kada vrsta narudžbe nije zasnovana na radu jer će dovesti do pogreške iznimke prazne reference.</span><span class="sxs-lookup"><span data-stu-id="cce0a-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="cce0a-133">Pri pokušaju navigacije s obrasca **Pojedinosti retka ponude** natrag na karticu **Ponuda**, obrazac se osvježava i prikazuje karticu **Sažetak**.</span><span class="sxs-lookup"><span data-stu-id="cce0a-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]