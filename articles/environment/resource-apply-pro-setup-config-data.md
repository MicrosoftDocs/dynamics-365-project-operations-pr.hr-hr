---
title: Postavljanje i primjena konfiguracijskih podataka na platfomi Common Data Service
description: U ovoj temi nalaze se informacije o načinu postavljanja i primjene konfiguracijskih podataka u aplikaciji Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001282"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="abfb8-103">Postavljanje i primjena konfiguracijskih podataka na platfomi Common Data Service</span><span class="sxs-lookup"><span data-stu-id="abfb8-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="abfb8-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="abfb8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="abfb8-105">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="abfb8-105">Prerequisites</span></span>

<span data-ttu-id="abfb8-106">Prije nego što počnete konfigurirati podatke u aplikaciji Common Data Service (CDS), moraju se ispuniti sljedeći preduvjeti:</span><span class="sxs-lookup"><span data-stu-id="abfb8-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="abfb8-107">Osigurana okruženja platforme CDS i sustava Dynamics 365 Finance za aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="abfb8-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="abfb8-108">Dijeljenje podataka o pravnoj osobi sustava Dynamics 365 Finance s okruženjem platforme CDS.</span><span class="sxs-lookup"><span data-stu-id="abfb8-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="abfb8-109">To znači da entitet **Tvrtka** na platformi CDS ima sljedeće zapise o poduzeću:</span><span class="sxs-lookup"><span data-stu-id="abfb8-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="abfb8-110">THPM</span><span class="sxs-lookup"><span data-stu-id="abfb8-110">THPM</span></span>
  - <span data-ttu-id="abfb8-111">USPM</span><span class="sxs-lookup"><span data-stu-id="abfb8-111">USPM</span></span>
  - <span data-ttu-id="abfb8-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="abfb8-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="abfb8-113">Instalacija postavljanja i konfiguracijskih podataka</span><span class="sxs-lookup"><span data-stu-id="abfb8-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="abfb8-114">Preuzmite, deblokirajte i raspakirajte [Paket podataka za postavljanje i konfiguraciju](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="abfb8-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="abfb8-115">Pomaknite se do raspakirane mape i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="abfb8-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="abfb8-116">Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="abfb8-118">Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu implementacije**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="abfb8-119">Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="abfb8-120">Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite mogućnost **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguracija prijave](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="abfb8-122">Na 3. stranici, s popisa tvrtki ili ustanova na klijentu, odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="abfb8-123">Na 4. stranici odaberite zip datoteku *SampleSetupAndConfigData* iz raspakirane mape.</span><span class="sxs-lookup"><span data-stu-id="abfb8-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Odabir zip datoteke](./media/3ZipFile.png)

![Odaberite datoteku](./media/4SelectAFile.png)

9. <span data-ttu-id="abfb8-126">Nakon odabira zip datoteke odaberite **Uvezi podatke**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-126">After the zip file is selected, select **Import Data**.</span></span>

![Uvoz podataka](./media/5ImportData.png)

10. <span data-ttu-id="abfb8-128">Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="abfb8-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="abfb8-129">Po završetku uvoza izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="abfb8-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="abfb8-130">U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 26 entiteta:</span><span class="sxs-lookup"><span data-stu-id="abfb8-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="abfb8-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="abfb8-131">Currency</span></span>
  - <span data-ttu-id="abfb8-132">Grafikon računa</span><span class="sxs-lookup"><span data-stu-id="abfb8-132">Chart of Accounts</span></span>
  - <span data-ttu-id="abfb8-133">Fiskalni kalendar</span><span class="sxs-lookup"><span data-stu-id="abfb8-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="abfb8-134">Vrste deviznih tečajeva</span><span class="sxs-lookup"><span data-stu-id="abfb8-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="abfb8-135">Dan plaćanja</span><span class="sxs-lookup"><span data-stu-id="abfb8-135">Payment Day</span></span>
  - <span data-ttu-id="abfb8-136">Raspored plaćanja</span><span class="sxs-lookup"><span data-stu-id="abfb8-136">Payment Schedule</span></span>
  - <span data-ttu-id="abfb8-137">Uvjet plaćanja</span><span class="sxs-lookup"><span data-stu-id="abfb8-137">Payment Term</span></span>
  - <span data-ttu-id="abfb8-138">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="abfb8-138">Organizational Unit</span></span>
  - <span data-ttu-id="abfb8-139">Kontakt</span><span class="sxs-lookup"><span data-stu-id="abfb8-139">Contact</span></span>
  - <span data-ttu-id="abfb8-140">Porezna grupa</span><span class="sxs-lookup"><span data-stu-id="abfb8-140">Tax Group</span></span>
  - <span data-ttu-id="abfb8-141">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="abfb8-141">Customer Group</span></span>
  - <span data-ttu-id="abfb8-142">Grupa dobavljača</span><span class="sxs-lookup"><span data-stu-id="abfb8-142">Vendor Group</span></span>
  - <span data-ttu-id="abfb8-143">Jedinica</span><span class="sxs-lookup"><span data-stu-id="abfb8-143">Unit</span></span>
  - <span data-ttu-id="abfb8-144">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="abfb8-144">Unit Group</span></span>
  - <span data-ttu-id="abfb8-145">Cjenik</span><span class="sxs-lookup"><span data-stu-id="abfb8-145">Price List</span></span>
  - <span data-ttu-id="abfb8-146">Cjenik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="abfb8-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="abfb8-147">Učestalost fakturiranja</span><span class="sxs-lookup"><span data-stu-id="abfb8-147">Invoice Frequency</span></span>
  - <span data-ttu-id="abfb8-148">Kategorija resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="abfb8-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="abfb8-149">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="abfb8-149">Transaction Category</span></span>
  - <span data-ttu-id="abfb8-150">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="abfb8-150">Expense Category</span></span>
  - <span data-ttu-id="abfb8-151">Cijena uloge</span><span class="sxs-lookup"><span data-stu-id="abfb8-151">Role Price</span></span>
  - <span data-ttu-id="abfb8-152">Cijena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="abfb8-152">Transaction Category Price</span></span>
  - <span data-ttu-id="abfb8-153">Značajka</span><span class="sxs-lookup"><span data-stu-id="abfb8-153">Characteristic</span></span>
  - <span data-ttu-id="abfb8-154">Resurs koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="abfb8-154">Bookable Resource</span></span>
  - <span data-ttu-id="abfb8-155">Dodjela kategorije resursa kojeg je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="abfb8-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="abfb8-156">Značajka kategorije resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="abfb8-156">Bookable Resource Characteristic</span></span>

![Dovrši uvoz](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="abfb8-158">Ažuriranje konfiguracija aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="abfb8-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="abfb8-159">Pomaknite se do CE okruženja.</span><span class="sxs-lookup"><span data-stu-id="abfb8-159">Navigate to the CE environment.</span></span> <span data-ttu-id="abfb8-160">Možete ga pronaći otvaranjem [Centra za administratore aplikacije Power Platform](https://admin.powerplatform.microsoft.com/environments), odabirom okruženja i potom mogućnosti **Otvori okruženje**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvaranje okruženja](./media/7OpenEnvironment.png)

2. <span data-ttu-id="abfb8-162">Idite na **Projekti** > **Resursi**, a zatim odaberite **Novi** kako biste svojem korisniku stvorili resurs koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="abfb8-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resursi koje je moguće rezervirati](./media/8BookableResources.png)

3. <span data-ttu-id="abfb8-164">Na kartici **Općenito** odaberite svog korisnika administratora.</span><span class="sxs-lookup"><span data-stu-id="abfb8-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="abfb8-165">Provjerite podudara li se vremenska zona s onom u kojoj se nalazite.</span><span class="sxs-lookup"><span data-stu-id="abfb8-165">Verify that the time zone matches the one you are in.</span></span> 

![Novi resurs koji se može rezervirati](./media/9NewBookableResource.png)

4. <span data-ttu-id="abfb8-167">Na kartici **Planiranje**, u polju **Tvrtka**, odaberite tvrtku **USPM**, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kartica planiranja](./media/10SchedulingTab.png)

5. <span data-ttu-id="abfb8-169">Odaberite karticu **Radno vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-169">Select the **Work hours** tab.</span></span>  

![Radno vrijeme](./media/11WorkHours.png)

6. <span data-ttu-id="abfb8-171">Dvaput kliknite neku vrijednost u kalendaru i odaberite **Uredi** > **Svi događaji u nizu**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Radni kalendar](./media/12WorkCalendar.png)

7. <span data-ttu-id="abfb8-173">Promijenite radno vrijeme u osmosatni (8) radni dan, obilježite vikende kao neradne dane i pobrinite se da se vremenska zona poklapa s vašom.</span><span class="sxs-lookup"><span data-stu-id="abfb8-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="abfb8-174">Odaberite **Spremi i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-174">Select **Save and close**.</span></span>

![Ažuriranje kalendara](./media/13UpdateCalendar.png)

9. <span data-ttu-id="abfb8-176">Idite na **Postavke** > **Predlošci kalendara** i odaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Predlošci kalendara](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="abfb8-178">Unesite naziv, odaberite resurs predloška koji ste stvorili, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Spremanje predloška kalendara](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="abfb8-180">Idite na stavku **Parametri** i dvaput kliknite zapis.</span><span class="sxs-lookup"><span data-stu-id="abfb8-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri projekta](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="abfb8-182">Ažurirajte sljedeća polja:</span><span class="sxs-lookup"><span data-stu-id="abfb8-182">Update the following fields:</span></span>

 - <span data-ttu-id="abfb8-183">**Zadana tvrtka**: USPM</span><span class="sxs-lookup"><span data-stu-id="abfb8-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="abfb8-184">**Zadana organizacijska jedinica**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="abfb8-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="abfb8-185">**Učestalost faktura**: Sedmi i posljednji dan</span><span class="sxs-lookup"><span data-stu-id="abfb8-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="abfb8-186">**Predložak radnog vremena**: Zamijenite s predloškom koji ste stvorili.</span><span class="sxs-lookup"><span data-stu-id="abfb8-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="abfb8-187">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="abfb8-187">Select **Save**.</span></span> 

![Ažuriranje parametara projekta](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
