---
title: Postavljanje integracije kreditne kartice
description: U ovoj se temi objašnjava način uvoza i održavanja transakcija kreditne kartice povezane s troškovima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276159"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="8e661-103">Postavljanje integracije kreditne kartice</span><span class="sxs-lookup"><span data-stu-id="8e661-103">Set up credit card integration</span></span>

<span data-ttu-id="8e661-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="8e661-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8e661-105">Transakcije kreditne kartice povezane s troškovima mogu se postaviti tako da se automatski uvoze ponavljajućim rasporedom.</span><span class="sxs-lookup"><span data-stu-id="8e661-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="8e661-106">Alternativno, transakcije se prema potrebi mogu ručno uvesti.</span><span class="sxs-lookup"><span data-stu-id="8e661-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="8e661-107">Transakcije kreditnom karticom uvoze se putem entiteta s podacima o transakcijama kreditnim karticama.</span><span class="sxs-lookup"><span data-stu-id="8e661-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="8e661-108">Uvoz transakcija kreditnom karticom</span><span class="sxs-lookup"><span data-stu-id="8e661-108">Import credit card transactions</span></span>

1. <span data-ttu-id="8e661-109">Na stranici **Transakcije kreditnom karticom** odaberite **Uvoz transakcija**.</span><span class="sxs-lookup"><span data-stu-id="8e661-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="8e661-110">Ako prvi put otvarate mogućnost upravljanja podacima, sustav mora ažurirati popis podatkovnih entiteta prije nego što nastavite.</span><span class="sxs-lookup"><span data-stu-id="8e661-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="8e661-111">U polje **Naziv** unesite jedinstveni opis posla koji se uvozi.</span><span class="sxs-lookup"><span data-stu-id="8e661-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="8e661-112">U polju **Oblik izvornih podataka** odaberite oblik datoteke koja sadrži transakcije kreditnom karticom za uvoz.</span><span class="sxs-lookup"><span data-stu-id="8e661-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="8e661-113">Odaberite **Prenesi**, a zatim pronađite i odaberite datoteku za uvoz.</span><span class="sxs-lookup"><span data-stu-id="8e661-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="8e661-114">Nakon što je datoteka prenesena, provjerite valjanost mapiranja datoteke s transakcijama kreditne kartice i stupaca entiteta podataka o transakcijama kreditnom karticom odabirom veze **Prikaz karte** na pločici.</span><span class="sxs-lookup"><span data-stu-id="8e661-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="8e661-115">Ako postoje pogreške mapiranja ili ako morate promijeniti mapiranje, napravite promjene mapiranja ili iz kartice **Vizualizacija mapiranja** ili iz kartice **Pojedinosti mapiranja**.</span><span class="sxs-lookup"><span data-stu-id="8e661-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="8e661-116">Kako biste automatizirali transakcije kreditnom karticom, odaberite mogućnost **Stvori posao ponavljajućih podataka**.</span><span class="sxs-lookup"><span data-stu-id="8e661-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="8e661-117">Tada možete postaviti ponavljanje koje definira učestalost uvoza transakcija kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="8e661-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="8e661-118">Kada dovršite, odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="8e661-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="8e661-119">Kako biste odmah uvezli odabranu datoteku, odaberite **Uvoz**.</span><span class="sxs-lookup"><span data-stu-id="8e661-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="8e661-120">Ako se tijekom uvoza pojave pogreške, možete pregledati zapis izvršavanja ili podatke o fazama kako biste vidjeli pogreške koje morate ispraviti kako biste zajamčili uspješan uvoz.</span><span class="sxs-lookup"><span data-stu-id="8e661-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="8e661-121">Ako morate uvesti više oblika datoteke, morate stvoriti zasebne poslove uvoza za svaku vrstu oblika.</span><span class="sxs-lookup"><span data-stu-id="8e661-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="8e661-122">Ponovna dodjela transakcije kreditnom karticom otkazanim zaposlenicima</span><span class="sxs-lookup"><span data-stu-id="8e661-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="8e661-123">Nakon prekidanja zapisa o zaposleniku, onemogućen je račun usluge domene Active Directory (AD DS, Active Directory Domain Services) zaposlenika.</span><span class="sxs-lookup"><span data-stu-id="8e661-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="8e661-124">Međutim, možda postoje aktivne transakcije kreditnom karticom koje se i dalje moraju trošiti i nadoknaditi.</span><span class="sxs-lookup"><span data-stu-id="8e661-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="8e661-125">Sa stranice **Transakcije kreditnom karticom** možete ponovno dodijeliti zaposlenika za svaku transakciju kreditnom karticom u kojoj je pridruženi zaposlenik otkazan.</span><span class="sxs-lookup"><span data-stu-id="8e661-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="8e661-126">Odaberite jednu ili više transakcija kreditnom karticom, a zatim odaberite **Ponovno dodijeli transakcije**.</span><span class="sxs-lookup"><span data-stu-id="8e661-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="8e661-127">Zatim možete odabrati drugog zaposlenika kojem ćete dodijeliti transakcije kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="8e661-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="8e661-128">Nakon što se transakcije kreditnom karticom ponovno dodijele, mogu se odabrati za izvješće o troškovima i platiti uobičajenim postupkom za nadoknadu prema izvješću o troškovima.</span><span class="sxs-lookup"><span data-stu-id="8e661-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]