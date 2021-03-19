---
title: Uvoz i održavanje transakcija kreditnim karticama
description: U ovoj se temi objašnjava način uvoza i održavanja transakcija kreditne kartice povezane s troškovima. Te se transakcije mogu postaviti tako da se automatski uvoze po ponavljajućem rasporedu ili se prema potrebi mogu ručno uvesti.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271569"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="14638-104">Uvoz i održavanje transakcija kreditnim karticama</span><span class="sxs-lookup"><span data-stu-id="14638-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="14638-105">Transakcije kreditne kartice povezane s troškovima mogu se postaviti tako da se automatski uvoze ponavljajućim rasporedom.</span><span class="sxs-lookup"><span data-stu-id="14638-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="14638-106">Alternativno, transakcije se prema potrebi mogu ručno uvesti.</span><span class="sxs-lookup"><span data-stu-id="14638-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="14638-107">Transakcije kreditnom karticom uvoze se putem entiteta s podacima o transakcijama kreditnim karticama.</span><span class="sxs-lookup"><span data-stu-id="14638-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="14638-108">Dodatne informacije o entitetima podataka potražite u članku [Entiteti podataka](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="14638-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="14638-109">Uvoz transakcija kreditnom karticom</span><span class="sxs-lookup"><span data-stu-id="14638-109">Import credit card transactions</span></span>

1. <span data-ttu-id="14638-110">Na stranici **Transakcije kreditnom karticom** odaberite **Uvoz transakcija**.</span><span class="sxs-lookup"><span data-stu-id="14638-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="14638-111">Ako prvi put otvarate mogućnost upravljanja podacima, sustav mora ažurirati popis podatkovnih entiteta prije nego što nastavite.</span><span class="sxs-lookup"><span data-stu-id="14638-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="14638-112">U polje **Naziv** unesite jedinstveni opis posla koji se uvozi.</span><span class="sxs-lookup"><span data-stu-id="14638-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="14638-113">U polju **Oblik izvornih podataka** odaberite oblik datoteke koja sadrži transakcije kreditnom karticom za uvoz.</span><span class="sxs-lookup"><span data-stu-id="14638-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="14638-114">Odaberite **Prenesi**, a zatim pronađite i odaberite datoteku za uvoz.</span><span class="sxs-lookup"><span data-stu-id="14638-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="14638-115">Nakon što je datoteka prenesena, provjerite valjanost mapiranja datoteke s transakcijama kreditne kartice i stupaca entiteta podataka o transakcijama kreditnom karticom odabirom veze **Prikaz karte** na pločici.</span><span class="sxs-lookup"><span data-stu-id="14638-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="14638-116">Ako postoje pogreške mapiranja ili ako morate promijeniti mapiranje, napravite promjene mapiranja ili iz kartice **Vizualizacija mapiranja** ili iz kartice **Pojedinosti mapiranja**.</span><span class="sxs-lookup"><span data-stu-id="14638-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="14638-117">Kako biste automatizirali transakcije kreditnom karticom, odaberite mogućnost **Stvori posao ponavljajućih podataka**.</span><span class="sxs-lookup"><span data-stu-id="14638-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="14638-118">Tada možete postaviti ponavljanje koje definira učestalost uvoza transakcija kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="14638-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="14638-119">Kada dovršite, odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="14638-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="14638-120">Kako biste odmah uvezli odabranu datoteku, odaberite **Uvoz**.</span><span class="sxs-lookup"><span data-stu-id="14638-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="14638-121">Ako se tijekom uvoza pojave pogreške, možete pregledati zapis izvršavanja ili podatke o fazama kako biste vidjeli pogreške koje morate ispraviti kako biste zajamčili uspješan uvoz.</span><span class="sxs-lookup"><span data-stu-id="14638-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="14638-122">Ako morate uvesti više oblika datoteke, morate stvoriti zasebne poslove uvoza za svaku vrstu oblika.</span><span class="sxs-lookup"><span data-stu-id="14638-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="14638-123">Ponovna dodjela transakcije kreditnom karticom otkazanim zaposlenicima</span><span class="sxs-lookup"><span data-stu-id="14638-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="14638-124">Nakon prekidanja zapisa o zaposleniku, onemogućen je račun usluge domene Active Directory (AD DS, Active Directory Domain Services) zaposlenika.</span><span class="sxs-lookup"><span data-stu-id="14638-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="14638-125">Međutim, možda postoje aktivne transakcije kreditnom karticom koje se i dalje moraju trošiti i nadoknaditi.</span><span class="sxs-lookup"><span data-stu-id="14638-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="14638-126">Sa stranice **Transakcije kreditnom karticom** možete ponovno dodijeliti zaposlenika za svaku transakciju kreditnom karticom u kojoj je pridruženi zaposlenik otkazan.</span><span class="sxs-lookup"><span data-stu-id="14638-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="14638-127">Odaberite jednu ili više transakcija kreditnom karticom, a zatim odaberite **Ponovno dodijeli transakcije**.</span><span class="sxs-lookup"><span data-stu-id="14638-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="14638-128">Zatim možete odabrati drugog zaposlenika kojem ćete dodijeliti transakcije kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="14638-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="14638-129">Nakon što se transakcije kreditnom karticom ponovno dodijele, mogu se odabrati za izvješće o troškovima i platiti uobičajenim postupkom za nadoknadu prema izvješću o troškovima.</span><span class="sxs-lookup"><span data-stu-id="14638-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]