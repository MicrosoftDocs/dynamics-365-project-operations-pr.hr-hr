---
title: Primjena probnog postavljanja i konfiguracija podataka – jednostavno
description: U ovoj temi nalaze se informacije o načinu primjene pokaznih postavki i konfiguracijskih podataka za aplikaciju Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642084"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="170dd-103">Primjena podataka postavljanja pokazne verzije i konfiguracije za aplikaciju Project Operations – jednostavno</span><span class="sxs-lookup"><span data-stu-id="170dd-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="170dd-104">_\*\*Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="170dd-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="170dd-105">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="170dd-105">Prerequisites</span></span>

<span data-ttu-id="170dd-106">Prije nego započnete konfiguriranje, morate imati okruženje platforme Common Data Service (CDS) pripremljeno za aplikaciju Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="170dd-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="170dd-107">Upute</span><span class="sxs-lookup"><span data-stu-id="170dd-107">Instructions</span></span>

1. <span data-ttu-id="170dd-108">Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="170dd-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="170dd-109">Pomaknite se do mape *ProjOpsDemoDataSetupAndMaster – Integrirani CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="170dd-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="170dd-110">Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="170dd-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="170dd-112">Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu implementacije**.</span><span class="sxs-lookup"><span data-stu-id="170dd-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="170dd-113">Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.</span><span class="sxs-lookup"><span data-stu-id="170dd-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="170dd-114">Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="170dd-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfiguracija prijave](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="170dd-116">Na 3. stranici, s popisa tvrtki ili ustanova na klijentu odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="170dd-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="170dd-117">Na 4. stranici odaberite zip datoteku *MasterAndSetupData* iz raspakirane mape *ProjOpsDemoDataSetupAndMaster – Integrirani CMT*.</span><span class="sxs-lookup"><span data-stu-id="170dd-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip datoteka](./media/3ZipFile.png)

![Odaberite datoteku](./media/4SelectAFile.png)

9. <span data-ttu-id="170dd-120">Nakon odabira zip datoteke odaberite **Uvezi podatke**.</span><span class="sxs-lookup"><span data-stu-id="170dd-120">After the zip file is selected, select **Import Data**.</span></span>

![Uvoz podataka](./media/5ImportData.png)

10. <span data-ttu-id="170dd-122">Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="170dd-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="170dd-123">Po završetku izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="170dd-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="170dd-124">U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 20 entiteta:</span><span class="sxs-lookup"><span data-stu-id="170dd-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="170dd-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="170dd-125">Currency</span></span>
-   <span data-ttu-id="170dd-126">Poslovni subjekt</span><span class="sxs-lookup"><span data-stu-id="170dd-126">Account</span></span>
-   <span data-ttu-id="170dd-127">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="170dd-127">Organizational Unit</span></span>
-   <span data-ttu-id="170dd-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="170dd-128">Contact</span></span>
-   <span data-ttu-id="170dd-129">Porezna grupa</span><span class="sxs-lookup"><span data-stu-id="170dd-129">Tax Group</span></span>
-   <span data-ttu-id="170dd-130">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="170dd-130">Customer Group</span></span>
-   <span data-ttu-id="170dd-131">Jedinica</span><span class="sxs-lookup"><span data-stu-id="170dd-131">Unit</span></span>
-   <span data-ttu-id="170dd-132">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="170dd-132">Unit Group</span></span>
-   <span data-ttu-id="170dd-133">Cjenik</span><span class="sxs-lookup"><span data-stu-id="170dd-133">Price List</span></span>
-   <span data-ttu-id="170dd-134">Cjenik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="170dd-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="170dd-135">Učestalost fakturiranja</span><span class="sxs-lookup"><span data-stu-id="170dd-135">Invoice Frequency</span></span>
-   <span data-ttu-id="170dd-136">Kategorija resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="170dd-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="170dd-137">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="170dd-137">Transaction Category</span></span>
-   <span data-ttu-id="170dd-138">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="170dd-138">Expense Category</span></span>
-   <span data-ttu-id="170dd-139">Cijena uloge</span><span class="sxs-lookup"><span data-stu-id="170dd-139">Role Price</span></span>
-   <span data-ttu-id="170dd-140">Cijena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="170dd-140">Transaction Category Price</span></span>
-   <span data-ttu-id="170dd-141">Značajka</span><span class="sxs-lookup"><span data-stu-id="170dd-141">Characteristic</span></span>
-   <span data-ttu-id="170dd-142">Resurs koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="170dd-142">Bookable Resource</span></span>
-   <span data-ttu-id="170dd-143">Dodjela kategorije resursa kojeg je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="170dd-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="170dd-144">Značajka kategorije resursa koji je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="170dd-144">Bookable Resource Characteristic</span></span>

![Dovrši uvoz](./media/6CompleteImport.png)
