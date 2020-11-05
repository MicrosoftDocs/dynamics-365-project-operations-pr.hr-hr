---
title: Redci prilike koji ser temelje na proizvodu
description: U ovoj temi nalaze se informacije o stavkama retka prilike koji se temelji na proizvodu u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073314"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="5d991-103">Redci prilike koji ser temelje na proizvodu</span><span class="sxs-lookup"><span data-stu-id="5d991-103">Product-based opportunity lines</span></span>

<span data-ttu-id="5d991-104">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="5d991-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d991-105">Redci prilike koji se temelje na proizvodu stavke su retka u Prilici.</span><span class="sxs-lookup"><span data-stu-id="5d991-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="5d991-106">Ti se redci dostavljaju kupcu kao zasebne stavke retka na konačnom računu bez ikakvih drugih usluga s dodanom vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="5d991-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="5d991-107">Povezani trošak i potrošnja ne prate se na zadacima bilo kojih povezanih projekata.</span><span class="sxs-lookup"><span data-stu-id="5d991-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="5d991-108">Redci koji se temelje na proizvodu mogu biti stavke iz kataloga ili proizvodi koji se upisuju.</span><span class="sxs-lookup"><span data-stu-id="5d991-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="5d991-109">Većina funkcionalnosti na redcima prilike koji se temelje na proizvodu slijedi funkcionalnost koju pruža aplikacija Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5d991-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="5d991-110">Dodatne informacije o redcima prilike koji se temelje na proizvodima potražite u članku [Dodavanje proizvoda prilici](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="5d991-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="5d991-111">Jedan koncept o redcima prilike koji se temelje na proizvodu koji je specifičan za priliku koja se temelji na projektu jest **Proračun klijenta**.</span><span class="sxs-lookup"><span data-stu-id="5d991-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="5d991-112">Ovo polje upotrebljavajte za praćenje iznosa koji je kupac spreman platiti za stavku retka.</span><span class="sxs-lookup"><span data-stu-id="5d991-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="5d991-113">Ako je metoda prihoda sažetka Prilike postavljena na **Izračunao sustav** , proračunske vrijednosti klijenta u svim redcima koji se temelje na proizvodu i projektu sažete su kako bi se izračunao procijenjeni prihod.</span><span class="sxs-lookup"><span data-stu-id="5d991-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
