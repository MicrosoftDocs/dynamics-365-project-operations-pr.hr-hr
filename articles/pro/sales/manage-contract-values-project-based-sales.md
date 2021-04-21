---
title: Pregled redaka ugovora koji se temelje na projektu
description: U ovoj temi nalaze se informacije o radu s redcima ugovora koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858149"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="b9e4e-103">Pregled redaka ugovora koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="b9e4e-103">Project-based contract lines overview</span></span>

<span data-ttu-id="b9e4e-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b9e4e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b9e4e-105">Redci ugovora koji se temelje na projektu u aplikaciji Dynamics 365 Project Operations dizajnirani su da drže angažirane ugovore o procjeni i naplati za određene komponente projektnog rada.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="b9e4e-106">Struktura retka ugovora koji se temelji na projektu proširena je za procjene projekta i scenarije naplate sa sljedećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="b9e4e-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="b9e4e-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="b9e4e-107">Billing method</span></span>
- <span data-ttu-id="b9e4e-108">Mapiranje projekta i zadatka</span><span class="sxs-lookup"><span data-stu-id="b9e4e-108">Project and task mapping</span></span>
- <span data-ttu-id="b9e4e-109">Uključene klase transakcije</span><span class="sxs-lookup"><span data-stu-id="b9e4e-109">Included transaction classes</span></span>
- <span data-ttu-id="b9e4e-110">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="b9e4e-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="b9e4e-111">Postavka naplativosti</span><span class="sxs-lookup"><span data-stu-id="b9e4e-111">Chargeability setup</span></span>
- <span data-ttu-id="b9e4e-112">Procjene s pomoću pojedinosti retka ugovora</span><span class="sxs-lookup"><span data-stu-id="b9e4e-112">Estimates using contract line details</span></span>
- <span data-ttu-id="b9e4e-113">Klijenti retka ugovora</span><span class="sxs-lookup"><span data-stu-id="b9e4e-113">Contract line customers</span></span>

<span data-ttu-id="b9e4e-114">Sljedeća tablica uključuje polja na kartici **Općenito** redaka ugovora koji se temelje na projektu koji pomažu u postavljanju osnove za podrobnu, temeljnu procjenu i aranžmane naplate za posao koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="b9e4e-115">Polje</span><span class="sxs-lookup"><span data-stu-id="b9e4e-115">Field</span></span> | <span data-ttu-id="b9e4e-116">Opis</span><span class="sxs-lookup"><span data-stu-id="b9e4e-116">Description</span></span> | <span data-ttu-id="b9e4e-117">Utjecaj na niže razine</span><span class="sxs-lookup"><span data-stu-id="b9e4e-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b9e4e-118">**Ime**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-118">**Name**</span></span> | <span data-ttu-id="b9e4e-119">Naziv retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-119">Name of the contract line.</span></span> <span data-ttu-id="b9e4e-120">Ovo identificira određenu komponentu ugovora koja se procjenjuje.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="b9e4e-121">Za ugovor o projektu stvoren iz ponude, ova se vrijednost kopira iz odgovarajuće vrijednosti retka ponude koja se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="b9e4e-122">Naziv koji se kopira na redak fakture za projekt koji se stvara iz ovog retka kada se stvara faktura.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="b9e4e-123">**Način naplate**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-123">**Billing Method**</span></span> | <span data-ttu-id="b9e4e-124">U ugovoru o projektu stvorenom iz ponude ova se vrijednost kopira iz odgovarajućeg polja retka ponude.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="b9e4e-125">Ovo je skup mogućnosti koji predstavlja dva glavna modela ugovaranja koje podržava aplikacija Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b9e4e-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="b9e4e-126">- **Fiksna cijena**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-126">- **Fixed Price**</span></span></br><span data-ttu-id="b9e4e-127">- **Vrijeme i materijal**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-127">- **Time and Material**</span></span> | <span data-ttu-id="b9e4e-128">Na temelju načina naplate navedenog retka ugovora, obradit će se stvarna transakcija.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="b9e4e-129">Ako redak ugovora na koji se odnosi stvarna vrijednost ima način naplate vremena i materijala, stvaraju se stvarni zapisi troška i nenaplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="b9e4e-130">Ako redak ugovora na koji se poziva stvarni podatak ima način naplate s fiksnom cijenom, stvara se samo stvarni trošak.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="b9e4e-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-131">**Project**</span></span> | <span data-ttu-id="b9e4e-132">Upotrijebite ovo polje za identificiranje projekta koji će se upotrijebiti za izvođenje posla na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="b9e4e-133">Ova vrijednost koristit će se zajedno sa mogućnostima **Uključeni zadaci** i **Uključeni razredi transakcija** kako bi se razriješila referenca retka ugovora na stvarnom ili procijenjenom zapisu u retku.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="b9e4e-134">**Uključeni zadaci**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-134">**Included Tasks**</span></span> | <span data-ttu-id="b9e4e-135">Označava uključuje li ovaj redak ugovora sve projektne zadatke za odabrani projekt ili samo podskup zadataka.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="b9e4e-136">To je skup mogućnosti koji ima sljedeće moguće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="b9e4e-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="b9e4e-137">- **Svi zadaci projekta**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-137">- **All Project Tasks**</span></span></br><span data-ttu-id="b9e4e-138">- **Samo odabrani projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="b9e4e-139">Prazna vrijednost u ovom polju jednaka je odabiru **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="b9e4e-140">Ako se odabere **Samo odabrani zadaci**, možete odabrati određene zadatke i povezati ih s ovim retkom ugovora na kartici **Postavljanje naplate zadatka** na stranici **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="b9e4e-141">Ta vrijednost upotrijebit će se zajedno sa klasama **Projekt** i **Uključena transakcija** za rješavanje reference retka ugovora na stvarnom ili procijenjenom zapisu.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b9e4e-142">**Uvrsti vrijeme**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-142">**Include Time**</span></span> | <span data-ttu-id="b9e4e-143">Vrijednost **Da**/**Ne** pokazuje hoće li se vremenske transakcije ili troškovi rada na odabranom projektu uključiti u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b9e4e-144">Vrijednost **Ne** znači da vremenske transakcije ili trošak rada neće biti uključeni u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="b9e4e-145">Vrijednost **Da** označava da hoće.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="b9e4e-146">Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b9e4e-147">**Uvrsti trošak**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-147">**Include Expense**</span></span> | <span data-ttu-id="b9e4e-148">Vrijednost **Da**/**Ne** označava hoće li se troškovi izdataka na odabranom projektu uključiti u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b9e4e-149">Vrijednost **Ne** znači da cijena troška neće biti uključena u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="b9e4e-150">Vrijednost **Da** označava da hoće.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="b9e4e-151">Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b9e4e-152">**Uključi materijale**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-152">**Include Materials**</span></span> | <span data-ttu-id="b9e4e-153">Vrijednost **Da**/**Ne** označava hoće li se troškovi materijala na odabranom projektu uključiti u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b9e4e-154">Vrijednost **Ne** označava da se troškovi materijala neće uključiti u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="b9e4e-155">Vrijednost **Da** označava da hoće.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="b9e4e-156">Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b9e4e-157">**Uvrsti naknadu**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-157">**Include Fee**</span></span> | <span data-ttu-id="b9e4e-158">Vrijednost **Da**/**Ne** označava hoće li se naknade na odabranom projektu uključiti u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="b9e4e-159">Vrijednost **Ne** znači da naknade neće biti uključene u ovaj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="b9e4e-160">Vrijednost **Da** označava da hoće.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="b9e4e-161">Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="b9e4e-162">**Ugovoreni iznos**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-162">**Contracted Amount**</span></span> | <span data-ttu-id="b9e4e-163">Na retku ugovora s fiksnom cijenom ovaj je iznos dogovorena vrijednost koja će se fakturirati klijentu za sve komponente posla povezane s ovim retkom ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="b9e4e-164">Na retku ugovora za vrijeme i materijal ovaj je iznos procijenjena vrijednost onoga što će se fakturirati klijentu za sve komponente posla povezane s ovim retkom ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="b9e4e-165">U ugovoru o projektu stvorenom iz ponude ova se vrijednost kopira iz odgovarajućeg polja retka ponude.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="b9e4e-166">Kada redak ugovora koji se temelji na projektu ima pojedinosti retka, ovo je polje zaključano za uređivanje i sažeto je od iznosa pojedinosti retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="b9e4e-167">Kada redak ugovora sadrži pojedinosti o retku, ta se vrijednost može izmijeniti promjenom iznosa na pojedinostima retka.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="b9e4e-168">Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje iznosa prije poreza na periodičnim kontrolnim točkama naplate.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="b9e4e-169">**Procijenjeni porez**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-169">**Estimated Tax**</span></span> | <span data-ttu-id="b9e4e-170">Korisnik može urediti ovo polje za unos procijenjenog iznosa poreza u redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="b9e4e-171">Kada redak ugovora koji se temelji na projektu ima pojedinosti retka, ovo je polje zaključano za uređivanje i sažeto je od iznosa poreza u pojedinostima retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="b9e4e-172">Kada redak ugovora sadrži pojedinosti o retku, ta se vrijednost može izmijeniti promjenom iznosa poreza na pojedinostima retka.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="b9e4e-173">Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje poreza na periodičnim kontrolnim točkama naplate.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="b9e4e-174">**Ugovoreni iznos nakon poreza**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="b9e4e-175">Iznos retka ugovora nakon poreza.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-175">The contract line amount after tax.</span></span> <span data-ttu-id="b9e4e-176">Ovo je polje samo za čitanje i izračunava se kao **Ugovoreni iznos + porez**.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="b9e4e-177">Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje periodičnih kontrolnih točaka naplate.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="b9e4e-178">**Ograničenje koje se ne smije prekoračiti**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="b9e4e-179">Korisnik može uređivati ovo polje i ono je dostupno samo na redcima ugovora koji se temelje na projektu i imaju način naplate postavljen kao vrijeme i materijal.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="b9e4e-180">Korisnik može uređivati ovo polje.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-180">The user can edit this field.</span></span> <span data-ttu-id="b9e4e-181">Kada se stvarni podatak o vremenu ili materijalu odnosi na ovaj redak ugovora za vrijeme i materijal, iznos stvarnog podatka procjenjuje se prema ograničenju koje se ne smije prekoračiti u retku ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="b9e4e-182">Ova procjena završava se nakon što se obračunaju već potrošeni i angažirani iznosi.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="b9e4e-183">**Proračun klijenta**</span><span class="sxs-lookup"><span data-stu-id="b9e4e-183">**Customer Budget**</span></span> | <span data-ttu-id="b9e4e-184">Ovo se polje može uređivati i kopira se iz odgovarajućeg polja na retku ponude, ako je ugovor stvoren iz ponude.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="b9e4e-185">Ovo se polje upotrebljava samo za informacije i nema nikakvo daljnje značenje.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="b9e4e-186">Pravila provjere valjanosti mogućnosti na kartici Općenito redaka ugovora koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="b9e4e-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="b9e4e-187">Pravilo 1: Ako je polje **Uključeni zadaci** prazno ili postavljeno na **Svi projektni zadaci**, svi zadaci projekta uključeni su u redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="b9e4e-188">Pravilo 2: Kada je polje **Uključeni zadaci** prazno ili je izričito postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcije mogu se uključiti samo u jedan redak ugovora koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="b9e4e-189">Pravilo 3: Kada je polje **Uključeni zadaci** postavljeno na **Samo odabrani projektni zadaci**, projekt i određena klasa transakcije mogu se uključiti u više redaka ugovora koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="b9e4e-190">
                    <strong>Ugovor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b9e4e-191">
                    <strong>Redak ugovora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b9e4e-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="b9e4e-193">
                    <strong>Uključeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="b9e4e-194">
                    <strong>Uvrsti vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="b9e4e-195">
                    <strong>Uvrsti trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b9e4e-196">
                    <strong>Uključi materijale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b9e4e-197">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="b9e4e-198">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="b9e4e-199">
                    <strong>Valjan / nije valjan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="b9e4e-200">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b9e4e-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-201">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-202">CL1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-203">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-204">Prazno</span><span class="sxs-lookup"><span data-stu-id="b9e4e-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-205">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-206">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-207">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-208">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-209">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="b9e4e-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-210">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-210">Violation of Rule #2.</span></span> <span data-ttu-id="b9e4e-211">Vrijeme, trošak, materijali i naknade za projekt P1 uključeni su u retke ugovora i CL1 i CL2.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-212">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-213">CL2</span><span class="sxs-lookup"><span data-stu-id="b9e4e-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-214">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-215">Prazno</span><span class="sxs-lookup"><span data-stu-id="b9e4e-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-216">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-217">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-218">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-219">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-220">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-221">CL1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-222">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="b9e4e-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-224">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-225">No</span><span class="sxs-lookup"><span data-stu-id="b9e4e-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-226">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-227">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-228">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="b9e4e-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-229">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-229">Violation of Rule #2.</span></span> <span data-ttu-id="b9e4e-230">Vrijeme, materijali i naknade za projekt P1 uključeni su u retke ugovora i CL1 i CL2.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-231">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-232">CL2</span><span class="sxs-lookup"><span data-stu-id="b9e4e-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-233">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-234">Prazno</span><span class="sxs-lookup"><span data-stu-id="b9e4e-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-235">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-236">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-237">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-238">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-239">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-240">CL1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-241">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-242">Prazno</span><span class="sxs-lookup"><span data-stu-id="b9e4e-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-243">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-244">No</span><span class="sxs-lookup"><span data-stu-id="b9e4e-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-245">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-246">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-247">Valjano</span><span class="sxs-lookup"><span data-stu-id="b9e4e-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-248">Vrijeme, materijali i naknade za projekt P1 uključeni su u CL1.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="b9e4e-249">Trošak za projekt P1 uključen je u CL2.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="b9e4e-250">Nema preklapanja onoga što je uključeno u svaki redak ugovora i stoga vrijedi.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-251">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-252">CL2</span><span class="sxs-lookup"><span data-stu-id="b9e4e-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-253">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-254">Prazno</span><span class="sxs-lookup"><span data-stu-id="b9e4e-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-255">No</span><span class="sxs-lookup"><span data-stu-id="b9e4e-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-256">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-257">No</span><span class="sxs-lookup"><span data-stu-id="b9e4e-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-258">No</span><span class="sxs-lookup"><span data-stu-id="b9e4e-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-259">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-260">CL1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-261">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-262">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b9e4e-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-263">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-264">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-265">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-266">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-267">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="b9e4e-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-268">Kršenje pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="b9e4e-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="b9e4e-269">C1 uključuje vrijeme, materijale, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b9e4e-270">CL2 uključuje vrijeme, materijale, troškove i naknade za cijeli projekt P1 i stoga se preklapa s onim što je uključeno u C1.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-271">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-272">CL2</span><span class="sxs-lookup"><span data-stu-id="b9e4e-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-273">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-274">Prazno</span><span class="sxs-lookup"><span data-stu-id="b9e4e-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-275">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-276">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-277">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-278">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-279">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-280">CL1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-281">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-282">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b9e4e-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-283">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-284">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-285">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-286">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-287">Valjano</span><span class="sxs-lookup"><span data-stu-id="b9e4e-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b9e4e-288">Prema pravilu #3</span><span class="sxs-lookup"><span data-stu-id="b9e4e-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="b9e4e-289">C1 uključuje vrijeme, troškove, materijale i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b9e4e-290">CL2 uključuje vrijeme, troškove, materijale i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b9e4e-291">Jedina dodatna provjera valjanosti odnosi se na podskup zadataka na CL1 koji se razlikuje od podskupa zadataka na CL2 kako bi se osiguralo da nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="b9e4e-292">To čini sustav kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="b9e4e-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b9e4e-293">C1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b9e4e-294">CL2</span><span class="sxs-lookup"><span data-stu-id="b9e4e-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-295">P1</span><span class="sxs-lookup"><span data-stu-id="b9e4e-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="b9e4e-296">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="b9e4e-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-297">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b9e4e-298">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-299">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b9e4e-300">Jest</span><span class="sxs-lookup"><span data-stu-id="b9e4e-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
