---
title: Stvaranje ručnog predračuna – jednostavno
description: U ovoj temi nalaze se informacije o načinu stvaranja ručnog predračuna u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274179"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="93f7b-103">Stvaranje ručnog predračuna – jednostavno</span><span class="sxs-lookup"><span data-stu-id="93f7b-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="93f7b-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="93f7b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="93f7b-105">U aplikaciji Dynamics 365 Project Operations, predračuni se po potrebi mogu stvarati ručno.</span><span class="sxs-lookup"><span data-stu-id="93f7b-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="93f7b-106">Možete ručno stvoriti predračun sa stranice s popisom **Ugovori o projektu** ili sa stranice s pojedinostima stavke **Ugovor o projektu**.</span><span class="sxs-lookup"><span data-stu-id="93f7b-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="93f7b-107">stranica s popisom ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="93f7b-107">Project Contracts list page</span></span>

<span data-ttu-id="93f7b-108">Na stranici s popisom **Ugovori o projektu** odaberite jedan ili više ugovora o projektu i stvorite račune za sve odabrane zapise.</span><span class="sxs-lookup"><span data-stu-id="93f7b-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="93f7b-109">Sustav provjerava koji od odabranih ugovora o projektu ima zaostale nefakturirane zadatke sa statusom **Spremni za fakturiranje** datirane prije današnjeg datuma.</span><span class="sxs-lookup"><span data-stu-id="93f7b-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="93f7b-110">Iz tih ugovora sustav stvara nacrte predračuna.</span><span class="sxs-lookup"><span data-stu-id="93f7b-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="93f7b-111">Ako projektni ugovor ima više klijenata, može se stvoriti jedna faktura po klijentu i više faktura po ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="93f7b-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="93f7b-112">Sve stvorene fakture za projekt dostupne su na stranici **Faktura** u odjeljku **Naplata** područja **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="93f7b-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="93f7b-113">Stranica s pojedinostima ugovora o projektu</span><span class="sxs-lookup"><span data-stu-id="93f7b-113">Project Contract details page</span></span>

<span data-ttu-id="93f7b-114">Predračun se također može stvoriti sa stranice s pojedinostima **Ugovor o projektu**.</span><span class="sxs-lookup"><span data-stu-id="93f7b-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="93f7b-115">Sustav provjerava ima li ugovor o projektu zaostalih nefakturiranih zadataka sa statusom **Spremni za fakturiranje** datiranih prije današnjeg datuma.</span><span class="sxs-lookup"><span data-stu-id="93f7b-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="93f7b-116">Iz tih ugovora sustav stvara nacrt predračuna na temelju broja klijenata u svakom retku ugovora.</span><span class="sxs-lookup"><span data-stu-id="93f7b-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="93f7b-117">Kada se stvori jedan predračun, otvara se stranica **Račun**.</span><span class="sxs-lookup"><span data-stu-id="93f7b-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="93f7b-118">Ako se stvori više računa za taj ugovor o projektu, otvara se stranica s popisom **Fakture** kako bi se prikazale sve stvorene fakture.</span><span class="sxs-lookup"><span data-stu-id="93f7b-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]