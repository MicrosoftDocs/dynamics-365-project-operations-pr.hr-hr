---
title: Ažuriranje aplikacije Project Operations u vašem okruženju aplikacije Financije
description: U ovoj temi nalaze se informacije o načinu ažuriranja rješenja Project Operations u vašem okruženju aplikacije Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011047"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="e600e-103">Ažuriranje aplikacije Project Operations u vašem okruženju aplikacije Financije</span><span class="sxs-lookup"><span data-stu-id="e600e-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="e600e-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="e600e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="e600e-105">U ovoj temi nalaze se informacije o načinu ažuriranja rješenja Dynamics 365 Project Operations u vašem okruženju aplikacije Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e600e-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="e600e-106">Tri su postupka potrebna za ažuriranje aplikacije Project Operations na Ažuriranje 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="e600e-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="e600e-107">Uvezite paket u pretpregled svojeg projekta</span><span class="sxs-lookup"><span data-stu-id="e600e-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="e600e-108">Primjena ažuriranja</span><span class="sxs-lookup"><span data-stu-id="e600e-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="e600e-109">Ažuriranje okruženja svoje platforme Dataverse</span><span class="sxs-lookup"><span data-stu-id="e600e-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="e600e-110">Uvezite paket u svoj projekt LCS</span><span class="sxs-lookup"><span data-stu-id="e600e-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="e600e-111">Prijavite se na portal [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kao vlasnik projekta ili upravitelj okruženja.</span><span class="sxs-lookup"><span data-stu-id="e600e-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="e600e-112">S popisa projekata odaberite svoj projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="e600e-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="e600e-113">Na stranici **Projekt** u grupi **Okruženja** otvorite okruženje koje želite ažurirati.</span><span class="sxs-lookup"><span data-stu-id="e600e-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="e600e-114">Provjerite radi li okruženje.</span><span class="sxs-lookup"><span data-stu-id="e600e-114">Verify that the environment is running.</span></span> <span data-ttu-id="e600e-115">Ako okruženje nije pokrenuto, pokrenite ga.</span><span class="sxs-lookup"><span data-stu-id="e600e-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="e600e-116">U odjeljku **Novo izdanje** pod stavkom **Dostupna ažuriranja** odaberite **Prikaži ažuriranje** za 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="e600e-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Gumb za prikaz ažuriranja](media/view-update.png)

6. <span data-ttu-id="e600e-118">Na stranici **Binarna ažuriranja** odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="e600e-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="e600e-119">Na stranici **Pregled i spremanje ažuriranja** odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="e600e-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="e600e-120">U oknu **Spremi paket u biblioteku sredstava** koje se otvori, unesite naziv paketa, a zatim odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="e600e-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="e600e-121">Kad LCS završi spremanje paketa, omogućuje se gumb **Gotovo**.</span><span class="sxs-lookup"><span data-stu-id="e600e-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="e600e-122">Odaberite **Gotovo**.</span><span class="sxs-lookup"><span data-stu-id="e600e-122">Select **Done**.</span></span> <span data-ttu-id="e600e-123">LCS će provjeriti paket.</span><span class="sxs-lookup"><span data-stu-id="e600e-123">LCS will verify the package.</span></span> <span data-ttu-id="e600e-124">Provjera može trajati nekoliko minuta ili do jedan sat.</span><span class="sxs-lookup"><span data-stu-id="e600e-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="e600e-125">Primjena paketa za ažuriranje</span><span class="sxs-lookup"><span data-stu-id="e600e-125">Apply the package update</span></span>

1. <span data-ttu-id="e600e-126">Na stranici **Pojedinosti okruženja** u LCS-u, odaberite **Održavaj** > **Primijeni ažuriranja**.</span><span class="sxs-lookup"><span data-stu-id="e600e-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="e600e-127">S popisa odaberite paket koji ste ranije spremili, a zatim odaberite **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="e600e-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="e600e-128">Odaberite **Da** kako biste potvrdili da želite implementirati paket.</span><span class="sxs-lookup"><span data-stu-id="e600e-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Potvrda dijaloškog okvira za implementaciju paketa](media/confirm-package-deployment.png)

4. <span data-ttu-id="e600e-130">Odaberite **Da** kako biste potvrdili da želite ažurirati aplikaciju.</span><span class="sxs-lookup"><span data-stu-id="e600e-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Potvrđivanje dijaloškog okvira za ažuriranje aplikacije](media/confirm-application-update.png)

<span data-ttu-id="e600e-132">Započet će implementacija i ažuriranje aplikacije.</span><span class="sxs-lookup"><span data-stu-id="e600e-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="e600e-133">U gornjem desnom kutu stranice **Pojedinosti okruženja** status okoliša ažurirat će se na **Servisiranje**.</span><span class="sxs-lookup"><span data-stu-id="e600e-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="e600e-134">Ažuriranje će se dovršiti za otprilike dva sata.</span><span class="sxs-lookup"><span data-stu-id="e600e-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="e600e-135">Podaci o izdanju aplikacije ažurirat će se na **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, a status okruženja ažurirat će se na **Implementiran**.</span><span class="sxs-lookup"><span data-stu-id="e600e-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="e600e-136">Ažuriranje okruženja platforme Dataverse</span><span class="sxs-lookup"><span data-stu-id="e600e-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="e600e-137">Prijavite se u [centar za administratore platforme Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="e600e-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="e600e-138">Na popisu pronađite i otvorite okruženje koje ste upotrebljavali za instalaciju aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e600e-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="e600e-139">Na stranici **Okruženja** odaberite **Resurs** > **Aplikacije sustava Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e600e-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="e600e-140">Na popisu pronađite **Microsoft Dynamics 365 Project Operations** i u stupcu **Status** odaberite **Ažuriranje dostupno**.</span><span class="sxs-lookup"><span data-stu-id="e600e-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="e600e-141">Odaberite potvrdni okvir **Slažem se s uvjetima pružanja usluge**, a zatim odaberite **Ažuriraj**.</span><span class="sxs-lookup"><span data-stu-id="e600e-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="e600e-142">Instalirat će se najnovija verzija rješenja.</span><span class="sxs-lookup"><span data-stu-id="e600e-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="e600e-143">Nakon završetka instalacije imat ćete instaliranu verziju 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="e600e-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="e600e-144">Konfiguriranje novih značajki</span><span class="sxs-lookup"><span data-stu-id="e600e-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="e600e-145">Omogućivanje mapiranja dvostrukog pisanja</span><span class="sxs-lookup"><span data-stu-id="e600e-145">Enable dual-write mapping</span></span>

<span data-ttu-id="e600e-146">Nakon što dovršite ažuriranje aplikacije Financije i okruženja platforme Dataverse možete omogućiti potrebna mapiranja dvostrukog pisanja.</span><span class="sxs-lookup"><span data-stu-id="e600e-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="e600e-147">Izvršite sljedeće postupke kako biste omogućili mapiranje dvostrukog pisanja:</span><span class="sxs-lookup"><span data-stu-id="e600e-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="e600e-148">Ažuriranje sigurnosnih postavki u okruženju aplikacije Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="e600e-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="e600e-149">Osvježavanje unosa podataka</span><span class="sxs-lookup"><span data-stu-id="e600e-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="e600e-150">Ažuriranje i pokretanje mapiranja dvostrukog pisanja</span><span class="sxs-lookup"><span data-stu-id="e600e-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="e600e-151">Ažuriranje sigurnosnih postavki u okruženju platforme Dataverse</span><span class="sxs-lookup"><span data-stu-id="e600e-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="e600e-152">Sljedeća ažuriranja sigurnosnih ovlasti za entitete potrebna su kao dio ažuriranja UR5.</span><span class="sxs-lookup"><span data-stu-id="e600e-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="e600e-153">U okruženju svoje platforme Dataverse idite na **Postavke** i u grupi **Sustav** odaberite **Sigurnost**.</span><span class="sxs-lookup"><span data-stu-id="e600e-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Postavke okruženja platforme Dataverse](media/Picture21.png)

2. <span data-ttu-id="e600e-155">Odaberite mogućnost **Sigurnosna uloga**.</span><span class="sxs-lookup"><span data-stu-id="e600e-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="e600e-156">S popisa uloga odaberite **korisnik aplikacije dvostrukog ispisa** i odaberite karticu **Prilagođeni entiteti**.</span><span class="sxs-lookup"><span data-stu-id="e600e-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="e600e-157">Provjerite ima li uloge **Čitanje** i **Dodaj u** dozvole za:</span><span class="sxs-lookup"><span data-stu-id="e600e-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="e600e-158">**Vrstu deviznog tečaja valute**</span><span class="sxs-lookup"><span data-stu-id="e600e-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="e600e-159">**Grafikon računa**</span><span class="sxs-lookup"><span data-stu-id="e600e-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="e600e-160">**Fiskalni kalendar**</span><span class="sxs-lookup"><span data-stu-id="e600e-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="e600e-161">**Knjiga**</span><span class="sxs-lookup"><span data-stu-id="e600e-161">**Ledger**</span></span>

5. <span data-ttu-id="e600e-162">Nakon ažuriranja sigurnosne uloge idite na **Postavke** > **Sigurnost** > **Teams**.</span><span class="sxs-lookup"><span data-stu-id="e600e-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="e600e-163">Provjerite primjenjuje li se uloga **korisnik aplikacije dvostrukog pisanja** na tim.</span><span class="sxs-lookup"><span data-stu-id="e600e-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="e600e-164">Osvježite podatkovne jedinice iz ažuriranja</span><span class="sxs-lookup"><span data-stu-id="e600e-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="e600e-165">U okruženju vaše aplikacije Financije otvorite radni prostor **Upravljanje podacima**, a zatim otvorite stranicu **Parametri okvira**.</span><span class="sxs-lookup"><span data-stu-id="e600e-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="e600e-166">Na kartici **Postavke entiteta** odaberite **Osvježi popis entiteta**.</span><span class="sxs-lookup"><span data-stu-id="e600e-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="e600e-167">Odaberite **Zatvori** za potvrdu osvježavanja entiteta.</span><span class="sxs-lookup"><span data-stu-id="e600e-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e600e-168">Za dovršenje ovog postupka treba približno 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="e600e-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="e600e-169">Kada se osvježavanje završi primit ćete obavijest.</span><span class="sxs-lookup"><span data-stu-id="e600e-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="e600e-170">Ažuriranje mapiranja dvostrukog pisanja</span><span class="sxs-lookup"><span data-stu-id="e600e-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="e600e-171">U radnom prostoru **Upravljanje podacima** odaberite **Dvostruko pisanje**.</span><span class="sxs-lookup"><span data-stu-id="e600e-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="e600e-172">Odaberite **Primijeniti rješenja**, odaberite oba rješenja s popisa, a zatim odaberite **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="e600e-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="e600e-173">Na stranici **Dvostruko pisanje** odaberite sljedeće karte tablice, a zatim odaberite **Zaustavi**.</span><span class="sxs-lookup"><span data-stu-id="e600e-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="e600e-174">**Stvarni podaci aplikacije Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="e600e-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="e600e-175">**Kategorije troškova projekta za integraciju aplikacije Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="e600e-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="e600e-176">**Entitet izvoza stvarnih troškova projekta za integraciju aplikacije Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e600e-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="e600e-177">Na stranici **Verzija karte tablice** primijenite novu verziju karte na svaki od tri entiteta.</span><span class="sxs-lookup"><span data-stu-id="e600e-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="e600e-178">Na stranici **Dvostruko pisanje** odaberite Pokreni za ponovno pokretanje karti.</span><span class="sxs-lookup"><span data-stu-id="e600e-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="e600e-179">S popisa karti odaberite kartu **Knjiga (msdyn_ledgers)** sa svim preduvjetima i odaberite potvrdni okvir **Početna sinkronizacija**.</span><span class="sxs-lookup"><span data-stu-id="e600e-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="e600e-180">U polju **Glavni za početnu sinkronizaciju** odaberite **Aplikacije rješenja Finance and Operations**, a zatim odaberite **Pokreni**.</span><span class="sxs-lookup"><span data-stu-id="e600e-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sinkronizacija karte knjige](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]