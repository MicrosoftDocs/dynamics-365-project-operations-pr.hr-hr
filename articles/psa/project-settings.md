---
title: Postavke projekta
description: Ova tema pruža informacije o upravljanju postavkama projekta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 24032a77834005c444972f8d234d3acb33d19135
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998312"
---
# <a name="project-settings"></a><span data-ttu-id="fb7e1-103">Postavke projekta</span><span class="sxs-lookup"><span data-stu-id="fb7e1-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fb7e1-104">Koristite sljedeće postavke da biste pristupili značajkama planiranja projekta.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="fb7e1-105">Poslovni predložak</span><span class="sxs-lookup"><span data-stu-id="fb7e1-105">Work template</span></span>

<span data-ttu-id="fb7e1-106">Da biste stvorili raspored projekta, stvorite predložak kalendara projekta koji definira radno vrijeme po danu i neradno vrijeme.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="fb7e1-107">Da biste stvorili predložak kalendara projekta, povežite radni predložak s poljem **Predložak kalendara** za projekt.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="fb7e1-108">Poduzmite ove korake da biste stvorili radni predložak.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="fb7e1-109">U PSA-u u navigacijskom oknu slijeva kliknite **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="fb7e1-110">Na stranici popisa **Resursi** otvorite zapis korisnika, a zatim odaberite **Prikaži radno vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="fb7e1-111">Provjerite jeste li omogućili skočne prozore na stranici preglednika.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="fb7e1-112">To vam omogućuje da vidite radno vrijeme postavljeno za resurs.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="fb7e1-113">Na kartici **Mjesečni prikaz** kliknite **Postavi**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="fb7e1-114">Prikazat će se popis s tri mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="fb7e1-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="fb7e1-115">Novi tjedni raspored</span><span class="sxs-lookup"><span data-stu-id="fb7e1-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="fb7e1-116">Radni raspored za jedan dan</span><span class="sxs-lookup"><span data-stu-id="fb7e1-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="fb7e1-117">Slobodno vrijeme</span><span class="sxs-lookup"><span data-stu-id="fb7e1-117">Time Off</span></span>

> ![Postavljanje mogućnosti](media/project-13.png)

4. <span data-ttu-id="fb7e1-119">Odaberite **Novi tjedni raspored**, a zatim postavite mogućnosti za ovaj raspored resursa.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="fb7e1-120">Možete postaviti tjedni raspored s ponavljanjem, parametre dnevnih sati, neradno vrijeme itd.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="fb7e1-121">Postavite datumski raspon, odaberite **Spremi**, a zatim kliknite **Zatvori**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="fb7e1-122">Vratite se na stranicu popisa **Resursi** i odaberite resurs za koji ste postavili radno vrijeme.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="fb7e1-123">Odaberite **Postavi kalendar kao** da biste postavili predložak rada.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="fb7e1-124">U dijaloškom okviru **Radni predložak** unesite naziv radnog predloška, a zatim odaberite **Primijeni**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="fb7e1-125">Sada možete povezati predložak rada s predloškom kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="fb7e1-126">Uloge resursa</span><span class="sxs-lookup"><span data-stu-id="fb7e1-126">Resource roles</span></span>

<span data-ttu-id="fb7e1-127">Izraz *uloga resursa* odnosi se na skup vještina, kompetencija i certifikacija koje osoba mora imati za obavljanje određenog skupa zadataka u projektu.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="fb7e1-128">PSA omogućuje određivanje troška i naplate vremena resursa na temelju uloge s kojim je resurs povezan.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="fb7e1-129">Svaka tvrtka ili ustanova mora postaviti te uloge pomoću lijeve navigacijske trake na izborniku **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="fb7e1-130">Svaka tvrtka ili ustanova mora postaviti te uloge na stranici **Kategorije aktivnih resursa**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="fb7e1-131">Da biste otvorili tu stranicu, u lijevom navigacijskom oknu odaberite **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="fb7e1-132">Cjenici</span><span class="sxs-lookup"><span data-stu-id="fb7e1-132">Price lists</span></span>

<span data-ttu-id="fb7e1-133">Cjenici vam omogućuju da odredite trošak i prodajne cijene za uloge resursa u organizaciji, kategorije troškova, proizvode i druge elemente u tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="fb7e1-134">Prije nego što postavite financijske procjene za isporučeni rad u projektu, trebate stvoriti sigurnosni trošak i prodajni cjenik.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="fb7e1-135">U odjeljku parametara također trebate postaviti zadani trošak i prodajni cjenik koji se primjenjuje na sve projekte koji su stvoreni u tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="fb7e1-136">Na stranici **Parametri aktivnog projekta** provjerite jeste li postavili zadani trošak i prodajni cjenik.</span><span class="sxs-lookup"><span data-stu-id="fb7e1-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]