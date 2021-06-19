---
title: Uklanjanje procjene projekta
description: U ovoj temi nalaze se informacije o uklanjanju procjene projekta nakon što se dovrši.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006907"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="4b91e-103">Uklanjanje procjene projekta</span><span class="sxs-lookup"><span data-stu-id="4b91e-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b91e-104">Procjena projekta daje financijski prikaz za procijenjeni i raspoređeni rad za projekt.</span><span class="sxs-lookup"><span data-stu-id="4b91e-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="4b91e-105">Kako biste radili s procjenama za projekt, projekt morate priložiti projektu procjene.</span><span class="sxs-lookup"><span data-stu-id="4b91e-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="4b91e-106">Projekt procjene uvijek se temelji na postojećem projektu, međutim više projekata može se odnositi na jedan projekt procjene.</span><span class="sxs-lookup"><span data-stu-id="4b91e-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="4b91e-107">Za projekte procjene mogu se priložiti samo projekti s fiksnom cijenom i investicijski projekti, a ti projekti moraju pripadati istoj projektnoj grupi kao i projekt procjene.</span><span class="sxs-lookup"><span data-stu-id="4b91e-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="4b91e-108">Kako bi se uklonio projekt procjene, on mora biti dovršen.</span><span class="sxs-lookup"><span data-stu-id="4b91e-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="4b91e-109">Sljedeći koraci objašnjavaju način uklanjanja procjene.</span><span class="sxs-lookup"><span data-stu-id="4b91e-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="4b91e-110">Idite na mogućnost **Upravljanje projektima i računovodstvo** > **Svi projekti** i otvorite projekt.</span><span class="sxs-lookup"><span data-stu-id="4b91e-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="4b91e-111">Na kartici **Upravljanje**, odaberite **Procjene** i na stranici **Procjena** odaberite **Ukloni**.</span><span class="sxs-lookup"><span data-stu-id="4b91e-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="4b91e-112">Na stranici **Ukloni procjenu**, na kartici **Općenito**, postavite sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="4b91e-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="4b91e-113">**Kod razdoblja**: Odaberite kod razdoblja kako biste odabrali odgovarajuće projekte procjene.</span><span class="sxs-lookup"><span data-stu-id="4b91e-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="4b91e-114">**Datum procjene**: Odaberite odgovarajući datum procjene za uklanjanje.</span><span class="sxs-lookup"><span data-stu-id="4b91e-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="4b91e-115">**Ukloni s pomoću WIP upozorenja**: Omogućite ovu mogućnost za pružanje obavijesti kada će procjena koja je povezana s radom u tijeku (WIP) biti uklonjena.</span><span class="sxs-lookup"><span data-stu-id="4b91e-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="4b91e-116">Kada ova mogućnost nije omogućena, uklanjanje se ne može nastaviti ako postoji neka transakcija koja nije procijenjena.</span><span class="sxs-lookup"><span data-stu-id="4b91e-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="4b91e-117">Ova je mogućnost dostupna samo kada se uklanjanje primjenjuje na projekt procjene.</span><span class="sxs-lookup"><span data-stu-id="4b91e-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="4b91e-118">Nije dostupno ako upotrebljavate periodična knjiženja.</span><span class="sxs-lookup"><span data-stu-id="4b91e-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="4b91e-119">Ova postavka radi s postavkama na kartici **Procjena**, na stranici **Parametri projekta**, u grupi polja **Dopusti eliminaciju kada postoje transakcije koje nisu procijenjene**.</span><span class="sxs-lookup"><span data-stu-id="4b91e-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="4b91e-120">**Postavljanje faze na Završeno**: Omogućite ovu mogućnost kako biste postavili fazu projekta procjene na **Završeno** nakon što pokrenete uklanjanje.</span><span class="sxs-lookup"><span data-stu-id="4b91e-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="4b91e-121">**Ispis popisa procjena**: Odaberite podatke koji će se uključiti pri ispisu popisa procjena.</span><span class="sxs-lookup"><span data-stu-id="4b91e-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="4b91e-122">**Prikaži dnevnik s informacijama**: Omogućite ovu mogućnost za prikaz dnevnika s informacijama.</span><span class="sxs-lookup"><span data-stu-id="4b91e-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="4b91e-123">**Datum knjiženja**: Odaberite datum knjiženja procjene u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="4b91e-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="4b91e-124">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="4b91e-124">Select **OK**.</span></span>
5. <span data-ttu-id="4b91e-125">Nakon završetka postupka uklanjanja, uklonjeni projekt procjene prikazuje se s negativnom vrijednošću.</span><span class="sxs-lookup"><span data-stu-id="4b91e-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="4b91e-126">Ako niste namjeravali ukloniti procjenu, možete odabrati uklonjenu procjenu i odabrati **Poništi uklanjanje**.</span><span class="sxs-lookup"><span data-stu-id="4b91e-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]