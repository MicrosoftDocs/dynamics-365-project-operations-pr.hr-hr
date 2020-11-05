---
title: Priprema novog okruženja
description: U ovoj temi nalaze se informacije o načinu pripreme novog okruženja aplikacije Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073275"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="e039f-103">Priprema novog okruženja</span><span class="sxs-lookup"><span data-stu-id="e039f-103">Provision a new environment</span></span>

<span data-ttu-id="e039f-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="e039f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e039f-105">U ovoj temi nalaze se informacije o načinu pripreme okruženja aplikacije Dynamics 365 Project Operations za scenarije koji se temelje na resursu / bez zalihe.</span><span class="sxs-lookup"><span data-stu-id="e039f-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="e039f-106">Omogućivanje automatiziranu pripremu aplikacije Project Operations u LCS projektu</span><span class="sxs-lookup"><span data-stu-id="e039f-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="e039f-107">Poduzmite sljedeće korake kako biste omogućili automatizirani tijek pripreme za LCS projekt.</span><span class="sxs-lookup"><span data-stu-id="e039f-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="e039f-108">Idite na [LCS](https://lcs.dynamics.com/v2) i odaberite pločicu **Pregled upravljanja značajkama**.</span><span class="sxs-lookup"><span data-stu-id="e039f-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="e039f-109">U popisu **Značajka pregleda** odaberite **Značajka aplikacije Project Operations** i zatim odaberite **Omogućena značajka pregleda** kako biste omogućili aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e039f-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e039f-110">Ovaj korak izvodi se samo jedanput po LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="e039f-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="e039f-111">Priprema okruženja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="e039f-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="e039f-112">Otvorite novo Dynamics 365 Finance [probno okruženje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili implementaciju [sigurnosne ograde / proizvodnog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="e039f-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="e039f-113">Upoznajte se s radom čarobnjaka **Priprema okruženja**.</span><span class="sxs-lookup"><span data-stu-id="e039f-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e039f-114">Provjerite je li odabrana verzija aplikacije 10.0.13 ili novija.</span><span class="sxs-lookup"><span data-stu-id="e039f-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="e039f-115">Za pripremu aplikacije Project Operations, pod stavkom **Napredne postavke** odaberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e039f-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="e039f-116">Omogućite **Postavljanje platforme Common Data Service** odabirom mogućnosti **Da** a zatim u obvezna polja unesite podatke:</span><span class="sxs-lookup"><span data-stu-id="e039f-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="e039f-117">Ime</span><span class="sxs-lookup"><span data-stu-id="e039f-117">Name</span></span>
  - <span data-ttu-id="e039f-118">Regija</span><span class="sxs-lookup"><span data-stu-id="e039f-118">Region</span></span>
  - <span data-ttu-id="e039f-119">Jezik</span><span class="sxs-lookup"><span data-stu-id="e039f-119">Language</span></span>
  - <span data-ttu-id="e039f-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="e039f-120">Currency</span></span>
 
5. <span data-ttu-id="e039f-121">U polju **Predložak platforme Common Data Service** odaberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="e039f-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="e039f-122">Odaberite vrstu okruženja za implementaciju.</span><span class="sxs-lookup"><span data-stu-id="e039f-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="e039f-123">Probno razdoblje koje se temelji na pretplati omogućit će vam postavljanje CDS okruženja na 30 dana.</span><span class="sxs-lookup"><span data-stu-id="e039f-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Postavke implementacije](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="e039f-125">Odaberite **Slažem se** kako biste se potvrdili uvjete usluge i zatim odaberite **Gotovo** za povratak na postavke implementacije.</span><span class="sxs-lookup"><span data-stu-id="e039f-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Pristanak za implementaciju](./media/2DeploymentConsent.png)

7. <span data-ttu-id="e039f-127">Ispunite preostala potrebna polja u čarobnjaku i potvrdite implementaciju.</span><span class="sxs-lookup"><span data-stu-id="e039f-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="e039f-128">Vrijeme pripreme okruženja razlikuje se ovisno o vrsti okruženja.</span><span class="sxs-lookup"><span data-stu-id="e039f-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="e039f-129">Priprema može potrajati do šest sati.</span><span class="sxs-lookup"><span data-stu-id="e039f-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="e039f-130">Nakon što se implementacija uspješno dovrši, okruženje će se prikazati kao **Implementirano**.</span><span class="sxs-lookup"><span data-stu-id="e039f-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="e039f-131">Kako biste potvrdili da je okruženje uspješno implementirano, odaberite mogućnost **Prijava** i prijavite se u okruženje kako biste to potvrdili.</span><span class="sxs-lookup"><span data-stu-id="e039f-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Pojedinosti  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="e039f-133">Primjena pokaznih podataka aplikacije Project Operations Finance (neobvezni korak)</span><span class="sxs-lookup"><span data-stu-id="e039f-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="e039f-134">Primijenite pokazne podatke aplikacije Project Operations Finance na izdanje usluge Okruženje hostirano u oblaku 10.0.13 na način opisan u [ovom članku](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="e039f-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="e039f-135">Primjena ažuriranja na okruženje aplikacije Finance.</span><span class="sxs-lookup"><span data-stu-id="e039f-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="e039f-136">Project Operations zahtijeva okruženje aplikacije Finance verzije **10.0.13 (10.0.569.20009)** ili više.</span><span class="sxs-lookup"><span data-stu-id="e039f-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="e039f-137">Možda ćete trebati primijeniti kvalitativna ažuriranja u svom okruženju aplikacije Finance kako biste primili ovu verziju.</span><span class="sxs-lookup"><span data-stu-id="e039f-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="e039f-138">Na stranici **Pojedinosti okruženja** LSC-a, u odjeljku **Dostupna ažuriranja** , odaberite **Pogledajte ažuriranje**.</span><span class="sxs-lookup"><span data-stu-id="e039f-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz ažuriranja](./media/5ViewUpdates.png)

2. <span data-ttu-id="e039f-140">Na stranici **Binarna ažuriranja** odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="e039f-140">On the **Binary updates** page, select **Save package.**</span></span>

![Spremanje paketa](./media/6SavePackage.png)

3. <span data-ttu-id="e039f-142">Kliknite **Odberi sve** i zatim odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="e039f-142">Click **Select all** and then select **Save package**.</span></span>

![Pregled i spremanje ažuriranja](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="e039f-144">Unesite ime i opis paketa, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="e039f-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="e039f-145">Ovisno o internetskoj vezi, ovaj postupak može potrajati.</span><span class="sxs-lookup"><span data-stu-id="e039f-145">Depending on the internet connection, this process might take some time.</span></span>

![Prenesite paket u biblioteku Sredstva](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="e039f-147">Nakon spremanja paketa odaberite **Gotovo** i spremite ovaj paket u biblioteku Sredstava svojeg LCS projekta.</span><span class="sxs-lookup"><span data-stu-id="e039f-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="e039f-148">Spremanje i provjera valjanosti paketa može potrajati oko 15 minuta.</span><span class="sxs-lookup"><span data-stu-id="e039f-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="e039f-149">Kako biste primijenili ažuriranje, pomaknite se na stranicu **Pojedinosti okruženja** u LCS-u i odaberite **Održavaj** > **Primijeni ažuriranja**.</span><span class="sxs-lookup"><span data-stu-id="e039f-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="e039f-151">Na popisu ažuriranja odaberite paket koji ste stvorili, a zatim **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="e039f-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Primjena ažuriranja](./media/10ApplyUpdates.png)

<span data-ttu-id="e039f-153">Održavanje okruženja potrajat će neko vrijeme.</span><span class="sxs-lookup"><span data-stu-id="e039f-153">Environment servicing will take some time.</span></span> <span data-ttu-id="e039f-154">Nakon završetka, okruženje će se vratiti u implementirano stanje.</span><span class="sxs-lookup"><span data-stu-id="e039f-154">After it is complete, the environment will return to a deployed state.</span></span>

![Okruženje implementirano](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="e039f-156">Uspostavljanje veze dvostrukog zapisivanja</span><span class="sxs-lookup"><span data-stu-id="e039f-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="e039f-157">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="e039f-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e039f-158">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="e039f-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="e039f-159">Nakon dovršetka veze ponovno odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="e039f-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="e039f-160">Bit ćete preusmjereni na dvostruko zapisivanje u aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="e039f-160">You will be redirected to Dual Write in Finance.</span></span>

![Veza na CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="e039f-162">Odaberite **Primjeni rješenje** kako biste pristupili entitetima koji će biti mapirani u integraciju.</span><span class="sxs-lookup"><span data-stu-id="e039f-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Primjena rješenja](./media/13ApplySolutions.png)

5. <span data-ttu-id="e039f-164">Odaberite oba rješenja, **Dvostruko zapisivanje mape entiteta aplikacije Dynamics 365 Finance and Operations** i **Dvostruko zapisivanje mapa entiteta aplikacije Dynamics 365 Project Operations** , a zatim odaberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="e039f-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Potvrda rješenja](./media/14ConfirmSolutions.png)

<span data-ttu-id="e039f-166">Nakon primjene rješenja, entiteti dvostrukog zapisivanja primjenjuju se na okruženje.</span><span class="sxs-lookup"><span data-stu-id="e039f-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Primjena rješenja](./media/15ApplyingSolutions.png)

<span data-ttu-id="e039f-168">Nakon primjene entiteta, sva raspoloživa mapiranja navedena su u okruženju.</span><span class="sxs-lookup"><span data-stu-id="e039f-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mape dvostrukog zapisivanja](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="e039f-170">Osvježavanje podatkovnih entiteta nakon ažuriranja</span><span class="sxs-lookup"><span data-stu-id="e039f-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="e039f-171">U aplikaciji Finance, idite na radni prostor **Upravljanje podacima**.</span><span class="sxs-lookup"><span data-stu-id="e039f-171">In Finance, go to the **Data management** workspace.</span></span>

![Radni prostor upravljanja podacima](./media/16DataManagement.png)

2. <span data-ttu-id="e039f-173">Odaberite pločicu **Parametri okvira**.</span><span class="sxs-lookup"><span data-stu-id="e039f-173">Select the **Framework parameters** tile.</span></span>

![Parametri okvira](./media/17FrameworkParameters.png)

3. <span data-ttu-id="e039f-175">Na stranici **Postavke entiteta** , odaberite mogućnost **Osvježi popis entiteta**.</span><span class="sxs-lookup"><span data-stu-id="e039f-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osvježavanje popisa entiteta](./media/18RefreshEntityList.png)

<span data-ttu-id="e039f-177">Osvježavanje će potrajati otprilike 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="e039f-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="e039f-178">Kada bude dovršeno dobit ćete upozorenje.</span><span class="sxs-lookup"><span data-stu-id="e039f-178">You will receive an alert when it is complete.</span></span>

![Potvrda osvježavanja](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="e039f-180">Pokretanje mapa dvostrukog zapisivanja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="e039f-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="e039f-181">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="e039f-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e039f-182">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="e039f-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="e039f-183">Nakon što odaberete vezu, bit ćete preusmjereni na popis entiteta u mapiranjima.</span><span class="sxs-lookup"><span data-stu-id="e039f-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="e039f-184">Pokrenite mape na način opisan u sljedećoj tablici.</span><span class="sxs-lookup"><span data-stu-id="e039f-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="e039f-185">Svakako slijedite redoslijed kako je naveden.</span><span class="sxs-lookup"><span data-stu-id="e039f-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="e039f-186">**Karta entiteta**</span><span class="sxs-lookup"><span data-stu-id="e039f-186">**Entity Map**</span></span> | <span data-ttu-id="e039f-187">**Osvježi entitet**</span><span class="sxs-lookup"><span data-stu-id="e039f-187">**Refresh entity**</span></span> | <span data-ttu-id="e039f-188">**Početna sinkronizacija**</span><span class="sxs-lookup"><span data-stu-id="e039f-188">**Initial sync**</span></span> | <span data-ttu-id="e039f-189">**Glavni za početnu sinkronizaciju**</span><span class="sxs-lookup"><span data-stu-id="e039f-189">**Master for initial sync**</span></span> | <span data-ttu-id="e039f-190">**Pokreni preduvjete**</span><span class="sxs-lookup"><span data-stu-id="e039f-190">**Run prerequisites**</span></span> | <span data-ttu-id="e039f-191">**Početna sinkronizacija preduvjeta**</span><span class="sxs-lookup"><span data-stu-id="e039f-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="e039f-192">**Uloge aplikacije Project Resource za sve tvrtke (kategorije resursa koji se mogu rezervirati)**</span><span class="sxs-lookup"><span data-stu-id="e039f-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="e039f-193">No</span><span class="sxs-lookup"><span data-stu-id="e039f-193">No</span></span> | <span data-ttu-id="e039f-194">Jest</span><span class="sxs-lookup"><span data-stu-id="e039f-194">Yes</span></span> | <span data-ttu-id="e039f-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e039f-195">Common Data Service</span></span> | <span data-ttu-id="e039f-196">No</span><span class="sxs-lookup"><span data-stu-id="e039f-196">No</span></span> | <span data-ttu-id="e039f-197">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-197">N\A</span></span> |
| <span data-ttu-id="e039f-198">**Pravne osobe (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="e039f-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="e039f-199">No</span><span class="sxs-lookup"><span data-stu-id="e039f-199">No</span></span> | <span data-ttu-id="e039f-200">Jest</span><span class="sxs-lookup"><span data-stu-id="e039f-200">Yes</span></span> | <span data-ttu-id="e039f-201">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e039f-201">Finance and Operations apps</span></span> | <span data-ttu-id="e039f-202">No</span><span class="sxs-lookup"><span data-stu-id="e039f-202">No</span></span> | <span data-ttu-id="e039f-203">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-203">N\A</span></span> |
| <span data-ttu-id="e039f-204">**Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="e039f-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="e039f-205">No</span><span class="sxs-lookup"><span data-stu-id="e039f-205">No</span></span> | <span data-ttu-id="e039f-206">No</span><span class="sxs-lookup"><span data-stu-id="e039f-206">No</span></span> | <span data-ttu-id="e039f-207">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-207">N\A</span></span> | <span data-ttu-id="e039f-208">Jest</span><span class="sxs-lookup"><span data-stu-id="e039f-208">Yes</span></span> | <span data-ttu-id="e039f-209">No</span><span class="sxs-lookup"><span data-stu-id="e039f-209">No</span></span> |
| <span data-ttu-id="e039f-210">**Redci ugovora o projektu (pojedinosti prodajnog naloga)**</span><span class="sxs-lookup"><span data-stu-id="e039f-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="e039f-211">No</span><span class="sxs-lookup"><span data-stu-id="e039f-211">No</span></span> | <span data-ttu-id="e039f-212">No</span><span class="sxs-lookup"><span data-stu-id="e039f-212">No</span></span> | <span data-ttu-id="e039f-213">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-213">N\A</span></span> | <span data-ttu-id="e039f-214">No</span><span class="sxs-lookup"><span data-stu-id="e039f-214">No</span></span> | <span data-ttu-id="e039f-215">No</span><span class="sxs-lookup"><span data-stu-id="e039f-215">No</span></span> |
| <span data-ttu-id="e039f-216">**Entitet integracije za odnose projektne transakcije (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="e039f-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="e039f-217">No</span><span class="sxs-lookup"><span data-stu-id="e039f-217">No</span></span> | <span data-ttu-id="e039f-218">No</span><span class="sxs-lookup"><span data-stu-id="e039f-218">No</span></span> | <span data-ttu-id="e039f-219">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-219">N\A</span></span> | <span data-ttu-id="e039f-220">No</span><span class="sxs-lookup"><span data-stu-id="e039f-220">No</span></span> | <span data-ttu-id="e039f-221">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-221">N\A</span></span> |
| <span data-ttu-id="e039f-222">**Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="e039f-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="e039f-223">No</span><span class="sxs-lookup"><span data-stu-id="e039f-223">No</span></span> | <span data-ttu-id="e039f-224">No</span><span class="sxs-lookup"><span data-stu-id="e039f-224">No</span></span> | <span data-ttu-id="e039f-225">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-225">N\A</span></span> | <span data-ttu-id="e039f-226">No</span><span class="sxs-lookup"><span data-stu-id="e039f-226">No</span></span> | <span data-ttu-id="e039f-227">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-227">N\A</span></span> |
| <span data-ttu-id="e039f-228">**Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="e039f-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="e039f-229">No</span><span class="sxs-lookup"><span data-stu-id="e039f-229">No</span></span> | <span data-ttu-id="e039f-230">No</span><span class="sxs-lookup"><span data-stu-id="e039f-230">No</span></span> | <span data-ttu-id="e039f-231">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-231">N\A</span></span> | <span data-ttu-id="e039f-232">No</span><span class="sxs-lookup"><span data-stu-id="e039f-232">No</span></span> | <span data-ttu-id="e039f-233">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-233">N\A</span></span> |
| <span data-ttu-id="e039f-234">**Entitet izvoza kategorija troškova projekta za integraciju aplikacije Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="e039f-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="e039f-235">No</span><span class="sxs-lookup"><span data-stu-id="e039f-235">No</span></span> | <span data-ttu-id="e039f-236">No</span><span class="sxs-lookup"><span data-stu-id="e039f-236">No</span></span> | <span data-ttu-id="e039f-237">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-237">N\A</span></span> | <span data-ttu-id="e039f-238">No</span><span class="sxs-lookup"><span data-stu-id="e039f-238">No</span></span> | <span data-ttu-id="e039f-239">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-239">N\A</span></span> |
| <span data-ttu-id="e039f-240">**Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e039f-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="e039f-241">Jest</span><span class="sxs-lookup"><span data-stu-id="e039f-241">Yes</span></span> | <span data-ttu-id="e039f-242">No</span><span class="sxs-lookup"><span data-stu-id="e039f-242">No</span></span> | <span data-ttu-id="e039f-243">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-243">N\A</span></span> | <span data-ttu-id="e039f-244">No</span><span class="sxs-lookup"><span data-stu-id="e039f-244">No</span></span> | <span data-ttu-id="e039f-245">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-245">N\A</span></span> |
| <span data-ttu-id="e039f-246">**Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="e039f-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="e039f-247">Jest</span><span class="sxs-lookup"><span data-stu-id="e039f-247">Yes</span></span> | <span data-ttu-id="e039f-248">No</span><span class="sxs-lookup"><span data-stu-id="e039f-248">No</span></span> | <span data-ttu-id="e039f-249">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-249">N\A</span></span> | <span data-ttu-id="e039f-250">No</span><span class="sxs-lookup"><span data-stu-id="e039f-250">No</span></span> | <span data-ttu-id="e039f-251">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="e039f-251">N\A</span></span> |


4. <span data-ttu-id="e039f-252">Kako biste osvježili entitet, odaberite naziv mape, a zatim odaberite **Osvježi entitete**.</span><span class="sxs-lookup"><span data-stu-id="e039f-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osvježavanje mape](./media/20RefreshMapping.png)

5. <span data-ttu-id="e039f-254">Nakon završetka osvježavanja pokrenite mapu.</span><span class="sxs-lookup"><span data-stu-id="e039f-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="e039f-255">Prije nego što omogućite sljedeću mapu, provjerite je li mapa u tablici u stanju **Izvodi se**.</span><span class="sxs-lookup"><span data-stu-id="e039f-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="e039f-256">Izvođenje mapa s većim brojem preduvjeta može potrajati.</span><span class="sxs-lookup"><span data-stu-id="e039f-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="e039f-257">Kako biste pokrenuli mapu s preduvjetima, omogućite preklopni gumb **Prikaži povezane mape entiteta**.</span><span class="sxs-lookup"><span data-stu-id="e039f-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="e039f-258">Ako je u tablici navedeno kako **Početna sinkronizacija preduvjeta** ima vrijednost **Ne** , prije pokretanja provjerite je li zastavica **Početna sinkronizacija** postavljena na **Isključeno** na svim mapama s preduvjetima.</span><span class="sxs-lookup"><span data-stu-id="e039f-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Pokretanje mape](./media/21RunMap.png)

6. <span data-ttu-id="e039f-260">Provjerite jesu li sve mape povezane s projektom u stanju aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="e039f-260">Validate all project related maps are in the running state.</span></span>

![Sve mape rade](./media/22AllMapsRunning.png)

<span data-ttu-id="e039f-262">Vaše okruženje Project Operations sada je pripremljeno i konfigurirano.</span><span class="sxs-lookup"><span data-stu-id="e039f-262">Your Project Operations environment is now provisioned and configured.</span></span>
