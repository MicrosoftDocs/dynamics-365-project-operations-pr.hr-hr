---
title: Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe
description: U ovoj temi nalaze se informacije o načinu pretplate i implementiranja aplikacije Project Operations za scenarije koji se temelje na resursu / bez zalihe.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948792"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="11c73-103">Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe</span><span class="sxs-lookup"><span data-stu-id="11c73-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="11c73-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="11c73-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="11c73-105">U ovoj temi pojašnjava se način pretplate na pretpregled / ponudu partnera i implementaciju okruženja aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="11c73-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="11c73-106">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="11c73-106">Prerequisites</span></span>

- <span data-ttu-id="11c73-107">Dobit ćete e-poštu s pozivom da sudjelujete u pretpregledu.</span><span class="sxs-lookup"><span data-stu-id="11c73-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="11c73-108">Možete zatražiti pretpregled na [Web-mjestu aplikacije Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="11c73-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="11c73-109">Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.</span><span class="sxs-lookup"><span data-stu-id="11c73-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="11c73-110">Za implementaciju okruženja aplikacije Finance potrebna je valjana pretplata za platformu Azure koja će se naplaćivati po okruženju.</span><span class="sxs-lookup"><span data-stu-id="11c73-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="11c73-111">Kako biste započeli, možete upotrijebiti postojeću pretplatu svoje tvrtke ili ustanove ili [probnu verziju platforme Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="11c73-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="11c73-112">CDS okruženje bit će besplatno za ograničeno razdoblje od 30 dana.</span><span class="sxs-lookup"><span data-stu-id="11c73-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="11c73-113">Pretplata</span><span class="sxs-lookup"><span data-stu-id="11c73-113">Subscribe</span></span>

<span data-ttu-id="11c73-114">Kada se odobri vaš [zahtjeva za pretpregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), e-poštom ćete primiti dvije ponude od tvrtke Microsoft.</span><span class="sxs-lookup"><span data-stu-id="11c73-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="11c73-115">Te ponude omogućuju vam postavljanje pretpregleda aplikacije Project Operations:</span><span class="sxs-lookup"><span data-stu-id="11c73-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="11c73-116">Dynamics 365 Project Operations – Probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="11c73-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="11c73-117">Probni pretpregled aplikacije Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11c73-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11c73-118">Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="11c73-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="11c73-119">Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.</span><span class="sxs-lookup"><span data-stu-id="11c73-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="11c73-120">Dynamics 365 Project Operations – probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="11c73-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="11c73-121">Iskoristite prvu ponudu **Probne aplikacije Dynamics 365 Project Operations** s pomoću URL-adrese navedene u poruci dobrodošlice koju ste dobili e-poštom.</span><span class="sxs-lookup"><span data-stu-id="11c73-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Prva ponuda](./media/1FirstOffer.png)

2. <span data-ttu-id="11c73-123">Provjerite jeste li prijavljeni kao korisnik koji pripada tvrtki ili ustanovi koja će se pretplatiti na uslugu.</span><span class="sxs-lookup"><span data-stu-id="11c73-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="11c73-124">Nastavite s iskorištavanjem ponude.</span><span class="sxs-lookup"><span data-stu-id="11c73-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="11c73-125">Odaberite **Da, dodaj na moj račun**.</span><span class="sxs-lookup"><span data-stu-id="11c73-125">Select **Yes, add it to my account**.</span></span>

![Korištenje ponude](./media/2RedeemFirstOffer.png)

![Potvrda ponude](./media/3ConfirmFirstOffer.png)

![Ponuda iskorištena](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="11c73-129">Probni pretpregled aplikacije Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="11c73-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="11c73-130">Ponovite iste korake s drugom ponudom iz e-pošte dobrodošlice.</span><span class="sxs-lookup"><span data-stu-id="11c73-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="11c73-131">Dodjela licenci</span><span class="sxs-lookup"><span data-stu-id="11c73-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11c73-132">Trebat će vam administrativni pristup portalu sustava Office 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.</span><span class="sxs-lookup"><span data-stu-id="11c73-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="11c73-133">Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.</span><span class="sxs-lookup"><span data-stu-id="11c73-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Administratorski portal aplikacije Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="11c73-135">Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.</span><span class="sxs-lookup"><span data-stu-id="11c73-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Dodjela licenci](./media/6AssignLicenses.png)

3. <span data-ttu-id="11c73-137">Provjerite je li odabrana licenca za aplikaciju Project Operations i odaberite **Spremi promjene**.</span><span class="sxs-lookup"><span data-stu-id="11c73-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="11c73-138">Ponudu za probnu aplikaciju Finance ne treba dodijeliti korisniku.</span><span class="sxs-lookup"><span data-stu-id="11c73-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="11c73-139">Pokretanje novog projekta u LCS-u</span><span class="sxs-lookup"><span data-stu-id="11c73-139">Start a new project in LCS</span></span>

<span data-ttu-id="11c73-140">Stvaranje novog LCS projekta kako je opisano u temi [Pokretanje novog projekta u LCS-u](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="11c73-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="11c73-141">Dodavanje pretplate za platformu Azure LCS projektu</span><span class="sxs-lookup"><span data-stu-id="11c73-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="11c73-142">Kako biste dovršili ovaj zadatak, slijedite korake u temi [Dodavanje pretplate za platformu Azure u LCS projekt](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="11c73-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="11c73-143">Implementiranje pokaznog okruženja aplikacije Finance s aplikacijom Project Operations za scenarije resursa / bez zalihe</span><span class="sxs-lookup"><span data-stu-id="11c73-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="11c73-144">Slijedite smjernice u temi [Dodjela novog okruženja](resource-provision-new-environment.md) kako biste dovršili implementaciju.</span><span class="sxs-lookup"><span data-stu-id="11c73-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="11c73-145">Upotrijebite vrstu implementacije [pokaznog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pretpregled.</span><span class="sxs-lookup"><span data-stu-id="11c73-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="11c73-146">Instalacija postavljanja CDS-a i konfiguracijskih podataka</span><span class="sxs-lookup"><span data-stu-id="11c73-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="11c73-147">Instalirajte podatke o postavljanju i konfiguraciji CDS-a na način opisan u temi [Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="11c73-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

