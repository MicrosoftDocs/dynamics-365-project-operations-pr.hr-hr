---
title: Pregled zaostalih faktura u projektima i ugovorima o projektima
description: Ovaj tema pruža informacije o tome kako pregledati vrijeme, trošak i zaostale podatke o proizvodu te kako ih označiti kao spremne za fakturiranje.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073597"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="933dd-103">Pregled zaostalih faktura u projektima i ugovorima o projektima</span><span class="sxs-lookup"><span data-stu-id="933dd-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="933dd-104">Kada je transakcija spremna za izradu i obradu fakture, transakcija bi trebala imati oznaku **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="933dd-105">Ovaj tema opisuje vrste transakcija koje se mogu izraditi.</span><span class="sxs-lookup"><span data-stu-id="933dd-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="933dd-106">Pregled zaostale naplate za vrijeme i materijal</span><span class="sxs-lookup"><span data-stu-id="933dd-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="933dd-107">Kada je Unos vremena ili troška poslan i odobren za projekt, PSA stvara stvarni podatak projekta.</span><span class="sxs-lookup"><span data-stu-id="933dd-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="933dd-108">Ako je kombinacija projekta i vrste transakcije preslikana u redak ugovora za projekt vremena i materijala, kad se unos odobri, nastaju dva stvarna podatka:</span><span class="sxs-lookup"><span data-stu-id="933dd-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="933dd-109">Stvarni podatak o trošku</span><span class="sxs-lookup"><span data-stu-id="933dd-109">Cost actual</span></span> 
- <span data-ttu-id="933dd-110">Stvarni podatak o nenaplaćenim prodajama</span><span class="sxs-lookup"><span data-stu-id="933dd-110">Unbilled sales actual</span></span>

<span data-ttu-id="933dd-111">Stvarni podaci o nenaplaćenim prodajama predstavljaju zaostale naplate, a njihov status naplate mora biti postavljen na **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="933dd-112">Kada se izradi faktura projekta, stvarni podaci o nenaplaćenim prodajama koji su označeni **Spremno za fakturiranje** kopiraju se kao pojedinosti retka fakture.</span><span class="sxs-lookup"><span data-stu-id="933dd-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="933dd-113">Da biste pregledali zaostale naplate za vrijeme i materijale, otvorite **Prodaja** \> **Naplata** \> **Zaostale naplate za vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="933dd-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="933dd-114">Odaberite sve nenaplaćene stvarne podatke o prodaji koji su spremni za fakturiranje, a zatim odaberite **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="933dd-115">Status naplate tih stvarnih podataka mijenja se u **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Zaostale naplate za vrijeme i materijal](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="933dd-117">Pregled zaostalih naplata za proizvod</span><span class="sxs-lookup"><span data-stu-id="933dd-117">Review the product billing backlog</span></span>

<span data-ttu-id="933dd-118">Kada ugovor o projektu ima retke ugovora temeljene na proizvodu, ti se reci uzimaju u obzir za fakturiranje kad god se izradi faktura za ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="933dd-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="933dd-119">Svaki proizvod koji ima retke ugovora koji su označeni sa **Spremno za fakturiranje** kopira se u fakturu projekta u obliku redaka fakture projekta.</span><span class="sxs-lookup"><span data-stu-id="933dd-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="933dd-120">Da biste pregledali zaostale naplate za proizvode, otvorite **Prodaja** \> **Naplata** \> **Zaostale naplate za proizvod**.</span><span class="sxs-lookup"><span data-stu-id="933dd-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="933dd-121">Odaberite sve retke ugovora temeljene na proizvodu koji su spremni za fakturiranje, a zatim odaberite **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="933dd-122">Status naplate tih redaka mijenja se u **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Zaostale naplate za proizvod](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="933dd-124">Pregled kontrolnih točaka naplate u ugovorima s fiksnom cijenom</span><span class="sxs-lookup"><span data-stu-id="933dd-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="933dd-125">Svaki redak ugovora o projektu koji ima način naplate s fiksnom cijenom mora imati kontrolne točke ugovora.</span><span class="sxs-lookup"><span data-stu-id="933dd-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="933dd-126">Te Kontrolne točke ugovora mogu se fakturirati samo ako imaju oznaku **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="933dd-127">Da biste pregledali kontrolne točke naplate, otvorite **Prodaja** \> **Naplata** \> **Kontrolne točke fiksne cijene**.</span><span class="sxs-lookup"><span data-stu-id="933dd-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="933dd-128">Odaberite kontrolne točke koje su spremne za fakturiranje, a zatim odaberite **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="933dd-129">Status naplate tih kontrolnih točaka mijenja se u **Spremno za fakturiranje**.</span><span class="sxs-lookup"><span data-stu-id="933dd-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Kontrolne točke fiksne cijene](media/FPBacklog.png)
