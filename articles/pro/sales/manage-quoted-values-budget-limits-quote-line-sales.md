---
title: Pregled redaka ponude koji se temelje na projektu
description: U ovoj temi nalaze se informacije o uporabi redaka ponude koji se temelje na projektu za rad na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994847"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="79a6b-103">Pregled redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="79a6b-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="79a6b-104">_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="79a6b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="79a6b-105">Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="79a6b-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="79a6b-106">Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="79a6b-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="79a6b-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="79a6b-107">Billing Method</span></span>
- <span data-ttu-id="79a6b-108">Mapiranje projekta i zadatka</span><span class="sxs-lookup"><span data-stu-id="79a6b-108">Project and Task Mapping</span></span>
- <span data-ttu-id="79a6b-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="79a6b-109">Included Transaction classes</span></span>
- <span data-ttu-id="79a6b-110">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="79a6b-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="79a6b-111">Postavka naplativosti</span><span class="sxs-lookup"><span data-stu-id="79a6b-111">Chargeability setup</span></span>
- <span data-ttu-id="79a6b-112">Procjena s pomoću pojedinosti retka ponude</span><span class="sxs-lookup"><span data-stu-id="79a6b-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="79a6b-113">Klijenti retka ponude</span><span class="sxs-lookup"><span data-stu-id="79a6b-113">Quote line Customers</span></span>

<span data-ttu-id="79a6b-114">Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="79a6b-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="79a6b-115">Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="79a6b-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="79a6b-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="79a6b-116">**Field**</span></span> | <span data-ttu-id="79a6b-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="79a6b-117">**Description**</span></span> | <span data-ttu-id="79a6b-118">**Utjecaj prema dolje**</span><span class="sxs-lookup"><span data-stu-id="79a6b-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="79a6b-119">Ime</span><span class="sxs-lookup"><span data-stu-id="79a6b-119">Name</span></span> | <span data-ttu-id="79a6b-120">Naziv retka ponude koji vam pomaže prepoznati diskretnu komponentu ponude koja se procjenjuje.</span><span class="sxs-lookup"><span data-stu-id="79a6b-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="79a6b-121">Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="79a6b-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-122">Način naplate</span><span class="sxs-lookup"><span data-stu-id="79a6b-122">Billing Method</span></span> | <span data-ttu-id="79a6b-123">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike.</span><span class="sxs-lookup"><span data-stu-id="79a6b-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="79a6b-124">Ovo polje uključuje dva glavna modela ugovaranja koja podržava aplikacija Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="79a6b-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="79a6b-125">- Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="79a6b-125">- Fixed price</span></span></br><span data-ttu-id="79a6b-126">- Vrijeme i materijal.</span><span class="sxs-lookup"><span data-stu-id="79a6b-126">- Time and material.</span></span>| <span data-ttu-id="79a6b-127">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-128">Project</span><span class="sxs-lookup"><span data-stu-id="79a6b-128">Project</span></span> | <span data-ttu-id="79a6b-129">Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="79a6b-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="79a6b-130">Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="79a6b-131">Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="79a6b-132">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="79a6b-133">Uključeni zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-133">Included Tasks</span></span> | <span data-ttu-id="79a6b-134">Označava upotrebljava li se ovaj redak ponude za sve ili samo neke projektne zadatke odabranog projekta.</span><span class="sxs-lookup"><span data-stu-id="79a6b-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="79a6b-135">Polje ima sljedeće moguće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="79a6b-135">This field has the following possible values:</span></span></br><span data-ttu-id="79a6b-136">- Svi projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-136">- All project tasks</span></span></br><span data-ttu-id="79a6b-137">- Samo odabrani projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-137">- Selected project tasks only</span></span></br><span data-ttu-id="79a6b-138">Nepostojanje vrijednosti u ovom polju jednako je mogućnosti **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="79a6b-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="79a6b-139">Kad se na stranici projekta odabere stavka **Samo odabrani projektni zadaci**, kartica **Postavljanje zadatka za naplatu** omogućuje odabir određenih zadataka kako biste ih povezali s ovim retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="79a6b-140">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-141">Uvrsti vrijeme</span><span class="sxs-lookup"><span data-stu-id="79a6b-141">Include Time</span></span> | <span data-ttu-id="79a6b-142">Vrijednost **Da**/**Ne** pokazuje hoće li se vremenske transakcije ili troškovi rada na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-143">Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-144">Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="79a6b-145">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-146">Uvrsti trošak</span><span class="sxs-lookup"><span data-stu-id="79a6b-146">Include Expense</span></span> | <span data-ttu-id="79a6b-147">Vrijednost **Da**/**Ne** označava hoće li se troškovi izdataka na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-148">Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-149">Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="79a6b-150">Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-151">Uvrsti materijal</span><span class="sxs-lookup"><span data-stu-id="79a6b-151">Include Material</span></span> | <span data-ttu-id="79a6b-152">Vrijednost **Da**/**Ne** označava hoće li se troškovi materijala na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-153">Vrijednost **Ne** označava da se troškovi materijala neće uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-154">Vrijednost **Da** označava da će se troškovi materijala uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="79a6b-155">Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-156">Uvrsti naknadu</span><span class="sxs-lookup"><span data-stu-id="79a6b-156">Include Fee</span></span> | <span data-ttu-id="79a6b-157">Vrijednost **Da**/**Ne** označava hoće li se naknade na odabranom projektu uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-158">Vrijednost **Ne** označava da se naknade neće uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="79a6b-159">Vrijednost **Da** označava da će se naknade uključiti u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="79a6b-160">Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-161">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="79a6b-161">Quoted Amount</span></span> | <span data-ttu-id="79a6b-162">Ovo je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koja se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="79a6b-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="79a6b-163">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike.</span><span class="sxs-lookup"><span data-stu-id="79a6b-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="79a6b-164">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="79a6b-165">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-166">Procijenjeni porez</span><span class="sxs-lookup"><span data-stu-id="79a6b-166">Estimated Tax</span></span> | <span data-ttu-id="79a6b-167">Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="79a6b-168">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="79a6b-169">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-170">Ponuđeni iznos nakon oporezivanja</span><span class="sxs-lookup"><span data-stu-id="79a6b-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="79a6b-171">Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="79a6b-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="79a6b-172">Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="79a6b-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="79a6b-173">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-174">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="79a6b-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="79a6b-175">Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="79a6b-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="79a6b-176">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="79a6b-177">Proračun klijenta</span><span class="sxs-lookup"><span data-stu-id="79a6b-177">Customer Budget</span></span> | <span data-ttu-id="79a6b-178">Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike.</span><span class="sxs-lookup"><span data-stu-id="79a6b-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="79a6b-179">Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="79a6b-180">Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="79a6b-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="79a6b-181">**Pravilo 1**: Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci**, projekt je uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="79a6b-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="79a6b-182">**Pravilo 2**: Ako je polje **Uključeni zadaci** prazno ili je postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti samo u jedan redak ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="79a6b-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="79a6b-183">**Pravilo 3**: Ako je polje **Uključeni zadaci** postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti u više redaka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="79a6b-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="79a6b-184">**Pravilo 4**: Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="79a6b-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="79a6b-185">**Pravilo 5**: Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="79a6b-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="79a6b-186">
                    <strong>Prilika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="79a6b-187">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="79a6b-188">
                    <strong>Redak ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="79a6b-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="79a6b-190">
                    <strong>Uključeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="79a6b-191">
                    <strong>Uvrsti vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="79a6b-192">
                    <strong>Uvrsti trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="79a6b-193">
                    <strong>Uvrsti materijal</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="79a6b-194">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="79a6b-195">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="79a6b-196">
                    <strong>Valjan / nije valjan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="79a6b-197">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="79a6b-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-198">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-199">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-200">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-201">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-202">Prazno</span><span class="sxs-lookup"><span data-stu-id="79a6b-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-203">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-204">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-205">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-206">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-207">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="79a6b-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-208">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="79a6b-208">Violation of Rule #2.</span></span> <span data-ttu-id="79a6b-209">Vrijeme, trošak i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-210">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-211">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-212">QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-213">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-214">Prazno</span><span class="sxs-lookup"><span data-stu-id="79a6b-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-215">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-216">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-217">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-218">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-218">Yes</span></span> </p>
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
<span data-ttu-id="79a6b-219">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-220">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-221">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-222">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="79a6b-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-224">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-225">No</span><span class="sxs-lookup"><span data-stu-id="79a6b-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-226">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-227">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-228">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="79a6b-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-229">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="79a6b-229">Violation of Rule #2.</span></span> <span data-ttu-id="79a6b-230">Vrijeme, materijal i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-231">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-232">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-233">QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-234">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="79a6b-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-236">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-237">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-238">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-239">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-239">Yes</span></span> </p>
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
<span data-ttu-id="79a6b-240">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-241">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-242">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-243">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-244">Prazno</span><span class="sxs-lookup"><span data-stu-id="79a6b-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-245">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-246">No</span><span class="sxs-lookup"><span data-stu-id="79a6b-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-247">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-248">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-249">Valjano</span><span class="sxs-lookup"><span data-stu-id="79a6b-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-250">Vrijeme, materijal i naknade za projekt P1 uključeni su u QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="79a6b-251">Trošak za projekt P1 uključen je u QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="79a6b-252">Nema preklapanja onoga što je uključeno u svaki redak ponude i stoga vrijedi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-253">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-254">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-255">QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-256">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-257">Prazno</span><span class="sxs-lookup"><span data-stu-id="79a6b-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-258">No</span><span class="sxs-lookup"><span data-stu-id="79a6b-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-259">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-260">No</span><span class="sxs-lookup"><span data-stu-id="79a6b-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-261">No</span><span class="sxs-lookup"><span data-stu-id="79a6b-261">No</span></span> </p>
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
<span data-ttu-id="79a6b-262">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-263">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-264">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-265">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-266">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-267">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-268">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-269">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-270">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-271">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="79a6b-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-272">Kršenje pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="79a6b-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="79a6b-273">Q1 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="79a6b-274">QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i stoga se preklapa s onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="79a6b-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-275">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-276">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-277">QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-278">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-279">Prazno</span><span class="sxs-lookup"><span data-stu-id="79a6b-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-280">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-281">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-282">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-283">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-283">Yes</span></span> </p>
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
<span data-ttu-id="79a6b-284">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-285">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-286">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-287">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-288">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-289">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-290">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-291">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-292">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-293">Valjano</span><span class="sxs-lookup"><span data-stu-id="79a6b-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-294">Prema pravilu br. 3,</span><span class="sxs-lookup"><span data-stu-id="79a6b-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="79a6b-295">Q1 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="79a6b-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="79a6b-296">QL2 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="79a6b-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="79a6b-297">Jedina dodatna provjera valjanosti odnosi se na podskup zadataka na QL1 koji se razlikuje od podskupa zadataka na QL2 kako bi se osiguralo da nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="79a6b-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="79a6b-298">To čini sustav kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="79a6b-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-299">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-300">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-301">QL2</span><span class="sxs-lookup"><span data-stu-id="79a6b-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-302">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-303">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-304">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-305">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-306">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-307">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-307">Yes</span></span> </p>
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
<span data-ttu-id="79a6b-308">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-309">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-310">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-311">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-312">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-313">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-314">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-315">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-316">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-317">Valjano</span><span class="sxs-lookup"><span data-stu-id="79a6b-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-318">Prema pravilu br. 5, Q1 i Q2 dvije su ponude u istoj prilici, tako da oboje mogu procijeniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="79a6b-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-319">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-320">2. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-321">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-322">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-323">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-324">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-325">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-326">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-327">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-327">Yes</span></span> </p>
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
<span data-ttu-id="79a6b-328">O1</span><span class="sxs-lookup"><span data-stu-id="79a6b-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-329">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-330">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-331">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-332">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-333">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-334">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-335">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-336">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-337">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="79a6b-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="79a6b-338">Prema pravilu br. 4, Q1 i Q2 dvije su ponude u različitim prilikama, tako da oboje ne mogu procijeniti iste komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="79a6b-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="79a6b-339">O2</span><span class="sxs-lookup"><span data-stu-id="79a6b-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="79a6b-340">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="79a6b-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="79a6b-341">QL1</span><span class="sxs-lookup"><span data-stu-id="79a6b-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-342">P1</span><span class="sxs-lookup"><span data-stu-id="79a6b-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="79a6b-343">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="79a6b-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="79a6b-344">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="79a6b-345">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="79a6b-346">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="79a6b-347">Jest</span><span class="sxs-lookup"><span data-stu-id="79a6b-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
