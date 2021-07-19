---
title: Pregled redaka ponude koji se temelje na projektu
description: U ovoj temi nalaze se informacije o uporabi redaka ponude koji se temelje na projektu za rad na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369862"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="764fa-103">Pregled redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="764fa-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="764fa-104">_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="764fa-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="764fa-105">Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="764fa-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="764fa-106">Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="764fa-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="764fa-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="764fa-107">Billing Method</span></span>
- <span data-ttu-id="764fa-108">Mapiranje projekta i zadatka</span><span class="sxs-lookup"><span data-stu-id="764fa-108">Project and Task Mapping</span></span>
- <span data-ttu-id="764fa-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="764fa-109">Included Transaction classes</span></span>
- <span data-ttu-id="764fa-110">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="764fa-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="764fa-111">Postavka naplativosti</span><span class="sxs-lookup"><span data-stu-id="764fa-111">Chargeability setup</span></span>
- <span data-ttu-id="764fa-112">Procjena s pomoću pojedinosti retka ponude</span><span class="sxs-lookup"><span data-stu-id="764fa-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="764fa-113">Klijenti retka ponude</span><span class="sxs-lookup"><span data-stu-id="764fa-113">Quote line Customers</span></span>

<span data-ttu-id="764fa-114">Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="764fa-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="764fa-115">Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="764fa-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="764fa-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="764fa-116">**Field**</span></span> | <span data-ttu-id="764fa-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="764fa-117">**Description**</span></span> | <span data-ttu-id="764fa-118">**Utjecaj prema dolje**</span><span class="sxs-lookup"><span data-stu-id="764fa-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="764fa-119">Ime</span><span class="sxs-lookup"><span data-stu-id="764fa-119">Name</span></span> | <span data-ttu-id="764fa-120">Naziv retka ponude koji vam pomaže prepoznati diskretnu komponentu ponude koja se procjenjuje.</span><span class="sxs-lookup"><span data-stu-id="764fa-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="764fa-121">Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="764fa-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-122">Način naplate</span><span class="sxs-lookup"><span data-stu-id="764fa-122">Billing Method</span></span> | <span data-ttu-id="764fa-123">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike.</span><span class="sxs-lookup"><span data-stu-id="764fa-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="764fa-124">Ovo polje uključuje dva glavna modela ugovaranja koja podržava aplikacija Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="764fa-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="764fa-125">- Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="764fa-125">- Fixed price</span></span></br><span data-ttu-id="764fa-126">- Vrijeme i materijal.</span><span class="sxs-lookup"><span data-stu-id="764fa-126">- Time and material.</span></span>| <span data-ttu-id="764fa-127">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-128">Project</span><span class="sxs-lookup"><span data-stu-id="764fa-128">Project</span></span> | <span data-ttu-id="764fa-129">Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="764fa-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="764fa-130">Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="764fa-131">Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="764fa-132">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="764fa-133">Uključeni zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-133">Included Tasks</span></span> | <span data-ttu-id="764fa-134">Označava upotrebljava li se ovaj redak ponude za sve ili samo neke projektne zadatke odabranog projekta.</span><span class="sxs-lookup"><span data-stu-id="764fa-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="764fa-135">Polje ima sljedeće moguće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="764fa-135">This field has the following possible values:</span></span></br><span data-ttu-id="764fa-136">- Svi projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-136">- All project tasks</span></span></br><span data-ttu-id="764fa-137">- Samo odabrani projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-137">- Selected project tasks only</span></span></br><span data-ttu-id="764fa-138">Nepostojanje vrijednosti u ovom polju jednako je mogućnosti **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="764fa-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="764fa-139">Kad se na stranici projekta odabere stavka **Samo odabrani projektni zadaci**, kartica **Postavljanje zadatka za naplatu** omogućuje odabir određenih zadataka kako biste ih povezali s ovim retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="764fa-140">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-141">Uvrsti vrijeme</span><span class="sxs-lookup"><span data-stu-id="764fa-141">Include Time</span></span> | <span data-ttu-id="764fa-142">Vrijednost **Da**/**Ne** pokazuje hoće li se vremenske transakcije ili troškovi rada na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-143">Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-144">Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="764fa-145">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-146">Uvrsti trošak</span><span class="sxs-lookup"><span data-stu-id="764fa-146">Include Expense</span></span> | <span data-ttu-id="764fa-147">Vrijednost **Da**/**Ne** označava hoće li se troškovi izdataka na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-148">Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-149">Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="764fa-150">Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-151">Uvrsti materijal</span><span class="sxs-lookup"><span data-stu-id="764fa-151">Include Material</span></span> | <span data-ttu-id="764fa-152">Vrijednost **Da**/**Ne** označava hoće li se troškovi materijala na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-153">Vrijednost **Ne** označava da se troškovi materijala neće uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-154">Vrijednost **Da** označava da će se troškovi materijala uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="764fa-155">Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-156">Uvrsti naknadu</span><span class="sxs-lookup"><span data-stu-id="764fa-156">Include Fee</span></span> | <span data-ttu-id="764fa-157">Vrijednost **Da**/**Ne** označava hoće li se naknade na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-158">Vrijednost **Ne** označava da se naknade neće uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="764fa-159">Vrijednost **Da** označava da će se naknade uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="764fa-160">Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-161">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="764fa-161">Quoted Amount</span></span> | <span data-ttu-id="764fa-162">Ovo je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koja se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="764fa-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="764fa-163">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike.</span><span class="sxs-lookup"><span data-stu-id="764fa-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="764fa-164">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="764fa-165">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-166">Procijenjeni porez</span><span class="sxs-lookup"><span data-stu-id="764fa-166">Estimated Tax</span></span> | <span data-ttu-id="764fa-167">Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="764fa-168">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="764fa-169">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-170">Ponuđeni iznos nakon oporezivanja</span><span class="sxs-lookup"><span data-stu-id="764fa-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="764fa-171">Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="764fa-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="764fa-172">Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="764fa-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="764fa-173">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-174">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="764fa-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="764fa-175">Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="764fa-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="764fa-176">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="764fa-177">Proračun klijenta</span><span class="sxs-lookup"><span data-stu-id="764fa-177">Customer Budget</span></span> | <span data-ttu-id="764fa-178">Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike.</span><span class="sxs-lookup"><span data-stu-id="764fa-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="764fa-179">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="764fa-180">Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="764fa-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="764fa-181">**Pravilo 1**: Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci**, projekt je uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="764fa-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="764fa-182">**Pravilo 2**: Ako je polje **Uključeni zadaci** prazno ili je postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti samo u jedan redak ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="764fa-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="764fa-183">**Pravilo 3**: Ako je polje **Uključeni zadaci** postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti u više redaka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="764fa-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="764fa-184">**Pravilo 4**: Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="764fa-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="764fa-185">**Pravilo 5**: Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="764fa-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="764fa-186">
                    <strong>Prilika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="764fa-187">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="764fa-188">
                    <strong>Redak ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="764fa-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="764fa-190">
                    <strong>Uključeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="764fa-191">
                    <strong>Uvrsti vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="764fa-192">
                    <strong>Uvrsti trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="764fa-193">
                    <strong>Uvrsti materijal</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="764fa-194">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="764fa-195">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="764fa-196">
                    <strong>Valjan / nije valjan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="764fa-197">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="764fa-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-198">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-199">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-200">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-201">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-202">Prazno</span><span class="sxs-lookup"><span data-stu-id="764fa-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-203">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-204">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-205">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-206">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-207">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="764fa-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-208">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="764fa-208">Violation of Rule #2.</span></span> <span data-ttu-id="764fa-209">Vrijeme, trošak i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-210">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-211">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-212">QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-213">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-214">Prazno</span><span class="sxs-lookup"><span data-stu-id="764fa-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-215">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-216">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-217">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-218">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-219">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-220">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-221">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-222">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="764fa-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-224">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-225">No</span><span class="sxs-lookup"><span data-stu-id="764fa-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-226">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-227">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-228">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="764fa-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-229">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="764fa-229">Violation of Rule #2.</span></span> <span data-ttu-id="764fa-230">Vrijeme, materijal i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-231">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-232">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-233">QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-234">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="764fa-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-236">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-237">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-238">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-239">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-240">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-241">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-242">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-243">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-244">Prazno</span><span class="sxs-lookup"><span data-stu-id="764fa-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-245">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-246">No</span><span class="sxs-lookup"><span data-stu-id="764fa-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-247">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-248">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-249">Valjano</span><span class="sxs-lookup"><span data-stu-id="764fa-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-250">Vrijeme, materijal i naknade za projekt P1 uključeni su u QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="764fa-251">Trošak za projekt P1 uključen je u QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="764fa-252">Nema preklapanja onoga što je uključeno u svaki redak ponude i stoga vrijedi.</span><span class="sxs-lookup"><span data-stu-id="764fa-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-253">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-254">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-255">QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-256">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-257">Prazno</span><span class="sxs-lookup"><span data-stu-id="764fa-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-258">No</span><span class="sxs-lookup"><span data-stu-id="764fa-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-259">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-260">No</span><span class="sxs-lookup"><span data-stu-id="764fa-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-261">No</span><span class="sxs-lookup"><span data-stu-id="764fa-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-262">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-263">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-264">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-265">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-266">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-267">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-268">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-269">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-270">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-271">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="764fa-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-272">Kršenje pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="764fa-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="764fa-273">Q1 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1</span><span class="sxs-lookup"><span data-stu-id="764fa-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="764fa-274">QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i stoga se preklapa s onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="764fa-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-275">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-276">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-277">QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-278">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-279">Prazno</span><span class="sxs-lookup"><span data-stu-id="764fa-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-280">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-281">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-282">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-283">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-284">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-285">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-286">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-287">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-288">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-289">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-290">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-291">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-292">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-293">Valjano</span><span class="sxs-lookup"><span data-stu-id="764fa-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-294">Prema pravilu br. 3,</span><span class="sxs-lookup"><span data-stu-id="764fa-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="764fa-295">Q1 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="764fa-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="764fa-296">QL2 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="764fa-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="764fa-297">Jedina dodatna provjera valjanosti odnosi se na podskup zadataka na QL1 koji se razlikuje od podskupa zadataka na QL2 kako bi se osiguralo da nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="764fa-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="764fa-298">To čini sustav kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="764fa-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-299">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-300">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-301">QL2</span><span class="sxs-lookup"><span data-stu-id="764fa-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-302">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-303">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-304">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-305">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-306">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-307">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-308">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-309">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-310">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-311">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-312">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-313">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-314">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-315">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-316">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-317">Valjano</span><span class="sxs-lookup"><span data-stu-id="764fa-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-318">Prema pravilu br. 5, Q1 i Q2 dvije su ponude u istoj prilici, tako da oboje mogu procijeniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="764fa-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-319">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-320">2. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-321">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-322">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-323">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-324">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-325">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-326">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-327">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-328">O1</span><span class="sxs-lookup"><span data-stu-id="764fa-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-329">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-330">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-331">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-332">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-333">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-334">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-335">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-336">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-337">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="764fa-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="764fa-338">Prema pravilu br. 4, Q1 i Q2 dvije su ponude u različitim prilikama, tako da oboje ne mogu procijeniti iste komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="764fa-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="764fa-339">O2</span><span class="sxs-lookup"><span data-stu-id="764fa-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="764fa-340">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="764fa-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="764fa-341">QL1</span><span class="sxs-lookup"><span data-stu-id="764fa-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-342">P1</span><span class="sxs-lookup"><span data-stu-id="764fa-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="764fa-343">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="764fa-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="764fa-344">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="764fa-345">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="764fa-346">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="764fa-347">Jest</span><span class="sxs-lookup"><span data-stu-id="764fa-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
