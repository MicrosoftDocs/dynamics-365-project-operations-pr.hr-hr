---
title: Prijava za pretplatu na pretpregled – jednostavno
description: U ovoj temi nalaze se informacije o načinu pretplate i implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290035"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="585e3-103">Prijava za pretplatu na pretpregled – jednostavno</span><span class="sxs-lookup"><span data-stu-id="585e3-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="585e3-104">U ovoj temi objašnjava se način za pretplatu na pretpregled ponude partnera i implementaciju osnovne aplikacije Dynamics 365 Project Operations – od sklapanja posla do predračuna.</span><span class="sxs-lookup"><span data-stu-id="585e3-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="585e3-105">Ovaj će se postupak promijeniti u predstojećim izdanjima aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="585e3-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="585e3-106">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="585e3-106">Prerequisites</span></span>

- <span data-ttu-id="585e3-107">Dobit ćete e-poštu s pozivom da sudjelujete u pretpregledu.</span><span class="sxs-lookup"><span data-stu-id="585e3-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="585e3-108">Možete zatražiti pretpregled na [Web-mjestu aplikacije Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="585e3-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="585e3-109">Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.</span><span class="sxs-lookup"><span data-stu-id="585e3-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="585e3-110">Pregledajte sve uvjete i odredbe.</span><span class="sxs-lookup"><span data-stu-id="585e3-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="585e3-111">Pretplata</span><span class="sxs-lookup"><span data-stu-id="585e3-111">Subscribe</span></span>

<span data-ttu-id="585e3-112">Kada primite odobrenje [zahtjeva za pretpregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), e-poštom ćete primiti dvije ponude od tvrtke Microsoft.</span><span class="sxs-lookup"><span data-stu-id="585e3-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="585e3-113">Te ponude omogućuju vam postavljanje pretpregleda aplikacije Project Operations:</span><span class="sxs-lookup"><span data-stu-id="585e3-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="585e3-114">Dynamics 365 Project Operations (CRM) – probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="585e3-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="585e3-115">Office 365 Project Operations –Probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="585e3-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="585e3-116">Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="585e3-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="585e3-117">Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.</span><span class="sxs-lookup"><span data-stu-id="585e3-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="585e3-118">Dynamics 365 Project Operations (CRM) – probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="585e3-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="585e3-119">Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="585e3-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="585e3-120">Iskoristite kod prve ponude, **Dynamics 365 Project Operations (CRM) – Pretpregled probe** tako da ga zalijepite na URL-adresu preglednika.</span><span class="sxs-lookup"><span data-stu-id="585e3-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Korištenje ponude](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="585e3-122">Potvrdite svoj nalog.</span><span class="sxs-lookup"><span data-stu-id="585e3-122">Confirm your order.</span></span>
<span data-ttu-id="585e3-123">![Potvrda naloga](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="585e3-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="585e3-124">Vidjet ćete da je nalog potvrde uspješno iskorišten.</span><span class="sxs-lookup"><span data-stu-id="585e3-124">You'll see confirmation offer was successfully redeemed.</span></span>

![Potvrda](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="585e3-126">Office 365 Project Operations –Probni pretpregled</span><span class="sxs-lookup"><span data-stu-id="585e3-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="585e3-127">Ponovite iste korake kao i s prvim kodom ponude.</span><span class="sxs-lookup"><span data-stu-id="585e3-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="585e3-128">Obvezno dodajte kod iz druge ponude s pomoću istog korisničkog računa koji je upotrebljavan s kodom iz prve ponude.</span><span class="sxs-lookup"><span data-stu-id="585e3-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="585e3-129">Dodjela licenci</span><span class="sxs-lookup"><span data-stu-id="585e3-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="585e3-130">Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.</span><span class="sxs-lookup"><span data-stu-id="585e3-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="585e3-131">Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.</span><span class="sxs-lookup"><span data-stu-id="585e3-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Početna stranica Centra za administratore](./media/14AdminPortal.png)

2. <span data-ttu-id="585e3-133">Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.</span><span class="sxs-lookup"><span data-stu-id="585e3-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Dodjela licenci](./media/15AssignLicenses.png)

3. <span data-ttu-id="585e3-135">Provjerite jesu li odabrane licence za **Pretpregled aplikacije Dynamics 365 Project Operations (CRM)** i **Office 365 Project Operations – pretpregled**.</span><span class="sxs-lookup"><span data-stu-id="585e3-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="585e3-136">Odaberite **Spremi promjene**.</span><span class="sxs-lookup"><span data-stu-id="585e3-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="585e3-137">Stvaranje novog CDS okruženja</span><span class="sxs-lookup"><span data-stu-id="585e3-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="585e3-138">Pripremite novo okruženje za implementaciju CDS-a aplikacije Project Operations slijedeći upute u temi [Model implementacije CDS-a](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="585e3-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="585e3-139">Kad odaberete vrstu okruženja, obvezno upotrijebite **Probno razdoblje (na temelju pretplate)**.</span><span class="sxs-lookup"><span data-stu-id="585e3-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="585e3-140">![Novo okruženje](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="585e3-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="585e3-141">Odaberite postavku **Omogući aplikacije sustava Dynamics 365** i mogućnost **Automatski postavi ove aplikacije** ostavite praznu.</span><span class="sxs-lookup"><span data-stu-id="585e3-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="585e3-142">Odaberite **Spremi** kako biste stvorili okruženje.</span><span class="sxs-lookup"><span data-stu-id="585e3-142">Select **Save** to create the environment.</span></span>

![Dodaj bazu podataka](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="585e3-144">Nakon stvaranja okruženja, instalirajte rješenje **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="585e3-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalacija rješenja](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="585e3-146">Instaliranje CDS konfiguracije i postavljanje pokaznih podataka</span><span class="sxs-lookup"><span data-stu-id="585e3-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="585e3-147">Instalirajte CDS konfiguraciju i postavite pokazne podatke slijedeći upute u temi [Primjena pokaznih postavki i konfiguracijskih podataka](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="585e3-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]