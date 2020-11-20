---
title: Pregled redaka ponude koji se temelje na projektu – jednostavno
description: U ovoj temi nalaze se informacije o uporabi redaka ponude koji se temelje na projektu za rad na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181083"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="98308-104">Pregled redaka ponude koji se temelje na projektu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="98308-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="98308-105">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="98308-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98308-106">Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="98308-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="98308-107">Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="98308-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="98308-108">Način naplate</span><span class="sxs-lookup"><span data-stu-id="98308-108">Billing Method</span></span>
- <span data-ttu-id="98308-109">Mapiranje projekta i zadatka</span><span class="sxs-lookup"><span data-stu-id="98308-109">Project and Task Mapping</span></span>
- <span data-ttu-id="98308-110">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="98308-110">Included Transaction classes</span></span>
- <span data-ttu-id="98308-111">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="98308-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="98308-112">Postavka naplativosti</span><span class="sxs-lookup"><span data-stu-id="98308-112">Chargeability setup</span></span>
- <span data-ttu-id="98308-113">Procjena s pomoću pojedinosti retka ponude</span><span class="sxs-lookup"><span data-stu-id="98308-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="98308-114">Klijenti retka ponude</span><span class="sxs-lookup"><span data-stu-id="98308-114">Quote line Customers</span></span>

<span data-ttu-id="98308-115">Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="98308-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="98308-116">Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="98308-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="98308-117">**Polje**</span><span class="sxs-lookup"><span data-stu-id="98308-117">**Field**</span></span> | <span data-ttu-id="98308-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="98308-118">**Description**</span></span> | <span data-ttu-id="98308-119">**Utjecaj prema dolje**</span><span class="sxs-lookup"><span data-stu-id="98308-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="98308-120">Ime</span><span class="sxs-lookup"><span data-stu-id="98308-120">Name</span></span> | <span data-ttu-id="98308-121">Naziv retka ponude koji bi vam trebao pomoći pri prepoznavanju diskretne komponente ponude koja se procjenjuje.</span><span class="sxs-lookup"><span data-stu-id="98308-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="98308-122">Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-123">Način naplate</span><span class="sxs-lookup"><span data-stu-id="98308-123">Billing Method</span></span> | <span data-ttu-id="98308-124">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike.</span><span class="sxs-lookup"><span data-stu-id="98308-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="98308-125">Ovo polje uključuje dva glavna načina ugovaranja koje podržava aplikacija Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="98308-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="98308-126">- Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="98308-126">- Fixed price</span></span></br><span data-ttu-id="98308-127">- Vrijeme i materijal.</span><span class="sxs-lookup"><span data-stu-id="98308-127">- Time and material.</span></span>| <span data-ttu-id="98308-128">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-129">Project</span><span class="sxs-lookup"><span data-stu-id="98308-129">Project</span></span> | <span data-ttu-id="98308-130">Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="98308-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="98308-131">Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="98308-132">Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="98308-133">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="98308-134">Uključeni zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-134">Included Tasks</span></span> | <span data-ttu-id="98308-135">Označava upotrebljava li se ovaj redak ponude za sve ili samo neke projektne zadatke odabranog projekta.</span><span class="sxs-lookup"><span data-stu-id="98308-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="98308-136">Polje ima sljedeće moguće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="98308-136">This field has the following possible values:</span></span></br><span data-ttu-id="98308-137">- Svi projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-137">- All project tasks</span></span></br><span data-ttu-id="98308-138">- Samo odabrani projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-138">- Selected project tasks only</span></span></br><span data-ttu-id="98308-139">Nepostojanje vrijednosti u ovom polju jednako je mogućnosti **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="98308-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="98308-140">Kada se odabere mogućnost **Samo odabrani projektni zadaci** na stranici projekta, kartica **Postavljanje naplate zadataka** omogućuje vam odabir određenih zadataka kako biste ih povezali s ovim retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="98308-141">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-142">Uvrsti vrijeme</span><span class="sxs-lookup"><span data-stu-id="98308-142">Include Time</span></span> | <span data-ttu-id="98308-143">Zastavica **Da**/**Ne** označava hoće li vremenske transakcije ili troškovi rada na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="98308-144">Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="98308-145">Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="98308-146">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-147">Uvrsti trošak</span><span class="sxs-lookup"><span data-stu-id="98308-147">Include Expense</span></span> | <span data-ttu-id="98308-148">Zastavica **Da**/**Ne** označava hoće li troškovi izdataka na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="98308-149">Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="98308-150">Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="98308-151">Ta se vrijednost polja kopira preko retka ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-152">Uvrsti naknadu</span><span class="sxs-lookup"><span data-stu-id="98308-152">Include Fee</span></span> | <span data-ttu-id="98308-153">Zastavica **Da**/**Ne** označava hoće li naknade na odabranom projektu biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="98308-154">Vrijednost **Ne** označava da naknade neće biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="98308-155">Vrijednost **Da** označava da će naknade biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="98308-156">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-157">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="98308-157">Quoted Amount</span></span> | <span data-ttu-id="98308-158">To je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="98308-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="98308-159">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike.</span><span class="sxs-lookup"><span data-stu-id="98308-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="98308-160">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="98308-161">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-162">Procijenjeni porez</span><span class="sxs-lookup"><span data-stu-id="98308-162">Estimated Tax</span></span> | <span data-ttu-id="98308-163">Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="98308-164">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="98308-165">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-166">Ponuđeni iznos nakon oporezivanja</span><span class="sxs-lookup"><span data-stu-id="98308-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="98308-167">Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="98308-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="98308-168">Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="98308-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="98308-169">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-170">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="98308-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="98308-171">Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="98308-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="98308-172">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="98308-173">Proračun klijenta</span><span class="sxs-lookup"><span data-stu-id="98308-173">Customer Budget</span></span> | <span data-ttu-id="98308-174">Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike.</span><span class="sxs-lookup"><span data-stu-id="98308-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="98308-175">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="98308-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="98308-176">Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="98308-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="98308-177">**Pravilo 1**: Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci**, projekt je uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="98308-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="98308-178">**Pravilo 2**: Ako je polje **Uključeni zadaci** prazno ili je postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti samo u jedan redak ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="98308-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="98308-179">**Pravilo 3**: Ako je polje **Uključeni zadaci** postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti u više redaka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="98308-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="98308-180">**Pravilo 4**: Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="98308-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="98308-181">**Pravilo 5**: Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="98308-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="98308-182">
                    <strong>Prilika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="98308-183">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="98308-184">
                    <strong>Redak ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="98308-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="98308-186">
                    <strong>Uključeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="98308-187">
                    <strong>Uvrsti vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="98308-188">
                    <strong>Uvrsti trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="98308-189">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="98308-190">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="98308-191">
                    <strong>Valjan / nije valjan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="98308-192">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="98308-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-193">O1</span><span class="sxs-lookup"><span data-stu-id="98308-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-194">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-195">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-196">P1</span><span class="sxs-lookup"><span data-stu-id="98308-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-197">Prazno</span><span class="sxs-lookup"><span data-stu-id="98308-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-198">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-199">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-200">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-201">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="98308-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-202">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="98308-202">Violation of Rule #2.</span></span> <span data-ttu-id="98308-203">Vrijeme, trošak i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="98308-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-204">O1</span><span class="sxs-lookup"><span data-stu-id="98308-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-205">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-206">QL2</span><span class="sxs-lookup"><span data-stu-id="98308-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-207">P1</span><span class="sxs-lookup"><span data-stu-id="98308-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-208">Prazno</span><span class="sxs-lookup"><span data-stu-id="98308-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-209">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-210">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-211">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="98308-212">O1</span><span class="sxs-lookup"><span data-stu-id="98308-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-213">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-214">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-215">P1</span><span class="sxs-lookup"><span data-stu-id="98308-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-216">Prazno</span><span class="sxs-lookup"><span data-stu-id="98308-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-217">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-218">No</span><span class="sxs-lookup"><span data-stu-id="98308-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-219">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-220">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="98308-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-221">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="98308-221">Violation of Rule #2.</span></span> <span data-ttu-id="98308-222">Vrijeme i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="98308-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-223">O1</span><span class="sxs-lookup"><span data-stu-id="98308-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-224">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-225">QL2</span><span class="sxs-lookup"><span data-stu-id="98308-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-226">P1</span><span class="sxs-lookup"><span data-stu-id="98308-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-227">Prazno</span><span class="sxs-lookup"><span data-stu-id="98308-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-228">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-229">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-230">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-231">O1</span><span class="sxs-lookup"><span data-stu-id="98308-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-232">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-233">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-234">P1</span><span class="sxs-lookup"><span data-stu-id="98308-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="98308-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-236">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-237">No</span><span class="sxs-lookup"><span data-stu-id="98308-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-238">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-239">Valjano</span><span class="sxs-lookup"><span data-stu-id="98308-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="98308-240">Vrijeme i naknade za projekt P1 uključeni su u QL1.</span><span class="sxs-lookup"><span data-stu-id="98308-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="98308-241">Trošak za projekt P1 uključen je u QL2.</span><span class="sxs-lookup"><span data-stu-id="98308-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="98308-242">Nema preklapanja onoga što je uključeno u svaki redak ponude, a valjano je.</span><span class="sxs-lookup"><span data-stu-id="98308-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-243">O1</span><span class="sxs-lookup"><span data-stu-id="98308-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-244">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-245">QL2</span><span class="sxs-lookup"><span data-stu-id="98308-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-246">P1</span><span class="sxs-lookup"><span data-stu-id="98308-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-247">Prazno</span><span class="sxs-lookup"><span data-stu-id="98308-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-248">No</span><span class="sxs-lookup"><span data-stu-id="98308-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-249">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-250">No</span><span class="sxs-lookup"><span data-stu-id="98308-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="98308-251">O1</span><span class="sxs-lookup"><span data-stu-id="98308-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-252">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-253">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-254">P1</span><span class="sxs-lookup"><span data-stu-id="98308-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-255">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-256">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-257">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-258">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-259">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="98308-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-260">Kršenje gornjeg pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="98308-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="98308-261">Q1 uključuje vrijeme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="98308-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="98308-262">QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i preklapa se s onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="98308-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-263">O1</span><span class="sxs-lookup"><span data-stu-id="98308-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-264">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-265">QL2</span><span class="sxs-lookup"><span data-stu-id="98308-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-266">P1</span><span class="sxs-lookup"><span data-stu-id="98308-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-267">Prazno</span><span class="sxs-lookup"><span data-stu-id="98308-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-268">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-269">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-270">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-271">O1</span><span class="sxs-lookup"><span data-stu-id="98308-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-272">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-273">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-274">P1</span><span class="sxs-lookup"><span data-stu-id="98308-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-275">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-276">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-277">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-278">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-279">Valjano</span><span class="sxs-lookup"><span data-stu-id="98308-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-280">Prema naprijed navedenom pravilu br. 3,</span><span class="sxs-lookup"><span data-stu-id="98308-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="98308-281">Q1 uključuje vrijeme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="98308-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="98308-282">QL2 uključuje vrijeme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="98308-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="98308-283">Jedina dodatna provjera valjanosti odnosi se na podskup zadataka na QL1 koji se razlikuju od podskupa zadataka na QL2.</span><span class="sxs-lookup"><span data-stu-id="98308-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="98308-284">To osigurava da nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="98308-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="98308-285">To čini sustav kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="98308-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-286">O1</span><span class="sxs-lookup"><span data-stu-id="98308-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-287">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-288">QL2</span><span class="sxs-lookup"><span data-stu-id="98308-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-289">P1</span><span class="sxs-lookup"><span data-stu-id="98308-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-290">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-291">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-292">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-293">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="98308-294">O1</span><span class="sxs-lookup"><span data-stu-id="98308-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-295">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-296">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-297">P1</span><span class="sxs-lookup"><span data-stu-id="98308-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-298">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-299">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-300">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-301">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="98308-302">Valjano</span><span class="sxs-lookup"><span data-stu-id="98308-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-303">Na temelju pravila br. 5, Q1 i Q2 dvije su ponude u istoj prilici, tako da obje mogu procijeniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="98308-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-304">O1</span><span class="sxs-lookup"><span data-stu-id="98308-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-305">2. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-306">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-307">P1</span><span class="sxs-lookup"><span data-stu-id="98308-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-308">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-309">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-310">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-311">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="98308-312">O1</span><span class="sxs-lookup"><span data-stu-id="98308-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-313">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-314">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-315">P1</span><span class="sxs-lookup"><span data-stu-id="98308-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-316">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-317">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-318">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-319">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="98308-320">Valjano</span><span class="sxs-lookup"><span data-stu-id="98308-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="98308-321">Na temelju pravila br. 4, Q1 i Q2 dvije su ponude u različitim prilikama, tako da ne mogu procijeniti iste komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="98308-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="98308-322">O2</span><span class="sxs-lookup"><span data-stu-id="98308-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="98308-323">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="98308-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-324">QL1</span><span class="sxs-lookup"><span data-stu-id="98308-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-325">P1</span><span class="sxs-lookup"><span data-stu-id="98308-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="98308-326">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="98308-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-327">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="98308-328">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="98308-329">Jest</span><span class="sxs-lookup"><span data-stu-id="98308-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="98308-330">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="98308-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

