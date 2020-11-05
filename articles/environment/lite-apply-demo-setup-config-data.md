---
title: Primjena pokaznog postavljanja i konfiguracijskih podataka
description: U ovoj temi nalaze se informacije o načinu primjene pokaznih postavki i konfiguracijskih podataka za aplikaciju Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073253"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="603d5-103">Primjena pokaznih postavki i konfiguracijskih podataka za uvođenje jednostavne aplikacije Project Operations – od sklapanja posla do predračuna</span><span class="sxs-lookup"><span data-stu-id="603d5-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="603d5-104">_\*\*Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="603d5-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="603d5-105">Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="603d5-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="603d5-106">Pomaknite se do mape *ProjOpsDemoDataSetupAndMaster – Integrirani CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="603d5-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="603d5-107">Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="603d5-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="603d5-109">Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu implementacije**.</span><span class="sxs-lookup"><span data-stu-id="603d5-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="603d5-110">Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.</span><span class="sxs-lookup"><span data-stu-id="603d5-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="603d5-111">Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="603d5-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguracija prijave](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="603d5-113">Na 3. stranici, s popisa tvrtki ili ustanova na klijentu odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="603d5-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="603d5-114">Na 4. stranici odaberite zip datoteku *MasterAndSetupData* iz raspakirane mape *ProjOpsDemoDataSetupAndMaster – Integrirani CMT*.</span><span class="sxs-lookup"><span data-stu-id="603d5-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip datoteka](./media/3ZipFile.png)

![Odaberite datoteku](./media/4SelectAFile.png)

9. <span data-ttu-id="603d5-117">Nakon odabira zip datoteke odaberite **Uvezi podatke**.</span><span class="sxs-lookup"><span data-stu-id="603d5-117">After the zip file is selected, select **Import Data**.</span></span>

![Uvoz podataka](./media/5ImportData.png)

10. <span data-ttu-id="603d5-119">Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="603d5-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="603d5-120">Po završetku izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="603d5-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="603d5-121">U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 20 entiteta:</span><span class="sxs-lookup"><span data-stu-id="603d5-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="603d5-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="603d5-122">Currency</span></span>
- <span data-ttu-id="603d5-123">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="603d5-123">Organizational Unit</span></span>
- <span data-ttu-id="603d5-124">Kontakt</span><span class="sxs-lookup"><span data-stu-id="603d5-124">Contact</span></span>
- <span data-ttu-id="603d5-125">Porezna grupa</span><span class="sxs-lookup"><span data-stu-id="603d5-125">Tax Group</span></span>
- <span data-ttu-id="603d5-126">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="603d5-126">Customer Group</span></span>
- <span data-ttu-id="603d5-127">Jedinica</span><span class="sxs-lookup"><span data-stu-id="603d5-127">Unit</span></span>
- <span data-ttu-id="603d5-128">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="603d5-128">Unit Group</span></span>
- <span data-ttu-id="603d5-129">Cjenik</span><span class="sxs-lookup"><span data-stu-id="603d5-129">Price List</span></span>
- <span data-ttu-id="603d5-130">Cjenik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="603d5-130">Project Parameter Price List</span></span>
- <span data-ttu-id="603d5-131">Učestalost fakturiranja</span><span class="sxs-lookup"><span data-stu-id="603d5-131">Invoice Frequency</span></span>
- <span data-ttu-id="603d5-132">Pojedinost učestalosti fakture</span><span class="sxs-lookup"><span data-stu-id="603d5-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="603d5-133">Kategorija resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="603d5-133">Bookable Resource Category</span></span>
- <span data-ttu-id="603d5-134">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="603d5-134">Transaction Category</span></span>
- <span data-ttu-id="603d5-135">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="603d5-135">Expense Category</span></span>
- <span data-ttu-id="603d5-136">Cijena uloge</span><span class="sxs-lookup"><span data-stu-id="603d5-136">Role Price</span></span>
- <span data-ttu-id="603d5-137">Cijena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="603d5-137">Transaction Category Price</span></span>
- <span data-ttu-id="603d5-138">Značajka</span><span class="sxs-lookup"><span data-stu-id="603d5-138">Characteristic</span></span>
- <span data-ttu-id="603d5-139">Resurs koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="603d5-139">Bookable Resource</span></span>
- <span data-ttu-id="603d5-140">Dodjela kategorije resursa kojeg je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="603d5-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="603d5-141">Značajka kategorije resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="603d5-141">Bookable Resource Characteristic</span></span>

![Dovrši uvoz](./media/6CompleteImport.png)
