---
title: Pregled fakturiranja unutar tvrtke
description: U ovoj temi nalaze se informacije i primjeri o načinu fakturiranja projekata unutar tvrtke.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595439"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="7f660-103">Pregled fakturiranja unutar tvrtke</span><span class="sxs-lookup"><span data-stu-id="7f660-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="7f660-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="7f660-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7f660-105">Vaša tvrtka ili ustanova može imati više sektora, podružnica i drugih pravnih osoba koje međusobno prenose proizvode i usluge za projekte.</span><span class="sxs-lookup"><span data-stu-id="7f660-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="7f660-106">Pravna osoba koja osigurava uslugu ili proizvod naziva se *pravna osoba koja kreditira*.</span><span class="sxs-lookup"><span data-stu-id="7f660-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="7f660-107">Pravna osoba koja prima uslugu ili proizvod naziva se *pravna osoba koja se zadužuje*.</span><span class="sxs-lookup"><span data-stu-id="7f660-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="7f660-108">Sljedeća ilustracija prikazuje uobičajeni scenarij u kojem dvije pravne osobe, Contoso Robotics USA (pravna osoba koja se zadužuje) i Contoso Robotics UK (pravna osoba koja kreditira) dijele resurse kako bi se isporučio projekt kupcu, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="7f660-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="7f660-109">Za ovaj scenarij unajmljena je tvrtka Contoso Robotics USA da posao isporuči tvrtki Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="7f660-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Fakturiranje unutar tvrtke](./media/IntercompanyScenario.png) 

<span data-ttu-id="7f660-111">Dynamics 365 Project Operations upotrebljava sljedeći tijek za obradu transakcija unutar tvrtke:</span><span class="sxs-lookup"><span data-stu-id="7f660-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="7f660-112">Resursi iz pravne osobe koja kreditira bilježe transakcije vremena ili troška unutar tvrtke rezervirajući vrijeme i trošak za projekte u pravnoj osobi koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="7f660-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="7f660-113">Troškovi vremena i koštanja zapisuju se u tvrtku koja kreditira s pomoću cjenika troškova jedinice tvrtke koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="7f660-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="7f660-114">Prodajne transakcije nenaplaćene unutar tvrtke evidentiraju se u tvrtku koja kreditira s pomoću cjenika troškova jedinice tvrtke koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="7f660-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="7f660-115">Nenaplaćeni prihod evidentira se u tvrtki koja se zadužuje s pomoću prodajnog cjenika ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="7f660-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="7f660-116">Klijentu se može naplatiti kada se evidentira nefakturirani prihod.</span><span class="sxs-lookup"><span data-stu-id="7f660-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="7f660-117">Klijent ne mora čekati završetak obrade fakture unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="7f660-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="7f660-118">Fakture za klijenta unutar tvrtke stvaraju se periodično u tvrtki koja kreditira.</span><span class="sxs-lookup"><span data-stu-id="7f660-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="7f660-119">Fakture se stvaraju ručno ili uporabom periodičnog automatiziranog postupka.</span><span class="sxs-lookup"><span data-stu-id="7f660-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="7f660-120">Za svaku pravnu osobu koja se zadužuje može se stvoriti pojedinačna faktura ili projekt može stvoriti zasebne fakture.</span><span class="sxs-lookup"><span data-stu-id="7f660-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="7f660-121">Kada se račun za klijenta unutar tvrtke knjiži u pravnoj osobi koja kreditira, u pravnoj osobi koja se zadužuje stvara se odgovarajuća faktura dobavljača na čekanju.</span><span class="sxs-lookup"><span data-stu-id="7f660-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="7f660-122">Troškovi na fakturi dobavljača na čekanju evidentirat će se u sporednoj knjizi projekta kada se faktura proknjiži.</span><span class="sxs-lookup"><span data-stu-id="7f660-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="7f660-123">Sljedeći dijagram ilustrira fakturiranje unutar tvrtke koje se odnosi na računovodstvene događaje i očekivana knjiženja u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="7f660-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Tijek rada unutar tvrtke](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="7f660-125">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="7f660-125">Additional resources</span></span>

- [<span data-ttu-id="7f660-126">Konfiguriranje fakturiranja unutar tvrtke</span><span class="sxs-lookup"><span data-stu-id="7f660-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="7f660-127">Bilježenje transakcija unutar tvrtke</span><span class="sxs-lookup"><span data-stu-id="7f660-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="7f660-128">Stvaranje faktura klijenta i dobavljača unutar tvrtke</span><span class="sxs-lookup"><span data-stu-id="7f660-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
