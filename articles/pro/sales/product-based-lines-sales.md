---
title: Redci prilike koji se temelje na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o stavkama retka prilike koji se temelji na proizvodu u aplikaciji Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7865da682ae607f017bf59ce1ae1addc9fefa60b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994487"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="d46d5-103">Redci prilike koji se temelje na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="d46d5-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="d46d5-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="d46d5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d46d5-105">Redci prilike koji se temelje na proizvodu stavke su retka u Prilici.</span><span class="sxs-lookup"><span data-stu-id="d46d5-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="d46d5-106">Te se različite stavke redaka nalaze na konačnoj fakturi koja se daje klijentu.</span><span class="sxs-lookup"><span data-stu-id="d46d5-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="d46d5-107">Faktura ne uključuje neke druge dodatne usluge.</span><span class="sxs-lookup"><span data-stu-id="d46d5-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="d46d5-108">Povezani trošak i potrošnja ne prate se na zadacima bilo kojih povezanih projekata.</span><span class="sxs-lookup"><span data-stu-id="d46d5-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="d46d5-109">Redci koji se temelje na proizvodu mogu biti stavke iz kataloga ili proizvodi koji se upisuju.</span><span class="sxs-lookup"><span data-stu-id="d46d5-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="d46d5-110">Većina funkcionalnosti na redcima prilike koji se temelje na proizvodu slijedi funkcionalnost koju pruža aplikacija Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d46d5-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="d46d5-111">Dodatne informacije o redcima prilike koji se temelje na proizvodima potražite u članku [Dodavanje proizvoda prilici](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="d46d5-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="d46d5-112">**Proračun klijenta** je koncept specifičan za retke prilika koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="d46d5-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="d46d5-113">Polje **Proračun klijenta** prati iznos koji je klijent spreman platiti za stavku.</span><span class="sxs-lookup"><span data-stu-id="d46d5-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="d46d5-114">Kada je metoda prihoda sažetka Prilike **Izračunao sustav**, vrijednosti proračuna klijenta u redcima prilika zbrojene su kako bi se izračunao procijenjeni prihod.</span><span class="sxs-lookup"><span data-stu-id="d46d5-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]