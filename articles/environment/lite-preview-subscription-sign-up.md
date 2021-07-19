---
title: Prijava za pretplatu na pretpregled – jednostavno
description: U ovoj temi nalaze se informacije o načinu pretplate i implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334773"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="85a68-103">Prijavite se za pretplatu na pretpregled – osnovno</span><span class="sxs-lookup"><span data-stu-id="85a68-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="85a68-104">U ovoj se temi objašnjava način na koji se vrši pretplata na probnu ponudu i implementacija osnovne verzije aplikacije Dynamics 365 Project Operations – od sklapanja posla do predračuna.</span><span class="sxs-lookup"><span data-stu-id="85a68-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="85a68-105">Ovaj će se postupak promijeniti u predstojećim izdanjima aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="85a68-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="85a68-106">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="85a68-106">Prerequisites</span></span>
- <span data-ttu-id="85a68-107">Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.</span><span class="sxs-lookup"><span data-stu-id="85a68-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="85a68-108">Klijenta možete stvoriti tijekom iskorištavanja prve ponude.</span><span class="sxs-lookup"><span data-stu-id="85a68-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85a68-109">Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="85a68-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="85a68-110">Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.</span><span class="sxs-lookup"><span data-stu-id="85a68-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="85a68-111">Probne verzije na klijentu upotrebljavaju se jednokratno.</span><span class="sxs-lookup"><span data-stu-id="85a68-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="85a68-112">Probnu verziju možete pokrenuti samo jednom.</span><span class="sxs-lookup"><span data-stu-id="85a68-112">You can only run a trial one time.</span></span> <span data-ttu-id="85a68-113">Preporučujemo vam da u svrhu probne verzije stvorite novog klijenta.</span><span class="sxs-lookup"><span data-stu-id="85a68-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="85a68-114">Probna verzija usluge Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="85a68-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="85a68-115">Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="85a68-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="85a68-116">Idite na [Probnu verziju aplikacije Project Operations](https://aka.ms/try-po) kako biste iskoristili kôd prve ponude, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="85a68-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="85a68-117">Potvrdite svoj nalog.</span><span class="sxs-lookup"><span data-stu-id="85a68-117">Confirm your order.</span></span>

  <span data-ttu-id="85a68-118">Vidjet ćete da je ponuda o potvrdi uspješno iskorištena.</span><span class="sxs-lookup"><span data-stu-id="85a68-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="85a68-119">Dodjela licenci</span><span class="sxs-lookup"><span data-stu-id="85a68-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85a68-120">Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.</span><span class="sxs-lookup"><span data-stu-id="85a68-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="85a68-121">Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.</span><span class="sxs-lookup"><span data-stu-id="85a68-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="85a68-122">Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.</span><span class="sxs-lookup"><span data-stu-id="85a68-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="85a68-123">Provjerite je li odabrana licenca **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="85a68-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="85a68-124">Odaberite **Spremi promjene**.</span><span class="sxs-lookup"><span data-stu-id="85a68-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="85a68-125">Izrada novog okruženja usluge Dataverse</span><span class="sxs-lookup"><span data-stu-id="85a68-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="85a68-126">Pripremite novo okruženje za implementaciju aplikacije Project Operations Dataverse slijedeći upute u temi, [Model implementacije aplikacije Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="85a68-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="85a68-127">Kad odaberete vrstu okruženja, obvezno upotrijebite **Probno razdoblje (na temelju pretplate)**.</span><span class="sxs-lookup"><span data-stu-id="85a68-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Novo okruženje](./media/19CreateEnvironment.png)

2. <span data-ttu-id="85a68-129">Odaberite postavku **Omogući aplikacije sustava Dynamics 365** i mogućnost **Automatski postavi ove aplikacije** ostavite praznu.</span><span class="sxs-lookup"><span data-stu-id="85a68-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="85a68-130">Odaberite **Spremi** kako biste stvorili okruženje.</span><span class="sxs-lookup"><span data-stu-id="85a68-130">Select **Save** to create the environment.</span></span>

  ![Dodaj bazu podataka](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="85a68-132">Nakon stvaranja okruženja, instalirajte rješenje **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="85a68-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalacija rješenja](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="85a68-134">Instaliranje CDS konfiguracije i postavljanje pokaznih podataka</span><span class="sxs-lookup"><span data-stu-id="85a68-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="85a68-135">Instalirajte CDS konfiguraciju i postavite pokazne podatke slijedeći upute u temi [Primjena pokaznih postavki i konfiguracijskih podataka](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="85a68-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
