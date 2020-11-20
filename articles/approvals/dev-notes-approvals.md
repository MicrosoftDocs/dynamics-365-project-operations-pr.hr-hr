---
title: Bilješke razvojnog inženjera za odobrenja
description: U ovoj temi nalaze se dodatne informacije za razvojne inženjere o radu s odobrenjima.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483939"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="2b247-103">Bilješke razvojnog inženjera za odobrenja</span><span class="sxs-lookup"><span data-stu-id="2b247-103">Developer notes for Approvals</span></span>

<span data-ttu-id="2b247-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="2b247-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b247-105">Dynamics 365 Project Operations uključuje logiku provjere valjanosti koja osigurava ispravan prijelaz zapisa kroz faze odobrenja.</span><span class="sxs-lookup"><span data-stu-id="2b247-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="2b247-106">Ispravni prijelazi zapisa osiguravaju sljedeće:</span><span class="sxs-lookup"><span data-stu-id="2b247-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="2b247-107">Svi potporni redci stvaraju se u povezanim tablicama, poput dnevnika i stvarnih podataka.</span><span class="sxs-lookup"><span data-stu-id="2b247-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="2b247-108">Prije nego što nastavite, odobravatelj se u projektu označava kao **Odobravtelj projekta**.</span><span class="sxs-lookup"><span data-stu-id="2b247-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
