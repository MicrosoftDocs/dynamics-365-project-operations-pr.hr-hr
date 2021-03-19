---
title: Ključni koncepti upravljanja resursima
description: U ovoj temi nalaze se informacije o mogućnostima Upravljanja resursima u aplikaciji Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bcdfc7296ec09421668673d8502e7103c887d667
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279489"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="2b107-103">Ključni koncepti upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="2b107-103">Resource management key concepts</span></span>

<span data-ttu-id="2b107-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="2b107-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b107-105">Resursi su najvažnije sredstvo za tvrtke ili ustanove koje su utemeljene na uslugama.</span><span class="sxs-lookup"><span data-stu-id="2b107-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="2b107-106">Mogućnost pronalaženja pravih resursa u pravo vrijeme, rezerviranje tih resursa u projektima i iskorištavanje tih resursa omogućuju da tvrtka ili ustanova ostvari ciljeve prihoda i zadovoljstva klijenata.</span><span class="sxs-lookup"><span data-stu-id="2b107-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="2b107-107">Funkcionalnost raspodjele resursa na projektu u aplikaciji Dynamics 365 Project Operations možete upotrebljavati za sljedeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="2b107-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="2b107-108">Formiranje projektnih timova rezerviranjem dostupnih i kvalificiranih resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="2b107-109">Stvaranje zapisa o članu generičkog tima i definiranje uloga i organizacijske jedinice resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="2b107-110">Generiranje preduvjeta resursa za članove generičkog tima iz njihove dodjele zadataka.</span><span class="sxs-lookup"><span data-stu-id="2b107-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="2b107-111">Usporedba vještina identificiranjem vještina definiranih u potražnji resursa u odnosu na vještine dostupnog resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="2b107-112">Zamjena resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-112">Substitute resources.</span></span>
- <span data-ttu-id="2b107-113">Poravnavanje dodjele rasporeda projekta i rezervacije resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="2b107-114">Usklađivanje razlika u rezervacijama i dodjelama.</span><span class="sxs-lookup"><span data-stu-id="2b107-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="2b107-115">Promjena rezervacija resursa kao odgovor na status izvan ureda.</span><span class="sxs-lookup"><span data-stu-id="2b107-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="2b107-116">Suradnja između voditelja projekata i upravitelja resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="2b107-117">Prikaz povijesti upotrebe resursa prema cilju, uključujući analizu načina iskorištavanja vremena resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="2b107-118">Održavanje spremišta vještina i stručnosti.</span><span class="sxs-lookup"><span data-stu-id="2b107-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="2b107-119">Projektu u aplikaciji Project Operations može se dodijeliti tim generičkih ili imenovanih resursa.</span><span class="sxs-lookup"><span data-stu-id="2b107-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="2b107-120">Možete koristiti različite metode za dodavanje i dodjeljivanje članova tima te upravljanje njihovim rezervacijama i dodjelama.</span><span class="sxs-lookup"><span data-stu-id="2b107-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]