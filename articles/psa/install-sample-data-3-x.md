---
title: Instalacija uzorka podataka
description: U ovoj temi nalaze se informacije o načinu instaliranju uzoraka podataka u aplikaciju Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: aaeb4163c7ace1c3bf4db61f1a10a13cfbdc4fc2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144494"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="cfe58-103">Instalacija oglednih podataka za aplikaciju Project Service</span><span class="sxs-lookup"><span data-stu-id="cfe58-103">Sample data installation for the Project Service application</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cfe58-104">Da biste mogli izraditi vlastita demonstracijska okruženja, Microsoft vam omogućuje da preuzmete pakete oglednih podataka pomoću kojih ćete vidjeti mogućnosti svojih aplikacija.</span><span class="sxs-lookup"><span data-stu-id="cfe58-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="cfe58-105">Postoje dvije vrste paketa oglednih podataka:</span><span class="sxs-lookup"><span data-stu-id="cfe58-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="cfe58-106">referentni podaci / podaci za postavljanje</span><span class="sxs-lookup"><span data-stu-id="cfe58-106">reference/setup data</span></span>
- <span data-ttu-id="cfe58-107">pokazni podaci (referentni podaci / podaci za postavljanje i transakcijski podaci kao što su radni nalozi i projekti)</span><span class="sxs-lookup"><span data-stu-id="cfe58-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="cfe58-108">Paketi oglednih **referentnih** podataka mogu se preuzeti u trima različitim paketima, pa možete instalirati samo podatke za Project Service ili samo za Field Service ili pak možete istodobno instalirati ogledne podatke za obje aplikacije.</span><span class="sxs-lookup"><span data-stu-id="cfe58-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="cfe58-109">Paketi oglednih podataka za postavljanje / referentnih podataka su sljedeći:</span><span class="sxs-lookup"><span data-stu-id="cfe58-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="cfe58-110">**V902PSMasterData** – samo verzija 3.x za Project Service</span><span class="sxs-lookup"><span data-stu-id="cfe58-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="cfe58-111">**V902FSMasterData** – samo verzija 8.x za Field Service</span><span class="sxs-lookup"><span data-stu-id="cfe58-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="cfe58-112">**V902FPSMasterData** - Field Service 8.x i Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="cfe58-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="cfe58-113">Najnoviji paket **pokaznih** podataka je sljedeći:</span><span class="sxs-lookup"><span data-stu-id="cfe58-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="cfe58-114">**FPSDemoData** – Field Service 8.x i Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="cfe58-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="cfe58-115">Upute za instalaciju malo se razlikuju u odjeljku korisnika za stvaranje i konfiguriranje, ali ostatak je isti kao u prethodnoj [**objavi na blogu**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="cfe58-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="cfe58-116">Ovaj paket sadrži smanjeni skup pokaznih podataka i njegova instalacija traje približno 3 sata.</span><span class="sxs-lookup"><span data-stu-id="cfe58-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="cfe58-117">Ti paketi oglednih podataka dostupni su samo na engleskom.</span><span class="sxs-lookup"><span data-stu-id="cfe58-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfe58-118">**Ogledne podatke nije moguće deinstalirati.**</span><span class="sxs-lookup"><span data-stu-id="cfe58-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="cfe58-119">Pakete biste trebali instalirati samo na probnim ili testnim sustavima te sustavima za procjenu i obuku.</span><span class="sxs-lookup"><span data-stu-id="cfe58-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="cfe58-120">Napominjemo i da nije podržano instaliranje jednog pojedinačnog paketa, a zatim instaliranje još jednog pojedinačnog paketa.</span><span class="sxs-lookup"><span data-stu-id="cfe58-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="cfe58-121">(Drugim riječima, ne možete instalirati **FSMasterData**, a nakon toga **PSMasterData** ili obrnuto.) Ako mislite da bi vam u budućnosti mogli zatrebati ogledni podaci za obje aplikacije, instalirajte paket **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="cfe58-122">Pri instaliranju bilo kojeg paketa oglednih podataka postupak instalacije izvodi sljedeće radnje:</span><span class="sxs-lookup"><span data-stu-id="cfe58-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="cfe58-123">Stvara ili postavlja zadane parametre za korištenje aplikacije Project Service, Field Service ili obje aplikacije (ako je to primjenjivo).</span><span class="sxs-lookup"><span data-stu-id="cfe58-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="cfe58-124">Uvozi ogledne podatke za aplikacije, kao što su resursi koji se mogu rezervirati, uloge za određenu aplikaciju, prodajne popise i cjenike, organizacijske jedinice, zapise o prodajnim procesima i druge entitete koji prikazuju ključne mogućnosti aplikacije.</span><span class="sxs-lookup"><span data-stu-id="cfe58-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="cfe58-125">U paketu **pokaznih podataka** dobivate sve gore navedene i dodatne transakcijske podatke kao što su radni nalozi i projekti.</span><span class="sxs-lookup"><span data-stu-id="cfe58-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="cfe58-126">Pitate se koje mogućnosti možete demonstrirati uz pomoć oglednih podataka?</span><span class="sxs-lookup"><span data-stu-id="cfe58-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="cfe58-127">Pogledajte izmišljeni scenarij za Fabrikam Robotics u [tehničkim napomenama](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="cfe58-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="cfe58-128">Ako imate pitanja o instaliranju tih paketa oglednih podataka, [pošaljite nam poruku e-pošte na adresu fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="cfe58-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe58-129">Uvjeti</span><span class="sxs-lookup"><span data-stu-id="cfe58-129">Requirements</span></span>

<span data-ttu-id="cfe58-130">Instalacijski protokol pretpostavlja sljedeće o vašoj ciljnoj instanci (organizaciji):</span><span class="sxs-lookup"><span data-stu-id="cfe58-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="cfe58-131">Osnovni jezik je engleski, a osnovna valuta američki dolar (USD, $).</span><span class="sxs-lookup"><span data-stu-id="cfe58-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="cfe58-132">Tvrtka ili ustanova nema već podatke za Field Service ili Project Service ili su to samo osnovni zadani podaci koji dolaze u svaku novu tvrtku ili ustanovu.</span><span class="sxs-lookup"><span data-stu-id="cfe58-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="cfe58-133">Već je instalirana ispravna verzija poslovne aplikacije:</span><span class="sxs-lookup"><span data-stu-id="cfe58-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="cfe58-134">**Za FPSDemoData ili v902FPSMasterData:** za tvrtku ili ustanovu instalirane su aplikacije Field Service, verzija 8.x i Project Service, verzija 3.x.</span><span class="sxs-lookup"><span data-stu-id="cfe58-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="cfe58-135">**Za v902PSMasterData:** za organizaciju je instalirana aplikacija Project Service verzija 3.x.</span><span class="sxs-lookup"><span data-stu-id="cfe58-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="cfe58-136">**Za v902FSMasterData:** za organizaciju je instalirana aplikacija Field Service verzija 8.x.</span><span class="sxs-lookup"><span data-stu-id="cfe58-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="cfe58-137">Ako ogledne podatke morate instalirati preko postojećeg probnog ili pokaznog okruženja za Project Service i Field Service koje već sadrži podatke (ne preporučuje se), morat ćete obustaviti sigurnosne predprovjere koje izvodi instalacijski program.</span><span class="sxs-lookup"><span data-stu-id="cfe58-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="cfe58-138">Dodatne informacije potražite u tehničkim napomenama u nastavku.</span><span class="sxs-lookup"><span data-stu-id="cfe58-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="cfe58-139">Priprema za instalaciju</span><span class="sxs-lookup"><span data-stu-id="cfe58-139">Prepare for installation</span></span>

<span data-ttu-id="cfe58-140">Morate pokrenuti instalacijski program na računalu s najnovijom verzijom sustava Windows (Windows 10 Preferirani).</span><span class="sxs-lookup"><span data-stu-id="cfe58-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="cfe58-141">Trebate planirati da računalo ostane povezano s mrežom te da instalacija **podataka za postavljanje / referentnih podataka** traje do **jednog sata**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="cfe58-142">(Instalacija paketa **FPSMasterData** obično traje oko 30 minuta, a taj paket sadrži ogledne podatke za obje aplikacije.) Instalacija paketa **FPSDemoData** trajat će oko **3 sata**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="cfe58-143">Na računalu mora biti isključena funkcija čuvara zaslona.</span><span class="sxs-lookup"><span data-stu-id="cfe58-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="cfe58-144">U suprotnom se vjerodajnice sesije za instalaciju mogu izgubiti kada se aktivira čuvar zaslona (osim ako sesija aktivna cijelo vrijeme).</span><span class="sxs-lookup"><span data-stu-id="cfe58-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="cfe58-145">![Snimka zaslona s prikazom postavki čuvara zaslona s isključenim čuvarom zaslona](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="cfe58-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="cfe58-146">Preuzimanje i raspakiravanje</span><span class="sxs-lookup"><span data-stu-id="cfe58-146">Download and unpack</span></span>

<span data-ttu-id="cfe58-147">Instalacijski program za ogledne podatke aplikacija Project Service i Field Service distribuira se kao izvršna datoteka s automatskim izdvajanjem.</span><span class="sxs-lookup"><span data-stu-id="cfe58-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="cfe58-148">Nazivi datoteka mogu se razlikovati ovisno o paketu oglednih podataka, ali inače su koraci isti bez obzira na to koji paket instalirate.</span><span class="sxs-lookup"><span data-stu-id="cfe58-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="cfe58-149">Nakon preuzimanja paketa pokrenite .exe datoteku, a zatim prihvatite ugovorne odredbe i uvjete da biste raspakirali komprimiranu zip datoteku.</span><span class="sxs-lookup"><span data-stu-id="cfe58-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="cfe58-150">Potom morate izdvojiti sadržaj te datoteke u mapu na računalu.</span><span class="sxs-lookup"><span data-stu-id="cfe58-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="cfe58-151">Ovisno o operacijskom sustavu i sigurnosnim postavkama, možda ćete morati izvršiti sljedeće korake nakon raspakiravanja zip datoteke:</span><span class="sxs-lookup"><span data-stu-id="cfe58-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="cfe58-152">Pronađite i desnom tipkom miša kliknite datoteku **FPSDemoData.dll** u mapi **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="cfe58-153">Odaberite **Deblokiraj**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="cfe58-154">Odaberite **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-154">Select **Apply**.</span></span>

4. <span data-ttu-id="cfe58-155">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="cfe58-156">Stvaranje ili konfiguriranje korisnika</span><span class="sxs-lookup"><span data-stu-id="cfe58-156">Create or configure users</span></span>

<span data-ttu-id="cfe58-157">Za paket **FPSDemoData** potrebno je šest korisnika, a za paket **FPSMasterData** jedan korisnik.</span><span class="sxs-lookup"><span data-stu-id="cfe58-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="cfe58-158">Potražite odgovarajući za svoj paket oglednih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="cfe58-159">Stvaranje ili konfiguriranje korisnika – paketi podataka za postavljanje / referentnih podataka</span><span class="sxs-lookup"><span data-stu-id="cfe58-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="cfe58-160">Pri instalaciji paketa **FPSMasterData** bit će potrebno odabrati korisnika Spencer Low i za njega koristiti ovdje opisane postavke.</span><span class="sxs-lookup"><span data-stu-id="cfe58-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="cfe58-161">Da biste ispravno instalirali paket, trebate stvoriti (ili privremeno preimenovati) korisnike u svom okruženju tako da odgovaraju konfiguraciji ulaznih oglednih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="cfe58-162">Da biste stvorili ili konfigurirali korisnike, idite na **Postavke** > **Sigurnost** > **Korisnici**, a zatim učinite sljedeće:</span><span class="sxs-lookup"><span data-stu-id="cfe58-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="cfe58-163">Korisniku UserFullname="Spencer Low" s korisničkim imenom „spencerl” (**mala slova**) dodijelite ulogu voditelja projekta i upravitelja prakse.</span><span class="sxs-lookup"><span data-stu-id="cfe58-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="cfe58-164">Odaberite korisnika **Spencer Low** , a zatim odaberite **Upravljanje ulogama**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="cfe58-165">Pronađite i odaberite ulogu **Administrator sustava**, a zatim odaberite **U redu** da biste dodijelili potpuna administratorska prava Spenceru Lowu.</span><span class="sxs-lookup"><span data-stu-id="cfe58-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="cfe58-166">Taj je korak potreban kako bi se osiguralo da stvoreni ogledni zapisi imaju ispravno korisničko vlasništvo te da se prikazi ispravno popune.</span><span class="sxs-lookup"><span data-stu-id="cfe58-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="cfe58-167">U preuzetom paketu morate ažurirati datoteku za mapiranje podataka adresama e-pošte zadanog korisničkog konteksta.</span><span class="sxs-lookup"><span data-stu-id="cfe58-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="cfe58-168">Kako biste to učinili, otvorite mapu **PkgFolder**, a zatim pronađite i otvorite datoteku **ImportUserMapFile.xml** u programu Notepad (alatu Visual Studio ili nekom drugom XML uređivaču).</span><span class="sxs-lookup"><span data-stu-id="cfe58-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="cfe58-169">Postavite polje **DefaultUserToMapTo =** na adresu e-pošte korisnika Spencera Lowa.</span><span class="sxs-lookup"><span data-stu-id="cfe58-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="cfe58-170">Ako za korisnika niste odabrali Spencera Lowa s korisničkim imenom **spencerl**, morate ažurirati dodatnu datoteku.</span><span class="sxs-lookup"><span data-stu-id="cfe58-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="cfe58-171">Otvorite datoteku **DemoDataPreImportConfig.xml**, a zatim pronađite oznaku **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="cfe58-172">Ažurirajte oznaku **\<login\>** korisničkim imenom korisnika Tome Debeljaka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="cfe58-173">Dodatne pojedinosti potražite u [tehničkim napomenama](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="cfe58-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="cfe58-174">Stvaranje ili konfiguriranje korisnika – paket pokaznih podataka</span><span class="sxs-lookup"><span data-stu-id="cfe58-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="cfe58-175">Za paket pokaznih podataka potrebno je šest korisnika.</span><span class="sxs-lookup"><span data-stu-id="cfe58-175">The demo data package requires six users.</span></span> <span data-ttu-id="cfe58-176">Da bi se paket pravilno instalirao, učinite sljedeće:</span><span class="sxs-lookup"><span data-stu-id="cfe58-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="cfe58-177">Stvorite nove korisnike ili privremeno preimenujte postojeće tako da odgovaraju ulaznoj konfiguraciji oglednih podataka. To možete učiniti u odjeljku **Postavke** > **Sigurnost** > **Korisnici**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="cfe58-178">Te su uloge potrebne samo za pokazne programe koji se temelje na osobama.</span><span class="sxs-lookup"><span data-stu-id="cfe58-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="cfe58-179">Ime i prezime korisnika = „David So” kao tehničar za upravljanje terenskom uslugom (Field Service)</span><span class="sxs-lookup"><span data-stu-id="cfe58-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="cfe58-180">Ime i prezime korisnika = „Reding Jamie” kao Otpremnik službe za korisnike (Customer Service) i Otpremnik terenske usluge (Field Service)</span><span class="sxs-lookup"><span data-stu-id="cfe58-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="cfe58-181">Ime i prezime korisnika = „Molly Clark” kao Upraviteljica računa</span><span class="sxs-lookup"><span data-stu-id="cfe58-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="cfe58-182">Ime i prezime korisnika = „Spencer Low” kao Upravitelj vježbi i Voditelj projekta</span><span class="sxs-lookup"><span data-stu-id="cfe58-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="cfe58-183">Ime i prezime korisnika = „Veronica Quek” kao član tima</span><span class="sxs-lookup"><span data-stu-id="cfe58-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="cfe58-184">Ime i prezime korisnika = „William Contoso”</span><span class="sxs-lookup"><span data-stu-id="cfe58-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="cfe58-185">U svrhe uvoza pokaznih podataka dodijelite šest korisnika s ulogom iznad uloge administratora da bi se uzorci zapisa pravilno uvezli.</span><span class="sxs-lookup"><span data-stu-id="cfe58-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="cfe58-186">Otvorite mapu **PkgFolder** i zatim pronađite i otvorite datoteku **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="cfe58-187">Ažurirajte polja **Novo=** tako da sadrže adrese e-pošte odgovarajućih korisnika u vašem sustavu.</span><span class="sxs-lookup"><span data-stu-id="cfe58-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cfe58-188">![Snimka zaslona s prikazom datoteke UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="cfe58-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="cfe58-189">Ako vaš korisnik s imenom i prezimenom „Spencer Low” ima drugačiji korisnički ID od **"spencerl**, morate ažurirati dodatnu datoteku.</span><span class="sxs-lookup"><span data-stu-id="cfe58-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="cfe58-190">Otvorite datoteku **DemoDataPreImportConfig.xml** pa pronađite oznaku **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="cfe58-191">Ažurirajte oznaku **\<login\>** s pomoću ID-a za prijavu (razlikovanje velikih i malih slova).</span><span class="sxs-lookup"><span data-stu-id="cfe58-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="cfe58-192">Kalendar prvog korisnika (u oznaci **userstocreateandconfigure**) upotrebljava se za ispunjavanje radnog vremena za sve resurse koje je moguće rezervirati pri uvozu pokaznih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="cfe58-193">Idite na **Postavke** > **Sigurnost** > **Korisnici**, pronađite svojeg korisnika „Spencer Low” i otvorite mogućnost „Radno vrijeme”.</span><span class="sxs-lookup"><span data-stu-id="cfe58-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="cfe58-194">Uredite postojeće radno vrijeme uz odabir mogućnosti **Cijeli tjedni raspored koji se ponavlja od početka do kraja**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="cfe58-195">Provjerite je li **radno vrijeme postavljeno na 8 – 17 sati (9 sati), od ponedjeljka do petka, s vremenskom zonom Pacifičko vrijeme (SAD i Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="cfe58-196">To je potrebno kako biste osigurali pravilan prikaz ploče projekta i rasporeda.</span><span class="sxs-lookup"><span data-stu-id="cfe58-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="cfe58-197">**Preporuka:** bilo bi dobro da odmah stvorite sigurnosnu kopiju svoje organizacije u slučaju da se morate vratiti na početnu točku ako nešto ne bude u redu tijekom instalacije oglednih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="cfe58-198">Dodatne informacije potražite u članku [Sigurnosno kopiranje i vraćanje instanci](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="cfe58-198">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="cfe58-199">Pokrenite Package Deployer</span><span class="sxs-lookup"><span data-stu-id="cfe58-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="cfe58-200">Pronađite i pokrenite datoteku **PackageDeployer.exe** u mapi **v902FPSMasterData** ILI **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="cfe58-201">Prihvatite uvjete i odredbe.</span><span class="sxs-lookup"><span data-stu-id="cfe58-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="cfe58-202">Na sljedećem prozoru:</span><span class="sxs-lookup"><span data-stu-id="cfe58-202">On the next window:</span></span>

   <span data-ttu-id="cfe58-203">a.</span><span class="sxs-lookup"><span data-stu-id="cfe58-203">a.</span></span> <span data-ttu-id="cfe58-204">Odaberite vrstu implementacije sustava **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="cfe58-205">b.</span><span class="sxs-lookup"><span data-stu-id="cfe58-205">b.</span></span> <span data-ttu-id="cfe58-206">Koristite korisničko ime i lozinku administratora sustava konfiguriranog u odjeljku „Stvaranje ili konfiguriranje korisnika” („Spencer Low” s korisničkim imenom „spencerl”).</span><span class="sxs-lookup"><span data-stu-id="cfe58-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="cfe58-207">c.</span><span class="sxs-lookup"><span data-stu-id="cfe58-207">c.</span></span> <span data-ttu-id="cfe58-208">Provjerite je li odabrana opcija **Prikaži popis dostupnih organizacija**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="cfe58-209">![Snimka zaslona s prikazom prozora aplikacije Package Deployer s odabranom mogućnošću „Prikaži popis dostupnih tvrtki ili ustanova”](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="cfe58-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="cfe58-210">Odaberite tvrtku ili ustanovu u koju želite instalirati ogledne podatke.</span><span class="sxs-lookup"><span data-stu-id="cfe58-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="cfe58-211">Odaberite **Sljedeće** dok se ne prikaže dijaloški okvir **Postavljanje demo podataka**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cfe58-212">![Snimka zaslona prozora statusa instalacijskog programa za demo podatke](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="cfe58-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="cfe58-213">Prije nastavka napominjemo da instaliranje oglednih podataka može potrajati do jedan sat (obično ~10 minuta).</span><span class="sxs-lookup"><span data-stu-id="cfe58-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="cfe58-214">Morate se pobrinuti da računalo ostane uključeno i povezano s mrežom tijekom cijelog postupka instalacije te da vaša sesija ostane aktivna.</span><span class="sxs-lookup"><span data-stu-id="cfe58-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="cfe58-215">Kada ste spremni, kliknite **Sljedeće** da biste pokrenuli postupak instalacije oglednih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="cfe58-216">Nakon što se ogledni podaci učitaju, pritisnite **Završi**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="cfe58-217">Provjera instalacije oglednih podataka</span><span class="sxs-lookup"><span data-stu-id="cfe58-217">Verify the sample data installation</span></span>

<span data-ttu-id="cfe58-218">Da biste provjerili je li sve u redu, pogledajte izgleda li broj zapisa i vrsta entiteta navedenih u izmišljenom scenariju za Fabrikam Robotics kako treba.</span><span class="sxs-lookup"><span data-stu-id="cfe58-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="cfe58-219">Nakon što se ogledni podaci potpuno učitaju, prijavite se kao korisnik Spencer Low i potvrdite sljedeće:</span><span class="sxs-lookup"><span data-stu-id="cfe58-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="cfe58-220">Ako je instalirana aplikacija Project Service, idite na **Project Service** > **Postavke** > **Cjenici**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="cfe58-221">Potvrdite jesu li u skupu podataka navedene stope naplate i troškova u odgovarajućoj valuti za svaku zemlju/regiju.</span><span class="sxs-lookup"><span data-stu-id="cfe58-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="cfe58-222">Ako je instalirana aplikacija Project Service, idite na stavku **Universal Resource Scheduling** > **Postavke** > **Organizacijska jedinica**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="cfe58-223">Potvrdite da je cjenik u odgovarajućoj valuti povezan sa svakom organizacijskom jedinicom (osim unosa gradova).</span><span class="sxs-lookup"><span data-stu-id="cfe58-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="cfe58-224">Ako bilo koji nedostaje, pronađite i povežite ispravni cjenik.</span><span class="sxs-lookup"><span data-stu-id="cfe58-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="cfe58-225">Ako je instalirana aplikacija Field Service, idite na **Project Service** > **Postavke** > **Cjenici**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="cfe58-226">Potvrdite jesu li navedene stope naplate i troškova.</span><span class="sxs-lookup"><span data-stu-id="cfe58-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="cfe58-227">Idite na **Field Service** > **Postavke** > **Cjenici** i provjerite jesu li u skupu podataka navedene stope naplate i troškova u odgovarajućoj valuti za svaku zemlju/regiju.</span><span class="sxs-lookup"><span data-stu-id="cfe58-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cfe58-228">![Snimka zaslona aktivnih cjenika](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="cfe58-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="cfe58-229">![Snimka zaslona aktivnih organizacijskih jedinica](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="cfe58-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="cfe58-230">Tehničke napomene</span><span class="sxs-lookup"><span data-stu-id="cfe58-230">Technical notes</span></span>

<span data-ttu-id="cfe58-231">U nastavku potražite više tehničkih podataka o instalaciji ovih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="cfe58-232">Instalacija oglednih podataka preko postojećih podataka (ne preporučuje se)</span><span class="sxs-lookup"><span data-stu-id="cfe58-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="cfe58-233">Ako ogledne podatke morate instalirati preko postojećeg probnog ili demonstracijskog okruženja za Project Service i Field Service koje već sadrži podatke (ne preporučuje se), morat ćete zaustaviti sigurnosne provjere koje izvodi instalacijski program.</span><span class="sxs-lookup"><span data-stu-id="cfe58-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="cfe58-234">Da biste to učinili, u mapi **PkgFolder** pronađite i otvorite datoteku **DemoDataPreImportConfig.xml** u programu Notepad (ili drugom XML uređivaču).</span><span class="sxs-lookup"><span data-stu-id="cfe58-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="cfe58-235">Pronađite sljedeću vrijednost, a zatim promijenite postavku iz true u false:</span><span class="sxs-lookup"><span data-stu-id="cfe58-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="cfe58-236">Zbog te promjene instalacijski program zaobilazi neke važne sigurnosne provjere kojima se između ostalog potvrđuje sljedeće:</span><span class="sxs-lookup"><span data-stu-id="cfe58-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="cfe58-237">aktivan je samo jedan zapis **Organizacijska jedinica** koji je potom potrebno preimenovati u **Fabrikam US**</span><span class="sxs-lookup"><span data-stu-id="cfe58-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="cfe58-238">aktivan je samo jedan zapis **Radni predložak**</span><span class="sxs-lookup"><span data-stu-id="cfe58-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="cfe58-239">aktivan je samo jedan zapis **Projektni parametar** koji je potom potrebno preimenovati u **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="cfe58-240">Komponente konfiguracije</span><span class="sxs-lookup"><span data-stu-id="cfe58-240">Configuration components</span></span>

<span data-ttu-id="cfe58-241">Postoji niz drugih komponenti konfiguracije u ovoj konfiguracijskoj datoteci za preduvoz.</span><span class="sxs-lookup"><span data-stu-id="cfe58-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="cfe58-242">Za tehničke korisnike neke od tih komponenti uključuju sljedeće:</span><span class="sxs-lookup"><span data-stu-id="cfe58-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="cfe58-243">**\<RequiredSolutions\>** navodi preduvjete instalacija rješenja i brojeve njihovih verzija.</span><span class="sxs-lookup"><span data-stu-id="cfe58-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="cfe58-244">**\<InstallSampleData\>** kontrolira jesu li instalirani gotovi ogledni podaci za aplikacije.</span><span class="sxs-lookup"><span data-stu-id="cfe58-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="cfe58-245">false – preskače instalaciju ovih ugrađenih podataka (koji se mogu ukloniti)</span><span class="sxs-lookup"><span data-stu-id="cfe58-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="cfe58-246">true – instalira ugrađene podatke istodobno s instalacijom oglednih podataka za FS i PSA</span><span class="sxs-lookup"><span data-stu-id="cfe58-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="cfe58-247">**\<PreImportDataCollection\>** navodi mape podataka s plošnim podacima i povezane zapise koji će se uvesti prije instalacije glavnih oglednih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="cfe58-248">**\<EntitiesToEnableScheduling\>** navodi koje bi entitete trebalo omogućiti za rezervaciju u sustavu Microsoft Dynamics Scheduling (poznatom i kao Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="cfe58-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="cfe58-249">**\<UsersToCreateAndConfigure\>** navodi resurse koje je moguće rezervirati, a koji će se stvoriti (ako već ne postoje) prije nego što se izvrši uvoz oglednih podataka.</span><span class="sxs-lookup"><span data-stu-id="cfe58-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="cfe58-250">Imajte na umu da se ime i prezime (FullName) i podaci za prijavu svakog resursa (koji se može rezervirati) oglednih podataka izvornog sustava podudaraju s imenom i prezimenom i podacima za prijavu zapisa resursa (koji se može rezervirati) ciljnog sustava.</span><span class="sxs-lookup"><span data-stu-id="cfe58-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="cfe58-251">Stoga NIJE moguće promijeniti nazive u toj predkonfiguracijskoj datoteci, osim ako najprije ne uvezete ogledne podatke u ciljni sustav pomoću tih imena, a zatim preimenujete resurse koje je moguće rezervirati u željeni skup naziva zajedno sa zapisima omogućenog korisnika te potom ponovno izvezete podatke u konačni odredišni sustav (ažurirajući na odgovarajući način stare i nove unose za **ImportUserMapFile.xml**).</span><span class="sxs-lookup"><span data-stu-id="cfe58-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="cfe58-252">**\<PluginsToDisable\>** navodi točne dodatke stavke retka koje je potrebno onemogućiti tijekom uvoza oglednih podataka, a zatim kasnije ponovno omogućiti.</span><span class="sxs-lookup"><span data-stu-id="cfe58-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="cfe58-253">Izmišljeni scenarij za Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="cfe58-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="cfe58-254">Paketi referentnih podataka za Field Service i Project Service instaliraju **rješenje Fabrikam Manufacturing Master Data (v3.0.0.0)** zajedno s približno 4000 zapisa i približno 40 različitih entiteta.</span><span class="sxs-lookup"><span data-stu-id="cfe58-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="cfe58-255">Zasebni paketi oglednih podataka za Field Service ili Project Service sadrži podskup oglednih podataka **v902FPSMasterData** za tu aplikaciju.</span><span class="sxs-lookup"><span data-stu-id="cfe58-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="cfe58-256">Paket **Pokazni podaci** instalira **rješenje Fabrikam Manufacturing Demo Data (v3.0.0.7)** s približno 22.000 zapisa u 148 entiteta.</span><span class="sxs-lookup"><span data-stu-id="cfe58-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="cfe58-257">Izmišljena tvrtka Fabrikam Robotics proizvođač je robota za pokretne trake za sastavljanje elektroničkih uređaja i poznata je po kvaliteti svojih proizvoda, inovacija te dobroj službi za korisnike, uključujući planiranje instalacija, implementaciju i trajne usluge održavanja.</span><span class="sxs-lookup"><span data-stu-id="cfe58-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="cfe58-258">Fabrikam ima sjedište u Sjedinjenim Američkim Državama (Fabrikam US) i projektne servisne operacije u Francuskoj, Indiji, Ujedinjenom Kraljevstvu i Švicarskoj.</span><span class="sxs-lookup"><span data-stu-id="cfe58-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="cfe58-259">Terenske operacije najzastupljenije su u Sjedinjenim Američkim Državama, uglavnom na širem području Seattlea.</span><span class="sxs-lookup"><span data-stu-id="cfe58-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="cfe58-260">Tvrtka nastoji povezivanjem interneta stvari (IoT) pratiti performanse sredstava klijenata i pružati proaktivnije usluge na lokaciji klijenta.</span><span class="sxs-lookup"><span data-stu-id="cfe58-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="cfe58-261">Detaljni pregled oglednih podataka je sljedeći:</span><span class="sxs-lookup"><span data-stu-id="cfe58-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="cfe58-262">uobičajeni elementi oglednih podataka (uključeno za obje aplikacije)</span><span class="sxs-lookup"><span data-stu-id="cfe58-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="cfe58-263">1 korisnik</span><span class="sxs-lookup"><span data-stu-id="cfe58-263">1 user</span></span>

    - <span data-ttu-id="cfe58-264">71 račun</span><span class="sxs-lookup"><span data-stu-id="cfe58-264">71 accounts</span></span>

    - <span data-ttu-id="cfe58-265">137 kontakata</span><span class="sxs-lookup"><span data-stu-id="cfe58-265">137 contacts</span></span>

    - <span data-ttu-id="cfe58-266">različite vrste i kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="cfe58-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="cfe58-267">50 proizvoda s jednim cjenikom</span><span class="sxs-lookup"><span data-stu-id="cfe58-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="cfe58-268">14 cjenika/troškovnika</span><span class="sxs-lookup"><span data-stu-id="cfe58-268">14 price/cost lists</span></span>

    - <span data-ttu-id="cfe58-269">31 karakteristika (vještine resursa) u 2 modela ocjenjivanja s 3 razine (vrijednosti ocjenjivanja)</span><span class="sxs-lookup"><span data-stu-id="cfe58-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="cfe58-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="cfe58-270">Project Service</span></span>

    - <span data-ttu-id="cfe58-271">8 organizacijskih jedinica</span><span class="sxs-lookup"><span data-stu-id="cfe58-271">8 organizational units</span></span>

    - <span data-ttu-id="cfe58-272">6 razina korištenja za određene uloge</span><span class="sxs-lookup"><span data-stu-id="cfe58-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="cfe58-273">više od 2800 specifikacija cijene uloge</span><span class="sxs-lookup"><span data-stu-id="cfe58-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="cfe58-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="cfe58-274">Field Service</span></span>

    - <span data-ttu-id="cfe58-275">4 teritorija</span><span class="sxs-lookup"><span data-stu-id="cfe58-275">4 territories</span></span>

    - <span data-ttu-id="cfe58-276">5 vrsta radnih naloga</span><span class="sxs-lookup"><span data-stu-id="cfe58-276">5 work order types</span></span>

    - <span data-ttu-id="cfe58-277">22 sredstva klijenta</span><span class="sxs-lookup"><span data-stu-id="cfe58-277">22 customer assets</span></span>

    - <span data-ttu-id="cfe58-278">9 vrsta incidenta s rasponom povezanih karakteristika resursa (9), usluga (13) i servisnih zadataka (13)</span><span class="sxs-lookup"><span data-stu-id="cfe58-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="cfe58-279">Paket **Pokazni podaci** instalira približno 179 radnih naloga, 12 projekata i povezane transakcijske podatke.</span><span class="sxs-lookup"><span data-stu-id="cfe58-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="cfe58-280">Promjena radnih sati za ogledne resurse</span><span class="sxs-lookup"><span data-stu-id="cfe58-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="cfe58-281">Prema zadanim postavkama, svi resursi koje je moguće rezervirati imaju kalendar s 24 radna sata.</span><span class="sxs-lookup"><span data-stu-id="cfe58-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="cfe58-282">Ako morate promijeniti radne sate za ogledne resurse koje je moguće rezervirati, idite na **Universal Resource Scheduling** > **Planiranje** > **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="cfe58-283">Odaberite korisnika (na primjer, Spencer Low) i promijenite radne sate za Spencera u sate koje želite primijeniti na više korisnika.</span><span class="sxs-lookup"><span data-stu-id="cfe58-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="cfe58-284">Idite na **Universal Resource Scheduling** > **Postavke** > **Predlošci radnih sati** i uredite zapis **Zadani radni predložak**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="cfe58-285">U polju **Resurs predloška** odaberite korisnika s radnim satima koje želite primijenite na druge resurse.</span><span class="sxs-lookup"><span data-stu-id="cfe58-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="cfe58-286">Idite na **Universal Resource Scheduling** > **Planiranje** > **Resursi** > **Aktivni resursi koje je moguće rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="cfe58-287">Odaberite resurse koje želite promijeniti, a zatim odaberite **Postavi kalendar**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="cfe58-288">Na padajućem popisu **Radni predložak** odaberite predložak **Zadani radni sat** ili drugi predložak s ispravnim resursom predloška.</span><span class="sxs-lookup"><span data-stu-id="cfe58-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="cfe58-289">Kada otvorite ploču s rasporedom, morali biste moći vidjeti da su resursi u međuvremenu ažurirali radne sate.</span><span class="sxs-lookup"><span data-stu-id="cfe58-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="cfe58-290">![Snimka zaslona aktivnih resursa koje je moguće rezervirati](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="cfe58-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
