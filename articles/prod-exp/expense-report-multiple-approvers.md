---
title: Više odobravatelja izvješća o troškovima
description: U ovoj se temi nalaze informacije o izvješćima o troškovima koje treba odobriti više osoba.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073544"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="5b536-103">Više odobravatelja izvješća o troškovima</span><span class="sxs-lookup"><span data-stu-id="5b536-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b536-104">Ovisno o pravilima vaše tvrtke ili ustanove za odobravanje troškova, možda će izvješće o troškovima koje je poslao zaposlenik morati odobriti više osoba.</span><span class="sxs-lookup"><span data-stu-id="5b536-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="5b536-105">Kada postavljate postupak tijeka rada za odobrenje izvješća o troškovima, možete dodati elemente tijeka rada koji obuhvaćaju zadatke ili korake za jednog ili više odobravatelja izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="5b536-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="5b536-106">Na primjer, možda ćete tražiti da sva izvješća o troškovima najprije odobri rukovoditelj zaposlenika koji je podnio izvješće, a zatim koordinator Dugovanja.</span><span class="sxs-lookup"><span data-stu-id="5b536-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="5b536-107">Ako odlučite tražiti više odobravatelja izvješća o troškovima, elemente tijeka rada možete dodati na jedan od sljedećih načina:</span><span class="sxs-lookup"><span data-stu-id="5b536-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="5b536-108">Dodajte jedan element odobrenja koji ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="5b536-108">Add one approval element that has one step.</span></span> <span data-ttu-id="5b536-109">Na primjer, korak može zahtijevati da se izvješće o troškovima dodijeli grupi korisnika i da ga odobri 50 posto članova grupe korisnika.</span><span class="sxs-lookup"><span data-stu-id="5b536-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="5b536-110">Dodajte jedan element odobrenja koji ima više koraka.</span><span class="sxs-lookup"><span data-stu-id="5b536-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="5b536-111">Na primjer, element odobrenja može imati sljedeće korake:</span><span class="sxs-lookup"><span data-stu-id="5b536-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="5b536-112">Izvješće o troškovima odobrava rukovoditelj zaposlenika koji je podnio izvješće.</span><span class="sxs-lookup"><span data-stu-id="5b536-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="5b536-113">Službenik za dugovanja provjerava račune i stavke izvješća o troškovima.</span><span class="sxs-lookup"><span data-stu-id="5b536-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="5b536-114">Izvješće o troškovima odobrava vlasnik proračuna.</span><span class="sxs-lookup"><span data-stu-id="5b536-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="5b536-115">Dodajte više elemenata odobrenja, od kojih svaki ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="5b536-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="5b536-116">Na primjer, možete dodati zasebni element odobrenja za svaki od sljedećih koraka:</span><span class="sxs-lookup"><span data-stu-id="5b536-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="5b536-117">Izvješće o troškovima odobrava rukovoditelj zaposlenika.</span><span class="sxs-lookup"><span data-stu-id="5b536-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="5b536-118">Izvješće o troškovima odobrava vlasnik proračuna.</span><span class="sxs-lookup"><span data-stu-id="5b536-118">The budget owner approves the expense report.</span></span>
