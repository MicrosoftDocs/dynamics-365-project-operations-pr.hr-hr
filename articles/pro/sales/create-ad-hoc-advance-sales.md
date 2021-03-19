---
title: Stvaranje ad hoc predujma za ugovor
description: U ovoj temi nalaze se informacije o stvaranju predujma za ugovor, ako je potrebno.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273588"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="cf4ac-103">Stvaranje ad hoc predujma za ugovor</span><span class="sxs-lookup"><span data-stu-id="cf4ac-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="cf4ac-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="cf4ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf4ac-105">Microsoft Dynamics 365 Project Operations podržava scenarije fakturiranja koji uključuju plaćanja unaprijed i predujmove.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="cf4ac-106">Postupak uporabe mogućnosti **Predujmovi** u aplikaciji **Project Operations** sličan je ugovorima o **Akontaciji**.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="cf4ac-107">Izvršite sljedeće korake kako biste klijentu fakturirali predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="cf4ac-108">Idite na stranicu **Ugovor o projektu**, a zatim odaberite karticu **Predujmovi i akontacije**.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="cf4ac-109">U podrešetki koja sadrži popis svih prethodno zabilježenih predujmova i plaćanja unaprijed odaberite **+ Nova akontacija ugovora o projektu**.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="cf4ac-110">Otvara se obrazac **Brzo stvaranje** za bilježenje plaćanja unaprijed ili predujma.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="cf4ac-111">U donjoj tablici navedena su polja za bilježenje predujma i razmatranja koja treba imati na umu tijekom stvaranja novih:</span><span class="sxs-lookup"><span data-stu-id="cf4ac-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="cf4ac-112">Polje</span><span class="sxs-lookup"><span data-stu-id="cf4ac-112">Field</span></span> | <span data-ttu-id="cf4ac-113">Opis</span><span class="sxs-lookup"><span data-stu-id="cf4ac-113">Description</span></span> | <span data-ttu-id="cf4ac-114">Utjecaj na niže razine</span><span class="sxs-lookup"><span data-stu-id="cf4ac-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="cf4ac-115">**Klijent ugovora projekta**</span><span class="sxs-lookup"><span data-stu-id="cf4ac-115">**Project Contract Customer**</span></span> | <span data-ttu-id="cf4ac-116">Ta polja označavaju klijenta na ugovoru kojem će se fakturirati za ovaj predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="cf4ac-117">Ako imate više klijenata na ugovoru i ako svakom od njih trebate fakturirati određeni iznos akontacije ili predujma, za svakog pojedinog klijenta stvorite predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="cf4ac-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="cf4ac-118">**Description**</span></span> | <span data-ttu-id="cf4ac-119">Opis svrhe ili vremena predujma koji će vam pomoći identificirati taj predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="cf4ac-120">Ovaj se opis prikazuje u retku fakture za taj predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="cf4ac-121">**Iznos**</span><span class="sxs-lookup"><span data-stu-id="cf4ac-121">**Amount**</span></span> | <span data-ttu-id="cf4ac-122">Iznos plaćanja unaprijed ili predujma.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="cf4ac-123">Ovaj se iznos prikazuje u retku fakture za taj predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="cf4ac-124">**Datum fakture**</span><span class="sxs-lookup"><span data-stu-id="cf4ac-124">**Invoice Date**</span></span> | <span data-ttu-id="cf4ac-125">Datum na koji se klijentu fakturira ovaj predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="cf4ac-126">Ovo je datum za automatizirani postupak stvaranja fakture za stvaranje retka fakture za ovaj predujam.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="cf4ac-127">**Status fakture**</span><span class="sxs-lookup"><span data-stu-id="cf4ac-127">**Invoice Status**</span></span> | <span data-ttu-id="cf4ac-128">Ovo je postavka mogućnosti koja označava dodaje li se taj predujam u nacrt fakture za ovog klijenta.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="cf4ac-129">Moguće su sljedeće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="cf4ac-129">The possible values are:</span></span></br><span data-ttu-id="cf4ac-130">- **Nije spremno za fakturiranje**</span><span class="sxs-lookup"><span data-stu-id="cf4ac-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="cf4ac-131">- **Spremno za fakturiranje**</span><span class="sxs-lookup"><span data-stu-id="cf4ac-131">- **Ready to invoice**</span></span> | <span data-ttu-id="cf4ac-132">Kada je avans ili plaćanje unaprijed označeno kao **Spremno za fakturiranje**, dodaje se kao vremenski redak na nacrtu fakture.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="cf4ac-133">Samo se potpuno fakturirani predujam može upotrijebiti za usklađivanje s troškovima projekta za sljedeće razdoblje fakture.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="cf4ac-134">Odaberite mogućnost **Spremi i zatvori** u dijaloškom okviru za brzo stvaranje kako biste zabilježili predujam ili plaćanje unaprijed.</span><span class="sxs-lookup"><span data-stu-id="cf4ac-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]