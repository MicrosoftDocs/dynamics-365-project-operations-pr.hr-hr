---
title: Kupnja materijala koji nisu na zalihama s pomoću fakture dobavljača na čekanju
description: U ovoj se temi objašnjava način bilježenja faktura dobavljača na čekanju.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880628"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="ceb82-103">Kupnja materijala koji nisu na zalihama s pomoću fakture dobavljača na čekanju</span><span class="sxs-lookup"><span data-stu-id="ceb82-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="ceb82-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ceb82-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ceb82-105">Kako tvrtka za projekt nabavlja materijale koji nisu na zalihi, troškovi se mogu odmah evidentirati u odnosu na projekt.</span><span class="sxs-lookup"><span data-stu-id="ceb82-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="ceb82-106">Na primjer, Contoso Robotics US izvodi projekt obnove opreme i treba softverske licence.</span><span class="sxs-lookup"><span data-stu-id="ceb82-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="ceb82-107">Te se licence nabavljaju od dobavljača koji je treća srana.</span><span class="sxs-lookup"><span data-stu-id="ceb82-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="ceb82-108">S pomoću aplikacije Dynamics 365 Finance, službenik za dugovanja evidentira dokument fakture dobavljača na čekanju i pripisuje troškove licence izravno na projekt obnove opreme.</span><span class="sxs-lookup"><span data-stu-id="ceb82-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ceb82-109">Prije nego što upotrijebite funkcionalnost opisanu u ovoj temi, pregledajte i primijenite potrebne konfiguracije.</span><span class="sxs-lookup"><span data-stu-id="ceb82-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="ceb82-110">Dodatne informacija potražite u članku [Omogućivanje materijala koji nisu na zalihi i fakture dobavljača na čekanju](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="ceb82-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="ceb82-111">Knjiženje fakture dobavljača na čekanju povezane s projektom</span><span class="sxs-lookup"><span data-stu-id="ceb82-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="ceb82-112">Fakture dobavljača na čekanju mogu se evidentirati na stranici **Fakture dobavljača na čekanju** (**Dugovanja** > **Fakture** > **Fakture dobavljača na čekanju**).</span><span class="sxs-lookup"><span data-stu-id="ceb82-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="ceb82-113">Poduzmite sljedeće korake za knjiženje fakture dobavljača na čekanju u vezi s projektom:</span><span class="sxs-lookup"><span data-stu-id="ceb82-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="ceb82-114">Idite na **Dugovanja** > **Fakture** i odaberite **Nova**.</span><span class="sxs-lookup"><span data-stu-id="ceb82-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="ceb82-115">U polju **Račun fakture** odaberite dobavljača, a u polje **Broj** unesite identifikaciju fakture dobavljača.</span><span class="sxs-lookup"><span data-stu-id="ceb82-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="ceb82-116">Dodajte redak fakturi dobavljača i u polju **Broj stavke** odaberite stavku koja nije na zalihi kupljenu od dobavljača.</span><span class="sxs-lookup"><span data-stu-id="ceb82-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ceb82-117">Redci fakture dobavljača koji se temelje na kategoriji nabave ne mogu se evidentirati u projektu.</span><span class="sxs-lookup"><span data-stu-id="ceb82-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="ceb82-118">Dodajte kupljenu količinu.</span><span class="sxs-lookup"><span data-stu-id="ceb82-118">Add the quantity purchased.</span></span> <span data-ttu-id="ceb82-119">Sustav će popuniti jediničnu cijenu na temelju konfiguracije cijene stavke koja nije na zalihi.</span><span class="sxs-lookup"><span data-stu-id="ceb82-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="ceb82-120">U retku provjerite ukupan iznos i ostale potrebne pojedinosti.</span><span class="sxs-lookup"><span data-stu-id="ceb82-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="ceb82-121">Na pojedinostima retka, na kartici **Projekt**, odaberite ID projekta na koji će se evidentirati ova stavka.</span><span class="sxs-lookup"><span data-stu-id="ceb82-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="ceb82-122">Po želji odaberite broj aktivnosti i ažurirajte kategoriju projekta i svojstvo retka.</span><span class="sxs-lookup"><span data-stu-id="ceb82-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="ceb82-123">Knjiženje fakture dobavljača na čekanju.</span><span class="sxs-lookup"><span data-stu-id="ceb82-123">Post pending vendor invoice.</span></span> <span data-ttu-id="ceb82-124">Kada se faktura proknjiži, sustav bilježi:</span><span class="sxs-lookup"><span data-stu-id="ceb82-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="ceb82-125">Iznos salda dobavljača.</span><span class="sxs-lookup"><span data-stu-id="ceb82-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="ceb82-126">Iznos poreza na promet.</span><span class="sxs-lookup"><span data-stu-id="ceb82-126">The sales tax amount.</span></span>
    - <span data-ttu-id="ceb82-127">Trošak u odnosu na projekt evidentira se na račun integracije nabave.</span><span class="sxs-lookup"><span data-stu-id="ceb82-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="ceb82-128">Stvarna transakcija projekta na platformi Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ceb82-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="ceb82-129">Ova se transakcija dalje obrađuje s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="ceb82-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="ceb82-130">Knjiženjem ovog dnevnika premješta se iznos s računa integracije nabave na račun troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="ceb82-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
