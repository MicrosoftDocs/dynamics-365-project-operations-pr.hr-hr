---
title: Konfiguracija računovodstva za interne projekte
description: U ovoj temi nalaze se informacije o načinu postavljanja računovodstvene prakse za interne projekte u projektnim operacijama.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287589"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="12241-103">Konfiguracija računovodstva za interne projekte</span><span class="sxs-lookup"><span data-stu-id="12241-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="12241-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="12241-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="12241-105">Interni projekti omogućuju tvrtkama praćenje troškova povezanih s aktivnostima koje se ne naplaćuju klijentu.</span><span class="sxs-lookup"><span data-stu-id="12241-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="12241-106">Primjeri internih projekata uključuju:</span><span class="sxs-lookup"><span data-stu-id="12241-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="12241-107">Razvoj proizvoda, poput mobilne aplikacije, i praćenje troškova povezanih s razvojem.</span><span class="sxs-lookup"><span data-stu-id="12241-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="12241-108">Upravljanje vremenom i troškovima pretprodaje.</span><span class="sxs-lookup"><span data-stu-id="12241-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="12241-109">Ovaj pretprodajni interni projekt može se kasnije pretvoriti u projekt koji se može naplatiti ako se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="12241-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="12241-110">Svaki projekt koji u aplikaciji Dynamics 365 Project Operations nije povezan s ugovorom, tretira se kao interni.</span><span class="sxs-lookup"><span data-stu-id="12241-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="12241-111">Profili troškova i prihoda projekta ne upotrebljavaju se za određivanje računovodstvenih pravila za projektne.</span><span class="sxs-lookup"><span data-stu-id="12241-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="12241-112">Interni trošak projekta uvijek se knjiži s pomoću načela dobiti i gubitka.</span><span class="sxs-lookup"><span data-stu-id="12241-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="12241-113">Računi glavne knjige za knjiženja definirani su na stranici **Postavljanje knjiženja u Glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="12241-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="12241-114">Vremenske transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Raspodjela plaća**.</span><span class="sxs-lookup"><span data-stu-id="12241-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="12241-115">Troškovne transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Račun poravnanja za troškove**.</span><span class="sxs-lookup"><span data-stu-id="12241-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="12241-116">Nakon što su transakcije knjižene u projekt, ako je projekt povezan s ugovorom o projektu, sustav poništava sve nakupljene transakcije i stvara nove naplative transakcije.</span><span class="sxs-lookup"><span data-stu-id="12241-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="12241-117">Transakcije koje se naplaćuju slijede računovodstvena pravila definirana u odgovarajućem profilu troškova i prihoda projekta.</span><span class="sxs-lookup"><span data-stu-id="12241-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]