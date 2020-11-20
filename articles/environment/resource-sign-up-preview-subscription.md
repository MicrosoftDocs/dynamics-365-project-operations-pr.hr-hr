---
title: Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe
description: U ovoj temi nalaze se informacije o načinu pretplate i implementiranja aplikacije Project Operations za scenarije koji se temelje na resursu / bez zalihe.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dc3b353f19b915f645aed91dc2a8127117027034
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121119"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="ec06b-103">Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe</span><span class="sxs-lookup"><span data-stu-id="ec06b-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="ec06b-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ec06b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ec06b-105">U ovoj temi pojašnjava se način pretplate na pretpregled / ponudu partnera i implementaciju okruženja aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="ec06b-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ec06b-106">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="ec06b-106">Prerequisites</span></span>

- <span data-ttu-id="ec06b-107">Dobit ćete e-poštu s pozivom da sudjelujete u pretpregledu.</span><span class="sxs-lookup"><span data-stu-id="ec06b-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="ec06b-108">Možete zatražiti pretpregled na [Web-mjestu aplikacije Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="ec06b-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="ec06b-109">Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.</span><span class="sxs-lookup"><span data-stu-id="ec06b-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="ec06b-110">Za implementaciju okruženja aplikacije Finance potrebna je valjana pretplata za platformu Azure koja će se naplaćivati po okruženju.</span><span class="sxs-lookup"><span data-stu-id="ec06b-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="ec06b-111">Kako biste započeli, možete upotrijebiti postojeću pretplatu svoje tvrtke ili ustanove ili [probnu verziju platforme Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="ec06b-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="ec06b-112">CDS okruženje bit će besplatno za ograničeno razdoblje od 30 dana.</span><span class="sxs-lookup"><span data-stu-id="ec06b-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="ec06b-113">Pretplata</span><span class="sxs-lookup"><span data-stu-id="ec06b-113">Subscribe</span></span>

<span data-ttu-id="ec06b-114">Kada se odobri vaš [zahtjeva za pretpregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), e-poštom ćete primiti tri ponude od tvrtke Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec06b-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="ec06b-115">Te ponude omogućuju vam postavljanje pretpregleda aplikacije Project Operations:</span><span class="sxs-lookup"><span data-stu-id="ec06b-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="ec06b-116">Dynamics 365 Project Operations (CRM) – Probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="ec06b-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="ec06b-117">Office 365 Project Operations –Probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="ec06b-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="ec06b-118">Probni pretpregled – Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ec06b-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec06b-119">Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="ec06b-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="ec06b-120">Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.</span><span class="sxs-lookup"><span data-stu-id="ec06b-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="ec06b-121">Dynamics 365 Project Operations (CRM) – Probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="ec06b-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="ec06b-122">Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ec06b-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="ec06b-123">Iskoristite kod iz prvu ponude, **Dynamics 365 Project Operations (CRM) – Probni pretpregled** tako da ga zalijepite u URL-adresu preglednika.</span><span class="sxs-lookup"><span data-stu-id="ec06b-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Korištenje ponude](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="ec06b-125">Potvrdite svoj nalog.</span><span class="sxs-lookup"><span data-stu-id="ec06b-125">Confirm your order.</span></span>

![Potvrda naloga](./media/17ConfirmOrderNew.png)

<span data-ttu-id="ec06b-127">Vidjet ćete da je nalog potvrde uspješno iskorišten.</span><span class="sxs-lookup"><span data-stu-id="ec06b-127">You will see confirmation offer was successfully redeemed.</span></span>

![Potvrda](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="ec06b-129">Office 365 Project Operations –Probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="ec06b-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="ec06b-130">Ponovite iste korake kao i s prvim kodom ponude.</span><span class="sxs-lookup"><span data-stu-id="ec06b-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="ec06b-131">Obvezno dodajte kod iz druge ponude s pomoću istog korisničkog računa koji je upotrebljavan s kodom iz prve ponude.</span><span class="sxs-lookup"><span data-stu-id="ec06b-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="ec06b-132">Probni pretpregled aplikacije Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ec06b-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="ec06b-133">Ponovite iste korake s posljednjom ponudom iz e-pošte dobrodošlice.</span><span class="sxs-lookup"><span data-stu-id="ec06b-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="ec06b-134">Dodjela licenci</span><span class="sxs-lookup"><span data-stu-id="ec06b-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec06b-135">Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.</span><span class="sxs-lookup"><span data-stu-id="ec06b-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="ec06b-136">Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.</span><span class="sxs-lookup"><span data-stu-id="ec06b-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Početna stranica Centra za administratore](./media/14AdminPortal.png)

2. <span data-ttu-id="ec06b-138">Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.</span><span class="sxs-lookup"><span data-stu-id="ec06b-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Dodjela licenci](./media/15AssignLicenses.png)

3. <span data-ttu-id="ec06b-140">Provjerite jesu li odabrane licence **Pretpregled aplikacije Dynamics 365 Project Operations (CRM)** i **Office 365 Project Operations – Pretpregled** i odaberite **Spremi promjene**.</span><span class="sxs-lookup"><span data-stu-id="ec06b-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="ec06b-141">Ponudu za probnu aplikaciju Finance ne treba dodijeliti korisniku.</span><span class="sxs-lookup"><span data-stu-id="ec06b-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="ec06b-142">Pokretanje novog projekta u LCS-u</span><span class="sxs-lookup"><span data-stu-id="ec06b-142">Start a new project in LCS</span></span>

<span data-ttu-id="ec06b-143">Stvaranje novog LCS projekta kako je opisano u temi [Pokretanje novog projekta u LCS-u](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="ec06b-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="ec06b-144">Dodavanje pretplate za platformu Azure LCS projektu</span><span class="sxs-lookup"><span data-stu-id="ec06b-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="ec06b-145">Kako biste dovršili ovaj zadatak, slijedite korake u temi [Dodavanje pretplate za platformu Azure u LCS projekt](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="ec06b-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="ec06b-146">Implementiranje pokaznog okruženja aplikacije Finance s aplikacijom Project Operations za scenarije resursa / bez zalihe</span><span class="sxs-lookup"><span data-stu-id="ec06b-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="ec06b-147">Slijedite smjernice u temi [Dodjela novog okruženja](resource-provision-new-environment.md) kako biste dovršili implementaciju.</span><span class="sxs-lookup"><span data-stu-id="ec06b-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="ec06b-148">Upotrijebite vrstu implementacije [pokaznog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pretpregled.</span><span class="sxs-lookup"><span data-stu-id="ec06b-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="ec06b-149">Instalacija postavljanja CDS-a i konfiguracijskih podataka</span><span class="sxs-lookup"><span data-stu-id="ec06b-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="ec06b-150">Instalirajte podatke o postavljanju i konfiguraciji CDS-a na način opisan u temi [Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="ec06b-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="ec06b-151">Dovršite ovaj korak tek nakon što se implementira pokazna verzija okruženja aplikacije Finance i budu spremni pokazni podaci u FO.</span><span class="sxs-lookup"><span data-stu-id="ec06b-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>
