---
title: Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena
description: Ovaj tema pruža informacije o ažuriranju atributa dodatka za dimenzije cijena.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012802"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="6a888-103">Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena</span><span class="sxs-lookup"><span data-stu-id="6a888-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="6a888-104">Ako ne upotrebljavate značajke sastavljanja ponuda i ugovora u programu Project Service Automation (PSA), možete preskočiti ovu tema.</span><span class="sxs-lookup"><span data-stu-id="6a888-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="6a888-105">Ova tema podrazumijeva da ste dovršili postupke opisane u temama [Izrada prilagođenih polja i entiteta](create-custom-fields-entities.md), [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](field-references.md) i [Postavljanje prilagođenih polja kao dimenzija cijena](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="6a888-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="6a888-106">Ako niste dovršili te postupke, vratite se i dovršite ih, a zatim se vratite na ovu temu.</span><span class="sxs-lookup"><span data-stu-id="6a888-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="6a888-107">Kada se pojedinost retka ponude izradi na stranici **Redak ponude** za redak ponude projekta, sustav stvara dva retka procjene u pozadini – jedan redak za stranu troška procjene i jedan za stranu prodaje.</span><span class="sxs-lookup"><span data-stu-id="6a888-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="6a888-108">Isto vrijedi i za retke ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="6a888-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="6a888-109">Kada uvedete promjenu u količinu ili polje na strani troška, ta se promjena prenosi na stranu prodaje.</span><span class="sxs-lookup"><span data-stu-id="6a888-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="6a888-110">To je moguće zbog sljedećih dodatka koji se moraju ponovno registrirati nakon promjene dimenzija cijena.</span><span class="sxs-lookup"><span data-stu-id="6a888-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="6a888-111">PreOperationContractLineDetailUpdate – Ažuriranja **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="6a888-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="6a888-112">PreOperationQuoteLineDetailUpdate – Ažuriranja **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="6a888-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="6a888-113">Koraci u nastavku objašnjavaju vam postupak registracije dodataka.</span><span class="sxs-lookup"><span data-stu-id="6a888-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="6a888-114">Otvorite **PluginRegistrationTool** i povežite se s mrežnom instancom.</span><span class="sxs-lookup"><span data-stu-id="6a888-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="6a888-115">Kliknite **Pretraži** i potražite dodatak za ažuriranje.</span><span class="sxs-lookup"><span data-stu-id="6a888-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Snimka zaslona stabla pretraživanja](media/PRT-1.png)

3. <span data-ttu-id="6a888-117">Nakon što pronađete dodatak, odaberite ga, a zatim kliknite **Odaberi u glavnom obrascu**.</span><span class="sxs-lookup"><span data-stu-id="6a888-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="6a888-118">Odaberite korak dodatka za ažuriranje, kliknite desnom tipkom miša, a zatim odaberite **Ažuriraj**.</span><span class="sxs-lookup"><span data-stu-id="6a888-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Snimka zaslona dodatka koji se ažurira](media/PRT-2.png)
 
5. <span data-ttu-id="6a888-120">U prozoru za ažuriranje kliknite tri točke (**...**) u atributima filtriranja.</span><span class="sxs-lookup"><span data-stu-id="6a888-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Snimka zaslona informacija o konfiguraciji ažuriranja postojećeg koraka](media/PRT-3.png)
 
6. <span data-ttu-id="6a888-122">Odaberite potvrdne okvire atributa cijena.</span><span class="sxs-lookup"><span data-stu-id="6a888-122">Select the pricing attribute check boxes.</span></span>

 ![Snimka zaslona s prikazom odabranog potvrdnog okvira za atribute cijena](media/PRT-4.png)

7. <span data-ttu-id="6a888-124">Kliknite **U redu** da biste zatvorili stranicu, a zatim odaberite **Ažuriraj korak**.</span><span class="sxs-lookup"><span data-stu-id="6a888-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Snimka zaslona s prikazom gumba „Ažuriraj korak”](media/PRT-5.png)
 
8. <span data-ttu-id="6a888-126">Ponovite ovaj postupak za drugi dodatak, **PreOperationQuoteLineDetail – Ažuriranje msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="6a888-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="6a888-127">Zatvorite alat za registraciju dodataka.</span><span class="sxs-lookup"><span data-stu-id="6a888-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]