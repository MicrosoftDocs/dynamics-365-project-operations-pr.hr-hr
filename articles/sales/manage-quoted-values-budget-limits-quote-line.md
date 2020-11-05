---
title: Redci ponude utemeljeni na projektu
description: U ovoj temi nalaze se informacije o uporabi redaka ponude koji se temelje na projektu za rad na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073255"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="faa37-103">Redci ponude utemeljeni na projektu</span><span class="sxs-lookup"><span data-stu-id="faa37-103">Project-based quote lines</span></span>

<span data-ttu-id="faa37-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="faa37-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="faa37-105">Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="faa37-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="faa37-106">Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="faa37-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="faa37-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="faa37-107">Billing Method</span></span>
- <span data-ttu-id="faa37-108">Mapiranje projekta</span><span class="sxs-lookup"><span data-stu-id="faa37-108">Project Mapping</span></span>
- <span data-ttu-id="faa37-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="faa37-109">Included Transaction classes</span></span>
- <span data-ttu-id="faa37-110">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="faa37-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="faa37-111">Postavka naplativosti</span><span class="sxs-lookup"><span data-stu-id="faa37-111">Chargeability setup</span></span>
- <span data-ttu-id="faa37-112">Procjena s pomoću pojedinosti retka ponude</span><span class="sxs-lookup"><span data-stu-id="faa37-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="faa37-113">Klijenti retka ponude</span><span class="sxs-lookup"><span data-stu-id="faa37-113">Quote line Customers</span></span>

<span data-ttu-id="faa37-114">Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="faa37-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="faa37-115">Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="faa37-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="faa37-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="faa37-116">**Field**</span></span> | <span data-ttu-id="faa37-117">**Relevantnost, svrha i smjernice**</span><span class="sxs-lookup"><span data-stu-id="faa37-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="faa37-118">**Utjecaj prema dolje**</span><span class="sxs-lookup"><span data-stu-id="faa37-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="faa37-119">Ime</span><span class="sxs-lookup"><span data-stu-id="faa37-119">Name</span></span> | <span data-ttu-id="faa37-120">Naziv retka ponude koji bi vam trebao pomoći pri prepoznavanju diskretne komponente ponude koja se procjenjuje.</span><span class="sxs-lookup"><span data-stu-id="faa37-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="faa37-121">Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-122">Način naplate</span><span class="sxs-lookup"><span data-stu-id="faa37-122">Billing Method</span></span> | <span data-ttu-id="faa37-123">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike.</span><span class="sxs-lookup"><span data-stu-id="faa37-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="faa37-124">Ovo polje uključuje dva glavna načina ugovaranja koje podržava aplikacija Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="faa37-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="faa37-125">- Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="faa37-125">- Fixed price</span></span></br><span data-ttu-id="faa37-126">- Vrijeme i materijal.</span><span class="sxs-lookup"><span data-stu-id="faa37-126">- Time and material.</span></span>| <span data-ttu-id="faa37-127">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-128">Project</span><span class="sxs-lookup"><span data-stu-id="faa37-128">Project</span></span> | <span data-ttu-id="faa37-129">Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="faa37-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="faa37-130">Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="faa37-131">Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="faa37-132">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-133">Uvrsti vrijeme</span><span class="sxs-lookup"><span data-stu-id="faa37-133">Include Time</span></span> | <span data-ttu-id="faa37-134">Zastavica **Da**/**Ne** označava hoće li vremenske transakcije ili troškovi rada na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="faa37-135">Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="faa37-136">Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="faa37-137">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-138">Uvrsti trošak</span><span class="sxs-lookup"><span data-stu-id="faa37-138">Include Expense</span></span> | <span data-ttu-id="faa37-139">Zastavica **Da**/**Ne** označava hoće li troškovi izdataka na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="faa37-140">Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="faa37-141">Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="faa37-142">Ta se vrijednost polja kopira preko retka ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-143">Uvrsti naknadu</span><span class="sxs-lookup"><span data-stu-id="faa37-143">Include Fee</span></span> | <span data-ttu-id="faa37-144">Zastavica **Da**/**Ne** označava hoće li naknade na odabranom projektu biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="faa37-145">Vrijednost **Ne** označava da naknade neće biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="faa37-146">Vrijednost **Da** označava da će naknade biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="faa37-147">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-148">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="faa37-148">Quoted Amount</span></span> | <span data-ttu-id="faa37-149">To je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="faa37-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="faa37-150">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike.</span><span class="sxs-lookup"><span data-stu-id="faa37-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="faa37-151">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="faa37-152">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-153">Procijenjeni porez</span><span class="sxs-lookup"><span data-stu-id="faa37-153">Estimated Tax</span></span> | <span data-ttu-id="faa37-154">Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="faa37-155">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="faa37-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="faa37-156">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-157">Ponuđeni iznos nakon oporezivanja</span><span class="sxs-lookup"><span data-stu-id="faa37-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="faa37-158">Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="faa37-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="faa37-159">Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="faa37-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="faa37-160">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-161">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="faa37-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="faa37-162">Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="faa37-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="faa37-163">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="faa37-164">Proračun klijenta</span><span class="sxs-lookup"><span data-stu-id="faa37-164">Customer Budget</span></span> | <span data-ttu-id="faa37-165">Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike.</span><span class="sxs-lookup"><span data-stu-id="faa37-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="faa37-166">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="faa37-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="faa37-167">Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="faa37-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="faa37-168">**Pravilo 1** : Određena klasa transakcije na odabranom projektu može se uključiti samo u jedan redak ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="faa37-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="faa37-169">**Pravilo 2** : Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="faa37-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="faa37-170">**Pravilo 3** : Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="faa37-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="faa37-171">
                    <strong>Prilika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="faa37-172">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="faa37-173">
                    <strong>Redak ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="faa37-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="faa37-175">
                    <strong>Uvrsti vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="faa37-176">
                    <strong>Uvrsti trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="faa37-177">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="faa37-178">
                    <strong>naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="faa37-179">
                    <strong>Valjan / nije valjan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="faa37-180">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="faa37-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="faa37-181">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-182">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-183">QL1</span><span class="sxs-lookup"><span data-stu-id="faa37-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-184">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-185">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-186">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-187">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-188">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="faa37-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-189">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="faa37-189">Violation of Rule #1.</span></span> <span data-ttu-id="faa37-190">Vrijeme, trošak i naknade za projekt P1 uključeni su u oba retka ponude, QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="faa37-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="faa37-191">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-192">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-193">QL2</span><span class="sxs-lookup"><span data-stu-id="faa37-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-194">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-195">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-196">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-197">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-197">Yes</span></span> </p>
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
<span data-ttu-id="faa37-198">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-199">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-200">QL1</span><span class="sxs-lookup"><span data-stu-id="faa37-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-201">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-202">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-203">No</span><span class="sxs-lookup"><span data-stu-id="faa37-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-204">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-205">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="faa37-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-206">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="faa37-206">Violation of Rule #1.</span></span> <span data-ttu-id="faa37-207">Vrijeme i naknade za projekt P1 uključeni su u oba retka ponude, QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="faa37-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="faa37-208">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-209">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-210">QL2</span><span class="sxs-lookup"><span data-stu-id="faa37-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-211">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-212">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-213">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-214">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-214">Yes</span></span> </p>
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
<span data-ttu-id="faa37-215">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-216">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-217">QL1</span><span class="sxs-lookup"><span data-stu-id="faa37-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-218">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-219">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-220">No</span><span class="sxs-lookup"><span data-stu-id="faa37-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-221">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-222">Valjano</span><span class="sxs-lookup"><span data-stu-id="faa37-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="faa37-223">Vrijeme i naknade za projekt P1 uključeni su u QL1.</span><span class="sxs-lookup"><span data-stu-id="faa37-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="faa37-224">Trošak za projekt P1 uključen je u QL2.</span><span class="sxs-lookup"><span data-stu-id="faa37-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="faa37-225">Nema preklapanja onoga što je uključeno u svaki redak ponude, tako da je valjan.</span><span class="sxs-lookup"><span data-stu-id="faa37-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="faa37-226">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-227">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-228">QL2</span><span class="sxs-lookup"><span data-stu-id="faa37-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-229">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-230">No</span><span class="sxs-lookup"><span data-stu-id="faa37-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-231">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-232">No</span><span class="sxs-lookup"><span data-stu-id="faa37-232">No</span></span> </p>
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
<span data-ttu-id="faa37-233">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-234">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-235">QL1</span><span class="sxs-lookup"><span data-stu-id="faa37-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-236">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-237">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-238">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-239">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-240">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="faa37-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-241">Kršenje gornjeg pravila br. 1</span><span class="sxs-lookup"><span data-stu-id="faa37-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="faa37-242">Q1 uključuje vrijeme, troškove i naknade za cijeli projekt P1.</span><span class="sxs-lookup"><span data-stu-id="faa37-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="faa37-243">QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i preklapa se s onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="faa37-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="faa37-244">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-245">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-246">QL2</span><span class="sxs-lookup"><span data-stu-id="faa37-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-247">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-248">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-249">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-250">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-250">Yes</span></span> </p>
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
<span data-ttu-id="faa37-251">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-252">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-253">QL1</span><span class="sxs-lookup"><span data-stu-id="faa37-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-254">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-255">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-256">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-257">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="faa37-258">Valjano</span><span class="sxs-lookup"><span data-stu-id="faa37-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-259">Na temelju pravila br. 2, Q1 i Q2 dvije su ponude u istoj prilici, tako da obje mogu procijeniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="faa37-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="faa37-260">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-261">2. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-262">QL1 u Q2</span><span class="sxs-lookup"><span data-stu-id="faa37-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-263">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-264">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-265">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-266">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-266">Yes</span></span> </p>
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
<span data-ttu-id="faa37-267">O1</span><span class="sxs-lookup"><span data-stu-id="faa37-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-268">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-269">QL1</span><span class="sxs-lookup"><span data-stu-id="faa37-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-270">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-271">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-272">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-273">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="faa37-274">Valjano</span><span class="sxs-lookup"><span data-stu-id="faa37-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="faa37-275">Na temelju pravila br. 3, Q1 i Q2 dvije su ponude u različitim prilikama, tako da ne mogu procijeniti iste komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="faa37-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="faa37-276">O2</span><span class="sxs-lookup"><span data-stu-id="faa37-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="faa37-277">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="faa37-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-278">QL1</span><span class="sxs-lookup"><span data-stu-id="faa37-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-279">P1</span><span class="sxs-lookup"><span data-stu-id="faa37-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-280">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="faa37-281">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="faa37-282">Jest</span><span class="sxs-lookup"><span data-stu-id="faa37-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="faa37-283">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="faa37-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

