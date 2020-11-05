---
title: Stvaranje ručnog predračuna
description: U ovoj temi nalaze se informacije o načinu stvaranja ručnog predračuna u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4073617"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="ef3dd-103">Stvaranje ručnog predračuna</span><span class="sxs-lookup"><span data-stu-id="ef3dd-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="ef3dd-104">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="ef3dd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ef3dd-105">Predračuni se u aplikaciji Dynamics 365 Project Operations, po potrebi mogu stvoriti ručno.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="ef3dd-106">Možete ručno stvoriti predračun sa stranice s popisom **Ugovori o projektu** ili sa stranice s pojedinostima stavke **Ugovor o projektu**.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="ef3dd-107">stranica s popisom ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="ef3dd-107">Project Contracts list page</span></span>

<span data-ttu-id="ef3dd-108">Na stranici s popisom **Ugovori o projektu** odaberite jedan ili više ugovora o projektu i stvorite račune za sve odabrane zapise.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="ef3dd-109">Sustav provjerava koji od odabranih ugovora o projektu ima zaostale nefakturirane zadatke **Spremni za fakturiranje** datirane prije današnjeg datuma.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="ef3dd-110">Iz tih ugovora sustav stvara nacrte predračuna.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="ef3dd-111">Ako projektni ugovor ima više klijenata, može se stvoriti jedna faktura po kupcu i više faktura po ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="ef3dd-112">Sve stvorene fakture za projekt dostupne su na stranici **Faktura** u odjeljku **Naplata** područja **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="ef3dd-113">Stranica s pojedinostima ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="ef3dd-113">Project Contract details page</span></span>

<span data-ttu-id="ef3dd-114">Predračun se može stvoriti i sa stranice s pojedinostima **Ugovor o projektu** koja stvara fakturu za taj određeni ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="ef3dd-115">Sustav provjerava ima li ugovor o projektu zaostale nefakturirane zadatke **Spremni za fakturiranje** datirane prije današnjeg datuma.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="ef3dd-116">Iz tih ugovora sustav stvara nacrt predračuna na temelju broja klijenata u svakom retku ugovora.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="ef3dd-117">Kada se stvori jedan predračun, otvara se stranica **Račun**.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="ef3dd-118">Ako postoji više računa izrađenih za taj ugovor o projektu, tada se otvara stranica s popisom **Računi** za prikaz svih stvorenih faktura.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
