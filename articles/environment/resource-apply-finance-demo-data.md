---
title: Primjena pokaznih podataka aplikacije Project Operations na okruženje aplikacije Finance hostirano u oblaku
description: U ovoj temi pojašnjava se način primjene pokaznih podataka iz aplikacije Project Operations na okruženje hostirano u oblaku aplikacije Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096613"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="52e94-103">Primjena pokaznih podataka aplikacije Project Operations na okruženje aplikacije Finance hostirano u oblaku</span><span class="sxs-lookup"><span data-stu-id="52e94-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="52e94-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="52e94-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52e94-105">Ova tema odnosi se samo na verziju 10.0.13 aplikacije Microsoft Dynamics 365 Finance i može se izvršavati samo u okruženju hostiranom u oblaku.</span><span class="sxs-lookup"><span data-stu-id="52e94-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="52e94-106">Dovršite korake iz ove teme **PRIJE** primjene kvalitativnih ažuriranja na okruženje.</span><span class="sxs-lookup"><span data-stu-id="52e94-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="52e94-107">U svom LCS projektu otvorite stranicu **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="52e94-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="52e94-108">Vidite da to uključuje pojedinosti potrebne za povezivanje s okruženjem s pomoću protokola udaljene radne površine (RDP, Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="52e94-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Pojedinosti  okruženja](./media/1EnvironmentDetails.png)

<span data-ttu-id="52e94-110">Prvi skup istaknutih vjerodajnica, vjerodajnice su lokalnog računa i sadrže hipervezu na vezu s udaljenom radnom površinom.</span><span class="sxs-lookup"><span data-stu-id="52e94-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="52e94-111">Vjerodajnice uključuju korisničko ime i lozinku administratora okruženja.</span><span class="sxs-lookup"><span data-stu-id="52e94-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="52e94-112">Drugi skup vjerodajnica upotrebljava se za prijavu na SQL Server u ovom okruženju.</span><span class="sxs-lookup"><span data-stu-id="52e94-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="52e94-113">Daljinski se povežite s okruženjem hipervezom u stavci **Lokalni računi** , a za provjeru autentičnosti upotrijebite **Vjerodajnice lokalnog računa**.</span><span class="sxs-lookup"><span data-stu-id="52e94-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="52e94-114">Idite na mogućnost **Internetske informacijske usluge** > **Skupine aplikacija** > **Usluga AOS** i zaustaviti uslugu.</span><span class="sxs-lookup"><span data-stu-id="52e94-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="52e94-115">Na ovoj točki zaustavljate uslugu kako biste mogli nastaviti mijenjati SQL bazu podataka.</span><span class="sxs-lookup"><span data-stu-id="52e94-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Zaustavljanje AOS-a](./media/2StopAOS.png)

4. <span data-ttu-id="52e94-117">Idite na stavku **Usluge** i zaustavite sljedeće dvije stavke:</span><span class="sxs-lookup"><span data-stu-id="52e94-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="52e94-118">Microsoft Dynamics 365 Unified Operations: Usluga upravljanja skupom podataka</span><span class="sxs-lookup"><span data-stu-id="52e94-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="52e94-119">Microsoft Dynamics 365 Unified Operations : Okvir za izvoz/uvoz podataka</span><span class="sxs-lookup"><span data-stu-id="52e94-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Zaustavljanje usluge](./media/3StopServices.png)

5. <span data-ttu-id="52e94-121">Otvorite aplikaciju Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="52e94-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="52e94-122">Prijavite se s vjerodajnicama SQL poslužitelja i upotrijebite axdbadmin korisnika i lozinku s LCS stranice **Pojedinosti okruženja**.</span><span class="sxs-lookup"><span data-stu-id="52e94-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="52e94-124">U Object Exploreru idite na postavku **Baze podataka** i pronađite **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="52e94-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="52e94-125">Bazu podataka zamijenit ćete novom bazom podataka koja se nalazi u [Centru za preuzimanje](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="52e94-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="52e94-126">Kopirajte zip datoteku u VM u koji ste udaljeni i izdvojite zip sadržaj.</span><span class="sxs-lookup"><span data-stu-id="52e94-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="52e94-127">U aplikaciji SQL Server Management Studio desnom tipkom miša kliknite **AxDB** , a zatim odaberite **Zadaci** > **Vrati** > **Baza podataka**.</span><span class="sxs-lookup"><span data-stu-id="52e94-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![Vraćanje baze podataka](./media/5RestoreDatabase.png)

9. <span data-ttu-id="52e94-129">Odaberite **Izvorni uređaj** i prijeđite na datoteku izdvojenu iz zip datoteke koju ste kopirali.</span><span class="sxs-lookup"><span data-stu-id="52e94-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Izvorni uređaji](./media/6SourceDevice.png)

10. <span data-ttu-id="52e94-131">Odaberite **Mogućnosti** , a zatim **Piši preko postojeće baze podataka** i **Zatvori postojeće veze s odredišnom bazom podataka**.</span><span class="sxs-lookup"><span data-stu-id="52e94-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="52e94-132">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="52e94-132">Select **OK**.</span></span>

![Vraćanje postavki](./media/7RestoreSetting.png)

<span data-ttu-id="52e94-134">Dobit ćete potvrdu kako je vraćanje AXDB-a bilo uspješno.</span><span class="sxs-lookup"><span data-stu-id="52e94-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="52e94-135">Nakon što primite ovu potvrdu, možete zatvoriti aplikaciju SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="52e94-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="52e94-136">Vratite se na mogućnost **Internetske informacijske usluge** > **Skupine aplikacija** > **Usluga AOS** i pokrenite uslugu AOS.</span><span class="sxs-lookup"><span data-stu-id="52e94-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="52e94-137">Idite na **Usluge** i pokrenite dvije usluge koje ste ranije zaustavili.</span><span class="sxs-lookup"><span data-stu-id="52e94-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="52e94-138">Pronađite alat AdminUserProvisioning na ovom VM-u.</span><span class="sxs-lookup"><span data-stu-id="52e94-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="52e94-139">Pogledajte na putanji K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="52e94-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="52e94-140">Pokrenite datoteku .ext s pomoću svoje korisničke adrese u polju **Adresa e pošte**.</span><span class="sxs-lookup"><span data-stu-id="52e94-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="52e94-141">Odaberite **Šalji**.</span><span class="sxs-lookup"><span data-stu-id="52e94-141">Select **Submit**.</span></span>

![Dodjela korisnika administratora](./media/8AdminUserProvisioning.png)

<span data-ttu-id="52e94-143">To traje nekoliko minuta.</span><span class="sxs-lookup"><span data-stu-id="52e94-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="52e94-144">Trebali biste primiti poruku s potvrdom kako je korisnik administrator uspješno ažuriran.</span><span class="sxs-lookup"><span data-stu-id="52e94-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="52e94-145">Na kraju, pokrenite Command Prompt kao Administrator i izvršite iisreset</span><span class="sxs-lookup"><span data-stu-id="52e94-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS vraćanje](./media/9IISReset.png)

18. <span data-ttu-id="52e94-147">Zatvorite sesiju udaljene radne površine i upotrijebite LCS stranicu **Pojedinosti okruženja** za prijavu u okruženje kako biste potvrdili da radi onako kako se očekivalo.</span><span class="sxs-lookup"><span data-stu-id="52e94-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
