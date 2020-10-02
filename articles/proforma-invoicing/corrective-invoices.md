---
title: Ispravljene fakture
description: U ovoj se temi nalaze informacije o ispravljenim fakturama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898072"
---
# <a name="corrected-invoices"></a><span data-ttu-id="2700c-103">Ispravljene fakture</span><span class="sxs-lookup"><span data-stu-id="2700c-103">Corrected invoices</span></span>

<span data-ttu-id="2700c-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="2700c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2700c-105">Potvrđene fakture mogu se urediti.</span><span class="sxs-lookup"><span data-stu-id="2700c-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="2700c-106">Kada uređujete potvrđenu fakturu, stvara se skica ispravljene fakture.</span><span class="sxs-lookup"><span data-stu-id="2700c-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="2700c-107">Budući da se pretpostavlja kako želite poništiti sve transakcije i količine iz izvorne fakture, ispravljena faktura uključuje sve transakcije iz izvorne fakture, a sve količine navedene u njoj iznose nula (0).</span><span class="sxs-lookup"><span data-stu-id="2700c-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="2700c-108">Kada transakcije ne treba ispravljati, možete ih ukloniti iz skice ispravljene fakture.</span><span class="sxs-lookup"><span data-stu-id="2700c-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="2700c-109">Kako biste poništili ili vratili samo djelomičnu količinu, polje Količina možete urediti u pojedinosti retka.</span><span class="sxs-lookup"><span data-stu-id="2700c-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="2700c-110">Ako otvorite pojedinost retka fakture, možete vidjeti izvornu količinu fakture.</span><span class="sxs-lookup"><span data-stu-id="2700c-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="2700c-111">Zatim možete urediti trenutačnu količinu fakture tako da je manja ili veća od izvorne količine fakture.</span><span class="sxs-lookup"><span data-stu-id="2700c-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="2700c-112">Kada potvrdite ispravljenu fakturu, izvorni naplaćeni stvarni podatak o prodaji mijenja se i stvara se novi naplaćeni stvarni podatak o prodaji.</span><span class="sxs-lookup"><span data-stu-id="2700c-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="2700c-113">Ako je količina manja, razlika će dovesti i do stvaranja novog nenaplaćenog stvarnog podatka o prodaji.</span><span class="sxs-lookup"><span data-stu-id="2700c-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="2700c-114">Na primjer, ako je izvorna naplaćena prodaja obuhvaćala osam sati, a pojedinost retka ispravljene fakture sadrži manju količinu od šest sati, vraća se izvorni redak naplaćene prodaje i stvaraju se dva nova stvarna podatka:</span><span class="sxs-lookup"><span data-stu-id="2700c-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="2700c-115">Naplaćeni stvarni podatak o prodaji za šest sati.</span><span class="sxs-lookup"><span data-stu-id="2700c-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="2700c-116">Nenaplaćeni stvarni podatak o prodaji za preostala dva sata.</span><span class="sxs-lookup"><span data-stu-id="2700c-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="2700c-117">Ova transakcija može biti naplaćena kasnije ili označena kao nenaplativa, ovisno o pregovorima s klijentom.</span><span class="sxs-lookup"><span data-stu-id="2700c-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
