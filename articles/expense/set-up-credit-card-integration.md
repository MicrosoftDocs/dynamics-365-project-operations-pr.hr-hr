---
title: Postavljanje integracije kreditne kartice
description: U ovoj se temi objašnjava način rada s transakcijama kreditnih kartica povezanih s troškovima.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866674"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="1292e-103">Postavljanje integracije kreditne kartice</span><span class="sxs-lookup"><span data-stu-id="1292e-103">Set up credit card integration</span></span>

<span data-ttu-id="1292e-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="1292e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1292e-105">Transakcije kreditne kartice povezane s troškovima mogu se postaviti tako da se automatski uvoze ponavljajućim rasporedom.</span><span class="sxs-lookup"><span data-stu-id="1292e-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="1292e-106">Alternativno, transakcije se prema potrebi mogu ručno uvesti.</span><span class="sxs-lookup"><span data-stu-id="1292e-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="1292e-107">Transakcije kreditnom karticom uvoze se putem entiteta s podacima o transakcijama kreditnim karticama.</span><span class="sxs-lookup"><span data-stu-id="1292e-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="1292e-108">Uvoz transakcija kreditnom karticom</span><span class="sxs-lookup"><span data-stu-id="1292e-108">Import credit card transactions</span></span>

<span data-ttu-id="1292e-109">Kako biste uvezli transakcije kreditnom karticom, slijedite ove korake:</span><span class="sxs-lookup"><span data-stu-id="1292e-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="1292e-110">Na stranici **Transakcije kreditnom karticom** odaberite **Uvoz transakcija**.</span><span class="sxs-lookup"><span data-stu-id="1292e-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="1292e-111">Ako prvi put otvarate mogućnost upravljanja podacima, sustav mora ažurirati popis podatkovnih entiteta prije nego što nastavite.</span><span class="sxs-lookup"><span data-stu-id="1292e-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="1292e-112">U polje **Naziv** unesite jedinstveni opis posla uvoza.</span><span class="sxs-lookup"><span data-stu-id="1292e-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="1292e-113">U polju **Oblik izvornih podataka** odaberite oblik datoteke koja sadrži transakcije kreditnom karticom za uvoz.</span><span class="sxs-lookup"><span data-stu-id="1292e-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="1292e-114">Odaberite **Prenesi**, a zatim pronađite i odaberite datoteku za uvoz.</span><span class="sxs-lookup"><span data-stu-id="1292e-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="1292e-115">Nakon što je datoteka prenesena, provjerite valjanost mapiranja datoteke s transakcijama kreditne kartice i stupaca entiteta podataka o transakcijama kreditnom karticom odabirom veze **Prikaz karte** na pločici.</span><span class="sxs-lookup"><span data-stu-id="1292e-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="1292e-116">Ako postoje pogreške mapiranja ili ako morate promijeniti mapiranje, napravite promjene mapiranja ili iz kartice **Vizualizacija mapiranja** ili iz kartice **Pojedinosti mapiranja**.</span><span class="sxs-lookup"><span data-stu-id="1292e-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="1292e-117">Kako biste automatizirali transakcije kreditnom karticom, odaberite mogućnost **Stvori posao ponavljajućih podataka**.</span><span class="sxs-lookup"><span data-stu-id="1292e-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="1292e-118">Tada možete postaviti ponavljanje koje definira učestalost uvoza transakcija kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="1292e-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="1292e-119">Kada dovršite, odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="1292e-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="1292e-120">Kako biste odmah uvezli odabranu datoteku, odaberite **Uvoz**.</span><span class="sxs-lookup"><span data-stu-id="1292e-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="1292e-121">Ako se tijekom uvoza prikažu pogreške, možete pregledati zapisnik izvršenja ili prikazati podatke kako biste vidjeli pogreške koje morate ispraviti kako biste osigurali uspješan uvoz.</span><span class="sxs-lookup"><span data-stu-id="1292e-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="1292e-122">Ako trebate uvesti više datotečnih oblika, morate stvoriti zasebne poslove uvoza za svaku vrstu oblika.</span><span class="sxs-lookup"><span data-stu-id="1292e-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="1292e-123">Ponovna dodjela transakcije kreditnom karticom otkazanim zaposlenicima</span><span class="sxs-lookup"><span data-stu-id="1292e-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="1292e-124">Nakon prekidanja zapisa o zaposleniku, onemogućen je račun usluge domene Active Directory (AD DS, Active Directory Domain Services) zaposlenika.</span><span class="sxs-lookup"><span data-stu-id="1292e-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="1292e-125">Međutim, možda postoje aktivne transakcije kreditnom karticom koje se i dalje moraju trošiti i nadoknaditi.</span><span class="sxs-lookup"><span data-stu-id="1292e-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="1292e-126">Na stranici **Transakcije kreditnim karticama** možete ponovno dodijeliti zaposlenika za bilo koju transakciju kreditnom karticom s koje je povezani zaposlenik izbrisan.</span><span class="sxs-lookup"><span data-stu-id="1292e-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="1292e-127">Odaberite jednu ili više transakcija kreditnom karticom, a zatim odaberite **Ponovno dodijeli transakcije**.</span><span class="sxs-lookup"><span data-stu-id="1292e-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="1292e-128">Zatim možete odabrati drugog zaposlenika kojem ćete dodijeliti transakcije kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="1292e-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="1292e-129">Nakon što se transakcije kreditnom karticom ponovno dodijele, mogu se odabrati za izvješće o troškovima i platiti uobičajenim postupkom za nadoknadu prema izvješću o troškovima.</span><span class="sxs-lookup"><span data-stu-id="1292e-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="1292e-130">Brisanje transakcija kreditnom karticom</span><span class="sxs-lookup"><span data-stu-id="1292e-130">Delete credit card transactions</span></span> 

<span data-ttu-id="1292e-131">Ponekad, nakon uvoza transakcija kreditnom karticom, određene transakcije možda će trebati izbrisati.</span><span class="sxs-lookup"><span data-stu-id="1292e-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="1292e-132">To će možda trebati učiniti zato što su transakcije duplikati ili što podaci možda nisu točni.</span><span class="sxs-lookup"><span data-stu-id="1292e-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="1292e-133">Administratori mogu upotrebljavati značajku **„Brisanje transakcija kreditnom karticom”** za odabir i brisanje transakcija kreditnom karticom koje **nisu priložene** izvješću o troškovima.</span><span class="sxs-lookup"><span data-stu-id="1292e-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="1292e-134">Idite na **Povremeni zadaci** > **Izbriši transakcije kreditnom karticom**.</span><span class="sxs-lookup"><span data-stu-id="1292e-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="1292e-135">Odaberite **Filtar** i osigurajte podatke za identifikaciju zapisa koje treba uključiti.</span><span class="sxs-lookup"><span data-stu-id="1292e-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="1292e-136">Za brisanje zapisa odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="1292e-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
