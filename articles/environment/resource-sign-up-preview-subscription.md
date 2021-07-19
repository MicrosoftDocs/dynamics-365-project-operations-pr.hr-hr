---
title: Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe
description: U ovoj temi nalaze se informacije o načinu pretplate i implementiranja aplikacije Project Operations za scenarije koji se temelje na resursu / bez zalihe.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334818"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="b5fca-103">Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe</span><span class="sxs-lookup"><span data-stu-id="b5fca-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="b5fca-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="b5fca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b5fca-105">U ovoj se temi objašnjava način na koji se vrši pretplata za probnu ponudu i implementacija okruženja aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="b5fca-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5fca-106">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="b5fca-106">Prerequisites</span></span>
- <span data-ttu-id="b5fca-107">Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fca-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="b5fca-108">Klijenta možete stvoriti tijekom iskorištavanja prve ponude.</span><span class="sxs-lookup"><span data-stu-id="b5fca-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="b5fca-109">Za implementaciju okruženja aplikacije Finance potrebna je valjana pretplata za platformu Azure koja će se naplaćivati po okruženju.</span><span class="sxs-lookup"><span data-stu-id="b5fca-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="b5fca-110">Kako biste započeli, možete upotrijebiti postojeću pretplatu svoje tvrtke ili ustanove ili [probnu verziju platforme Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="b5fca-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="b5fca-111">CDS okruženje bit će besplatno za ograničeno razdoblje od 30 dana.</span><span class="sxs-lookup"><span data-stu-id="b5fca-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5fca-112">Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="b5fca-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="b5fca-113">Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.</span><span class="sxs-lookup"><span data-stu-id="b5fca-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="b5fca-114">Probne verzije na klijentu upotrebljavaju se jednokratno.</span><span class="sxs-lookup"><span data-stu-id="b5fca-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="b5fca-115">Probnu verziju možete pokrenuti samo jednom.</span><span class="sxs-lookup"><span data-stu-id="b5fca-115">You can only run a trial one time.</span></span> <span data-ttu-id="b5fca-116">Preporučujemo vam da u svrhu probne verzije stvorite novog klijenta.</span><span class="sxs-lookup"><span data-stu-id="b5fca-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="b5fca-117">Dynamics 365 Project Operations (CE) – Probna verzija pretpregleda</span><span class="sxs-lookup"><span data-stu-id="b5fca-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="b5fca-118">Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b5fca-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="b5fca-119">Iskoristite prvu šifru ponude, **Dynamics 365 Project Operations** ovdje [probna verzija aplikacije Project Operations](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="b5fca-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="b5fca-120">Potvrdite svoj nalog.</span><span class="sxs-lookup"><span data-stu-id="b5fca-120">Confirm your order.</span></span>

  <span data-ttu-id="b5fca-121">Vidjet ćete da je nalog potvrde uspješno iskorišten.</span><span class="sxs-lookup"><span data-stu-id="b5fca-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="b5fca-122">Probni pretpregled aplikacije Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="b5fca-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="b5fca-123">Idite na [Probnu verziju pretpregleda aplikacije Dynamics 365 for Finance](https://aka.ms/trypoche) i ponovite korake iz prethodnog odjeljka s ponudom, prijavite se za okruženje hostirano u oblaku.</span><span class="sxs-lookup"><span data-stu-id="b5fca-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="b5fca-124">Dodjela licenci</span><span class="sxs-lookup"><span data-stu-id="b5fca-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5fca-125">Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.</span><span class="sxs-lookup"><span data-stu-id="b5fca-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="b5fca-126">Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.</span><span class="sxs-lookup"><span data-stu-id="b5fca-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="b5fca-127">Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.</span><span class="sxs-lookup"><span data-stu-id="b5fca-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="b5fca-128">Provjerite je li odabrana licenca **Dynamics 365 Project Operations** i odaberite **Spremi promjene**.</span><span class="sxs-lookup"><span data-stu-id="b5fca-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="b5fca-129">Ponudu za probnu aplikaciju Finance ne treba dodijeliti korisniku.</span><span class="sxs-lookup"><span data-stu-id="b5fca-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="b5fca-130">Pokretanje novog projekta u LCS-u</span><span class="sxs-lookup"><span data-stu-id="b5fca-130">Start a new project in LCS</span></span>

<span data-ttu-id="b5fca-131">Stvaranje novog LCS projekta kako je opisano u temi [Pokretanje novog projekta u LCS-u](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="b5fca-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="b5fca-132">Dodavanje pretplate za platformu Azure LCS projektu</span><span class="sxs-lookup"><span data-stu-id="b5fca-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="b5fca-133">Kako biste dovršili ovaj zadatak, slijedite korake u temi [Dodavanje pretplate za platformu Azure u LCS projekt](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="b5fca-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="b5fca-134">Implementiranje pokaznog okruženja aplikacije Finance s aplikacijom Project Operations za scenarije resursa / bez zalihe</span><span class="sxs-lookup"><span data-stu-id="b5fca-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="b5fca-135">Slijedite smjernice u temi [Dodjela novog okruženja](resource-provision-new-environment.md) kako biste dovršili implementaciju.</span><span class="sxs-lookup"><span data-stu-id="b5fca-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="b5fca-136">Upotrijebite vrstu implementacije [pokaznog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pretpregled.</span><span class="sxs-lookup"><span data-stu-id="b5fca-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="b5fca-137">Instalacija postavljanja CDS-a i konfiguracijskih podataka</span><span class="sxs-lookup"><span data-stu-id="b5fca-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="b5fca-138">Instalirajte podatke o postavljanju i konfiguraciji CDS-a na način opisan u temi [Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="b5fca-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="b5fca-139">Dovršite ovaj korak tek nakon što se implementira pokazna verzija okruženja aplikacije Financije i pokazni podaci budu spremni.</span><span class="sxs-lookup"><span data-stu-id="b5fca-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
