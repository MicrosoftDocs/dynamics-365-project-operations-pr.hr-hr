---
title: Bilješke razvojnog inženjera za odobrenja
description: U ovoj temi nalaze se dodatne informacije za razvojne inženjere o radu s odobrenjima.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996782"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="c82d4-103">Bilješke razvojnog inženjera za odobrenja</span><span class="sxs-lookup"><span data-stu-id="c82d4-103">Developer notes for Approvals</span></span>

<span data-ttu-id="c82d4-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="c82d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c82d4-105">Dynamics 365 Project Operations uključuje logiku provjere valjanosti koja osigurava ispravan prijelaz zapisa kroz faze odobrenja.</span><span class="sxs-lookup"><span data-stu-id="c82d4-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="c82d4-106">Ispravni prijelazi zapisa osiguravaju sljedeće:</span><span class="sxs-lookup"><span data-stu-id="c82d4-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="c82d4-107">Svi potporni redci stvaraju se u povezanim tablicama, poput dnevnika i stvarnih podataka.</span><span class="sxs-lookup"><span data-stu-id="c82d4-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="c82d4-108">Prije nego što nastavite, odobravatelj se u projektu označava kao **Odobravtelj projekta**.</span><span class="sxs-lookup"><span data-stu-id="c82d4-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]