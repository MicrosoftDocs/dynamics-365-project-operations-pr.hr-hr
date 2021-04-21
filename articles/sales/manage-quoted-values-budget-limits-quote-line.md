---
title: Pregled redaka ponude projekta
description: U ovoj temi nalaze se informacije o uporabi redaka ponude projekta za rad na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858014"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="713b7-103">Pregled redaka ponude projekta</span><span class="sxs-lookup"><span data-stu-id="713b7-103">Project quote lines overview</span></span>

<span data-ttu-id="713b7-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="713b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="713b7-105">Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="713b7-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="713b7-106">Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="713b7-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="713b7-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="713b7-107">Billing Method</span></span>
- <span data-ttu-id="713b7-108">Mapiranje projekta</span><span class="sxs-lookup"><span data-stu-id="713b7-108">Project Mapping</span></span>
- <span data-ttu-id="713b7-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="713b7-109">Included Transaction classes</span></span>
- <span data-ttu-id="713b7-110">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="713b7-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="713b7-111">Postavka naplativosti</span><span class="sxs-lookup"><span data-stu-id="713b7-111">Chargeability setup</span></span>
- <span data-ttu-id="713b7-112">Procjena s pomoću pojedinosti retka ponude</span><span class="sxs-lookup"><span data-stu-id="713b7-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="713b7-113">Klijenti retka ponude</span><span class="sxs-lookup"><span data-stu-id="713b7-113">Quote line Customers</span></span>

<span data-ttu-id="713b7-114">Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="713b7-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="713b7-115">Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="713b7-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="713b7-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="713b7-116">**Field**</span></span> | <span data-ttu-id="713b7-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="713b7-117">**Description**</span></span> | <span data-ttu-id="713b7-118">**Utjecaj prema dolje**</span><span class="sxs-lookup"><span data-stu-id="713b7-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="713b7-119">Ime</span><span class="sxs-lookup"><span data-stu-id="713b7-119">Name</span></span> | <span data-ttu-id="713b7-120">Naziv retka ponude koji bi vam trebao pomoći pri prepoznavanju diskretne komponente ponude koja se procjenjuje.</span><span class="sxs-lookup"><span data-stu-id="713b7-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="713b7-121">Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-122">Način naplate</span><span class="sxs-lookup"><span data-stu-id="713b7-122">Billing Method</span></span> | <span data-ttu-id="713b7-123">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike.</span><span class="sxs-lookup"><span data-stu-id="713b7-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="713b7-124">Ovo polje uključuje dva glavna modela ugovaranja koja podržava aplikacija Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="713b7-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="713b7-125">- Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="713b7-125">- Fixed price</span></span></br><span data-ttu-id="713b7-126">- Vrijeme i materijal.</span><span class="sxs-lookup"><span data-stu-id="713b7-126">- Time and material.</span></span>| <span data-ttu-id="713b7-127">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-128">Project</span><span class="sxs-lookup"><span data-stu-id="713b7-128">Project</span></span> | <span data-ttu-id="713b7-129">Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="713b7-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="713b7-130">Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="713b7-131">Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="713b7-132">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-133">Uvrsti vrijeme</span><span class="sxs-lookup"><span data-stu-id="713b7-133">Include Time</span></span> | <span data-ttu-id="713b7-134">Zastavica **Da**/**Ne** označava hoće li vremenske transakcije ili troškovi rada na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="713b7-135">Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="713b7-136">Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="713b7-137">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-138">Uvrsti trošak</span><span class="sxs-lookup"><span data-stu-id="713b7-138">Include Expense</span></span> | <span data-ttu-id="713b7-139">Zastavica **Da**/**Ne** označava hoće li troškovi izdataka na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="713b7-140">Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="713b7-141">Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="713b7-142">Ta se vrijednost polja kopira preko retka ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-143">Uvrsti naknadu</span><span class="sxs-lookup"><span data-stu-id="713b7-143">Include Fee</span></span> | <span data-ttu-id="713b7-144">Zastavica **Da**/**Ne** označava hoće li naknade na odabranom projektu biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="713b7-145">Vrijednost **Ne** označava da naknade neće biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="713b7-146">Vrijednost **Da** označava da će naknade biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="713b7-147">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-148">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="713b7-148">Quoted Amount</span></span> | <span data-ttu-id="713b7-149">To je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="713b7-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="713b7-150">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike.</span><span class="sxs-lookup"><span data-stu-id="713b7-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="713b7-151">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="713b7-152">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-153">Procijenjeni porez</span><span class="sxs-lookup"><span data-stu-id="713b7-153">Estimated Tax</span></span> | <span data-ttu-id="713b7-154">Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="713b7-155">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="713b7-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="713b7-156">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-157">Ponuđeni iznos nakon oporezivanja</span><span class="sxs-lookup"><span data-stu-id="713b7-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="713b7-158">Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="713b7-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="713b7-159">Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="713b7-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="713b7-160">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-161">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="713b7-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="713b7-162">Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="713b7-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="713b7-163">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="713b7-164">Proračun klijenta</span><span class="sxs-lookup"><span data-stu-id="713b7-164">Customer Budget</span></span> | <span data-ttu-id="713b7-165">Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike.</span><span class="sxs-lookup"><span data-stu-id="713b7-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="713b7-166">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="713b7-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="713b7-167">Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="713b7-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="713b7-168">**Pravilo 1**: Određena klasa transakcije na odabranom projektu može se uključiti samo u jedan redak ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="713b7-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="713b7-169">**Pravilo 2**: Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="713b7-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="713b7-170">**Pravilo 3**: Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="713b7-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="713b7-171">
                    <strong>Prilika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="713b7-172">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="713b7-173">
                    <strong>Redak ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="713b7-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="713b7-175">
                    <strong>Uvrsti vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="713b7-176">
                    <strong>Uvrsti trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="713b7-177">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="713b7-178">
                    <strong>naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="713b7-179">
                    <strong>Valjan / nije valjan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="713b7-180">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="713b7-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-181">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-182">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-183">QL1</span><span class="sxs-lookup"><span data-stu-id="713b7-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-184">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-185">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-186">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-187">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-188">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="713b7-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-189">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="713b7-189">Violation of Rule #1.</span></span> <span data-ttu-id="713b7-190">Vrijeme, trošak i naknade za projekt P1 uključeni su u oba retka ponude, QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="713b7-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-191">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-192">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-193">QL2</span><span class="sxs-lookup"><span data-stu-id="713b7-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-194">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-195">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-196">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-197">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-198">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-199">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-200">QL1</span><span class="sxs-lookup"><span data-stu-id="713b7-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-201">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-202">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-203">No</span><span class="sxs-lookup"><span data-stu-id="713b7-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-204">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-205">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="713b7-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-206">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="713b7-206">Violation of Rule #1.</span></span> <span data-ttu-id="713b7-207">Vrijeme i naknade za projekt P1 uključeni su u oba retka ponude, QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="713b7-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-208">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-209">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-210">QL2</span><span class="sxs-lookup"><span data-stu-id="713b7-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-211">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-212">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-213">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-214">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-215">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-216">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-217">QL1</span><span class="sxs-lookup"><span data-stu-id="713b7-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-218">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-219">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-220">No</span><span class="sxs-lookup"><span data-stu-id="713b7-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-221">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-222">Valjano</span><span class="sxs-lookup"><span data-stu-id="713b7-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="713b7-223">Vrijeme i naknade za projekt P1 uključeni su u QL1.</span><span class="sxs-lookup"><span data-stu-id="713b7-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="713b7-224">Trošak za projekt P1 uključen je u QL2.</span><span class="sxs-lookup"><span data-stu-id="713b7-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="713b7-225">Nema preklapanja onoga što je uključeno u svaki redak ponude, tako da je valjan.</span><span class="sxs-lookup"><span data-stu-id="713b7-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-226">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-227">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-228">QL2</span><span class="sxs-lookup"><span data-stu-id="713b7-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-229">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-230">No</span><span class="sxs-lookup"><span data-stu-id="713b7-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-231">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-232">No</span><span class="sxs-lookup"><span data-stu-id="713b7-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-233">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-234">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-235">QL1</span><span class="sxs-lookup"><span data-stu-id="713b7-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-236">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-237">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-238">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-239">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-240">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="713b7-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-241">Kršenje gornjeg pravila br. 1</span><span class="sxs-lookup"><span data-stu-id="713b7-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="713b7-242">Q1 uključuje vrijeme, troškove i naknade za cijeli projekt P1.</span><span class="sxs-lookup"><span data-stu-id="713b7-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="713b7-243">QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i preklapa se s onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="713b7-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-244">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-245">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-246">QL2</span><span class="sxs-lookup"><span data-stu-id="713b7-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-247">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-248">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-249">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-250">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-251">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-252">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-253">QL1</span><span class="sxs-lookup"><span data-stu-id="713b7-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-254">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-255">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-256">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-257">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="713b7-258">Valjano</span><span class="sxs-lookup"><span data-stu-id="713b7-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-259">Na temelju pravila br. 2, Q1 i Q2 dvije su ponude u istoj prilici, tako da obje mogu procijeniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="713b7-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-260">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-261">2. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-262">QL1 u Q2</span><span class="sxs-lookup"><span data-stu-id="713b7-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-263">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-264">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-265">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-266">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-267">O1</span><span class="sxs-lookup"><span data-stu-id="713b7-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-268">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-269">QL1</span><span class="sxs-lookup"><span data-stu-id="713b7-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-270">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-271">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-272">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-273">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="713b7-274">Valjano</span><span class="sxs-lookup"><span data-stu-id="713b7-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="713b7-275">Na temelju pravila br. 3, Q1 i Q2 dvije su ponude u različitim prilikama, tako da ne mogu procijeniti iste komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="713b7-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="713b7-276">O2</span><span class="sxs-lookup"><span data-stu-id="713b7-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="713b7-277">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="713b7-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-278">QL1</span><span class="sxs-lookup"><span data-stu-id="713b7-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-279">P1</span><span class="sxs-lookup"><span data-stu-id="713b7-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-280">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="713b7-281">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="713b7-282">Jest</span><span class="sxs-lookup"><span data-stu-id="713b7-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="713b7-283">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="713b7-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
