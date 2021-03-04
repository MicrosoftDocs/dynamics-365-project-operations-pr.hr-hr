---
title: Priprema novog okruženja
description: U ovoj temi nalaze se informacije o načinu pripreme novog okruženja aplikacije Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727781"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="deb28-103">Priprema novog okruženja</span><span class="sxs-lookup"><span data-stu-id="deb28-103">Provision a new environment</span></span>

<span data-ttu-id="deb28-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="deb28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="deb28-105">U ovoj temi nalaze se informacije o načinu omogućivanja novog okruženja aplikacije Dynamics 365 Project Operations za scenarije koji se temelje na resursu / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="deb28-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="deb28-106">Omogućivanje automatiziranu pripremu aplikacije Project Operations u LCS projektu</span><span class="sxs-lookup"><span data-stu-id="deb28-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="deb28-107">Poduzmite sljedeće korake kako biste omogućili automatizirani tijek pripreme za LCS projekt.</span><span class="sxs-lookup"><span data-stu-id="deb28-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="deb28-108">Idite na [LCS](https://lcs.dynamics.com/v2) i odaberite pločicu **Pregled upravljanja značajkama**.</span><span class="sxs-lookup"><span data-stu-id="deb28-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="deb28-109">U popisu **Značajka pregleda** odaberite **Značajka aplikacije Project Operations** i zatim odaberite **Omogućena značajka pregleda** kako biste omogućili aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="deb28-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="deb28-110">Ovaj korak izvodi se samo jedanput po LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="deb28-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="deb28-111">Priprema okruženja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="deb28-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="deb28-112">Otvorite novo Dynamics 365 Finance [probno okruženje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili implementaciju [sigurnosne ograde / proizvodnog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="deb28-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="deb28-113">Upoznajte se s radom čarobnjaka **Priprema okruženja**.</span><span class="sxs-lookup"><span data-stu-id="deb28-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="deb28-114">Provjerite je li odabrana verzija aplikacije 10.0.13 ili novija.</span><span class="sxs-lookup"><span data-stu-id="deb28-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="deb28-115">Za pripremu aplikacije Project Operations, pod stavkom **Napredne postavke** odaberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="deb28-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="deb28-116">Omogućite **Postavljanje platforme Common Data Service** odabirom mogućnosti **Da** a zatim u obvezna polja unesite podatke:</span><span class="sxs-lookup"><span data-stu-id="deb28-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="deb28-117">Ime</span><span class="sxs-lookup"><span data-stu-id="deb28-117">Name</span></span>
  - <span data-ttu-id="deb28-118">Regija</span><span class="sxs-lookup"><span data-stu-id="deb28-118">Region</span></span>
  - <span data-ttu-id="deb28-119">Jezik</span><span class="sxs-lookup"><span data-stu-id="deb28-119">Language</span></span>
  - <span data-ttu-id="deb28-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="deb28-120">Currency</span></span>
 
5. <span data-ttu-id="deb28-121">U polju **Predložak platforme Common Data Service** odaberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="deb28-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="deb28-122">Odaberite vrstu okruženja za implementaciju.</span><span class="sxs-lookup"><span data-stu-id="deb28-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="deb28-123">Probno razdoblje koje se temelji na pretplati omogućit će vam postavljanje CDS okruženja na 30 dana.</span><span class="sxs-lookup"><span data-stu-id="deb28-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Postavke implementacije](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="deb28-125">Odaberite **Slažem se** kako biste se potvrdili uvjete usluge i zatim odaberite **Gotovo** za povratak na postavke implementacije.</span><span class="sxs-lookup"><span data-stu-id="deb28-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Pristanak za implementaciju](./media/2DeploymentConsent.png)

7. <span data-ttu-id="deb28-127">Neobvezno – Primijenite pokazne podatke na okruženje.</span><span class="sxs-lookup"><span data-stu-id="deb28-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="deb28-128">Idite na **Napredne postavke**, odaberite **Prilagodi konfiguraciju baze podataka SQL** i postavite mogućnost **Navedi skup podataka za bazu podataka aplikacije** na **Pokazno**.</span><span class="sxs-lookup"><span data-stu-id="deb28-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="deb28-129">Ispunite preostala potrebna polja u čarobnjaku i potvrdite implementaciju.</span><span class="sxs-lookup"><span data-stu-id="deb28-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="deb28-130">Vrijeme pripreme okruženja razlikuje se ovisno o vrsti okruženja.</span><span class="sxs-lookup"><span data-stu-id="deb28-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="deb28-131">Priprema može potrajati do šest sati.</span><span class="sxs-lookup"><span data-stu-id="deb28-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="deb28-132">Nakon što se implementacija uspješno dovrši, okruženje će se prikazati kao **Implementirano**.</span><span class="sxs-lookup"><span data-stu-id="deb28-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="deb28-133">Kako biste potvrdili da se okruženje uspješno implementiralo, odaberite **Prijava** i prijavite se u okruženje radi potvrde.</span><span class="sxs-lookup"><span data-stu-id="deb28-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Pojedinosti  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="deb28-135">Primjena ažuriranja na okruženje aplikacije Finance.</span><span class="sxs-lookup"><span data-stu-id="deb28-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="deb28-136">Project Operations zahtijeva okruženje aplikacije Finance verzije **10.0.13 (10.0.569.20009)** ili više.</span><span class="sxs-lookup"><span data-stu-id="deb28-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="deb28-137">Možda ćete trebati primijeniti kvalitativna ažuriranja u svom okruženju aplikacije Finance kako biste primili ovu verziju.</span><span class="sxs-lookup"><span data-stu-id="deb28-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="deb28-138">Na stranici **Pojedinosti okruženja** LSC-a, u odjeljku **Dostupna ažuriranja**, odaberite **Pogledajte ažuriranje**.</span><span class="sxs-lookup"><span data-stu-id="deb28-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz ažuriranja](./media/5ViewUpdates.png)

2. <span data-ttu-id="deb28-140">Na stranici **Binarna ažuriranja** odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="deb28-140">On the **Binary updates** page, select **Save package.**</span></span>

![Spremanje paketa](./media/6SavePackage.png)

3. <span data-ttu-id="deb28-142">Kliknite **Odberi sve** i zatim odaberite **Spremi paket**.</span><span class="sxs-lookup"><span data-stu-id="deb28-142">Click **Select all** and then select **Save package**.</span></span>

![Pregled i spremanje ažuriranja](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="deb28-144">Unesite ime i opis paketa, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="deb28-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="deb28-145">Ovisno o internetskoj vezi, ovaj postupak može potrajati.</span><span class="sxs-lookup"><span data-stu-id="deb28-145">Depending on the internet connection, this process might take some time.</span></span>

![Prenesite paket u biblioteku Sredstva](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="deb28-147">Nakon spremanja paketa odaberite **Gotovo** i spremite ovaj paket u biblioteku Sredstava svojeg LCS projekta.</span><span class="sxs-lookup"><span data-stu-id="deb28-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="deb28-148">Spremanje i provjera valjanosti paketa može potrajati oko 15 minuta.</span><span class="sxs-lookup"><span data-stu-id="deb28-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="deb28-149">Kako biste primijenili ažuriranje, pomaknite se na stranicu **Pojedinosti okruženja** u LCS-u i odaberite **Održavaj** > **Primijeni ažuriranja**.</span><span class="sxs-lookup"><span data-stu-id="deb28-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="deb28-151">Na popisu ažuriranja odaberite paket koji ste stvorili, a zatim **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="deb28-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Primjena ažuriranja](./media/10ApplyUpdates.png)

<span data-ttu-id="deb28-153">Održavanje okruženja potrajat će neko vrijeme.</span><span class="sxs-lookup"><span data-stu-id="deb28-153">Environment servicing will take some time.</span></span> <span data-ttu-id="deb28-154">Nakon završetka, okruženje će se vratiti u implementirano stanje.</span><span class="sxs-lookup"><span data-stu-id="deb28-154">After it is complete, the environment will return to a deployed state.</span></span>

![Okruženje implementirano](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="deb28-156">Uspostavljanje veze dvostrukog zapisivanja</span><span class="sxs-lookup"><span data-stu-id="deb28-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="deb28-157">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="deb28-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="deb28-158">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="deb28-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="deb28-159">Nakon dovršetka veze ponovno odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="deb28-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="deb28-160">Bit ćete preusmjereni na dvostruko zapisivanje u aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="deb28-160">You will be redirected to Dual Write in Finance.</span></span>

![Veza na CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="deb28-162">Odaberite **Primjeni rješenje** kako biste pristupili entitetima koji će biti mapirani u integraciju.</span><span class="sxs-lookup"><span data-stu-id="deb28-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Primjena rješenja](./media/13ApplySolutions.png)

5. <span data-ttu-id="deb28-164">Odaberite oba rješenja, **Karta entiteta aplikacije Dynamics 365 Finance and Operations za dvostruko upisivanje** i **Karte entiteta aplikacije Dynamics 365 Project Operations za dvostruko upisivanje**, a zatim odaberite mogućnost **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="deb28-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potvrda rješenja](./media/14ConfirmSolutions.png)

<span data-ttu-id="deb28-166">Nakon primjene rješenja, entiteti dvostrukog zapisivanja primjenjuju se na okruženje.</span><span class="sxs-lookup"><span data-stu-id="deb28-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Primjena rješenja](./media/15ApplyingSolutions.png)

<span data-ttu-id="deb28-168">Nakon primjene entiteta, sva raspoloživa mapiranja navedena su u okruženju.</span><span class="sxs-lookup"><span data-stu-id="deb28-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mape dvostrukog zapisivanja](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="deb28-170">Osvježavanje podatkovnih entiteta nakon ažuriranja</span><span class="sxs-lookup"><span data-stu-id="deb28-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="deb28-171">U aplikaciji Finance, idite na radni prostor **Upravljanje podacima**.</span><span class="sxs-lookup"><span data-stu-id="deb28-171">In Finance, go to the **Data management** workspace.</span></span>

![Radni prostor upravljanja podacima](./media/16DataManagement.png)

2. <span data-ttu-id="deb28-173">Odaberite pločicu **Parametri okvira**.</span><span class="sxs-lookup"><span data-stu-id="deb28-173">Select the **Framework parameters** tile.</span></span>

![Parametri okvira](./media/17FrameworkParameters.png)

3. <span data-ttu-id="deb28-175">Na stranici **Postavke entiteta**, odaberite mogućnost **Osvježi popis entiteta**.</span><span class="sxs-lookup"><span data-stu-id="deb28-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osvježavanje popisa entiteta](./media/18RefreshEntityList.png)

<span data-ttu-id="deb28-177">Osvježavanje će potrajati otprilike 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="deb28-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="deb28-178">Kada bude dovršeno dobit ćete upozorenje.</span><span class="sxs-lookup"><span data-stu-id="deb28-178">You will receive an alert when it is complete.</span></span>

![Potvrda osvježavanja](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="deb28-180">Ažuriranje sigurnosnih postavki aplikacije Project Operations na platformi Dataverse</span><span class="sxs-lookup"><span data-stu-id="deb28-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="deb28-181">Idite na aplikaciju Project Operations u okruženju svoje platforme Dataverse.</span><span class="sxs-lookup"><span data-stu-id="deb28-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="deb28-182">Idite na **Postavke** > **Sigurnost** > **Sigurnosne uloge**.</span><span class="sxs-lookup"><span data-stu-id="deb28-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="deb28-183">S popisa uloga na stranici **Sigurnosne uloge**, odaberite **korisnik aplikacije dvostrukog ispisa** i odaberite karticu **Prilagođeni entiteti**.</span><span class="sxs-lookup"><span data-stu-id="deb28-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="deb28-184">Provjerite ima li uloga dozvole **Čitanje** i **Dodaj na** za:</span><span class="sxs-lookup"><span data-stu-id="deb28-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="deb28-185">**Vrstu deviznog tečaja valute**</span><span class="sxs-lookup"><span data-stu-id="deb28-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="deb28-186">**Grafikon računa**</span><span class="sxs-lookup"><span data-stu-id="deb28-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="deb28-187">**Fiskalni kalendar**</span><span class="sxs-lookup"><span data-stu-id="deb28-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="deb28-188">**Knjiga**</span><span class="sxs-lookup"><span data-stu-id="deb28-188">**Ledger**</span></span>

5. <span data-ttu-id="deb28-189">Nakon ažuriranja sigurnosne uloge idite na **Postavke** > **Sigurnost** > **Teams** i odaberite zadani tim u timskom prikazu **Vlasnik lokalne tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="deb28-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="deb28-190">Odaberite **Upravljanje ulogama** i provjerite primjenjuje li se sigurnosna ovlast **korisnik aplikacije dvostrukog pisanja** na ovaj tim.</span><span class="sxs-lookup"><span data-stu-id="deb28-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="deb28-191">Pokretanje mapa dvostrukog zapisivanja aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="deb28-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="deb28-192">U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="deb28-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="deb28-193">Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="deb28-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="deb28-194">Nakon što odaberete vezu, bit ćete preusmjereni na popis entiteta u mapiranjima.</span><span class="sxs-lookup"><span data-stu-id="deb28-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="deb28-195">Pokrenite mape na način opisan u sljedećoj tablici.</span><span class="sxs-lookup"><span data-stu-id="deb28-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="deb28-196">Svakako slijedite redoslijed kako je naveden.</span><span class="sxs-lookup"><span data-stu-id="deb28-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="deb28-197">**Karta entiteta**</span><span class="sxs-lookup"><span data-stu-id="deb28-197">**Entity Map**</span></span> | <span data-ttu-id="deb28-198">**Osvježi entitet**</span><span class="sxs-lookup"><span data-stu-id="deb28-198">**Refresh entity**</span></span> | <span data-ttu-id="deb28-199">**Početna sinkronizacija**</span><span class="sxs-lookup"><span data-stu-id="deb28-199">**Initial sync**</span></span> | <span data-ttu-id="deb28-200">**Glavni za početnu sinkronizaciju**</span><span class="sxs-lookup"><span data-stu-id="deb28-200">**Master for initial sync**</span></span> | <span data-ttu-id="deb28-201">**Pokreni preduvjete**</span><span class="sxs-lookup"><span data-stu-id="deb28-201">**Run prerequisites**</span></span> | <span data-ttu-id="deb28-202">**Početna sinkronizacija preduvjeta**</span><span class="sxs-lookup"><span data-stu-id="deb28-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="deb28-203">**Uloge aplikacije Project Resource za sve tvrtke (kategorije resursa koji se mogu rezervirati)**</span><span class="sxs-lookup"><span data-stu-id="deb28-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="deb28-204">No</span><span class="sxs-lookup"><span data-stu-id="deb28-204">No</span></span> | <span data-ttu-id="deb28-205">Jest</span><span class="sxs-lookup"><span data-stu-id="deb28-205">Yes</span></span> | <span data-ttu-id="deb28-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="deb28-206">Common Data Service</span></span> | <span data-ttu-id="deb28-207">No</span><span class="sxs-lookup"><span data-stu-id="deb28-207">No</span></span> | <span data-ttu-id="deb28-208">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-208">N\A</span></span> |
| <span data-ttu-id="deb28-209">**Pravne osobe (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="deb28-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="deb28-210">No</span><span class="sxs-lookup"><span data-stu-id="deb28-210">No</span></span> | <span data-ttu-id="deb28-211">Jest</span><span class="sxs-lookup"><span data-stu-id="deb28-211">Yes</span></span> | <span data-ttu-id="deb28-212">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="deb28-212">Finance and Operations apps</span></span> | <span data-ttu-id="deb28-213">No</span><span class="sxs-lookup"><span data-stu-id="deb28-213">No</span></span> | <span data-ttu-id="deb28-214">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-214">N\A</span></span> |
| <span data-ttu-id="deb28-215">**Glavna knjiga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="deb28-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="deb28-216">No</span><span class="sxs-lookup"><span data-stu-id="deb28-216">No</span></span> | <span data-ttu-id="deb28-217">Jest</span><span class="sxs-lookup"><span data-stu-id="deb28-217">Yes</span></span> | <span data-ttu-id="deb28-218">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="deb28-218">Finance and Operations apps</span></span> | <span data-ttu-id="deb28-219">Jest</span><span class="sxs-lookup"><span data-stu-id="deb28-219">Yes</span></span> | <span data-ttu-id="deb28-220">Da, aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="deb28-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="deb28-221">**Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="deb28-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="deb28-222">No</span><span class="sxs-lookup"><span data-stu-id="deb28-222">No</span></span> | <span data-ttu-id="deb28-223">No</span><span class="sxs-lookup"><span data-stu-id="deb28-223">No</span></span> | <span data-ttu-id="deb28-224">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-224">N\A</span></span> | <span data-ttu-id="deb28-225">Jest</span><span class="sxs-lookup"><span data-stu-id="deb28-225">Yes</span></span> | <span data-ttu-id="deb28-226">No</span><span class="sxs-lookup"><span data-stu-id="deb28-226">No</span></span> |
| <span data-ttu-id="deb28-227">**Redci ugovora o projektu (pojedinosti prodajnog naloga)**</span><span class="sxs-lookup"><span data-stu-id="deb28-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="deb28-228">No</span><span class="sxs-lookup"><span data-stu-id="deb28-228">No</span></span> | <span data-ttu-id="deb28-229">No</span><span class="sxs-lookup"><span data-stu-id="deb28-229">No</span></span> | <span data-ttu-id="deb28-230">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-230">N\A</span></span> | <span data-ttu-id="deb28-231">No</span><span class="sxs-lookup"><span data-stu-id="deb28-231">No</span></span> | <span data-ttu-id="deb28-232">No</span><span class="sxs-lookup"><span data-stu-id="deb28-232">No</span></span> |
| <span data-ttu-id="deb28-233">**Entitet integracije za odnose projektne transakcije (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="deb28-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="deb28-234">No</span><span class="sxs-lookup"><span data-stu-id="deb28-234">No</span></span> | <span data-ttu-id="deb28-235">No</span><span class="sxs-lookup"><span data-stu-id="deb28-235">No</span></span> | <span data-ttu-id="deb28-236">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-236">N\A</span></span> | <span data-ttu-id="deb28-237">No</span><span class="sxs-lookup"><span data-stu-id="deb28-237">No</span></span> | <span data-ttu-id="deb28-238">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-238">N\A</span></span> |
| <span data-ttu-id="deb28-239">**Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="deb28-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="deb28-240">No</span><span class="sxs-lookup"><span data-stu-id="deb28-240">No</span></span> | <span data-ttu-id="deb28-241">No</span><span class="sxs-lookup"><span data-stu-id="deb28-241">No</span></span> | <span data-ttu-id="deb28-242">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-242">N\A</span></span> | <span data-ttu-id="deb28-243">No</span><span class="sxs-lookup"><span data-stu-id="deb28-243">No</span></span> | <span data-ttu-id="deb28-244">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-244">N\A</span></span> |
| <span data-ttu-id="deb28-245">**Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="deb28-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="deb28-246">No</span><span class="sxs-lookup"><span data-stu-id="deb28-246">No</span></span> | <span data-ttu-id="deb28-247">No</span><span class="sxs-lookup"><span data-stu-id="deb28-247">No</span></span> | <span data-ttu-id="deb28-248">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-248">N\A</span></span> | <span data-ttu-id="deb28-249">No</span><span class="sxs-lookup"><span data-stu-id="deb28-249">No</span></span> | <span data-ttu-id="deb28-250">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-250">N\A</span></span> |
| <span data-ttu-id="deb28-251">**Entitet izvoza kategorija troškova projekta za integraciju aplikacije Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="deb28-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="deb28-252">No</span><span class="sxs-lookup"><span data-stu-id="deb28-252">No</span></span> | <span data-ttu-id="deb28-253">No</span><span class="sxs-lookup"><span data-stu-id="deb28-253">No</span></span> | <span data-ttu-id="deb28-254">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-254">N\A</span></span> | <span data-ttu-id="deb28-255">No</span><span class="sxs-lookup"><span data-stu-id="deb28-255">No</span></span> | <span data-ttu-id="deb28-256">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-256">N\A</span></span> |
| <span data-ttu-id="deb28-257">**Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="deb28-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="deb28-258">Jest</span><span class="sxs-lookup"><span data-stu-id="deb28-258">Yes</span></span> | <span data-ttu-id="deb28-259">No</span><span class="sxs-lookup"><span data-stu-id="deb28-259">No</span></span> | <span data-ttu-id="deb28-260">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-260">N\A</span></span> | <span data-ttu-id="deb28-261">No</span><span class="sxs-lookup"><span data-stu-id="deb28-261">No</span></span> | <span data-ttu-id="deb28-262">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-262">N\A</span></span> |
| <span data-ttu-id="deb28-263">**Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="deb28-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="deb28-264">Jest</span><span class="sxs-lookup"><span data-stu-id="deb28-264">Yes</span></span> | <span data-ttu-id="deb28-265">No</span><span class="sxs-lookup"><span data-stu-id="deb28-265">No</span></span> | <span data-ttu-id="deb28-266">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-266">N\A</span></span> | <span data-ttu-id="deb28-267">No</span><span class="sxs-lookup"><span data-stu-id="deb28-267">No</span></span> | <span data-ttu-id="deb28-268">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="deb28-268">N\A</span></span> |


4. <span data-ttu-id="deb28-269">Kako biste osvježili entitet, odaberite naziv mape, a zatim odaberite **Osvježi entitete**.</span><span class="sxs-lookup"><span data-stu-id="deb28-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osvježavanje mape](./media/20RefreshMapping.png)

5. <span data-ttu-id="deb28-271">Nakon završetka osvježavanja pokrenite mapu.</span><span class="sxs-lookup"><span data-stu-id="deb28-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="deb28-272">Prije nego što omogućite sljedeću mapu, provjerite je li mapa u tablici u stanju **Izvodi se**.</span><span class="sxs-lookup"><span data-stu-id="deb28-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="deb28-273">Izvođenje mapa s većim brojem preduvjeta može potrajati.</span><span class="sxs-lookup"><span data-stu-id="deb28-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="deb28-274">Kako biste pokrenuli mapu s preduvjetima, omogućite preklopni gumb **Prikaži povezane mape entiteta**.</span><span class="sxs-lookup"><span data-stu-id="deb28-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="deb28-275">Ako je u tablici navedeno kako **Početna sinkronizacija preduvjeta** ima vrijednost **Ne**, prije pokretanja provjerite je li zastavica **Početna sinkronizacija** postavljena na **Isključeno** na svim mapama s preduvjetima.</span><span class="sxs-lookup"><span data-stu-id="deb28-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Pokretanje mape](./media/21RunMap.png)

6. <span data-ttu-id="deb28-277">Provjerite jesu li sve mape povezane s projektom u stanju aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="deb28-277">Validate all project related maps are in the running state.</span></span>

![Sve mape rade](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="deb28-279">Primjena konfiguracijskih podataka na platformi CDS za aplikaciju Project Operations (neobvezno)</span><span class="sxs-lookup"><span data-stu-id="deb28-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="deb28-280">Ako ste primijenili pokazne podatke u okruženju aplikacije Finance, pogledajte odjeljak [Postavljanje i primjena podataka na platformi Common Data Service za aplikaciju Project Operations](resource-apply-pro-setup-config-data.md) kako biste pokazne podatke primijenili na okruženje platforme CDS.</span><span class="sxs-lookup"><span data-stu-id="deb28-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="deb28-281">Vaše okruženje Project Operations sada je pripremljeno i konfigurirano.</span><span class="sxs-lookup"><span data-stu-id="deb28-281">Your Project Operations environment is now provisioned and configured.</span></span> 
