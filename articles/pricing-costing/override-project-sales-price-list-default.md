---
title: Nadjačavanje prodajnih cjenika za projekt
description: U ovoj temi nalaze se informacije o stvaranju prilagođenih prodajnih cjenika.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672222"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="d509e-103">Nadjačavanje prodajnih cjenika za projekt</span><span class="sxs-lookup"><span data-stu-id="d509e-103">Override project sales price lists</span></span>

<span data-ttu-id="d509e-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="d509e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="d509e-105">Cjenici za projekt specifični za klijenta</span><span class="sxs-lookup"><span data-stu-id="d509e-105">Customer-specific project price lists</span></span>

<span data-ttu-id="d509e-106">Ugovori o cijenama specifičnim za klijenta mogu se postaviti kao cjenici projekta na zapisu računa u aplikaciji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d509e-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="d509e-107">Kako biste postavili cjenik projekta specifičan za kupca, u području **Prodaja**, pomaknite se do zapisa računa.</span><span class="sxs-lookup"><span data-stu-id="d509e-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="d509e-108">Otvorite stranicu s popisom **Računi**.</span><span class="sxs-lookup"><span data-stu-id="d509e-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="d509e-109">Pronađite i dvaput kliknite zapis o klijentu kako biste otvorili stranicu s pojedinostima **Računa**.</span><span class="sxs-lookup"><span data-stu-id="d509e-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="d509e-110">Na kartici **Cjenici za projekt** odaberite **+ Novi cjenik za projekt**.</span><span class="sxs-lookup"><span data-stu-id="d509e-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="d509e-111">Na stranici **Novi cjenik za projekt**, s padajućeg izbornika odaberite cjenik.</span><span class="sxs-lookup"><span data-stu-id="d509e-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="d509e-112">Samo cjenici kojima je kontekst postavljen na **Prodaja** i čija se valuta podudara s valutom računa.</span><span class="sxs-lookup"><span data-stu-id="d509e-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="d509e-113">Ime i veza, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="d509e-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="d509e-114">Stvoren je cjenik za projekt specifičan za klijenta.</span><span class="sxs-lookup"><span data-stu-id="d509e-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="d509e-115">Ovaj će se cjenik upotrebljavati za zadavanje cijena za projekt na ponudama projekta ili ugovorima o projektu stvorenim za ovog klijenta ako datum stvaranja ponude ili ugovora o projektu pada unutar datuma kada je cjenik na snazi.</span><span class="sxs-lookup"><span data-stu-id="d509e-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="d509e-116">Prilagođene cijene za ponude projekta</span><span class="sxs-lookup"><span data-stu-id="d509e-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="d509e-117">Na ponudama projekta možete imati cijene za projekt koje započinju sa zadanim standardnim cjenikom koji zadaje klijent ili parametri projekta.</span><span class="sxs-lookup"><span data-stu-id="d509e-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="d509e-118">Kada su vam potrebne prilagođene cijene za radove povezane s projektom na određenoj ponudi, to možete dobiti iz entiteta povezanog s cjenicima za projekt.</span><span class="sxs-lookup"><span data-stu-id="d509e-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="d509e-119">Dovršite sljedeće korake za postavljanje cijena projekata specifičnih za ponudu.</span><span class="sxs-lookup"><span data-stu-id="d509e-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="d509e-120">Otvorite ponudu projekta i odaberite karticu **Cjenici za projekt**.</span><span class="sxs-lookup"><span data-stu-id="d509e-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="d509e-121">U podrešetki odaberite **Stvori prilagođene cijene**.</span><span class="sxs-lookup"><span data-stu-id="d509e-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="d509e-122">Svi cjenici za projekt koji su priloženi uz ponudu, kopiraju se u nove cjenike.</span><span class="sxs-lookup"><span data-stu-id="d509e-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="d509e-123">Nazivi novih cjenika odražavaju naziv ponude s oznakom datuma i vremena kada su ti cjenici stvoreni.</span><span class="sxs-lookup"><span data-stu-id="d509e-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="d509e-124">Možete upotrijebiti svaki od tih cjenika i ažurirati cijene rada (cijena uloge) i troškova (cijena kategorije).</span><span class="sxs-lookup"><span data-stu-id="d509e-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="d509e-125">Ove cijene primjenjivat će se samo na ovu ponudu projekta.</span><span class="sxs-lookup"><span data-stu-id="d509e-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="d509e-126">Cjenici u ugovoru o projektu</span><span class="sxs-lookup"><span data-stu-id="d509e-126">Price lists on a project contract</span></span>

<span data-ttu-id="d509e-127">Na ugovoru o projektu, cijene za projekt uvijek su zadane kao prilagođeni cjenik s nazivom ugovora i stvorenom oznakom datuma i vremena koja se dodaje nazivu.</span><span class="sxs-lookup"><span data-stu-id="d509e-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="d509e-128">To vrijedi bez obzira je li ugovor stvoren kada je prihvaćena ponuda ili je ugovor stvoren od početka.</span><span class="sxs-lookup"><span data-stu-id="d509e-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="d509e-129">Ako je potrebno, možete ukloniti ovu povezanost s prilagođenim cjenikom i umjesto toga s ugovorom o projektu povezati standardni cjenik.</span><span class="sxs-lookup"><span data-stu-id="d509e-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="d509e-130">Kada standardni cjenik povežete s projektnim cjenicima na ponudi ili ugovoru, sve promjene cijena u cjeniku utjecat će na sve ponude i ugovore koji upotrebljavaju cjenik.</span><span class="sxs-lookup"><span data-stu-id="d509e-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
