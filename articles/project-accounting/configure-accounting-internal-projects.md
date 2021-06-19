---
title: Konfiguracija računovodstva za interne projekte
description: U ovoj temi nalaze se informacije o načinu postavljanja računovodstvene prakse za interne projekte u projektnim operacijama.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012847"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="b23c8-103">Konfiguracija računovodstva za interne projekte</span><span class="sxs-lookup"><span data-stu-id="b23c8-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="b23c8-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="b23c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b23c8-105">Interni projekti omogućuju tvrtkama praćenje troškova povezanih s aktivnostima koje se ne naplaćuju klijentu.</span><span class="sxs-lookup"><span data-stu-id="b23c8-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="b23c8-106">Primjeri internih projekata uključuju:</span><span class="sxs-lookup"><span data-stu-id="b23c8-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="b23c8-107">Razvoj proizvoda, poput mobilne aplikacije, i praćenje troškova povezanih s razvojem.</span><span class="sxs-lookup"><span data-stu-id="b23c8-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="b23c8-108">Upravljanje vremenom i troškovima pretprodaje.</span><span class="sxs-lookup"><span data-stu-id="b23c8-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="b23c8-109">Ovaj pretprodajni interni projekt može se kasnije pretvoriti u projekt koji se može naplatiti ako se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="b23c8-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="b23c8-110">Svaki projekt koji u aplikaciji Dynamics 365 Project Operations nije povezan s ugovorom, tretira se kao interni.</span><span class="sxs-lookup"><span data-stu-id="b23c8-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="b23c8-111">Profili troškova i prihoda projekta ne upotrebljavaju se za određivanje računovodstvenih pravila za projektne.</span><span class="sxs-lookup"><span data-stu-id="b23c8-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="b23c8-112">Interni trošak projekta uvijek se knjiži s pomoću načela dobiti i gubitka.</span><span class="sxs-lookup"><span data-stu-id="b23c8-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="b23c8-113">Računi glavne knjige za knjiženja definirani su na stranici **Postavljanje knjiženja u Glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="b23c8-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="b23c8-114">Vremenske transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Raspodjela plaća**.</span><span class="sxs-lookup"><span data-stu-id="b23c8-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="b23c8-115">Troškovne transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Račun poravnanja za troškove**.</span><span class="sxs-lookup"><span data-stu-id="b23c8-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="b23c8-116">Transakcije stavki knjiže se terećenjem računa **Trošak**, a u korist računa **Trošak – Stavka**.</span><span class="sxs-lookup"><span data-stu-id="b23c8-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="b23c8-117">Nakon što su transakcije knjižene u projekt, ako je projekt povezan s ugovorom o projektu, sustav poništava sve nakupljene transakcije i stvara nove naplative transakcije.</span><span class="sxs-lookup"><span data-stu-id="b23c8-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="b23c8-118">Transakcije koje se naplaćuju slijede računovodstvena pravila definirana u odgovarajućem profilu troškova i prihoda projekta.</span><span class="sxs-lookup"><span data-stu-id="b23c8-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
