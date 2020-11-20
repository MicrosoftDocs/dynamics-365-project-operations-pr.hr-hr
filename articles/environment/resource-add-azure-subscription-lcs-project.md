---
title: Dodavanje pretplate za platformu Azure LCS projektu
description: U ovoj temi nalaze se informacije o načinu povezivanja pretplate za platformu Azure s LCS projektom.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175792"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="1784b-103">Dodavanje pretplate za platformu Azure LCS projektu</span><span class="sxs-lookup"><span data-stu-id="1784b-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="1784b-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="1784b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1784b-105">Okruženja hostirana u oblaku moraju se implementirati s pomoću postojeće pretplate za platformu Azure.</span><span class="sxs-lookup"><span data-stu-id="1784b-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="1784b-106">U ovoj temi pojašnjava se način povezivanja pretplate za platformu Azure s LCS projektom.</span><span class="sxs-lookup"><span data-stu-id="1784b-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="1784b-107">Davanje pristanka administratora</span><span class="sxs-lookup"><span data-stu-id="1784b-107">Grant admin consent</span></span>

1. <span data-ttu-id="1784b-108">U vašem LCS projektu, u odjeljku **Okruženja**, odaberite **Postavke platforme Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="1784b-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Postavke značajke Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="1784b-110">Na stranici **Postavke projekta**, na kartici **Poveznici platforme Azure**, odaberite **Autoriziraj**.</span><span class="sxs-lookup"><span data-stu-id="1784b-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="1784b-111">To omogućuje implementaciju okruženja na ovaj projekt.</span><span class="sxs-lookup"><span data-stu-id="1784b-111">This allows environments to be deployed to this project.</span></span>

![Poveznici platforme Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="1784b-113">Ponovno odaberite **Autoriziraj** kako biste dali pristanak administratora.</span><span class="sxs-lookup"><span data-stu-id="1784b-113">Select **Authorize** again to provide admin consent.</span></span>

![Davanje pristanka administratora](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="1784b-115">Prihvatite zahtjev za dozvolama.</span><span class="sxs-lookup"><span data-stu-id="1784b-115">Accept the permissions request.</span></span>

![Prihvaćanje zahtjeva za dozvolom](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="1784b-117">Sada je autorizacija završena.</span><span class="sxs-lookup"><span data-stu-id="1784b-117">The authorization is now complete.</span></span> 

![Autorizacija je uspješna](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="1784b-119">Omogućivanje pristupa uslugama sustava Dynamics za implementaciju pretplati za platformu Azure</span><span class="sxs-lookup"><span data-stu-id="1784b-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="1784b-120">Idite na odjeljak [Naplata platforme Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i odaberite svoju pretplatu.</span><span class="sxs-lookup"><span data-stu-id="1784b-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="1784b-121">Usluge sustava Dynamics za implementaciju moraju pristupiti ovoj pretplati kako bi se okruženja mogla implementirati.</span><span class="sxs-lookup"><span data-stu-id="1784b-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Pojedinosti o pretplati za platformu Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="1784b-123">Odaberite **Kontrola pristupa (IAM)** u navigacijskom oknu, a zatim odaberite **Dodaj dodjelu uloge**.</span><span class="sxs-lookup"><span data-stu-id="1784b-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="1784b-124">U klizaču s desne strane odaberite **Uloga suradnika** i na navedenom popisu pronađite i odaberite **Usluge sustava Dynamics za implementaciju**.</span><span class="sxs-lookup"><span data-stu-id="1784b-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="1784b-125">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="1784b-125">Select **Save**.</span></span>

![Pretplatnički pristup](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="1784b-127">Dodavanje poveznika pretplate LCS projektu</span><span class="sxs-lookup"><span data-stu-id="1784b-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="1784b-128">U vašem LCS projektu, na stranici **Postavke platforme Microsoft Azure** odaberite **Dodaj** za dodavanje novog poveznika.</span><span class="sxs-lookup"><span data-stu-id="1784b-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="1784b-129">Unesite svoj ID pretplate za platformu Azure.</span><span class="sxs-lookup"><span data-stu-id="1784b-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="1784b-130">Svoj ID pretplate za platformu Azure možete pronaći na [portalu platforme Azure](https://ms.portal.azure.com/), pod stavkom **Postavke** u donjem lijevom dijelu zaslona.</span><span class="sxs-lookup"><span data-stu-id="1784b-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="1784b-131">U polju **Konfiguriraj uporabu usluge Resource Manager za platformu Azure** odaberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="1784b-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="1784b-132">Obvezno provjerite podudara li se pretplatnička domena platforme Azure AAD domena klijenta s Azure pretplatom koja je vlasnik domene koju upotrebljavate i odaberite **Dalje**.</span><span class="sxs-lookup"><span data-stu-id="1784b-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="1784b-133">Na zaslonu **Postavke platforme Microsoft Azure** odaberite **Dalje** za potvrdu.</span><span class="sxs-lookup"><span data-stu-id="1784b-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="1784b-134">Ako se ovom zaslonu prikaže pogreška, vratite se na odjeljak [Omogućivanje uslugama sustava Dynamics za implementaciju pristupa pretplati za platformu Azure](#provide) u ovoj temi i provjerite jeste li izvršili sve korake.</span><span class="sxs-lookup"><span data-stu-id="1784b-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="1784b-135">Preuzmite certifikat platforme Azure za upravljanje u lokalnu mapu na računalu, a zatim ga prenesite na portal platforme Azure za upravljanje tako da odete na **Postavke** > **Certifikati za upravljanje**.</span><span class="sxs-lookup"><span data-stu-id="1784b-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="1784b-136">Ovaj certifikat omogućit će LCS-u da u vaše ime komunicira s platformom Azure.</span><span class="sxs-lookup"><span data-stu-id="1784b-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="1784b-137">Ovaj korak možete preskočiti ako vaš korisnik ima pristup pretplati.</span><span class="sxs-lookup"><span data-stu-id="1784b-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="1784b-138">Odaberite **Dalje**.</span><span class="sxs-lookup"><span data-stu-id="1784b-138">Select  **Next**.</span></span>
8. <span data-ttu-id="1784b-139">Odaberite regiju platforme Azure za implementaciju i odaberite podatkovni centar koji je blizu mjesta na kojem planirate upotrebljavati ovaj sustav.</span><span class="sxs-lookup"><span data-stu-id="1784b-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="1784b-140">Odaberite **Poveži**.</span><span class="sxs-lookup"><span data-stu-id="1784b-140">Select  **Connect**.</span></span>

<span data-ttu-id="1784b-141">Uspješno ste povezali svoju pretplatu za platformu Azure.</span><span class="sxs-lookup"><span data-stu-id="1784b-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="1784b-142">Sada možete implementirati okruženja aplikacije Dynamics 365 Finance u oblaku.</span><span class="sxs-lookup"><span data-stu-id="1784b-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


