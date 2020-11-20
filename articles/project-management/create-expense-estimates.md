---
title: Procjena troška
description: U ovoj temi nalaze se informacije o načinu definiranja ili procjene troškova koji se temelje na projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131694"
---
# <a name="expense-estimates"></a><span data-ttu-id="0ab3c-103">Procjena troška</span><span class="sxs-lookup"><span data-stu-id="0ab3c-103">Expense estimates</span></span>
<span data-ttu-id="0ab3c-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="0ab3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0ab3c-105">Uz definiranje procjena koje se temelje na resursu, Dynamics 365 Project Operations omogućuje voditeljima projekata definiranje troškova koji se temelje na projektu za svaki projekt.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="0ab3c-106">Svaka stavka troška može se povezati s određenim projektnim zadatkom ili kategorijom troška.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="0ab3c-107">Kategorije troškova obično se definiraju na organizacijskoj razini.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="0ab3c-108">Određivanje cijene za svaku kategoriju troška obično su definirane u sljedećoj hijerarhiji:</span><span class="sxs-lookup"><span data-stu-id="0ab3c-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="0ab3c-109">Organizacija</span><span class="sxs-lookup"><span data-stu-id="0ab3c-109">Organization</span></span>
- <span data-ttu-id="0ab3c-110">Klijent</span><span class="sxs-lookup"><span data-stu-id="0ab3c-110">Customer</span></span>
- <span data-ttu-id="0ab3c-111">Ponuda/ugovor</span><span class="sxs-lookup"><span data-stu-id="0ab3c-111">Quote/contract</span></span>

<span data-ttu-id="0ab3c-112">Poduzmite sljedeće korake za prikaz, dodavanje ili brisanje troška projekta.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="0ab3c-113">Idite na mogućnost **Projekti** i odaberite projekt na kojem želite raditi.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="0ab3c-114">Odaberite karticu **Procjene projekta** i pogledajte popis troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="0ab3c-115">Odaberite **Novi trošak** kako biste dodali trošak.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="0ab3c-116">Ili odaberite trošak za brisanje, a zatim odaberite **Izbriši trošak**.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="0ab3c-117">Sljedeći atributi definirani su za svaku stavku retka troška:</span><span class="sxs-lookup"><span data-stu-id="0ab3c-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="0ab3c-118">**Kategorija**: Uobičajena grupiranja koja su se upotrebljavala za opisivanje svih troškova nastalih na projektu.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="0ab3c-119">**Početni datum**: Datum kada se predviđa da će nastati trošak.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="0ab3c-120">**Količina**: Procijenjeni broj stavki troška za određenu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="0ab3c-121">**Jedinična cijena koštanja**: Jedinična cijena koja se upotrebljava za izračun koštanja troška.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="0ab3c-122">**Jedinična prodajna cijena**: Jedinična cijena koja se upotrebljava za izračun prodajne cijene troška.</span><span class="sxs-lookup"><span data-stu-id="0ab3c-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

