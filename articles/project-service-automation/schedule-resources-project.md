---
title: Zakažite resurse za projekt
description: Zakazivanje resursa za projekt u programu Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750198"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="f36d9-103">Zakazivanje resursa za projekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f36d9-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f36d9-104">Moguća je provjera raspoloživosti resursa da biste dobili opći pregled o tome koliko su rezervirani resursi ili možete filtrirati prikaze po vještinama, timu, lokacijama i drugim mogućnostima.</span><span class="sxs-lookup"><span data-stu-id="f36d9-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="f36d9-105">Ploča s rasporedom prikazuje popis resursa i njihovu raspoloživost.</span><span class="sxs-lookup"><span data-stu-id="f36d9-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="f36d9-106">Odaberite način prikaza za prikaz raspoloživosti po **Satima**, **Danu**, **Tjednu**, ili **Mjesecu**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="f36d9-107">Prije nego što koristite raspored, važno je da ga postavite.</span><span class="sxs-lookup"><span data-stu-id="f36d9-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="f36d9-108">Dodatne informacije potražite u članku [Konfiguriranje ploče rasporeda (Field Service, Project Service Automation)](../field-service/configure-schedule-board.md).</span><span class="sxs-lookup"><span data-stu-id="f36d9-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](../field-service/configure-schedule-board.md).</span></span>
  
<span data-ttu-id="f36d9-109">Ako koristite stariju verziju, za dostupnost resursa pogledajte članak [Prikaz dostupnosti resursa](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="f36d9-109">If you are using an older version, for resource availability, see [View resource availability](../project-service/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="f36d9-110">Da biste upotrebljavali funkcije rezervacija ploče s rasporedom, geokodiranje i usluge lokacije, trebate uključiti karte.</span><span class="sxs-lookup"><span data-stu-id="f36d9-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="f36d9-111">Na glavnom izborniku odaberite mogućnost **Zakazivanje resursa** > **Administracija**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="f36d9-112">Kliknite **Parametri zakazivanja**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="f36d9-113">Otvorite zapis i pomaknite se prema dolje do odjeljka **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="f36d9-114">U polju **Povezivanje s kartama** odaberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="f36d9-115">Prihvatite uvjete i spremite zapis.</span><span class="sxs-lookup"><span data-stu-id="f36d9-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="f36d9-116">Na glavnom izborniku odaberite mogućnost **Project Service** > **Ploča s rasporedom**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="f36d9-117">Postoji nekoliko različitih načina da biste ručno zakazali zahtjev za rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="f36d9-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="f36d9-118">Odaberite metodu koja radi za vas.</span><span class="sxs-lookup"><span data-stu-id="f36d9-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="f36d9-119">Traženje dostupnih resursa</span><span class="sxs-lookup"><span data-stu-id="f36d9-119">Find available resources</span></span>

1.  <span data-ttu-id="f36d9-120">Na popisu **Rezervacija zahtjeva** desnom tipkom miša kliknite nezakazanu rezervaciju i odaberite nešto od sljedećeg:</span><span class="sxs-lookup"><span data-stu-id="f36d9-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="f36d9-121">Odaberite **Pronađi dostupnost – trenutačni resursi**da biste pronašli dostupan resurs na popisu resursa na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="f36d9-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="f36d9-122">Odaberite **Pronađi dostupnost – Svi resursi** da biste pronašli dostupan resurs među resursima u sustavu.</span><span class="sxs-lookup"><span data-stu-id="f36d9-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="f36d9-123">Kada to učinite, filtri će prikazati mogućnosti odabranog zahtjeva rezervacije.</span><span class="sxs-lookup"><span data-stu-id="f36d9-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="f36d9-124">Kada se pojavi dostupan termin, desnom tipkom miša kliknite vremensko razdoblje na ploči s rasporedom, a zatim odaberite mogućnost **Rezerviraj ovdje**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="f36d9-125">Možete i povući i ispustiti rezervaciju u dostupan termin.</span><span class="sxs-lookup"><span data-stu-id="f36d9-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="f36d9-126">Rezervirajte resurs pomoću dnevnog prikaza i saznajte tko je nedovoljno rezerviran</span><span class="sxs-lookup"><span data-stu-id="f36d9-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="f36d9-127">Na ploči rasporeda odaberite mogućnost **Način prikaza** i odaberite stavku **Dani**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="f36d9-128">Prikazuje prikaz rešetke s brojem radnih sati koliko je resurs rezerviran po danu i koji dani su slobodni.</span><span class="sxs-lookup"><span data-stu-id="f36d9-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="f36d9-129">Kliknite naziv resursa koji želite rezervirati, a zatim odaberite mogućnost **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="f36d9-130">Na dijaloškom okviru **Rezervacija resursa (stvori)** odaberite projekt za koji želite rezervirati resurs i način rezervacije i termine početka i kraja.</span><span class="sxs-lookup"><span data-stu-id="f36d9-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="f36d9-131">Kada završite, odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="f36d9-132">Pogled na ploču s rasporedom</span><span class="sxs-lookup"><span data-stu-id="f36d9-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="f36d9-133">Odaberite nezakazani zahtjev za rezervaciju s popisa na dnu.</span><span class="sxs-lookup"><span data-stu-id="f36d9-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="f36d9-134">Povucite preduvjet za rezervaciju na dostupni resurs/termin za raspored na ploču s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="f36d9-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="f36d9-135">Kada završite, odaberite mogućnost **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="f36d9-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="f36d9-136">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="f36d9-136">Additional resources</span></span>  
 [<span data-ttu-id="f36d9-137">Vodič za upravitelje resursa</span><span class="sxs-lookup"><span data-stu-id="f36d9-137">Resource manager guide</span></span>](../project-service/resource-manager-guide.md)
