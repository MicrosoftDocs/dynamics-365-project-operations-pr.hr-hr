---
title: Izvješća o trošku i više odobravatelja
description: U ovoj se temi nalaze informacije o izvješćima o troškovima koje treba odobriti više osoba.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897082"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="8c2c9-103">Izvješća o trošku i više odobravatelja</span><span class="sxs-lookup"><span data-stu-id="8c2c9-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="8c2c9-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="8c2c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c2c9-105">Ovisno o pravilima vaše tvrtke ili ustanove za odobravanje troškova, možda će podneseno izvješće o troškovima morati odobriti više osoba.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="8c2c9-106">Kada postavljate postupak tijeka rada za odobrenje izvješća o troškovima, možete dodati elemente tijeka rada koji obuhvaćaju zadatke ili korake za jednog ili više odobravatelja izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="8c2c9-107">Na primjer, možda ćete tražiti da sva izvješća o troškovima odobre dvije odvojene osobe, rukovoditelj zaposlenika koji je podnio izvješće i koordinator dugovanja.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="8c2c9-108">Ako odlučite tražiti više odobravatelja izvješća o troškovima, elemente tijeka rada možete dodati na jedan od sljedećih načina:</span><span class="sxs-lookup"><span data-stu-id="8c2c9-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="8c2c9-109">Dodajte jedan element odobrenja koji ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-109">Add one approval element that has one step.</span></span> <span data-ttu-id="8c2c9-110">Na primjer, korak može zahtijevati da se izvješće o troškovima dodijeli grupi korisnika i da ga odobri 50 posto članova grupe korisnika.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="8c2c9-111">Dodajte jedan element odobrenja koji ima više koraka.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="8c2c9-112">Na primjer, element odobrenja može imati sljedeće korake:</span><span class="sxs-lookup"><span data-stu-id="8c2c9-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="8c2c9-113">Izvješće o troškovima odobrava rukovoditelj zaposlenika koji je podnio izvješće.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="8c2c9-114">Službenik za dugovanja provjerava račune i stavke izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="8c2c9-115">Izvješće o troškovima odobrava vlasnik proračuna.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="8c2c9-116">Dodajte više elemenata odobrenja, od kojih svaki ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="8c2c9-117">Na primjer, možete dodati zasebni element odobrenja za svaki od sljedećih koraka:</span><span class="sxs-lookup"><span data-stu-id="8c2c9-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="8c2c9-118">Izvješće o troškovima odobrava rukovoditelj zaposlenika.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="8c2c9-119">Izvješće o troškovima odobrava vlasnik proračuna.</span><span class="sxs-lookup"><span data-stu-id="8c2c9-119">The budget owner approves the expense report.</span></span>
