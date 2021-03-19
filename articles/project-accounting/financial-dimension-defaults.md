---
title: Zadane postavke financijske dimenzije
description: U ovoj temi nalaze se informacije o načinu postavljanja zadanih financijskih veličina.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287364"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="d2e2c-103">Zadane postavke financijske dimenzije</span><span class="sxs-lookup"><span data-stu-id="d2e2c-103">Financial dimension defaults</span></span>

<span data-ttu-id="d2e2c-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="d2e2c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d2e2c-105">Dynamics 365 Project Operations upotrebljava okvir [Financijske veličine](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) u aplikaciji Dynamics 365 Finance za pružanje dodatnih uvida u transakcije sporednih i glavne knjige.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="d2e2c-106">Zadane financijske dimenzije mogu se postaviti na kupca, izvor financiranja projekta, kontrolnu točku, redak ugovora o projektu ili projekt.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="d2e2c-107">Definiranje zadanih financijskih veličina za klijenta</span><span class="sxs-lookup"><span data-stu-id="d2e2c-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="d2e2c-108">Zadane postavke veličine kupca navedene su u aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="d2e2c-109">Kako biste postavili zadane postavke veličine, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="d2e2c-110">Idite na **Potraživanja** > **Klijenti** > **Svi klijenti**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="d2e2c-111">Na stranici **Klijenti**, na kartici **Financijske veličine**, postavite vrijednosti financijske veličine za određenog kupca.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="d2e2c-112">Definiranje zadanih financijskih veličina za ugovore o projektu</span><span class="sxs-lookup"><span data-stu-id="d2e2c-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="d2e2c-113">Projektni ugovori stvaraju se i održavaju na platformi Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="d2e2c-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="d2e2c-114">Atributi računovodstva za ugovore o projektu postavljeni su u modulu **Upravljanje projektom i računovodstvo** u aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="d2e2c-115">Postavljanje financijskih veličina za izvor financiranja projekta</span><span class="sxs-lookup"><span data-stu-id="d2e2c-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="d2e2c-116">Idite na **Upravljanje projektom i računovodstvo** > **Projekti** > **Ugovori o projektu**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="d2e2c-117">Odaberite zapis koji želite ažurirati, a zatim na kartici **Ugovor o projektu** odaberite **Prikaži zadano računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="d2e2c-118">Proširite mogućnost **Povezane informacije** i odaberite karticu **Izvori financiranja**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="d2e2c-119">Postavite zadane postavke financijske veličine.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="d2e2c-120">Primjećujete kako se financijske veličine zadaju iz korisničkog računa.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="d2e2c-121">Postavljanje financijskih veličina za redak ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="d2e2c-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="d2e2c-122">Idite na **Upravljanje projektom i računovodstvo** > **Projekti** > **Ugovori o projektu**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="d2e2c-123">Odaberite zapis koji želite ažurirati, a zatim na kartici **Ugovor o projektu** odaberite **Prikaži zadano računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="d2e2c-124">Proširite mogućnost **Povezane informacije** i odaberite karticu **Redci ugovora**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="d2e2c-125">Postavite zadane postavke financijske veličine.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="d2e2c-126">Zadane postavke financijske veličine primjenjive su i mogu se upotrebljavati samo s redcima ugovora s fiksnom cijenom (kontrolna točka).</span><span class="sxs-lookup"><span data-stu-id="d2e2c-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="d2e2c-127">Te zadane vrijednosti upotrebljavaju se za transakcije po računu i retke fakture.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="d2e2c-128">Definiranje zadanih financijskih veličina za projekte</span><span class="sxs-lookup"><span data-stu-id="d2e2c-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="d2e2c-129">Projekti se stvaraju i održavaju na platformi CDS.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="d2e2c-130">Atributi računovodstva za projekte postavljeni su u modulu **Upravljanje projektom i računovodstvo** u aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="d2e2c-131">Idite na mogućnost **Upravljanje projektom i računovodstvo** > **Projekti** > **Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="d2e2c-132">Odaberite zapis koji želite ažurirati, a zatim na kartici **Projekt** odaberite **Prikaži zadano računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="d2e2c-133">Proširite mogućnost **Povezane informacije** i odaberite karticu **Postavke**.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="d2e2c-134">Postavite zadane postavke financijske veličine.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="d2e2c-135">Primjećujete kako se financijske veličine zadaju iz korisničkog računa.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="d2e2c-136">Ako je projekt povezan s retkom ugovora koji ima više klijenata ugovora o projektu, za zadane financijske veličine upotrebljava se primarni klijent.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="d2e2c-137">Zadane financijske veličine projekta upotrebljavaju se za postavljanje zadanih vrijednosti retka dnevnika za vrijeme, troškove i transakcije naknada u **Dnevniku integracije aplikacije Project Operations** i na povezanim redcima fakture za projekt.</span><span class="sxs-lookup"><span data-stu-id="d2e2c-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]