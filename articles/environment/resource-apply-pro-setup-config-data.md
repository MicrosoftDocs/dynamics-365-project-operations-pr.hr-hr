---
title: Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service za aplikaciju Project Operations
description: U ovoj temi nalaze se informacije o načinu postavljanja i primjene konfiguracijskih podataka u aplikaciji Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948790"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="ac29b-103">Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service za aplikaciju Project Operations</span><span class="sxs-lookup"><span data-stu-id="ac29b-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="ac29b-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ac29b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="ac29b-105">Instalacija postavljanja i konfiguracijskih podataka</span><span class="sxs-lookup"><span data-stu-id="ac29b-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="ac29b-106">Preuzmite, deblokirajte i raspakirajte [Paket podataka za postavljanje i konfiguraciju](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="ac29b-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="ac29b-107">Pomaknite se do raspakirane mape i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="ac29b-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="ac29b-108">Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="ac29b-110">Na 2. stranici CMT čarobnjaka odaberite **Office 365** kao **Vrstu uvođenja**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="ac29b-111">Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="ac29b-112">Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite mogućnost **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfiguracija prijave](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="ac29b-114">Na 3. stranici, s popisa tvrtki ili ustanova na klijentu, odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="ac29b-115">Na 4. stranici odaberite zip datoteku *SampleSetupAndConfigData* iz raspakirane mape.</span><span class="sxs-lookup"><span data-stu-id="ac29b-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Odabir zip datoteke](./media/3ZipFile.png)

![Odaberite datoteku](./media/4SelectAFile.png)

9. <span data-ttu-id="ac29b-118">Nakon odabira zip datoteke odaberite **Uvezi podatke**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-118">After the zip file is selected, select **Import Data**.</span></span>

![Uvoz podataka](./media/5ImportData.png)

10. <span data-ttu-id="ac29b-120">Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="ac29b-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="ac29b-121">Po završetku uvoza izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="ac29b-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="ac29b-122">U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 19 entiteta:</span><span class="sxs-lookup"><span data-stu-id="ac29b-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="ac29b-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="ac29b-123">Currency</span></span>
  - <span data-ttu-id="ac29b-124">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="ac29b-124">Organizational Unit</span></span>
  - <span data-ttu-id="ac29b-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="ac29b-125">Contact</span></span>
  - <span data-ttu-id="ac29b-126">Porezna grupa</span><span class="sxs-lookup"><span data-stu-id="ac29b-126">Tax Group</span></span>
  - <span data-ttu-id="ac29b-127">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="ac29b-127">Customer Group</span></span>
  - <span data-ttu-id="ac29b-128">Jedinica</span><span class="sxs-lookup"><span data-stu-id="ac29b-128">Unit</span></span>
  - <span data-ttu-id="ac29b-129">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="ac29b-129">Unit Group</span></span>
  - <span data-ttu-id="ac29b-130">Cjenik</span><span class="sxs-lookup"><span data-stu-id="ac29b-130">Price List</span></span>
  - <span data-ttu-id="ac29b-131">Cjenik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="ac29b-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="ac29b-132">Učestalost fakturiranja</span><span class="sxs-lookup"><span data-stu-id="ac29b-132">Invoice Frequency</span></span>
  - <span data-ttu-id="ac29b-133">Kategorija resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="ac29b-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="ac29b-134">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="ac29b-134">Transaction Category</span></span>
  - <span data-ttu-id="ac29b-135">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="ac29b-135">Expense Category</span></span>
  - <span data-ttu-id="ac29b-136">Cijena uloge</span><span class="sxs-lookup"><span data-stu-id="ac29b-136">Role Price</span></span>
  - <span data-ttu-id="ac29b-137">Cijena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="ac29b-137">Transaction Category Price</span></span>
  - <span data-ttu-id="ac29b-138">Značajka</span><span class="sxs-lookup"><span data-stu-id="ac29b-138">Characteristic</span></span>
  - <span data-ttu-id="ac29b-139">Resurs koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="ac29b-139">Bookable Resource</span></span>
  - <span data-ttu-id="ac29b-140">Dodjela kategorije resursa kojeg je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="ac29b-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="ac29b-141">Značajka kategorije resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="ac29b-141">Bookable Resource Characteristic</span></span>

![Dovrši uvoz](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="ac29b-143">Ažuriranje konfiguracija aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="ac29b-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="ac29b-144">Pomaknite se do CE okruženja.</span><span class="sxs-lookup"><span data-stu-id="ac29b-144">Navigate to the CE environment.</span></span> <span data-ttu-id="ac29b-145">Možete ga pronaći otvaranjem [Centra za administratore aplikacije Power Platform](https://admin.powerplatform.microsoft.com/environments), odabirom okruženja i potom mogućnosti **Otvori okruženje**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvaranje okruženja](./media/7OpenEnvironment.png)

2. <span data-ttu-id="ac29b-147">Idite na **Projekti** > **Resursi**, a zatim odaberite **Novi** kako biste svojem korisniku stvorili resurs koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="ac29b-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resursi koje je moguće rezervirati](./media/8BookableResources.png)

3. <span data-ttu-id="ac29b-149">Na kartici **Općenito** odaberite svog korisnika administratora.</span><span class="sxs-lookup"><span data-stu-id="ac29b-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="ac29b-150">Provjerite podudara li se vremenska zona s onom u kojoj se nalazite.</span><span class="sxs-lookup"><span data-stu-id="ac29b-150">Verify that the time zone matches the one you are in.</span></span> 

![Novi resurs koji se može rezervirati](./media/9NewBookableResource.png)

4. <span data-ttu-id="ac29b-152">Na kartici **Planiranje**, u polju **Tvrtka**, odaberite tvrtku **USPM**, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kartica planiranja](./media/10SchedulingTab.png)

5. <span data-ttu-id="ac29b-154">Odaberite karticu **Radno vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-154">Select the **Work hours** tab.</span></span>  

![Radno vrijeme](./media/11WorkHours.png)

6. <span data-ttu-id="ac29b-156">Dvaput kliknite neku vrijednost u kalendaru i odaberite **Uredi** > **Svi događaji u nizu**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Radni kalendar](./media/12WorkCalendar.png)

7. <span data-ttu-id="ac29b-158">Promijenite radno vrijeme u osmosatni (8) radni dan, obilježite vikende kao neradne dane i pobrinite se da se vremenska zona poklapa s vašom.</span><span class="sxs-lookup"><span data-stu-id="ac29b-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="ac29b-159">Odaberite **Spremi i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-159">Select **Save and close**.</span></span>

![Ažuriranje kalendara](./media/13UpdateCalendar.png)

9. <span data-ttu-id="ac29b-161">Idite na **Postavke** > **Predlošci kalendara** i odaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Predlošci kalendara](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="ac29b-163">Unesite naziv, odaberite resurs predloška koji ste stvorili, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Spremanje predloška kalendara](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="ac29b-165">Idite na stavku **Parametri** i dvaput kliknite zapis.</span><span class="sxs-lookup"><span data-stu-id="ac29b-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri projekta](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="ac29b-167">Ažurirajte sljedeća polja:</span><span class="sxs-lookup"><span data-stu-id="ac29b-167">Update the following fields:</span></span>

 - <span data-ttu-id="ac29b-168">**Zadana tvrtka**: USPM</span><span class="sxs-lookup"><span data-stu-id="ac29b-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="ac29b-169">**Zadana organizacijska jedinica** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="ac29b-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="ac29b-170">**Učestalost faktura**: Sedmi i posljednji dan</span><span class="sxs-lookup"><span data-stu-id="ac29b-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="ac29b-171">**Predložak radnog vremena**: Zamijenite s predloškom koji ste stvorili.</span><span class="sxs-lookup"><span data-stu-id="ac29b-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="ac29b-172">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="ac29b-172">Select **Save**.</span></span> 

![Ažuriranje parametara projekta](./media/17UpdatedProjectParameters.png)
