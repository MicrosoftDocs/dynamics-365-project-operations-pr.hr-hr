---
title: Sinkronizacija kategorija izdataka za projekt između aplikacija Finance and Operations i Project Service Automation
description: U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju kategorija izdataka za projekt između sustava Microsoft Dynamics 365 Finance i aplikacije Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999842"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="dc924-103">Sinkronizacija kategorija izdataka za projekt između aplikacija Finance and Operations i Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dc924-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dc924-104">U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju kategorija izdataka za projekt između sustava Dynamics 365 Finance i aplikacije Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dc924-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc924-105">Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.</span><span class="sxs-lookup"><span data-stu-id="dc924-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="dc924-106">Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.</span><span class="sxs-lookup"><span data-stu-id="dc924-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="dc924-107">Ako upotrebljavate Enterprise Edition 7.3.0, nakon što instalirate zakrpe KB 4132657 i KB 4132660 moći ćete upotrebljavati predloške za integraciju projektnih zadataka, kategorija transakcija izdataka, procjena sati rada, procjena izdataka i stvarnih podataka te za konfiguraciju funkcije zaključavanja.</span><span class="sxs-lookup"><span data-stu-id="dc924-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="dc924-108">Ako morate vratiti zadane računovodstvene distribucije, preporučujemo da instalirate i zakrpu KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="dc924-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="dc924-109">Tijek podataka za aplikacije Project Service Automation i Financije</span><span class="sxs-lookup"><span data-stu-id="dc924-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="dc924-110">Rješenje za integraciju aplikacija Project Service Automation i Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije.</span><span class="sxs-lookup"><span data-stu-id="dc924-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="dc924-111">Predlošci integracije koji su dostupni uz značajku Integracija podataka omogućuju tijek podataka o kategorijama transakcija izdataka za projekt između aplikacija Financije i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dc924-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="dc924-112">Ako se kategorije izdataka za projekt obrade u Financijama, tijek integracije ide od Financija do aplikacije Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dc924-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="dc924-113">ID-ovi integracije kategorija izdataka za projekt potom se ažuriraju sinkronizacijom iz aplikacije Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="dc924-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dc924-114">Ako se kategorije izdataka za projekt obrade u aplikaciji Project Service Automation, tijek integracije ide od aplikacije Project Service Automation do Financija.</span><span class="sxs-lookup"><span data-stu-id="dc924-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="dc924-115">Prije sinkronizacije iz aplikacije Project Service Automation kategorije projekata već moraju biti konfigurirane u aplikaciji Financije.</span><span class="sxs-lookup"><span data-stu-id="dc924-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="dc924-116">Zatim sinkronizirajte iz Financija natrag u aplikaciju Project Service Automation, pa ponovno iz aplikacije Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="dc924-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="dc924-117">Na taj način zajamčena je povezanosti kategorija i nemogućnost stvaranja duplikata.</span><span class="sxs-lookup"><span data-stu-id="dc924-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="dc924-118">Kategorije izdataka za projekt obično se obrađuju u Financijama.</span><span class="sxs-lookup"><span data-stu-id="dc924-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="dc924-119">Međutim, ako to nije slučaj ili ako su kategorije izdataka već stvorene u aplikaciji Project Service Automation, prvo morate sinkronizirati s pomoću predloška kategorija transakcija izdataka za projekt (PSA u Fin i Ops).</span><span class="sxs-lookup"><span data-stu-id="dc924-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="dc924-120">Zatim sinkronizirajte s pomoću predloška kategorija transakcija izdataka za projekt (Fin i Ops u PSA).</span><span class="sxs-lookup"><span data-stu-id="dc924-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="dc924-121">Tada biste trebali još jednom pokrenuti sinkronizaciju od aplikacije Project Service Automation do Financija.</span><span class="sxs-lookup"><span data-stu-id="dc924-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="dc924-122">Ako prvo sinkronizirate iz aplikacije Project Service Automation, u aplikaciji Financije prije pokretanja sinkronizacije moraju biti ispunjeni sljedeći zahtjevi:</span><span class="sxs-lookup"><span data-stu-id="dc924-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="dc924-123">Dijeljena kategorija podudarna s kategorijom projekta koja je postavljena u aplikaciju Project Service Automation mora postojati i mora biti omogućena kako za **Projekt** tako i za **Izdatak**.</span><span class="sxs-lookup"><span data-stu-id="dc924-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="dc924-124">Za svaku pravnu osobu u Financijama s kojom se mora integrirati moraju postojati sljedeće kategorije projekata:</span><span class="sxs-lookup"><span data-stu-id="dc924-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="dc924-125">Postoji stavka **Kategorija projekta**.</span><span class="sxs-lookup"><span data-stu-id="dc924-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="dc924-126">Omogućena je stavka **Upotrijebi u izdatku**.</span><span class="sxs-lookup"><span data-stu-id="dc924-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="dc924-127">Omogućena je stavka **Aktivan u dnevniku**.</span><span class="sxs-lookup"><span data-stu-id="dc924-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="dc924-128">**Vrsta transakcije** postavljena je na **Izdatak**.</span><span class="sxs-lookup"><span data-stu-id="dc924-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="dc924-129">Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.</span><span class="sxs-lookup"><span data-stu-id="dc924-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="dc924-130">[![Tijek podataka za integraciju usluge Project Service Automation s Financijama](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="dc924-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="dc924-131">Sinkronizacija kategorije izdataka za projekt iz aplikacije Financije u aplikaciju Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dc924-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="dc924-132">Predložak i zadatak</span><span class="sxs-lookup"><span data-stu-id="dc924-132">Template and task</span></span>

<span data-ttu-id="dc924-133">Kako biste pristupili predlošku, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti**, a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.</span><span class="sxs-lookup"><span data-stu-id="dc924-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="dc924-134">Predložak u nastavku i temeljni zadatak upotrebljavaju se za sinkronizaciju kategorija izdataka za izdataka za projekt iz Financija u aplikaciju Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="dc924-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="dc924-135">**Naziv predloška u Integraciji podataka:** Kategorije transakcije izdataka za projekt (Fin i Ops u PSA)</span><span class="sxs-lookup"><span data-stu-id="dc924-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="dc924-136">**Naziv zadatka u projektu:** Sinkronizacija kategorija s PSA</span><span class="sxs-lookup"><span data-stu-id="dc924-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="dc924-137">Postavljanje entiteta</span><span class="sxs-lookup"><span data-stu-id="dc924-137">Entity set</span></span>

| <span data-ttu-id="dc924-138">Financije</span><span class="sxs-lookup"><span data-stu-id="dc924-138">Finance</span></span>                           | <span data-ttu-id="dc924-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dc924-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="dc924-140">Entitet integracije za kategorije</span><span class="sxs-lookup"><span data-stu-id="dc924-140">Integration entity for categories</span></span> | <span data-ttu-id="dc924-141">Kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="dc924-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="dc924-142">Tijek entiteta</span><span class="sxs-lookup"><span data-stu-id="dc924-142">Entity flow</span></span>

<span data-ttu-id="dc924-143">Kategorijama izdataka za projekt upravlja se u usluzi Financije, a sinkroniziraju se s aplikacijom Project Service Automation kao kategorije transakcija.</span><span class="sxs-lookup"><span data-stu-id="dc924-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="dc924-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="dc924-144">Power Query</span></span>

<span data-ttu-id="dc924-145">Kada se sinkronizirate s aplikacijom Project Service Automation, morate upotrebljavati aplikaciju Microsoft Power Query za Excel kako biste postavili vrstu naplate za kategoriju transakcije.</span><span class="sxs-lookup"><span data-stu-id="dc924-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="dc924-146">Predložak kategorija transakcija izdataka za projekt (Fin i Ops u PSA) omogućuje zadani stupac i mapiranje.</span><span class="sxs-lookup"><span data-stu-id="dc924-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="dc924-147">Ako stvorite vlastiti predložak, ovaj uvjetni stupac morate dodati modulu Power Query.</span><span class="sxs-lookup"><span data-stu-id="dc924-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="dc924-148">Slijedite ove korake.</span><span class="sxs-lookup"><span data-stu-id="dc924-148">Follow these steps.</span></span>

1. <span data-ttu-id="dc924-149">Kliknite strelicu kako biste otvorili mapiranje zadatka kategorija izdataka za projekt u predlošku kategorija transakcija izdataka za projekt (Fin i Ops u PSA).</span><span class="sxs-lookup"><span data-stu-id="dc924-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="dc924-150">Kliknite vezu **Napredni upit i filtriranje** kako biste otvorili modul Power Query.</span><span class="sxs-lookup"><span data-stu-id="dc924-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="dc924-151">Odaberite **Dodaj uvjetni stupac**.</span><span class="sxs-lookup"><span data-stu-id="dc924-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="dc924-152">Unesite naziv novog stupca, kao što je **Vrsta naplate**.</span><span class="sxs-lookup"><span data-stu-id="dc924-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="dc924-153">Unesite sljedeći uvjet: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="dc924-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="dc924-154">Kliknite **U redu** na stupcu.</span><span class="sxs-lookup"><span data-stu-id="dc924-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="dc924-155">Uvjerite se kako ste ovaj novi stupac mapirali na stranicu za mapiranje.</span><span class="sxs-lookup"><span data-stu-id="dc924-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="dc924-156">Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka.</span><span class="sxs-lookup"><span data-stu-id="dc924-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="dc924-157">Mapiranje prikazuje podatke polja koji će se sinkronizirati iz Financija u aplikaciju Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dc924-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="dc924-158">[![Mapiranje predloška Kategorije izdataka za projekt u aplikaciju Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dc924-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="dc924-159">Sinkronizacija kategorije izdataka za projekt iz aplikacije Project Service Automation u Financije</span><span class="sxs-lookup"><span data-stu-id="dc924-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="dc924-160">Predložak i zadatak</span><span class="sxs-lookup"><span data-stu-id="dc924-160">Template and task</span></span>

<span data-ttu-id="dc924-161">Predložak u nastavku i temeljni zadatak upotrebljavaju se za sinkronizaciju kategorija izdataka za izdataka za projekt iz aplikacije Project Service Automation u Financije:</span><span class="sxs-lookup"><span data-stu-id="dc924-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="dc924-162">**Naziv predloška u Integraciji podataka:** Kategorije transakcije izdataka za projekt (PSA u Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="dc924-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="dc924-163">**Naziv zadatka u projektu:** Sinkronizacija kategorija s Fin Ops</span><span class="sxs-lookup"><span data-stu-id="dc924-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="dc924-164">Postavljanje entiteta</span><span class="sxs-lookup"><span data-stu-id="dc924-164">Entity set</span></span>

| <span data-ttu-id="dc924-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dc924-165">Project Service Automation</span></span> | <span data-ttu-id="dc924-166">Financije</span><span class="sxs-lookup"><span data-stu-id="dc924-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="dc924-167">Kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="dc924-167">Transaction categories</span></span>     | <span data-ttu-id="dc924-168">Entitet integracije za kategorije</span><span class="sxs-lookup"><span data-stu-id="dc924-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="dc924-169">Tijek entiteta</span><span class="sxs-lookup"><span data-stu-id="dc924-169">Entity flow</span></span>

<span data-ttu-id="dc924-170">Kategorijama izdataka za projekt upravlja se u usluzi Financije, a sinkroniziraju se s aplikacijom Project Service Automation kao kategorije transakcija.</span><span class="sxs-lookup"><span data-stu-id="dc924-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="dc924-171">Sinkronizacija natrag na Financije ažurira kategoriju projekta u Financijama s pomoću ID-a integracije iz aplikacije Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dc924-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dc924-172">Mapiranje predloška u integraciji podataka</span><span class="sxs-lookup"><span data-stu-id="dc924-172">Template mapping in Data integration</span></span>

<span data-ttu-id="dc924-173">Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka.</span><span class="sxs-lookup"><span data-stu-id="dc924-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="dc924-174">Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="dc924-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dc924-175">[![Mapiranje predloška iz aplikacije Project Service Automation u aplikaciju Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dc924-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]