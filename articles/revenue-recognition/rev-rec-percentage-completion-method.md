---
title: Projekti s procjenom prihoda od fiksne cijene
description: U ovoj temi nalaze se informacije o prihodu od projekta s fiksnom cijenom.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531384"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="f01eb-103">Projekti s procjenom prihoda od fiksne cijene</span><span class="sxs-lookup"><span data-stu-id="f01eb-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="f01eb-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="f01eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f01eb-105">Kada stvarate redak ugovora o projektu sa sljedećim atributima u aplikaciji Dynamics 365 Project Operations rješenja Microsoft Dataverse, sustav automatski stvara projekt s procjenom prihoda od fiksne cijene.</span><span class="sxs-lookup"><span data-stu-id="f01eb-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="f01eb-106">Podaci u ovom projektu temelje se na sljedećem:</span><span class="sxs-lookup"><span data-stu-id="f01eb-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="f01eb-107">Načinu naplate s fiksnom cijenom.</span><span class="sxs-lookup"><span data-stu-id="f01eb-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="f01eb-108">Povezanom projektu.</span><span class="sxs-lookup"><span data-stu-id="f01eb-108">An associated project.</span></span>
  - <span data-ttu-id="f01eb-109">Najmanje jednoj kontrolnoj točki definiranoj na kartici **Raspored faktura**, na stranici **Redak ugovora o projektu**.</span><span class="sxs-lookup"><span data-stu-id="f01eb-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="f01eb-110">Pregled projekata s procjenom prihoda od fiksne cijene</span><span class="sxs-lookup"><span data-stu-id="f01eb-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="f01eb-111">Kako biste pregledali projekte s procjenom prihoda od fiksne cijene, poduzmite sljedeće korake:</span><span class="sxs-lookup"><span data-stu-id="f01eb-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="f01eb-112">U okruženju aplikacije Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Projekti s procjenom prihoda od fiksne cijene**.</span><span class="sxs-lookup"><span data-stu-id="f01eb-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="f01eb-113">Odaberite projekt koji želite pogledati i dvaput kliknite na stavku **ID procjene projekta** kako biste otvorili zapisnik i pregledati pojedinosti projekta.</span><span class="sxs-lookup"><span data-stu-id="f01eb-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="f01eb-114">Proširite karticu **Projekt**. Vidjet ćete jedan projekt u rešetki **Odabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="f01eb-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="f01eb-115">Sustav to upotrebljava kao zadani projekt jer je to projekt povezan s retkom ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="f01eb-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="f01eb-116">Kako biste promijenili povezanost, odaberite dodatne projekte i dodajte ih rešetki **Odabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="f01eb-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="f01eb-117">Ako je u ovoj rešetki odabrano više projekata, postotak dovršenosti projekta i procjene prihoda izračunavaju se zajedno za sve odabrane projekte.</span><span class="sxs-lookup"><span data-stu-id="f01eb-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="f01eb-118">Troškovi projekta, profil prihoda, predložak troškova i kôd razdoblja mogu se postaviti ručno.</span><span class="sxs-lookup"><span data-stu-id="f01eb-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="f01eb-119">Ako se ne postave ručno, vrijednosti će se zadati tijekom prvog izračuna procjene za projekt s pomoću pravila konfiguriranih za profile troškova i prihoda projekta.</span><span class="sxs-lookup"><span data-stu-id="f01eb-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

