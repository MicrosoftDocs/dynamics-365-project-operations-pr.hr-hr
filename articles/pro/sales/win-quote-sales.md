---
title: Zatvaranje ponuda
description: U ovoj temi nalaze se informacije o zatvaranju ponude u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896182"
---
# <a name="close-quotes"></a><span data-ttu-id="dfa45-103">Zatvaranje ponuda</span><span class="sxs-lookup"><span data-stu-id="dfa45-103">Close quotes</span></span> 

<span data-ttu-id="dfa45-104">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="dfa45-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dfa45-105">Ponuda projekta mogu se zatvoriti kao ostvarene ili neostvarene.</span><span class="sxs-lookup"><span data-stu-id="dfa45-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="dfa45-106">Operacije aktiviranja i revizije ponuda nisu podržane u aplikaciji Microsoft Dynamics 365 Project Operations, tako da se nacrt ponude može zatvoriti.</span><span class="sxs-lookup"><span data-stu-id="dfa45-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="dfa45-107">Zatvaranje ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="dfa45-107">Close a quote as Won</span></span>

<span data-ttu-id="dfa45-108">Zatvaranje ponude za projekt kao Ostvarene zatvorit će ponudu sa statusom postavljenim na Zatvorena i razlogom statusa postavljenim na Ostvaren.</span><span class="sxs-lookup"><span data-stu-id="dfa45-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="dfa45-109">Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje i stvara nacrt ugovora o projektu koji sadrži podatke o ponudi.</span><span class="sxs-lookup"><span data-stu-id="dfa45-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="dfa45-110">Postoji dijaloški okvir za potvrdu prije nego što se promjene izvrše, jer se zatvorena ponuda ne može ponovo otvoriti i promjene su nepovratne.</span><span class="sxs-lookup"><span data-stu-id="dfa45-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="dfa45-111">Ako je ponuda priložena uz priliku, svaka druga ponuda projekta za priliku automatski se zatvaraju kao Izgubljena.</span><span class="sxs-lookup"><span data-stu-id="dfa45-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="dfa45-112">Financijski utjecaj zatvaranja ponude kao ostvarene</span><span class="sxs-lookup"><span data-stu-id="dfa45-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="dfa45-113">Ako postoje stvarni podaci o vremenu zabilježenom na projektu, dok je on još uvijek priložen nacrtu ponude, bilježe se samo troškovi vremena ili izdataka.</span><span class="sxs-lookup"><span data-stu-id="dfa45-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="dfa45-114">Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorirati troškove poništavanjem starijih stvarnih podataka o trošku i ponovnim stvaranjem novih stvarnih podataka o trošku.</span><span class="sxs-lookup"><span data-stu-id="dfa45-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="dfa45-115">Aplikacija će obraditi ove stvarne podatke o trošku na temelju metode naplate retka ugovora povezanog projekta.</span><span class="sxs-lookup"><span data-stu-id="dfa45-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="dfa45-116">Ako se stvarni podaci o trošku odnose na redak ugovora o vremenu i materijalu, sustav će automatski stvoriti odgovarajuće nenaplaćene stvarne prodajne podatke za vrijeme zatvaranja ponude i izrade ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="dfa45-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="dfa45-117">Ako se stvarni podaci o trošku odnose na redak ugovora s fiksnom cijenom, aplikacija će zaustaviti ponovnu obradu stvarnih podataka o trošku na temelju pravila podijeljene naplate za klijente ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="dfa45-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="dfa45-118">Zatvaranje ponude kao neostvarene:</span><span class="sxs-lookup"><span data-stu-id="dfa45-118">Closing a quote as lost:</span></span>

<span data-ttu-id="dfa45-119">Zatvaranjem ponude projekta kao neostvarene postavit će status na Zatvoreno, a razlog statusa na Izgubljena.</span><span class="sxs-lookup"><span data-stu-id="dfa45-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="dfa45-120">Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="dfa45-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="dfa45-121">Budući da se zatvorena ponuda ne može ponovno otvoriti, prije nego što zatvorite ponudu, dijaloški okvir potvrdit će vaše promjene.</span><span class="sxs-lookup"><span data-stu-id="dfa45-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="dfa45-122">Ako ponuda projekta koja je zatvorena kao Izgubljena ima projekt naveden na nekom od svojih redaka, taj projekt se također označava kao Zatvoren i sve rezervacije resursa od toga dana nadalje otkazuju se.</span><span class="sxs-lookup"><span data-stu-id="dfa45-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="dfa45-123">U aplikaciji Project Operations zatvaranje ponude kao Ostvarene ili Neostvarene neće utjecati na status Prilike, koji će ostati otvoren sve dok se ručno ne zatvori.</span><span class="sxs-lookup"><span data-stu-id="dfa45-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
