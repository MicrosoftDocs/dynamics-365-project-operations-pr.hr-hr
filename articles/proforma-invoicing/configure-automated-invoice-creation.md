---
title: Konfiguriranje automatskog stvaranja fakture
description: U ovoj temi nalaze se informacije o načinu konfiguriranja sustava za automatsko generiranje faktura.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287904"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="10714-103">Konfiguriranje automatskog stvaranja fakture</span><span class="sxs-lookup"><span data-stu-id="10714-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="10714-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="10714-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="10714-105">Dovršite sljedeće korake kako biste konfigurirali automatiziranu fakturu koja se izvršava u aplikaciji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="10714-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="10714-106">Idite na **Postavke** > **Skupni poslovi**.</span><span class="sxs-lookup"><span data-stu-id="10714-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="10714-107">Stvorite skupni posao i dodijelite mu naziv **Fakture stvorene u aplikacije Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="10714-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="10714-108">Naziv skupnog posla mora sadržavati riječi „stvaranje faktura”.</span><span class="sxs-lookup"><span data-stu-id="10714-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="10714-109">U polju **Vrsta posla** odaberite **Ništa**.</span><span class="sxs-lookup"><span data-stu-id="10714-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="10714-110">Prema zadanim postavkama mogućnosti **Dnevna učestalost** i **Aktivno** postavljene su na **Da**.</span><span class="sxs-lookup"><span data-stu-id="10714-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="10714-111">Odaberite **Pokreni tijek rada**.</span><span class="sxs-lookup"><span data-stu-id="10714-111">Select **Run Workflow**.</span></span> <span data-ttu-id="10714-112">U dijaloškom okviru **Pretraživanje zapisa** vidjet ćete tri tijeka rada:</span><span class="sxs-lookup"><span data-stu-id="10714-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="10714-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="10714-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="10714-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="10714-114">ProcessRunner</span></span>
    - <span data-ttu-id="10714-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="10714-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="10714-116">Odaberite **ProcessRunCaller**, a zatim **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="10714-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="10714-117">U sljedećem dijaloškom okviru odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="10714-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="10714-118">Nakon tijeka rada **Sleep** slijedi tijek rada **Process**.</span><span class="sxs-lookup"><span data-stu-id="10714-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="10714-119">U petom koraku možete odabrati i **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="10714-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="10714-120">Zatim, kada odaberete **U redu**, nakon tijeka rada **Process** slijedi tijek rada **Sleep**.</span><span class="sxs-lookup"><span data-stu-id="10714-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="10714-121">Tijekovi rada **ProcessRunCaller** i **ProcessRunner** stvaraju fakture.</span><span class="sxs-lookup"><span data-stu-id="10714-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="10714-122">**ProcessRunCaller** poziva **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="10714-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="10714-123">**ProcessRunner** jest tijek rada koji stvara fakture.</span><span class="sxs-lookup"><span data-stu-id="10714-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="10714-124">Prolazi kroz sve retke ugovora za koje je potrebno stvoriti fakture i stvara fakture za te retke.</span><span class="sxs-lookup"><span data-stu-id="10714-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="10714-125">Da bi se odredili reci ugovora za koje je potrebno stvoriti fakture, posao traži datume stvaranja faktura za retke ugovora.</span><span class="sxs-lookup"><span data-stu-id="10714-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="10714-126">Ako reci ugovora koji pripadaju jednom ugovoru imaju isti datum stvaranja fakture, transakcije se kombiniraju u jednu fakturu koja ima dva retka fakture.</span><span class="sxs-lookup"><span data-stu-id="10714-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="10714-127">Ako nema transakcija za stvaranje faktura, posao preskače stvaranje faktura.</span><span class="sxs-lookup"><span data-stu-id="10714-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="10714-128">Nakon pokretanja funkcije **ProcessRunner** poziva se **ProcessRunCaller**, navodi se vrijeme završetka i funkcija se zatvara.</span><span class="sxs-lookup"><span data-stu-id="10714-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="10714-129">**ProcessRunCaller** zatim pokreće mjerač vremena koji se izvodi 24 sata od navedenog vremena završetka.</span><span class="sxs-lookup"><span data-stu-id="10714-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="10714-130">Po završetku izvođenja mjerača vremena funkcija **ProcessRunCaller** zatvara se.</span><span class="sxs-lookup"><span data-stu-id="10714-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="10714-131">Skupni postupak stvaranja faktura ponavljajući je posao.</span><span class="sxs-lookup"><span data-stu-id="10714-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="10714-132">Ako se taj skupni postupak izvodi više puta, stvaraju se višestruke instance posla koje uzrokuju pogreške.</span><span class="sxs-lookup"><span data-stu-id="10714-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="10714-133">Stoga biste trebali pokrenuti skupni postupak samo jednom i ponovno ga pokrenuti samo ako se prestane izvoditi.</span><span class="sxs-lookup"><span data-stu-id="10714-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="10714-134">Skupno fakturiranje izvršava se samo za retke ugovora o projektu koji su konfigurirani prema rasporedu faktura.</span><span class="sxs-lookup"><span data-stu-id="10714-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="10714-135">Ugovorni redci s načinom naplate fiksne cijene moraju imati konfigurirane prekretnice.</span><span class="sxs-lookup"><span data-stu-id="10714-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="10714-136">Redak projektnog ugovora s vremenskim i materijalnim načinom naplate treba imati postavku rasporeda računa na temelju datuma.</span><span class="sxs-lookup"><span data-stu-id="10714-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="10714-137">Isto se odnosi i na redak ugovora koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="10714-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]