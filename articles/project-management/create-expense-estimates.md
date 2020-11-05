---
title: Procjena troška
description: U ovoj temi nalaze se informacije o načinu definiranja ili procjene troškova koji se temelje na projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073310"
---
# <a name="expense-estimates"></a><span data-ttu-id="defd6-103">Procjena troška</span><span class="sxs-lookup"><span data-stu-id="defd6-103">Expense estimates</span></span>
<span data-ttu-id="defd6-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="defd6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="defd6-105">Uz definiranje procjena koje se temelje na resursu, Dynamics 365 Project Operations omogućuje voditeljima projekata definiranje troškova koji se temelje na projektu za svaki projekt.</span><span class="sxs-lookup"><span data-stu-id="defd6-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="defd6-106">Svaka stavka troška može se povezati s određenim projektnim zadatkom ili kategorijom troška.</span><span class="sxs-lookup"><span data-stu-id="defd6-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="defd6-107">Kategorije troškova obično se definiraju na organizacijskoj razini.</span><span class="sxs-lookup"><span data-stu-id="defd6-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="defd6-108">Određivanje cijene za svaku kategoriju troška obično su definirane u sljedećoj hijerarhiji:</span><span class="sxs-lookup"><span data-stu-id="defd6-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="defd6-109">Organizacija</span><span class="sxs-lookup"><span data-stu-id="defd6-109">Organization</span></span>
- <span data-ttu-id="defd6-110">Klijent</span><span class="sxs-lookup"><span data-stu-id="defd6-110">Customer</span></span>
- <span data-ttu-id="defd6-111">Ponuda/ugovor</span><span class="sxs-lookup"><span data-stu-id="defd6-111">Quote/contract</span></span>

<span data-ttu-id="defd6-112">Poduzmite sljedeće korake za prikaz, dodavanje ili brisanje troška projekta.</span><span class="sxs-lookup"><span data-stu-id="defd6-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="defd6-113">Idite na mogućnost **Projekti** i odaberite projekt na kojem želite raditi.</span><span class="sxs-lookup"><span data-stu-id="defd6-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="defd6-114">Odaberite karticu **Procjene projekta** i pogledajte popis troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="defd6-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="defd6-115">Odaberite **Novi trošak** kako biste dodali trošak.</span><span class="sxs-lookup"><span data-stu-id="defd6-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="defd6-116">Ili odaberite trošak za brisanje, a zatim odaberite **Izbriši trošak**.</span><span class="sxs-lookup"><span data-stu-id="defd6-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="defd6-117">Sljedeći atributi definirani su za svaku stavku retka troška:</span><span class="sxs-lookup"><span data-stu-id="defd6-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="defd6-118">**Kategorija** : Uobičajena grupiranja koja su se upotrebljavala za opisivanje svih troškova nastalih na projektu.</span><span class="sxs-lookup"><span data-stu-id="defd6-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="defd6-119">**Početni datum** : Datum kada se predviđa da će nastati trošak.</span><span class="sxs-lookup"><span data-stu-id="defd6-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="defd6-120">**Količina** : Procijenjeni broj stavki troška za određenu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="defd6-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="defd6-121">**Jedinična cijena koštanja** : Jedinična cijena koja se upotrebljava za izračun koštanja troška.</span><span class="sxs-lookup"><span data-stu-id="defd6-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="defd6-122">**Jedinična prodajna cijena** : Jedinična cijena koja se upotrebljava za izračun prodajne cijene troška.</span><span class="sxs-lookup"><span data-stu-id="defd6-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

