---
title: Priprema novog okruženja
description: U ovoj temi nalaze se informacije o načinu pripreme novog okruženja aplikacije Project Operations.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995477"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="b8616-103">Priprema novog okruženja</span><span class="sxs-lookup"><span data-stu-id="b8616-103">Provision a new environment</span></span>

<span data-ttu-id="b8616-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="b8616-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b8616-105">U ovoj temi nalaze se informacije o načinu omogućivanja novog okruženja aplikacije Dynamics 365 Project Operations za scenarije koji se temelje na resursu / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="b8616-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="b8616-106">Omogućivanje automatiziranu pripremu aplikacije Project Operations u LCS projektu</span><span class="sxs-lookup"><span data-stu-id="b8616-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="b8616-107">Poduzmite sljedeće korake kako biste omogućili automatizirani tijek pripreme za LCS projekt.</span><span class="sxs-lookup"><span data-stu-id="b8616-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="b8616-108">Idite na [LCS](https://lcs.dynamics.com/v2) i odaberite pločicu **Pregled upravljanja značajkama**.</span><span class="sxs-lookup"><span data-stu-id="b8616-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="b8616-109">U popisu **Značajka pregleda** odaberite **Značajka aplikacije Project Operations** i zatim odaberite **Omogućena značajka pregleda** kako biste omogućili aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b8616-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="b8616-110">Ovaj korak izvodi se samo jedanput po LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="b8616-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="b8616-111">Priprema okruženja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="b8616-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="b8616-112">Otvorite novo Dynamics 365 Finance [probno okruženje](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili implementaciju [sigurnosne ograde / proizvodnog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="b8616-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="b8616-113">Upoznajte se s radom čarobnjaka **Priprema okruženja**.</span><span class="sxs-lookup"><span data-stu-id="b8616-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="b8616-114">Provjerite je li odabrana verzija aplikacije 10.0.13 ili novija.</span><span class="sxs-lookup"><span data-stu-id="b8616-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="b8616-115">Za pripremu aplikacije Project Operations, pod stavkom **Napredne postavke** odaberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="b8616-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="b8616-116">Omogućite **Postavljanje platforme Common Data Service** odabirom mogućnosti **Da** a zatim u obvezna polja unesite podatke:</span><span class="sxs-lookup"><span data-stu-id="b8616-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="b8616-117">Ime</span><span class="sxs-lookup"><span data-stu-id="b8616-117">Name</span></span>
  - <span data-ttu-id="b8616-118">Regija</span><span class="sxs-lookup"><span data-stu-id="b8616-118">Region</span></span>
  - <span data-ttu-id="b8616-119">Jezik</span><span class="sxs-lookup"><span data-stu-id="b8616-119">Language</span></span>
  - <span data-ttu-id="b8616-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="b8616-120">Currency</span></span>
 
5. <span data-ttu-id="b8616-121">U polju **Predložak platforme Common Data Service** odaberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="b8616-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="b8616-122">Odaberite vrstu okruženja za implementaciju.</span><span class="sxs-lookup"><span data-stu-id="b8616-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="b8616-123">Probno razdoblje koje se temelji na pretplati omogućit će vam postavljanje CDS okruženja na 30 dana.</span><span class="sxs-lookup"><span data-stu-id="b8616-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Postavke implementacije](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="b8616-125">Odaberite **Slažem se** kako biste se potvrdili uvjete usluge i zatim odaberite **Gotovo** za povratak na postavke implementacije.</span><span class="sxs-lookup"><span data-stu-id="b8616-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Pristanak za implementaciju](./media/2DeploymentConsent.png)

7. <span data-ttu-id="b8616-127">Neobvezno – Primijenite pokazne podatke na okruženje.</span><span class="sxs-lookup"><span data-stu-id="b8616-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="b8616-128">Idite na **Napredne postavke**, odaberite **Prilagodi konfiguraciju baze podataka SQL** i postavite mogućnost **Navedi skup podataka za bazu podataka aplikacije** na **Pokazno**.</span><span class="sxs-lookup"><span data-stu-id="b8616-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="b8616-129">Ispunite preostala potrebna polja u čarobnjaku i potvrdite implementaciju.</span><span class="sxs-lookup"><span data-stu-id="b8616-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="b8616-130">Vrijeme pripreme okruženja razlikuje se ovisno o vrsti okruženja.</span><span class="sxs-lookup"><span data-stu-id="b8616-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="b8616-131">Priprema može potrajati do šest sati.</span><span class="sxs-lookup"><span data-stu-id="b8616-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="b8616-132">Nakon što se implementacija uspješno dovrši, okruženje će se prikazati kao **Implementirano**.</span><span class="sxs-lookup"><span data-stu-id="b8616-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="b8616-133">Kako biste potvrdili da se okruženje uspješno implementiralo, odaberite **Prijava** i prijavite se u okruženje radi potvrde.</span><span class="sxs-lookup"><span data-stu-id="b8616-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Pojedinosti  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="b8616-135">Primjena ažuriranja na okruženje aplikacije Finance.</span><span class="sxs-lookup"><span data-stu-id="b8616-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="b8616-136">Project Operations zahtijeva okruženje aplikacije Finance verzije **10.0.13 (10.0.569.20009)** ili više.</span><span class="sxs-lookup"><span data-stu-id="b8616-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="b8616-137">Možda ćete trebati primijeniti kvalitativna ažuriranja u svom okruženju aplikacije Finance kako biste primili ovu verziju.</span><span class="sxs-lookup"><span data-stu-id="b8616-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="b8616-138">Na stranici **Pojedinosti okruženja** LSC-a, u odjeljku **Dostupna ažuriranja**, odaberite **Pogledajte ažuriranje**.</span><span class="sxs-lookup"><span data-stu-id="b8616-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz ažuriranja](./media/5ViewUpdates.png)

2. <span data-ttu-id="b8616-140">Na stranici **Binarna ažuriranja** odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="b8616-140">On the **Binary updates** page, select **Save package.**</span></span>

![Spremanje paketa](./media/6SavePackage.png)

3. <span data-ttu-id="b8616-142">Kliknite **Odberi sve** i zatim odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="b8616-142">Click **Select all** and then select **Save package**.</span></span>

![Pregled i spremanje ažuriranja](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="b8616-144">Unesite ime i opis paketa, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="b8616-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="b8616-145">Ovisno o internetskoj vezi, ovaj postupak može potrajati.</span><span class="sxs-lookup"><span data-stu-id="b8616-145">Depending on the internet connection, this process might take some time.</span></span>

![Prenesite paket u biblioteku Sredstva](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="b8616-147">Nakon spremanja paketa odaberite **Gotovo** i spremite ovaj paket u biblioteku Sredstava svojeg LCS projekta.</span><span class="sxs-lookup"><span data-stu-id="b8616-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="b8616-148">Spremanje i provjera valjanosti paketa može potrajati oko 15 minuta.</span><span class="sxs-lookup"><span data-stu-id="b8616-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="b8616-149">Kako biste primijenili ažuriranje, pomaknite se na stranicu **Pojedinosti okruženja** u LCS-u i odaberite **Održavaj** > **Primijeni ažuriranja**.</span><span class="sxs-lookup"><span data-stu-id="b8616-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="b8616-151">Na popisu ažuriranja odaberite paket koji ste stvorili, a zatim **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="b8616-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Primjena ažuriranja](./media/10ApplyUpdates.png)

<span data-ttu-id="b8616-153">Održavanje okruženja potrajat će neko vrijeme.</span><span class="sxs-lookup"><span data-stu-id="b8616-153">Environment servicing will take some time.</span></span> <span data-ttu-id="b8616-154">Nakon završetka, okruženje će se vratiti u implementirano stanje.</span><span class="sxs-lookup"><span data-stu-id="b8616-154">After it is complete, the environment will return to a deployed state.</span></span>

![Okruženje implementirano](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="b8616-156">Uspostavljanje veze dvostrukog zapisivanja</span><span class="sxs-lookup"><span data-stu-id="b8616-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="b8616-157">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="b8616-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="b8616-158">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="b8616-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="b8616-159">Nakon dovršetka veze ponovno odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="b8616-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="b8616-160">Bit ćete preusmjereni na dvostruko zapisivanje u aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="b8616-160">You will be redirected to Dual Write in Finance.</span></span>

![Veza na CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="b8616-162">Odaberite **Primjeni rješenje** kako biste pristupili entitetima koji će biti mapirani u integraciju.</span><span class="sxs-lookup"><span data-stu-id="b8616-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Primjena rješenja](./media/13ApplySolutions.png)

5. <span data-ttu-id="b8616-164">Odaberite oba rješenja, **Karta entiteta aplikacije Dynamics 365 Finance and Operations za dvostruko upisivanje** i **Karte entiteta aplikacije Dynamics 365 Project Operations za dvostruko upisivanje**, a zatim odaberite mogućnost **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="b8616-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potvrda rješenja](./media/14ConfirmSolutions.png)

<span data-ttu-id="b8616-166">Nakon primjene rješenja, entiteti dvostrukog zapisivanja primjenjuju se na okruženje.</span><span class="sxs-lookup"><span data-stu-id="b8616-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Primjena rješenja](./media/15ApplyingSolutions.png)

<span data-ttu-id="b8616-168">Nakon primjene entiteta, sva raspoloživa mapiranja navedena su u okruženju.</span><span class="sxs-lookup"><span data-stu-id="b8616-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mape dvostrukog zapisivanja](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="b8616-170">Osvježavanje podatkovnih entiteta nakon ažuriranja</span><span class="sxs-lookup"><span data-stu-id="b8616-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="b8616-171">U aplikaciji Finance, idite na radni prostor **Upravljanje podacima**.</span><span class="sxs-lookup"><span data-stu-id="b8616-171">In Finance, go to the **Data management** workspace.</span></span>

![Radni prostor upravljanja podacima](./media/16DataManagement.png)

2. <span data-ttu-id="b8616-173">Odaberite pločicu **Parametri okvira**.</span><span class="sxs-lookup"><span data-stu-id="b8616-173">Select the **Framework parameters** tile.</span></span>

![Parametri okvira](./media/17FrameworkParameters.png)

3. <span data-ttu-id="b8616-175">Na stranici **Postavke entiteta**, odaberite mogućnost **Osvježi popis entiteta**.</span><span class="sxs-lookup"><span data-stu-id="b8616-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osvježavanje popisa entiteta](./media/18RefreshEntityList.png)

<span data-ttu-id="b8616-177">Osvježavanje će potrajati otprilike 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="b8616-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="b8616-178">Kada bude dovršeno dobit ćete upozorenje.</span><span class="sxs-lookup"><span data-stu-id="b8616-178">You will receive an alert when it is complete.</span></span>

![Potvrda osvježavanja](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="b8616-180">Ažuriranje sigurnosnih postavki aplikacije Project Operations na platformi Dataverse</span><span class="sxs-lookup"><span data-stu-id="b8616-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="b8616-181">Idite na aplikaciju Project Operations u okruženju svoje platforme Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b8616-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="b8616-182">Idite na **Postavke** > **Sigurnost** > **Sigurnosne uloge**.</span><span class="sxs-lookup"><span data-stu-id="b8616-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="b8616-183">S popisa uloga na stranici **Sigurnosne uloge**, odaberite **korisnik aplikacije za dvostruko pisanje** i odaberite karticu **Prilagođeni entiteti**.</span><span class="sxs-lookup"><span data-stu-id="b8616-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="b8616-184">Provjerite ima li uloga dozvole **Čitanje** i **Dodaj na** za:</span><span class="sxs-lookup"><span data-stu-id="b8616-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="b8616-185">**Vrstu deviznog tečaja valute**</span><span class="sxs-lookup"><span data-stu-id="b8616-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="b8616-186">**Grafikon računa**</span><span class="sxs-lookup"><span data-stu-id="b8616-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="b8616-187">**Fiskalni kalendar**</span><span class="sxs-lookup"><span data-stu-id="b8616-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="b8616-188">**Knjiga**</span><span class="sxs-lookup"><span data-stu-id="b8616-188">**Ledger**</span></span>

5. <span data-ttu-id="b8616-189">Nakon ažuriranja sigurnosne uloge idite na **Postavke** > **Sigurnost** > **Teams** i odaberite zadani tim u timskom prikazu **Vlasnik lokalne tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="b8616-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="b8616-190">Odaberite **Upravljanje ulogama** i provjerite primjenjuje li se sigurnosna ovlast **korisnik aplikacije za dvostruko pisanje** na ovaj tim.</span><span class="sxs-lookup"><span data-stu-id="b8616-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="b8616-191">Pokretanje mapa dvostrukog zapisivanja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="b8616-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="b8616-192">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="b8616-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="b8616-193">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="b8616-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="b8616-194">Nakon što odaberete vezu, bit ćete preusmjereni na popis entiteta u mapiranjima.</span><span class="sxs-lookup"><span data-stu-id="b8616-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="b8616-195">Pokrenite mape na način opisan u sljedećoj tablici.</span><span class="sxs-lookup"><span data-stu-id="b8616-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="b8616-196">Svakako slijedite redoslijed kako je naveden.</span><span class="sxs-lookup"><span data-stu-id="b8616-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="b8616-197">**Karta entiteta**</span><span class="sxs-lookup"><span data-stu-id="b8616-197">**Entity Map**</span></span> | <span data-ttu-id="b8616-198">**Osvježi entitet**</span><span class="sxs-lookup"><span data-stu-id="b8616-198">**Refresh entity**</span></span> | <span data-ttu-id="b8616-199">**Početna sinkronizacija**</span><span class="sxs-lookup"><span data-stu-id="b8616-199">**Initial sync**</span></span> | <span data-ttu-id="b8616-200">**Glavni za početnu sinkronizaciju**</span><span class="sxs-lookup"><span data-stu-id="b8616-200">**Master for initial sync**</span></span> | <span data-ttu-id="b8616-201">**Pokreni preduvjete**</span><span class="sxs-lookup"><span data-stu-id="b8616-201">**Run prerequisites**</span></span> | <span data-ttu-id="b8616-202">**Početna sinkronizacija preduvjeta**</span><span class="sxs-lookup"><span data-stu-id="b8616-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="b8616-203">**Uloge aplikacije Project Resource za sve tvrtke (kategorije resursa koji se mogu rezervirati)**</span><span class="sxs-lookup"><span data-stu-id="b8616-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="b8616-204">No</span><span class="sxs-lookup"><span data-stu-id="b8616-204">No</span></span> | <span data-ttu-id="b8616-205">Jest</span><span class="sxs-lookup"><span data-stu-id="b8616-205">Yes</span></span> | <span data-ttu-id="b8616-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b8616-206">Common Data Service</span></span> | <span data-ttu-id="b8616-207">No</span><span class="sxs-lookup"><span data-stu-id="b8616-207">No</span></span> | <span data-ttu-id="b8616-208">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-208">N\A</span></span> |
| <span data-ttu-id="b8616-209">**Pravne osobe (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="b8616-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="b8616-210">No</span><span class="sxs-lookup"><span data-stu-id="b8616-210">No</span></span> | <span data-ttu-id="b8616-211">Jest</span><span class="sxs-lookup"><span data-stu-id="b8616-211">Yes</span></span> | <span data-ttu-id="b8616-212">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b8616-212">Finance and Operations apps</span></span> | <span data-ttu-id="b8616-213">No</span><span class="sxs-lookup"><span data-stu-id="b8616-213">No</span></span> | <span data-ttu-id="b8616-214">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-214">N\A</span></span> |
| <span data-ttu-id="b8616-215">**Glavna knjiga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="b8616-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="b8616-216">No</span><span class="sxs-lookup"><span data-stu-id="b8616-216">No</span></span> | <span data-ttu-id="b8616-217">Jest</span><span class="sxs-lookup"><span data-stu-id="b8616-217">Yes</span></span> | <span data-ttu-id="b8616-218">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b8616-218">Finance and Operations apps</span></span> | <span data-ttu-id="b8616-219">Jest</span><span class="sxs-lookup"><span data-stu-id="b8616-219">Yes</span></span> | <span data-ttu-id="b8616-220">Da, aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b8616-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="b8616-221">**Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="b8616-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="b8616-222">No</span><span class="sxs-lookup"><span data-stu-id="b8616-222">No</span></span> | <span data-ttu-id="b8616-223">No</span><span class="sxs-lookup"><span data-stu-id="b8616-223">No</span></span> | <span data-ttu-id="b8616-224">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-224">N\A</span></span> | <span data-ttu-id="b8616-225">Jest</span><span class="sxs-lookup"><span data-stu-id="b8616-225">Yes</span></span> | <span data-ttu-id="b8616-226">No</span><span class="sxs-lookup"><span data-stu-id="b8616-226">No</span></span> |
| <span data-ttu-id="b8616-227">**Redci ugovora o projektu (pojedinosti prodajnog naloga)**</span><span class="sxs-lookup"><span data-stu-id="b8616-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="b8616-228">No</span><span class="sxs-lookup"><span data-stu-id="b8616-228">No</span></span> | <span data-ttu-id="b8616-229">No</span><span class="sxs-lookup"><span data-stu-id="b8616-229">No</span></span> | <span data-ttu-id="b8616-230">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-230">N\A</span></span> | <span data-ttu-id="b8616-231">No</span><span class="sxs-lookup"><span data-stu-id="b8616-231">No</span></span> | <span data-ttu-id="b8616-232">No</span><span class="sxs-lookup"><span data-stu-id="b8616-232">No</span></span> |
| <span data-ttu-id="b8616-233">**Entitet integracije za odnose projektne transakcije (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="b8616-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="b8616-234">No</span><span class="sxs-lookup"><span data-stu-id="b8616-234">No</span></span> | <span data-ttu-id="b8616-235">No</span><span class="sxs-lookup"><span data-stu-id="b8616-235">No</span></span> | <span data-ttu-id="b8616-236">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-236">N\A</span></span> | <span data-ttu-id="b8616-237">No</span><span class="sxs-lookup"><span data-stu-id="b8616-237">No</span></span> | <span data-ttu-id="b8616-238">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-238">N\A</span></span> |
| <span data-ttu-id="b8616-239">**Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="b8616-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="b8616-240">No</span><span class="sxs-lookup"><span data-stu-id="b8616-240">No</span></span> | <span data-ttu-id="b8616-241">No</span><span class="sxs-lookup"><span data-stu-id="b8616-241">No</span></span> | <span data-ttu-id="b8616-242">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-242">N\A</span></span> | <span data-ttu-id="b8616-243">No</span><span class="sxs-lookup"><span data-stu-id="b8616-243">No</span></span> | <span data-ttu-id="b8616-244">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-244">N\A</span></span> |
| <span data-ttu-id="b8616-245">**Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="b8616-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="b8616-246">No</span><span class="sxs-lookup"><span data-stu-id="b8616-246">No</span></span> | <span data-ttu-id="b8616-247">No</span><span class="sxs-lookup"><span data-stu-id="b8616-247">No</span></span> | <span data-ttu-id="b8616-248">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-248">N\A</span></span> | <span data-ttu-id="b8616-249">No</span><span class="sxs-lookup"><span data-stu-id="b8616-249">No</span></span> | <span data-ttu-id="b8616-250">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-250">N\A</span></span> |
| <span data-ttu-id="b8616-251">**Entitet izvoza kategorija troškova projekta za integraciju aplikacije Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="b8616-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="b8616-252">No</span><span class="sxs-lookup"><span data-stu-id="b8616-252">No</span></span> | <span data-ttu-id="b8616-253">No</span><span class="sxs-lookup"><span data-stu-id="b8616-253">No</span></span> | <span data-ttu-id="b8616-254">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-254">N\A</span></span> | <span data-ttu-id="b8616-255">No</span><span class="sxs-lookup"><span data-stu-id="b8616-255">No</span></span> | <span data-ttu-id="b8616-256">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-256">N\A</span></span> |
| <span data-ttu-id="b8616-257">**Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="b8616-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="b8616-258">Jest</span><span class="sxs-lookup"><span data-stu-id="b8616-258">Yes</span></span> | <span data-ttu-id="b8616-259">No</span><span class="sxs-lookup"><span data-stu-id="b8616-259">No</span></span> | <span data-ttu-id="b8616-260">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-260">N\A</span></span> | <span data-ttu-id="b8616-261">No</span><span class="sxs-lookup"><span data-stu-id="b8616-261">No</span></span> | <span data-ttu-id="b8616-262">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-262">N\A</span></span> |
| <span data-ttu-id="b8616-263">**Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="b8616-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="b8616-264">Jest</span><span class="sxs-lookup"><span data-stu-id="b8616-264">Yes</span></span> | <span data-ttu-id="b8616-265">No</span><span class="sxs-lookup"><span data-stu-id="b8616-265">No</span></span> | <span data-ttu-id="b8616-266">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-266">N\A</span></span> | <span data-ttu-id="b8616-267">No</span><span class="sxs-lookup"><span data-stu-id="b8616-267">No</span></span> | <span data-ttu-id="b8616-268">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="b8616-268">N\A</span></span> |


4. <span data-ttu-id="b8616-269">Kako biste osvježili entitet, odaberite naziv mape, a zatim odaberite **Osvježi entitete**.</span><span class="sxs-lookup"><span data-stu-id="b8616-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osvježavanje mape](./media/20RefreshMapping.png)

5. <span data-ttu-id="b8616-271">Nakon završetka osvježavanja pokrenite mapu.</span><span class="sxs-lookup"><span data-stu-id="b8616-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="b8616-272">Prije nego što omogućite sljedeću mapu, provjerite je li mapa u tablici u stanju **Izvodi se**.</span><span class="sxs-lookup"><span data-stu-id="b8616-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="b8616-273">Izvođenje mapa s većim brojem preduvjeta može potrajati.</span><span class="sxs-lookup"><span data-stu-id="b8616-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="b8616-274">Kako biste pokrenuli mapu s preduvjetima, omogućite preklopni gumb **Prikaži povezane mape entiteta**.</span><span class="sxs-lookup"><span data-stu-id="b8616-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="b8616-275">Ako je u tablici navedeno kako **Početna sinkronizacija preduvjeta** ima vrijednost **Ne**, prije pokretanja provjerite je li zastavica **Početna sinkronizacija** postavljena na **Isključeno** na svim mapama s preduvjetima.</span><span class="sxs-lookup"><span data-stu-id="b8616-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Pokretanje mape](./media/21RunMap.png)

6. <span data-ttu-id="b8616-277">Provjerite jesu li sve mape povezane s projektom u stanju aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="b8616-277">Validate all project related maps are in the running state.</span></span>

![Sve mape rade](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="b8616-279">Primjena konfiguracijskih podataka na platformi CDS za aplikaciju Project Operations (neobvezno)</span><span class="sxs-lookup"><span data-stu-id="b8616-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="b8616-280">Ako ste primijenili pokazne podatke u okruženju aplikacije Finance, pogledajte odjeljak [Postavljanje i primjena podataka na platformi Common Data Service za aplikaciju Project Operations](resource-apply-pro-setup-config-data.md) kako biste pokazne podatke primijenili na okruženje platforme CDS.</span><span class="sxs-lookup"><span data-stu-id="b8616-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="b8616-281">Vaše okruženje Project Operations sada je pripremljeno i konfigurirano.</span><span class="sxs-lookup"><span data-stu-id="b8616-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]