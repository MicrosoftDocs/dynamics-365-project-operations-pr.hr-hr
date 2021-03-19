---
title: Po danima
description: U ovoj temi nalaze se informacije o pravilima za dnevnice koja se upotrebljavaju za upravljanje troškovima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276294"
---
# <a name="per-diems"></a><span data-ttu-id="ba4e4-103">Po danima</span><span class="sxs-lookup"><span data-stu-id="ba4e4-103">Per diems</span></span>

<span data-ttu-id="ba4e4-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ba4e4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="ba4e4-105">Dnevnica je naknada koja se isplaćuje radniku koji putuje zbog posla.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="ba4e4-106">U upravljanju troškovima možete stvoriti pravila za dnevnice za različite situacije putovanja.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="ba4e4-107">Cijene dnevnica mogu se temeljiti na dobu godine, mjestu putovanja ili oboje.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="ba4e4-108">Kada stvarate pravilo za dnevnice, možete odrediti da se od dnevnice odbija postotak ako radnik prima besplatne obroke ili usluge.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="ba4e4-109">Također možete postaviti minimalni i maksimalni broj sati za koji se dnevnica može primijeniti kada je radnik na putu.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="ba4e4-110">Konfiguracija</span><span class="sxs-lookup"><span data-stu-id="ba4e4-110">Configuration</span></span> 

1. <span data-ttu-id="ba4e4-111">Kako biste dodali mjesta za dnevnice, idite na **Postavljanje** > **Izračuni i kodovi** > **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="ba4e4-112">Za svaku od gore dodanih lokacija odaberite cijenu dnevnice i valutu koja vrijedi između određenog datuma početka i završetka za hotel, obroke i ostale troškove.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="ba4e4-113">Stope dnevnica i valute konfigurirane su pod stavkom **Postavljanje** > **Izračuni i kodovi** > **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="ba4e4-114">Na stranici **Dnevnice**, konfigurirajte razine dnevnica.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="ba4e4-115">Razine dnevnica omogućuju vam definiranje postotka podjele dnevnice za hotelske, prehrambene i druge troškove.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="ba4e4-116">Kako biste odredili postotak smanjenja za doručak, ručak ili večeru, ažurirajte polja na stranici **Parametri upravljanja troškovima**, na kartici **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="ba4e4-117">Slanje troškova s pomoću dnevnice</span><span class="sxs-lookup"><span data-stu-id="ba4e4-117">Submit expenses using per diem</span></span>
<span data-ttu-id="ba4e4-118">Kako biste poslali troškove korištenja dnevnica, kada stvarate izvješće o troškovima upotrijebite kategoriju troška **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="ba4e4-119">Unesite podatke **Dnevnica od datuma**, **Dnevnica do datuma** i **Dnevnica za mjesto**.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="ba4e4-120">Iznos će se izračunati na temelju iznosa dnevnice za odabranu lokaciju, a smanjenje obroka na temelju razina dnevnica.</span><span class="sxs-lookup"><span data-stu-id="ba4e4-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]