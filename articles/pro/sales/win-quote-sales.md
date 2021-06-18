---
title: Zatvaranje ponude – jednostavno
description: U ovoj temi nalaze se informacije o zatvaranju ponude u aplikaciji Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994127"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="7ed48-103">Zatvaranje ponude – jednostavno</span><span class="sxs-lookup"><span data-stu-id="7ed48-103">Close a quote - lite</span></span>

<span data-ttu-id="7ed48-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="7ed48-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7ed48-105">Ponuda projekta mogu se zatvoriti kao ostvarene ili neostvarene.</span><span class="sxs-lookup"><span data-stu-id="7ed48-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="7ed48-106">Nacrt ponude može se zatvoriti jer operacije Aktiviranje i Revizija ponude nisu podržane u aplikaciji Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7ed48-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="7ed48-107">Zatvaranje ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="7ed48-107">Close a quote as Won</span></span>

<span data-ttu-id="7ed48-108">Kada ponudu za projekt zatvorite kao Dobivena, stanje se postavlja na Zatvorena, a razlog stanja je Dobiveno.</span><span class="sxs-lookup"><span data-stu-id="7ed48-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="7ed48-109">Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje i stvara nacrt ugovora o projektu koji sadrži podatke o ponudi.</span><span class="sxs-lookup"><span data-stu-id="7ed48-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="7ed48-110">Budući da se zatvorena ponuda ne može ponovo otvoriti, dijaloški okvir za potvrdu potvrdit će vaše promjene.</span><span class="sxs-lookup"><span data-stu-id="7ed48-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="7ed48-111">Ako je ponuda priložena uz priliku, svaka druga ponuda projekta za priliku automatski se zatvaraju kao Izgubljena.</span><span class="sxs-lookup"><span data-stu-id="7ed48-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="7ed48-112">Financijski utjecaj zatvaranja ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="7ed48-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="7ed48-113">Ako postoje stvarni podaci o vremenu utrošenom na projektu dok je još uvijek priložen nacrtu ponude, bilježe se samo troškovi vremena ili izdataka.</span><span class="sxs-lookup"><span data-stu-id="7ed48-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="7ed48-114">Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorirati troškove poništavanjem starijih stvarnih podataka o trošku i ponovnim stvaranjem novih stvarnih podataka o trošku.</span><span class="sxs-lookup"><span data-stu-id="7ed48-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="7ed48-115">Aplikacija će obraditi ove stvarne podatke o trošku na temelju metode naplate retka ugovora povezanog projekta.</span><span class="sxs-lookup"><span data-stu-id="7ed48-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="7ed48-116">Ako se stvarni podaci o troškovima odnose na redak ugovora o vremenu i materijalu, odgovarajući se nenaplaćeni stvarni podaci o prodaji stvaraju nakon zatvaranja ponude i stvaranja ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="7ed48-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="7ed48-117">Ako se stvarni trošak odnosi na redak ugovora s fiksnom cijenom, aplikacija će zaustaviti ponovnu obradu stvarnog troška koji se temelji na pravilima podijeljene naplate za klijente ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="7ed48-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="7ed48-118">Zatvaranje ponude kao neostvarene:</span><span class="sxs-lookup"><span data-stu-id="7ed48-118">Closing a quote as lost:</span></span>

<span data-ttu-id="7ed48-119">Kada ponudu za projekt zatvorite kao Izgubljenu, stanje se postavlja na Zatvorena, a razlog stanja je Izgubljena.</span><span class="sxs-lookup"><span data-stu-id="7ed48-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="7ed48-120">Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="7ed48-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="7ed48-121">Budući da se zatvorena ponuda ne može ponovno otvoriti, prije nego što zatvorite ponudu, dijaloški okvir potvrdit će vaše promjene.</span><span class="sxs-lookup"><span data-stu-id="7ed48-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="7ed48-122">Ako se ponuda projekta koja je zatvorena kao Izgubljena odnosi na neki od redaka projekta, taj se projekt također označuje kao Zatvoren.</span><span class="sxs-lookup"><span data-stu-id="7ed48-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="7ed48-123">Sve se rezervacije resursa od tog dana nadalje otkazuju.</span><span class="sxs-lookup"><span data-stu-id="7ed48-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="7ed48-124">U aplikaciji Project Operations zatvaranje ponude kao Ostvarene ili Neostvarene neće utjecati na status Prilike, koji će ostati otvoren sve dok se ručno ne zatvori.</span><span class="sxs-lookup"><span data-stu-id="7ed48-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]