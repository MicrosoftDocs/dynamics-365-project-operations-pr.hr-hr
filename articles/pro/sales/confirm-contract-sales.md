---
title: Potvrda ugovora o projektu
description: U ovoj temi nalaze se informacije o načinu potvrde ugovora u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073508"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="ddd4b-103">Potvrda ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="ddd4b-103">Confirm a project contract</span></span>

<span data-ttu-id="ddd4b-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="ddd4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ddd4b-105">Ugovor o projektu u aplikaciji Dynamics 365 Project Operations može biti aktivan s razlogom **Potvrđeno** ili zatvoren s razlogom **Izgubljeno**.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed** , or closed with a reason of **Lost**.</span></span> <span data-ttu-id="ddd4b-106">Kada potvrdite ugovor o projektu, status se ažurira iz **Nacrt** u **Aktivan** , a razlog statusa je **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="ddd4b-107">Aktivni ili zatvoreni ugovor ne može se uređivati ili ponovno otvarati.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="ddd4b-108">Financijski učinak potvrde ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="ddd4b-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="ddd4b-109">Nakon potvrde ugovora o projektu, aplikacija će preračunati troškove storniranjem starijih stvarnih troškova i stvaranjem novih.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="ddd4b-110">Novi stvarni podaci o trošku zatim se obrađuju na temelju načina naplate retka ugovora povezanog projekta.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="ddd4b-111">Ako se stvarni podaci o troškovima odnose na redak ugovora za vrijeme i materijal, aplikacija automatski ponovno stvara odgovarajuće nenaplaćene stvarne podatke prodaje.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="ddd4b-112">Ako se stvarni podaci o troškovima odnose na redak ugovora s fiksnom cijenom, aplikacija zaustavlja ponovnu obradu stvarnih podataka o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="ddd4b-113">Ograničenja koja se ne smiju prekoračiti, postavljanje naplativosti te utvrđivanje cijena i troškova na stvarnim podacima procjenjuju se, a zatim ažuriraju kao dio postupka potvrde.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="ddd4b-114">Zatvaranje ugovora o projektu kao izgubljenog</span><span class="sxs-lookup"><span data-stu-id="ddd4b-114">Close a project contract as lost</span></span>

<span data-ttu-id="ddd4b-115">Kada ugovor o projektu zatvorite kao izgubljen, status ugovora ažurira se na **Zatvoreno** a razlog statusa je **Izgubljeno**.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="ddd4b-116">Ugovor o projektu postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-116">The project contract becomes read-only.</span></span> <span data-ttu-id="ddd4b-117">Dijaloški okvir za potvrdu osiguran je prije dovršetka promjena jer ne možete ponovo otvoriti zatvoreni ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="ddd4b-118">Ako se ugovor o projektu koji je zatvoren kao izgubljen u svojim redcima poziva na projekt i taj se projekt označava kao zatvoren.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="ddd4b-119">Sve se rezervacije resursa od tog dana nadalje otkazuju.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="ddd4b-120">Svi stvarni podaci nenaplaćene prodaje iz ugovora o projektu koji još nisu na računu, stornirat će se.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="ddd4b-121">Zatvaranje ugovora o projektu kao izgubljenog u aplikaciji Dynamics 365 Project Operations, neće utjecati na taj status povezane prilike.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="ddd4b-122">Prilika će ostati otvorena i mora se ručno zatvoriti.</span><span class="sxs-lookup"><span data-stu-id="ddd4b-122">The opportunity will remain open and must be manually closed.</span></span>
