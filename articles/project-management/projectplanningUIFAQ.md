---
title: Rješavanje problema s radom u rešetki sa zadacima
description: U ovoj temi nalaze se informacije o rješavanju problema potrebne za rad u rešetki sa zadacima.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031528"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="922d9-103">Rješavanje problema s radom u rešetki sa zadacima</span><span class="sxs-lookup"><span data-stu-id="922d9-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="922d9-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="922d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="922d9-105">U ovoj temi opisuje se način rješavanja problema s kojima biste se mogli susresti tijekom rada na upravljanju troškovima.</span><span class="sxs-lookup"><span data-stu-id="922d9-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="922d9-106">Omogućivanje kolačića</span><span class="sxs-lookup"><span data-stu-id="922d9-106">Enable cookies</span></span>

<span data-ttu-id="922d9-107">Project Operations zahtijeva da se omoguće kolačići treće strane kako bi se prikazala strukturna analiza rada.</span><span class="sxs-lookup"><span data-stu-id="922d9-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="922d9-108">Kada kolačići trećih strana nisu omogućeni, umjesto da vidite zadatke, vidjet ćete praznu stranicu kada odaberete karticu **Zadaci** na stranici **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="922d9-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Prazna kartica kada kolačići treće strane nisu omogućeni](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="922d9-110">Zaobilazno rješenje</span><span class="sxs-lookup"><span data-stu-id="922d9-110">Workaround</span></span>
<span data-ttu-id="922d9-111">Postupci u nastavku opisuju način ažuriranja postavki preglednika Microsoft Edge ili Google Chrome kako biste omogućili kolačiće treće strane.</span><span class="sxs-lookup"><span data-stu-id="922d9-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="922d9-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="922d9-112">Microsoft Edge</span></span>

1. <span data-ttu-id="922d9-113">Otvorite preglednik Edge.</span><span class="sxs-lookup"><span data-stu-id="922d9-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="922d9-114">U gornjem desnom kutu odaberite **tri točke** (...), a zatim odaberite mogućnost **Postavke**.</span><span class="sxs-lookup"><span data-stu-id="922d9-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="922d9-115">Pod stavkom **Kolačići i dozvole web-mjesta** odaberite **Kolačići i podaci o web mjestu**.</span><span class="sxs-lookup"><span data-stu-id="922d9-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="922d9-116">Isključite **Blokiraj kolačiće treće strane**.</span><span class="sxs-lookup"><span data-stu-id="922d9-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="922d9-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="922d9-117">Google Chrome</span></span>

1. <span data-ttu-id="922d9-118">Otvorite preglednik Chrome.</span><span class="sxs-lookup"><span data-stu-id="922d9-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="922d9-119">U gornjem desnom kutu odaberite tri uspravne točke, a zatim odaberite mogućnost **Postavke**.</span><span class="sxs-lookup"><span data-stu-id="922d9-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="922d9-120">Pod stavkom **Privatnost i sigurnost** odaberite **Kolačići i ostali podaci o web mjestu**.</span><span class="sxs-lookup"><span data-stu-id="922d9-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="922d9-121">Odaberite **Dopusti sve kolačiće**.</span><span class="sxs-lookup"><span data-stu-id="922d9-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="922d9-122">Ako blokirate kolačiće treće strane, blokirat će se svi kolačići i podaci o web-mjestu s drugih web-mjesta, čak i ako je web-mjesto dopušteno na vašem popisu iznimaka.</span><span class="sxs-lookup"><span data-stu-id="922d9-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="922d9-123">Krajnja točka PEX-a</span><span class="sxs-lookup"><span data-stu-id="922d9-123">PEX Endpoint</span></span>

<span data-ttu-id="922d9-124">Project Operations zahtijeva da parametar projekta upućuje na krajnju točku PEX.</span><span class="sxs-lookup"><span data-stu-id="922d9-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="922d9-125">Ovaj krajnja točka potrebna je za komunikaciju s uslugom koja se upotrebljava za prikazivanje strukturne analize rada.</span><span class="sxs-lookup"><span data-stu-id="922d9-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="922d9-126">Ako parametar nije omogućen, dobit ćete pogrešku „Parametar projekta nije valjan”.</span><span class="sxs-lookup"><span data-stu-id="922d9-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="922d9-127">Zaobilazno rješenje</span><span class="sxs-lookup"><span data-stu-id="922d9-127">Workaround</span></span>
 ![Polje krajnje točke PEX na parametru projekta](media/projectparameter.png)

1. <span data-ttu-id="922d9-129">Dodajte polje **Krajnja točka PEX** na stranicu **Parametri projekta**.</span><span class="sxs-lookup"><span data-stu-id="922d9-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="922d9-130">Ažurirajte polje sljedećim vrijednostima: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="922d9-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="922d9-131">Uklonite polje sa stranice **Parametri projekta**.</span><span class="sxs-lookup"><span data-stu-id="922d9-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="922d9-132">Ovlasti za projekt za web</span><span class="sxs-lookup"><span data-stu-id="922d9-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="922d9-133">Project Operations oslanja se na vanjsku uslugu planiranja.</span><span class="sxs-lookup"><span data-stu-id="922d9-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="922d9-134">Usluga zahtijeva da korisnik ima nekoliko uloga dodijeljenih za čitanje i pisanje u entitete povezane sa strukturnom analizom rada.</span><span class="sxs-lookup"><span data-stu-id="922d9-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="922d9-135">Ti entiteti uključuju projektne zadatke, dodjele resursa i ovisnosti zadataka.</span><span class="sxs-lookup"><span data-stu-id="922d9-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="922d9-136">Ako korisnik ne može prikazati strukturnu analizu rada kad ode na karticu **Zadaci**, to je vjerojatno zato što Project za aplikaciju Project Operations nije omogućen.</span><span class="sxs-lookup"><span data-stu-id="922d9-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="922d9-137">Korisnik može dobiti pogrešku sigurnosne uloge ili pogrešku povezanu s uskraćivanjem pristupa.</span><span class="sxs-lookup"><span data-stu-id="922d9-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="922d9-138">Zaobilazno rješenje</span><span class="sxs-lookup"><span data-stu-id="922d9-138">Workaround</span></span>

1. <span data-ttu-id="922d9-139">Idite na **Postavke > Sigurnost > Korisnici > Korisnici aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="922d9-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Alat za čitanje aplikacije](media/applicationuser.jpg)
   
2. <span data-ttu-id="922d9-141">Dvaput kliknite korisnički zapis aplikacije kako biste provjerili sljedeće:</span><span class="sxs-lookup"><span data-stu-id="922d9-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="922d9-142">Korisnik ima pristup projektu.</span><span class="sxs-lookup"><span data-stu-id="922d9-142">The user has access to the project.</span></span> <span data-ttu-id="922d9-143">Ova se provjera obično vrši osiguravanjem da korisnik ima sigurnosnu ulogu **Voditelj projekta**.</span><span class="sxs-lookup"><span data-stu-id="922d9-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="922d9-144">Korisnik aplikacije Microsoft Project postoji i ispravno je konfiguriran.</span><span class="sxs-lookup"><span data-stu-id="922d9-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="922d9-145">Ako taj korisnik ne postoji, možete stvoriti novi korisnički zapis.</span><span class="sxs-lookup"><span data-stu-id="922d9-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="922d9-146">Odaberite **Novi korisnici**.</span><span class="sxs-lookup"><span data-stu-id="922d9-146">Select **New Users**.</span></span> <span data-ttu-id="922d9-147">Promijenite obrazac za unos u **Korisnik aplikacije**, a zatim dodajte **ID aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="922d9-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Pojedinosti o korisniku aplikacije](media/applicationuserdetails.jpg)

4. <span data-ttu-id="922d9-149">Provjerite je li korisniku dodijeljena ispravna licenca i je li usluga omogućena u pojedinostima licencnih planova usluga.</span><span class="sxs-lookup"><span data-stu-id="922d9-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="922d9-150">Provjerite može li korisnik otvoriti project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="922d9-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="922d9-151">Provjerite kroz parametre projekta usmjerava li sustav na ispravu krajnju točku projekta.</span><span class="sxs-lookup"><span data-stu-id="922d9-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="922d9-152">Provjerite je li stvoren korisnik projektne aplikacije.</span><span class="sxs-lookup"><span data-stu-id="922d9-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="922d9-153">Primijenite sljedeće sigurnosne uloge na korisnika:</span><span class="sxs-lookup"><span data-stu-id="922d9-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="922d9-154">Korisnik rješenja Dataverse</span><span class="sxs-lookup"><span data-stu-id="922d9-154">Dataverse User</span></span>
  - <span data-ttu-id="922d9-155">Sustav aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="922d9-155">Project Operations System</span></span>
  - <span data-ttu-id="922d9-156">Sustav projekta</span><span class="sxs-lookup"><span data-stu-id="922d9-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="922d9-157">Pogreška tijekom ažuriranja strukturne analize rada</span><span class="sxs-lookup"><span data-stu-id="922d9-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="922d9-158">Kada se izvrši jedno ili više ažuriranja strukturne analize rada, promjene na kraju ne uspiju i ne spremaju se.</span><span class="sxs-lookup"><span data-stu-id="922d9-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="922d9-159">Dolazi do pogreške u rešetki rasporeda uz napomenu da „Nije bilo moguće spremiti promjenu koju ste nedavno unijeli.”</span><span class="sxs-lookup"><span data-stu-id="922d9-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="922d9-160">Zaobilazno rješenje</span><span class="sxs-lookup"><span data-stu-id="922d9-160">Workaround</span></span>

1. <span data-ttu-id="922d9-161">Provjerite je li korisniku dodijeljena ispravna licenca i je li usluga omogućena u pojedinostima licencnih planova usluga.</span><span class="sxs-lookup"><span data-stu-id="922d9-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="922d9-162">Provjerite može li korisnik otvoriti project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="922d9-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="922d9-163">Provjerite usmjerava li sustav na ispravu krajnju točku projekta.</span><span class="sxs-lookup"><span data-stu-id="922d9-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="922d9-164">Provjerite je li stvoren korisnik projektne aplikacije.</span><span class="sxs-lookup"><span data-stu-id="922d9-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="922d9-165">Primijenite sljedeće sigurnosne uloge na korisnika:</span><span class="sxs-lookup"><span data-stu-id="922d9-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="922d9-166">Korisnik ili osnovni korisnik platforme Dataverse</span><span class="sxs-lookup"><span data-stu-id="922d9-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="922d9-167">Sustav aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="922d9-167">Project Operations System</span></span>
  - <span data-ttu-id="922d9-168">Sustav projekta</span><span class="sxs-lookup"><span data-stu-id="922d9-168">Project System</span></span>
  - <span data-ttu-id="922d9-169">Sustav dvostrukog pisanja aplikacije Project Operations (ova je uloga potrebna ako za aplikaciju Project Operations postavljate scenarij temeljen na resursima / bez zaliha.)</span><span class="sxs-lookup"><span data-stu-id="922d9-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
