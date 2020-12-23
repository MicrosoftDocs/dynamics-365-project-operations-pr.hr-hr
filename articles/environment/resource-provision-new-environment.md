---
title: Priprema novog okruženja
description: U ovoj temi nalaze se informacije o načinu pripreme novog okruženja aplikacije Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642953"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="1cbec-103">Priprema novog okruženja</span><span class="sxs-lookup"><span data-stu-id="1cbec-103">Provision a new environment</span></span>

<span data-ttu-id="1cbec-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="1cbec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1cbec-105">U ovoj temi nalaze se informacije o načinu omogućivanja novog okruženja aplikacije Dynamics 365 Project Operations za scenarije koji se temelje na resursu / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="1cbec-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="1cbec-106">Omogućivanje automatiziranu pripremu aplikacije Project Operations u LCS projektu</span><span class="sxs-lookup"><span data-stu-id="1cbec-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="1cbec-107">Poduzmite sljedeće korake kako biste omogućili automatizirani tijek pripreme za LCS projekt.</span><span class="sxs-lookup"><span data-stu-id="1cbec-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="1cbec-108">Idite na [LCS](https://lcs.dynamics.com/v2) i odaberite pločicu **Pregled upravljanja značajkama**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="1cbec-109">U popisu **Značajka pregleda** odaberite **Značajka aplikacije Project Operations** i zatim odaberite **Omogućena značajka pregleda** kako biste omogućili aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1cbec-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="1cbec-110">Ovaj korak izvodi se samo jedanput po LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="1cbec-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="1cbec-111">Priprema okruženja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="1cbec-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="1cbec-112">Otvorite novo Dynamics 365 Finance [probno okruženje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili implementaciju [sigurnosne ograde / proizvodnog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="1cbec-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="1cbec-113">Upoznajte se s radom čarobnjaka **Priprema okruženja**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="1cbec-114">Provjerite je li odabrana verzija aplikacije 10.0.13 ili novija.</span><span class="sxs-lookup"><span data-stu-id="1cbec-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="1cbec-115">Za pripremu aplikacije Project Operations, pod stavkom **Napredne postavke** odaberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="1cbec-116">Omogućite **Postavljanje platforme Common Data Service** odabirom mogućnosti **Da** a zatim u obvezna polja unesite podatke:</span><span class="sxs-lookup"><span data-stu-id="1cbec-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="1cbec-117">Ime</span><span class="sxs-lookup"><span data-stu-id="1cbec-117">Name</span></span>
  - <span data-ttu-id="1cbec-118">Regija</span><span class="sxs-lookup"><span data-stu-id="1cbec-118">Region</span></span>
  - <span data-ttu-id="1cbec-119">Jezik</span><span class="sxs-lookup"><span data-stu-id="1cbec-119">Language</span></span>
  - <span data-ttu-id="1cbec-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="1cbec-120">Currency</span></span>
 
5. <span data-ttu-id="1cbec-121">U polju **Predložak platforme Common Data Service** odaberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="1cbec-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="1cbec-122">Odaberite vrstu okruženja za implementaciju.</span><span class="sxs-lookup"><span data-stu-id="1cbec-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="1cbec-123">Probno razdoblje koje se temelji na pretplati omogućit će vam postavljanje CDS okruženja na 30 dana.</span><span class="sxs-lookup"><span data-stu-id="1cbec-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Postavke implementacije](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="1cbec-125">Odaberite **Slažem se** kako biste se potvrdili uvjete usluge i zatim odaberite **Gotovo** za povratak na postavke implementacije.</span><span class="sxs-lookup"><span data-stu-id="1cbec-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Pristanak za implementaciju](./media/2DeploymentConsent.png)

7. <span data-ttu-id="1cbec-127">Ispunite preostala potrebna polja u čarobnjaku i potvrdite implementaciju.</span><span class="sxs-lookup"><span data-stu-id="1cbec-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="1cbec-128">Vrijeme pripreme okruženja razlikuje se ovisno o vrsti okruženja.</span><span class="sxs-lookup"><span data-stu-id="1cbec-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="1cbec-129">Priprema može potrajati do šest sati.</span><span class="sxs-lookup"><span data-stu-id="1cbec-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="1cbec-130">Nakon što se implementacija uspješno dovrši, okruženje će se prikazati kao **Implementirano**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="1cbec-131">Kako biste potvrdili da je okruženje uspješno implementirano, odaberite mogućnost **Prijava** i prijavite se u okruženje kako biste to potvrdili.</span><span class="sxs-lookup"><span data-stu-id="1cbec-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Pojedinosti  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="1cbec-133">Primjena pokaznih podataka aplikacije Project Operations Finance (neobvezni korak)</span><span class="sxs-lookup"><span data-stu-id="1cbec-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="1cbec-134">Primijenite pokazne podatke aplikacije Project Operations Finance na izdanje usluge Okruženje hostirano u oblaku 10.0.13 na način opisan u [ovom članku](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="1cbec-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="1cbec-135">Primjena ažuriranja na okruženje aplikacije Finance.</span><span class="sxs-lookup"><span data-stu-id="1cbec-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="1cbec-136">Project Operations zahtijeva okruženje aplikacije Finance verzije **10.0.13 (10.0.569.20009)** ili više.</span><span class="sxs-lookup"><span data-stu-id="1cbec-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="1cbec-137">Možda ćete trebati primijeniti kvalitativna ažuriranja u svom okruženju aplikacije Finance kako biste primili ovu verziju.</span><span class="sxs-lookup"><span data-stu-id="1cbec-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="1cbec-138">Na stranici **Pojedinosti okruženja** LSC-a, u odjeljku **Dostupna ažuriranja**, odaberite **Pogledajte ažuriranje**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz ažuriranja](./media/5ViewUpdates.png)

2. <span data-ttu-id="1cbec-140">Na stranici **Binarna ažuriranja** odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-140">On the **Binary updates** page, select **Save package.**</span></span>

![Spremanje paketa](./media/6SavePackage.png)

3. <span data-ttu-id="1cbec-142">Kliknite **Odberi sve** i zatim odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-142">Click **Select all** and then select **Save package**.</span></span>

![Pregled i spremanje ažuriranja](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="1cbec-144">Unesite ime i opis paketa, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="1cbec-145">Ovisno o internetskoj vezi, ovaj postupak može potrajati.</span><span class="sxs-lookup"><span data-stu-id="1cbec-145">Depending on the internet connection, this process might take some time.</span></span>

![Prenesite paket u biblioteku Sredstva](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="1cbec-147">Nakon spremanja paketa odaberite **Gotovo** i spremite ovaj paket u biblioteku Sredstava svojeg LCS projekta.</span><span class="sxs-lookup"><span data-stu-id="1cbec-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="1cbec-148">Spremanje i provjera valjanosti paketa može potrajati oko 15 minuta.</span><span class="sxs-lookup"><span data-stu-id="1cbec-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="1cbec-149">Kako biste primijenili ažuriranje, pomaknite se na stranicu **Pojedinosti okruženja** u LCS-u i odaberite **Održavaj** > **Primijeni ažuriranja**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="1cbec-151">Na popisu ažuriranja odaberite paket koji ste stvorili, a zatim **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Primjena ažuriranja](./media/10ApplyUpdates.png)

<span data-ttu-id="1cbec-153">Održavanje okruženja potrajat će neko vrijeme.</span><span class="sxs-lookup"><span data-stu-id="1cbec-153">Environment servicing will take some time.</span></span> <span data-ttu-id="1cbec-154">Nakon završetka, okruženje će se vratiti u implementirano stanje.</span><span class="sxs-lookup"><span data-stu-id="1cbec-154">After it is complete, the environment will return to a deployed state.</span></span>

![Okruženje implementirano](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="1cbec-156">Uspostavljanje veze dvostrukog zapisivanja</span><span class="sxs-lookup"><span data-stu-id="1cbec-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="1cbec-157">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="1cbec-158">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="1cbec-159">Nakon dovršetka veze ponovno odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="1cbec-160">Bit ćete preusmjereni na dvostruko zapisivanje u aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="1cbec-160">You will be redirected to Dual Write in Finance.</span></span>

![Veza na CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="1cbec-162">Odaberite **Primjeni rješenje** kako biste pristupili entitetima koji će biti mapirani u integraciju.</span><span class="sxs-lookup"><span data-stu-id="1cbec-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Primjena rješenja](./media/13ApplySolutions.png)

5. <span data-ttu-id="1cbec-164">Odaberite oba rješenja, **Karta entiteta aplikacije Dynamics 365 Finance and Operations za dvostruko upisivanje** i **Karte entiteta aplikacije Dynamics 365 Project Operations za dvostruko upisivanje**, a zatim odaberite mogućnost **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potvrda rješenja](./media/14ConfirmSolutions.png)

<span data-ttu-id="1cbec-166">Nakon primjene rješenja, entiteti dvostrukog zapisivanja primjenjuju se na okruženje.</span><span class="sxs-lookup"><span data-stu-id="1cbec-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Primjena rješenja](./media/15ApplyingSolutions.png)

<span data-ttu-id="1cbec-168">Nakon primjene entiteta, sva raspoloživa mapiranja navedena su u okruženju.</span><span class="sxs-lookup"><span data-stu-id="1cbec-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mape dvostrukog zapisivanja](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="1cbec-170">Osvježavanje podatkovnih entiteta nakon ažuriranja</span><span class="sxs-lookup"><span data-stu-id="1cbec-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="1cbec-171">U aplikaciji Finance, idite na radni prostor **Upravljanje podacima**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-171">In Finance, go to the **Data management** workspace.</span></span>

![Radni prostor upravljanja podacima](./media/16DataManagement.png)

2. <span data-ttu-id="1cbec-173">Odaberite pločicu **Parametri okvira**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-173">Select the **Framework parameters** tile.</span></span>

![Parametri okvira](./media/17FrameworkParameters.png)

3. <span data-ttu-id="1cbec-175">Na stranici **Postavke entiteta**, odaberite mogućnost **Osvježi popis entiteta**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osvježavanje popisa entiteta](./media/18RefreshEntityList.png)

<span data-ttu-id="1cbec-177">Osvježavanje će potrajati otprilike 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="1cbec-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="1cbec-178">Kada bude dovršeno dobit ćete upozorenje.</span><span class="sxs-lookup"><span data-stu-id="1cbec-178">You will receive an alert when it is complete.</span></span>

![Potvrda osvježavanja](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="1cbec-180">Pokretanje mapa dvostrukog zapisivanja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="1cbec-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="1cbec-181">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="1cbec-182">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="1cbec-183">Nakon što odaberete vezu, bit ćete preusmjereni na popis entiteta u mapiranjima.</span><span class="sxs-lookup"><span data-stu-id="1cbec-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="1cbec-184">Pokrenite mape na način opisan u sljedećoj tablici.</span><span class="sxs-lookup"><span data-stu-id="1cbec-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="1cbec-185">Svakako slijedite redoslijed kako je naveden.</span><span class="sxs-lookup"><span data-stu-id="1cbec-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="1cbec-186">**Karta entiteta**</span><span class="sxs-lookup"><span data-stu-id="1cbec-186">**Entity Map**</span></span> | <span data-ttu-id="1cbec-187">**Osvježi entitet**</span><span class="sxs-lookup"><span data-stu-id="1cbec-187">**Refresh entity**</span></span> | <span data-ttu-id="1cbec-188">**Početna sinkronizacija**</span><span class="sxs-lookup"><span data-stu-id="1cbec-188">**Initial sync**</span></span> | <span data-ttu-id="1cbec-189">**Glavni za početnu sinkronizaciju**</span><span class="sxs-lookup"><span data-stu-id="1cbec-189">**Master for initial sync**</span></span> | <span data-ttu-id="1cbec-190">**Pokreni preduvjete**</span><span class="sxs-lookup"><span data-stu-id="1cbec-190">**Run prerequisites**</span></span> | <span data-ttu-id="1cbec-191">**Početna sinkronizacija preduvjeta**</span><span class="sxs-lookup"><span data-stu-id="1cbec-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="1cbec-192">**Uloge aplikacije Project Resource za sve tvrtke (kategorije resursa koji se mogu rezervirati)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="1cbec-193">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-193">No</span></span> | <span data-ttu-id="1cbec-194">Jest</span><span class="sxs-lookup"><span data-stu-id="1cbec-194">Yes</span></span> | <span data-ttu-id="1cbec-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1cbec-195">Common Data Service</span></span> | <span data-ttu-id="1cbec-196">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-196">No</span></span> | <span data-ttu-id="1cbec-197">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-197">N\A</span></span> |
| <span data-ttu-id="1cbec-198">**Pravne osobe (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="1cbec-199">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-199">No</span></span> | <span data-ttu-id="1cbec-200">Jest</span><span class="sxs-lookup"><span data-stu-id="1cbec-200">Yes</span></span> | <span data-ttu-id="1cbec-201">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1cbec-201">Finance and Operations apps</span></span> | <span data-ttu-id="1cbec-202">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-202">No</span></span> | <span data-ttu-id="1cbec-203">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-203">N\A</span></span> |
| <span data-ttu-id="1cbec-204">**Glavna knjiga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="1cbec-205">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-205">No</span></span> | <span data-ttu-id="1cbec-206">Jest</span><span class="sxs-lookup"><span data-stu-id="1cbec-206">Yes</span></span> | <span data-ttu-id="1cbec-207">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1cbec-207">Finance and Operations apps</span></span> | <span data-ttu-id="1cbec-208">Jest</span><span class="sxs-lookup"><span data-stu-id="1cbec-208">Yes</span></span> | <span data-ttu-id="1cbec-209">Da, aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1cbec-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="1cbec-210">**Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="1cbec-211">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-211">No</span></span> | <span data-ttu-id="1cbec-212">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-212">No</span></span> | <span data-ttu-id="1cbec-213">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-213">N\A</span></span> | <span data-ttu-id="1cbec-214">Jest</span><span class="sxs-lookup"><span data-stu-id="1cbec-214">Yes</span></span> | <span data-ttu-id="1cbec-215">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-215">No</span></span> |
| <span data-ttu-id="1cbec-216">**Redci ugovora o projektu (pojedinosti prodajnog naloga)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="1cbec-217">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-217">No</span></span> | <span data-ttu-id="1cbec-218">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-218">No</span></span> | <span data-ttu-id="1cbec-219">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-219">N\A</span></span> | <span data-ttu-id="1cbec-220">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-220">No</span></span> | <span data-ttu-id="1cbec-221">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-221">No</span></span> |
| <span data-ttu-id="1cbec-222">**Entitet integracije za odnose projektne transakcije (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="1cbec-223">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-223">No</span></span> | <span data-ttu-id="1cbec-224">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-224">No</span></span> | <span data-ttu-id="1cbec-225">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-225">N\A</span></span> | <span data-ttu-id="1cbec-226">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-226">No</span></span> | <span data-ttu-id="1cbec-227">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-227">N\A</span></span> |
| <span data-ttu-id="1cbec-228">**Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="1cbec-229">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-229">No</span></span> | <span data-ttu-id="1cbec-230">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-230">No</span></span> | <span data-ttu-id="1cbec-231">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-231">N\A</span></span> | <span data-ttu-id="1cbec-232">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-232">No</span></span> | <span data-ttu-id="1cbec-233">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-233">N\A</span></span> |
| <span data-ttu-id="1cbec-234">**Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="1cbec-235">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-235">No</span></span> | <span data-ttu-id="1cbec-236">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-236">No</span></span> | <span data-ttu-id="1cbec-237">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-237">N\A</span></span> | <span data-ttu-id="1cbec-238">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-238">No</span></span> | <span data-ttu-id="1cbec-239">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-239">N\A</span></span> |
| <span data-ttu-id="1cbec-240">**Entitet izvoza kategorija troškova projekta za integraciju aplikacije Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="1cbec-241">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-241">No</span></span> | <span data-ttu-id="1cbec-242">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-242">No</span></span> | <span data-ttu-id="1cbec-243">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-243">N\A</span></span> | <span data-ttu-id="1cbec-244">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-244">No</span></span> | <span data-ttu-id="1cbec-245">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-245">N\A</span></span> |
| <span data-ttu-id="1cbec-246">**Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="1cbec-247">Jest</span><span class="sxs-lookup"><span data-stu-id="1cbec-247">Yes</span></span> | <span data-ttu-id="1cbec-248">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-248">No</span></span> | <span data-ttu-id="1cbec-249">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-249">N\A</span></span> | <span data-ttu-id="1cbec-250">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-250">No</span></span> | <span data-ttu-id="1cbec-251">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-251">N\A</span></span> |
| <span data-ttu-id="1cbec-252">**Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="1cbec-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="1cbec-253">Jest</span><span class="sxs-lookup"><span data-stu-id="1cbec-253">Yes</span></span> | <span data-ttu-id="1cbec-254">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-254">No</span></span> | <span data-ttu-id="1cbec-255">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-255">N\A</span></span> | <span data-ttu-id="1cbec-256">No</span><span class="sxs-lookup"><span data-stu-id="1cbec-256">No</span></span> | <span data-ttu-id="1cbec-257">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="1cbec-257">N\A</span></span> |


4. <span data-ttu-id="1cbec-258">Kako biste osvježili entitet, odaberite naziv mape, a zatim odaberite **Osvježi entitete**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osvježavanje mape](./media/20RefreshMapping.png)

5. <span data-ttu-id="1cbec-260">Nakon završetka osvježavanja pokrenite mapu.</span><span class="sxs-lookup"><span data-stu-id="1cbec-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="1cbec-261">Prije nego što omogućite sljedeću mapu, provjerite je li mapa u tablici u stanju **Izvodi se**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="1cbec-262">Izvođenje mapa s većim brojem preduvjeta može potrajati.</span><span class="sxs-lookup"><span data-stu-id="1cbec-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="1cbec-263">Kako biste pokrenuli mapu s preduvjetima, omogućite preklopni gumb **Prikaži povezane mape entiteta**.</span><span class="sxs-lookup"><span data-stu-id="1cbec-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="1cbec-264">Ako je u tablici navedeno kako **Početna sinkronizacija preduvjeta** ima vrijednost **Ne**, prije pokretanja provjerite je li zastavica **Početna sinkronizacija** postavljena na **Isključeno** na svim mapama s preduvjetima.</span><span class="sxs-lookup"><span data-stu-id="1cbec-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Pokretanje mape](./media/21RunMap.png)

6. <span data-ttu-id="1cbec-266">Provjerite jesu li sve mape povezane s projektom u stanju aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="1cbec-266">Validate all project related maps are in the running state.</span></span>

![Sve mape rade](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="1cbec-268">Primjena konfiguracijskih podataka na platformi CDS za aplikaciju Project Operations (neobvezno)</span><span class="sxs-lookup"><span data-stu-id="1cbec-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="1cbec-269">Ako ste primijenili pokazne podatke u okruženju aplikacije Finance, pogledajte odjeljak [Postavljanje i primjena podataka na platformi Common Data Service za aplikaciju Project Operations](resource-apply-pro-setup-config-data.md) kako biste pokazne podatke primijenili na okruženje platforme CDS.</span><span class="sxs-lookup"><span data-stu-id="1cbec-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="1cbec-270">Vaše okruženje Project Operations sada je pripremljeno i konfigurirano.</span><span class="sxs-lookup"><span data-stu-id="1cbec-270">Your Project Operations environment is now provisioned and configured.</span></span> 
