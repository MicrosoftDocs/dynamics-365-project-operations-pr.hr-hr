---
title: Rad s osobnim troškovima na izvješću o troškovima
description: U ovoj temi nalaze se informacije o načinu rada s osobnim troškovima zaposlenih za putovanja u poslovne svrhe.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025675"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="ea61e-103">Rad s osobnim troškovima na izvješću o troškovima</span><span class="sxs-lookup"><span data-stu-id="ea61e-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="ea61e-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="ea61e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea61e-105">Tijekom poslovnog putovanja zaposlenik može platiti osobne troškove svojom korporativnom kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="ea61e-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="ea61e-106">Ako postupak nije određen za rukovanje osobnim troškovima, postupak odobravanja izvješća o troškovima mogao bi biti poremećen kad zaposlenik pošalje svoje podrobno izvješće o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ea61e-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="ea61e-107">Dva su načina s pomoću kojih možete raditi s osobnim troškovima zaposlenika:</span><span class="sxs-lookup"><span data-stu-id="ea61e-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="ea61e-108">**Plaća zaposlenik**: Vaša tvrtka ili ustanova ne plaća osobne troškove koji se prikazuju za naplatu po kreditnoj kartici poduzeća.</span><span class="sxs-lookup"><span data-stu-id="ea61e-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="ea61e-109">Umjesto toga, zaposlenik izravno plaća dobavljača kreditne kartice za troškove.</span><span class="sxs-lookup"><span data-stu-id="ea61e-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="ea61e-110">**Plaća tvrtka** : Vaša tvrtka ili ustanova plaća puni račun za korporativnu kreditnu karticu, a zatim tereti račun radnika za osobne troškove.</span><span class="sxs-lookup"><span data-stu-id="ea61e-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="ea61e-111">Način koji vaša tvrtka ili ustanova upotrebljava možete odabrati na stranici **Parametri upravljanja troškovima**.</span><span class="sxs-lookup"><span data-stu-id="ea61e-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="ea61e-112">Omogućivanje funkcije podijeljenog troška kada polje osobnog iznosa ima definiranu vrijednost</span><span class="sxs-lookup"><span data-stu-id="ea61e-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="ea61e-113">Značajka **Omogući funkciju podijeljenog troška kada polje osobnog iznosa ima definiranu vrijednost** odnosi se samo na izvješća o troškovima koja su odobrena s pomoću tijeka rada na razini retka.</span><span class="sxs-lookup"><span data-stu-id="ea61e-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="ea61e-114">Izvješća se odobravaju odlaskom na **Obradi izvješća o troškovima** > **Izvješća o troškovima dodijeljena meni** > **Otvori izvješće o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="ea61e-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="ea61e-115">Kako biste omogućili ovu značajku, idite na mogućnost **Radni prostori** > **Upravljanje značajkama**, odaberite **Omogući funkciju podijeljenog troška kada polje osobni iznos ima definiranu vrijednost**, a zatim odaberite **Omogući odmah**.</span><span class="sxs-lookup"><span data-stu-id="ea61e-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="ea61e-116">Kada je značajka omogućena, redci troškova koji upotrebljavaju ovu funkciju generiraju dva retka kada se šalje izvješće.</span><span class="sxs-lookup"><span data-stu-id="ea61e-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="ea61e-117">Generiraju se dva retka tako da odobravatelj može odobriti svaki redak zasebno.</span><span class="sxs-lookup"><span data-stu-id="ea61e-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
