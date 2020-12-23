---
title: Ažuriranje atributa programskih dodataka s pomoću novih veličina za određivanje cijena
description: U ovoj temi nalaze se informacije o načinu ažuriranja atributa programskih dodatka za veličine za određivanje cijena.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643209"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="300d5-103">Ažuriranje atributa programskih dodataka s pomoću novih veličina za određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="300d5-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="300d5-104">U ovoj temi nalaze se informacije o načinu ažuriranja atributa programskih dodatka za veličine za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="300d5-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="300d5-105">Ova se tema primjenjuje samo na ponude i značajke ugovora u aplikaciji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="300d5-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="300d5-106">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="300d5-106">Prerequisites</span></span>
<span data-ttu-id="300d5-107">Prije nego što dovršite korake navedene u ovoj temi, morate dovršiti postupke u sljedećim temama:</span><span class="sxs-lookup"><span data-stu-id="300d5-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="300d5-108">Stvaranje prilagođenih polja i entiteta</span><span class="sxs-lookup"><span data-stu-id="300d5-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="300d5-109">Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima</span><span class="sxs-lookup"><span data-stu-id="300d5-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="300d5-110">[Postavljanje prilagođenih polja kao cjenovnih veličina](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="300d5-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="300d5-111">Ako niste dovršili te postupke, dovršite ih, a zatim se vratite na ovu temu.</span><span class="sxs-lookup"><span data-stu-id="300d5-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="300d5-112">Registrirajte programski dodatak</span><span class="sxs-lookup"><span data-stu-id="300d5-112">Register a plug-in</span></span>
<span data-ttu-id="300d5-113">Kada se stvara pojedinost ponude na stranici **Redak ponude** za redak ponude projekta, sustav stvara dva retka procjene.</span><span class="sxs-lookup"><span data-stu-id="300d5-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="300d5-114">Jedan redak odnosi se na troškovnu stranu procjene, a drugi na prodajnu stranu.</span><span class="sxs-lookup"><span data-stu-id="300d5-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="300d5-115">Isto vrijedi i za retke ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="300d5-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="300d5-116">Kada uvedete promjenu u količinu ili polje na strani troška, ta se promjena unosi i na stranu prodaje.</span><span class="sxs-lookup"><span data-stu-id="300d5-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="300d5-117">To je moguće jer programski dodaci PreOperation na entitetima Pojedinosti retka ponude i Pojedinosti retka ugovora povezuju određene atribute na troškovnoj i prodajnoj strani transakcije.</span><span class="sxs-lookup"><span data-stu-id="300d5-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="300d5-118">Ako trebate unijeti promjene u vrijednosti veličina za određivanje cijena na prodajnoj strani kako bi se izvršile i na troškovnoj strani, sljedeći se programski dodaci moraju ponovno registrirati nakon unošenja promjena u veličinu za određivanje cijene.</span><span class="sxs-lookup"><span data-stu-id="300d5-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="300d5-119">Ovo su programski dodaci za ažuriranje i ponovnu registraciju:</span><span class="sxs-lookup"><span data-stu-id="300d5-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="300d5-120">PreOperationContractLineDetailUpdate – **Ažuriraj msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="300d5-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="300d5-121">PreOperationQuoteLineDetailUpdate – **Ažurira msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="300d5-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="300d5-122">Za ažuriranje i ponovnu registraciju programskih dodataka poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="300d5-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="300d5-123">Otvorite **PluginRegistrationTool** i povežite se s okruženjem aplikacije Project Operations platforme Dataverse.</span><span class="sxs-lookup"><span data-stu-id="300d5-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="300d5-124">Odaberite **Traži** i upišite prvih nekoliko slova programskog dodatka koji će se ažurirati.</span><span class="sxs-lookup"><span data-stu-id="300d5-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="300d5-125">Nakon što pronađete dodatak, odaberite ga, a zatim odaberite **Odaberi u glavnom obrascu**.</span><span class="sxs-lookup"><span data-stu-id="300d5-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="300d5-126">Odaberite korak **Ažuriraj msdyn_orderlinetransaction**, kliknite desnu tipku miša i zatim odaberite **Ažuriraj**.</span><span class="sxs-lookup"><span data-stu-id="300d5-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="300d5-127">Na dijaloškoj stranici **Ažuriranje** odaberite tri točke (**...**) u atributima za filtriranje.</span><span class="sxs-lookup"><span data-stu-id="300d5-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="300d5-128">Otvara se prozor za filtriranje atributa na kojem se navodi popis svih atributa u entitetu i veličina za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="300d5-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="300d5-129">Označite potvrdne okvire za atribute veličina za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="300d5-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="300d5-130">Odaberite **U redu** kako biste zatvorili stranicu, a zatim odaberite **Ažuriraj korak**.</span><span class="sxs-lookup"><span data-stu-id="300d5-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="300d5-131">Ponovite korake od 2 do 7 za drugi programski dodatak, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="300d5-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="300d5-132">Za ovaj programski dodatak, morate ažurirati korak **Ažuriranje msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="300d5-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="300d5-133">Zatvorite **Alat za registraciju programskih dodataka**.</span><span class="sxs-lookup"><span data-stu-id="300d5-133">Close **PluginRegistrationTool**.</span></span>
