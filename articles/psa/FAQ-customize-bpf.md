---
title: Kako mogu prilagoditi tijek poslovnog procesa faza projekta?
description: Pregled načina na koji je moguće prilagoditi tijek poslovnog procesa faza projekta.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073574"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="66dd6-103">Kako mogu prilagoditi tijek poslovnog procesa faza projekta?</span><span class="sxs-lookup"><span data-stu-id="66dd6-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="66dd6-104">Postoji poznato ograničenje u ranijim verzijama aplikacije Project Service da imena faza u tijeku poslovnog procesa faza projekta moraju biti potpuno jednaka očekivanim engleskim imenima ( **Quote** , **Plan** , **Close** ).</span><span class="sxs-lookup"><span data-stu-id="66dd6-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names ( **Quote** , **Plan** , **Close** ).</span></span> <span data-ttu-id="66dd6-105">U suprotnom poslovna logika koja se oslanja na engleska imena faza neće raditi kako se očekuje.</span><span class="sxs-lookup"><span data-stu-id="66dd6-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="66dd6-106">Zato ne možete vidjeti poznate radnje poput **Zamjena procesa** ili **Uređivanje procesa** dostupne na projektnom obrascu, te se prilagođavanje tijeka poslovnog procesa ne potiče.</span><span class="sxs-lookup"><span data-stu-id="66dd6-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="66dd6-107">Ovo ograničenje navedeno je u verziji 2.4.5.48 i novijim verzijama.</span><span class="sxs-lookup"><span data-stu-id="66dd6-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="66dd6-108">U ovom članku navedena su preporučena zaobilazna rješenja za ranije verzije ako trebate prilagoditi zadani tijek poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="66dd6-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="66dd6-109">Poslovna logika traži točno podudaranje s engleskim imenima faza</span><span class="sxs-lookup"><span data-stu-id="66dd6-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="66dd6-110">Tijek poslovnog procesa faza projekta uključuje poslovnu logiku koja pokreće sljedeća ponašanja u aplikaciji:</span><span class="sxs-lookup"><span data-stu-id="66dd6-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="66dd6-111">Kada se ponuda pridruži projektu, šifra postavlja tijek poslovnog procesa u fazu **Quote**.</span><span class="sxs-lookup"><span data-stu-id="66dd6-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="66dd6-112">Kada se ugovor pridruži projektu, šifra postavlja tijek poslovnog procesa u fazu **Plan**.</span><span class="sxs-lookup"><span data-stu-id="66dd6-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="66dd6-113">Kada tijek poslovnog procesa napreduje do faze **Close** , zapis projekta se deaktivira.</span><span class="sxs-lookup"><span data-stu-id="66dd6-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="66dd6-114">Kada se projekat deaktivira, obrazac projekta i strukturna analiza rada (SAR) postaju samo za čitanje, imenovane rezervacije resursa se poništavaju i bilo kakvi povezani cjenici se deaktiviraju.</span><span class="sxs-lookup"><span data-stu-id="66dd6-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="66dd6-115">Poslovna logika oslanja se na engleske nazive za faze projekta.</span><span class="sxs-lookup"><span data-stu-id="66dd6-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="66dd6-116">To oslanjanje na engleske nazive faza je glavni razlog zašto se ne preporučuje prilagođavanje tijeka poslovnog procesa faza projekta, kao i zašto na entitetu projekta ne možete vidjeti uobičajene radnje tijeka poslovnog procesa, poput **Zamjena procesa** ili **Uređivanje procesa**.</span><span class="sxs-lookup"><span data-stu-id="66dd6-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="66dd6-117">Što će se dogoditi ako se nazivi faza ne podudaraju sa engleskim nazivima?</span><span class="sxs-lookup"><span data-stu-id="66dd6-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="66dd6-118">Kada se nazivi faza u tijeku poslovnog procesa u verziji 1.x aplikacije Project Service na platformi 8.2 ne podudaraju potpuno sa engleskim nazivima faza, poslovna logika koja postavlja ispravnu fazu za ponude ili ugovore ili koja zatvara projekat se preskače.</span><span class="sxs-lookup"><span data-stu-id="66dd6-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="66dd6-119">Ne prikazuju se poruke o pogrešci.</span><span class="sxs-lookup"><span data-stu-id="66dd6-119">No error messages are displayed.</span></span> <span data-ttu-id="66dd6-120">Stoga se čini da možete prilagoditi tijek poslovnog procesa faza projekta.</span><span class="sxs-lookup"><span data-stu-id="66dd6-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="66dd6-121">Međutim, nećete moći vidjeti nikakve automatske procese rada za ponude, ugovore i zatvaranje projekta.</span><span class="sxs-lookup"><span data-stu-id="66dd6-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="66dd6-122">Desila se značajna arhitektonska izmjena tijeka poslovnog procesa u verziji 2.4.4.30 i ranijim verzijama aplikacije Project Service na platformi 9.0, zbog koje je bila potrebna izmjena poslovne logike tijeka poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="66dd6-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="66dd6-123">Zato ćete dobiti poruku o pogrešci ako nazivi faza procesa ne odgovaraju očekivanim engleskim nazivima.</span><span class="sxs-lookup"><span data-stu-id="66dd6-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="66dd6-124">Stoga, ako želite prilagoditi tijek poslovnog procesa faza projekta za entitet projekta možete samo dodati potpuno nove faze zadanom tijeku poslovnog procesa za entitet projekta, a faze **Quote** , **Plan** i **Close** moraju ostati iste.</span><span class="sxs-lookup"><span data-stu-id="66dd6-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote** , **Plan** , and **Close** stages as-is.</span></span> <span data-ttu-id="66dd6-125">Zahvaljujući ovom ograničenju nećete dobiti poruke o pogrešci zbog poslovne logike koja očekuje engleske nazive faza u tijeku poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="66dd6-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="66dd6-126">U verziji 2.4.5.48 ili novijim verzijama poslovna logika opisana u ovom članku uklonjena je iz zadanog tijeka poslovnog procesa za entitet projekta.</span><span class="sxs-lookup"><span data-stu-id="66dd6-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="66dd6-127">Nadogradnja na tu ili noviju verziju omogućit će vam da prilagodite ili zamijenite zadani tijek poslovnog procesa s nekim od svojih.</span><span class="sxs-lookup"><span data-stu-id="66dd6-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="66dd6-128">Zaobilazna rješenja za starije verzije</span><span class="sxs-lookup"><span data-stu-id="66dd6-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="66dd6-129">Ako nemate mogućnost nadogradnje, možete prilagoditi tijek poslovnog procesa faza projekta za entitet projekta na jedan od sljedećih načina:</span><span class="sxs-lookup"><span data-stu-id="66dd6-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="66dd6-130">Dodajte dodatne faze zadanoj konfiguraciji bez mijenjanja engleskih naziva faza za **Quote** , **Plan** i **Close**.</span><span class="sxs-lookup"><span data-stu-id="66dd6-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote** , **Plan** , and **Close**.</span></span>


![Slnimka zaslona dodavanja faza zadanoj konfiguraciji](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="66dd6-132">Stvorite vlastiti tijek poslovnog procesa i učinite ga primarnim tijekom poslovnog procesa za entitet projekta, nakon čega ćete moći imati kakve god želite nazive faza.</span><span class="sxs-lookup"><span data-stu-id="66dd6-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="66dd6-133">Međutim, ako želite koristiti iste standardne faze projekta **Quote** , **Plan** i **Close** , morate odraditi odrađena prilagođavanja radi prilagođenih naziva faza.</span><span class="sxs-lookup"><span data-stu-id="66dd6-133">However, if you want to use the same standard project stages **Quote** , **Plan** , and **Close** , you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="66dd6-134">Složenija logika je u zatvaranju projekta, a možete ju pokrenuti i samim deaktiviranjem zapisa projekta.</span><span class="sxs-lookup"><span data-stu-id="66dd6-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BFP prilagođavanje](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="66dd6-136">Dodatne napomene za verziju 2.4.4.30 ili starije verzije aplikacije Project Service na platformi 9.0</span><span class="sxs-lookup"><span data-stu-id="66dd6-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="66dd6-137">U verziji 2.4.4.30 ili ranijim verzijama aplikacije Project Service na platformi 9.0, s prilagođenim tijekom poslovnog procesa, polje **Naziv faze** u entitetu projekta, korišteno na grafikonu **Projekat po fazi** , i prikazi popisa projekta neće biti ažurirani jer su usklađeni s zadanim tijekom poslovnog procesa faza projekta.</span><span class="sxs-lookup"><span data-stu-id="66dd6-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="66dd6-138">Taj problem možete riješiti na sljedeći način:</span><span class="sxs-lookup"><span data-stu-id="66dd6-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="66dd6-139">Dodajte prilagođeno polje da biste zabilježili trenutnu fazu tijeka poslovnog procesa koja se ažurira dok korisnik napreduje u prilagođeom tijeku poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="66dd6-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="66dd6-140">Izmijenite grafikon **Projekat po fazi** da biste radili s prilagođenim poljem umjesto s zadanom konfiguracijom.</span><span class="sxs-lookup"><span data-stu-id="66dd6-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="66dd6-141">Koraci za stvaranje vlastitog tijeka poslovnog procesa za entitet projekta</span><span class="sxs-lookup"><span data-stu-id="66dd6-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="66dd6-142">Slijedite sljedeće korake da biste stvorili vlastiti tijek poslovnog procesa za entitet projekta:</span><span class="sxs-lookup"><span data-stu-id="66dd6-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="66dd6-143">Idite na **Postavke** > **Procesni centar**.</span><span class="sxs-lookup"><span data-stu-id="66dd6-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="66dd6-144">Nemojte kopirati tijek poslovnog procesa faza projekta jer time ćete kopirati i poslovnu logiku aplikacije Project Service.</span><span class="sxs-lookup"><span data-stu-id="66dd6-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Postupak stvaranja](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="66dd6-146">Koristite dizajnera procesa za stvaranje naziva faza koje želite.</span><span class="sxs-lookup"><span data-stu-id="66dd6-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="66dd6-147">Ako želite iste funkcije koje imaju zadane faze za **Quote** , **Plan** i **Close** , morat ćete to stvoriti na temelju prilagođenih naziva faza tijeka poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="66dd6-147">If you want the same functionality as the default stages for **Quote** , **Plan** , and **Close** , you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Snimka zaslona dizajnera procesa koji se koristi za prilagođavanje BPF-a](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="66dd6-149">U dizajneru procesa kliknite **Narudžba tijeka procesa** da biste prilagođeni tijek poslovnog procesa učinili primarnim tijekom poslovnog procesa za entitet projekta time što ćete ga premjestiti na vrh popisa iznad tijeka poslovnog procesa faza projekta.</span><span class="sxs-lookup"><span data-stu-id="66dd6-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="66dd6-150">Snimka zaslona korištenja narudžbe tijeka procesa</span><span class="sxs-lookup"><span data-stu-id="66dd6-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="66dd6-151">Sljedeći koraci se odnose na verziju 2.4.4.30 ili starije verzije aplikacije Project Service na platformi 9.0</span><span class="sxs-lookup"><span data-stu-id="66dd6-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="66dd6-152">Dodajte novo prilagođeno polje entitetu projekta da biste zabilježili prilagođene faze u prilagođenom poslovnom procesu.</span><span class="sxs-lookup"><span data-stu-id="66dd6-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="66dd6-153">Morat ćete dodati poslovnu logiku (dodatak/tijek rada) da biste ažurirali ovo polje kada ažurirate fazu u prilagođenom tijeku poslovnog procesa.</span><span class="sxs-lookup"><span data-stu-id="66dd6-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Snimka zaslona prilagođavanja entiteta projekta](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="66dd6-155">Izmijenite grafikon **Projekat po fazi** da biste koristili novo prilagođeno polje za faze.</span><span class="sxs-lookup"><span data-stu-id="66dd6-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Snimka zaslona korištenja grafikona projekta po fazi](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="66dd6-157">Izmijenite bilo koje prikaze za entitet projekta da biste uključili novo prilagođeno polje za faze.</span><span class="sxs-lookup"><span data-stu-id="66dd6-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Snimka zaslona mijenjanja prikaza na entitetu projekta](media/FAQ-Customize-BPF-8-720.png)

