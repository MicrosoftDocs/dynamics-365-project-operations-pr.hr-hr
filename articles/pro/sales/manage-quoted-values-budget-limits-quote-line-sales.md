---
title: Redci ponude utemeljeni na projektu (Pro)
description: U ovoj temi nalaze se informacije o uporabi redaka ponude koji se temelje na projektu za rad na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073318"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="fb9c7-104">Redci ponude utemeljeni na projektu (Pro)</span><span class="sxs-lookup"><span data-stu-id="fb9c7-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="fb9c7-105">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="fb9c7-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fb9c7-106">Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="fb9c7-107">Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="fb9c7-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="fb9c7-108">Način naplate</span><span class="sxs-lookup"><span data-stu-id="fb9c7-108">Billing Method</span></span>
- <span data-ttu-id="fb9c7-109">Mapiranje projekta i zadatka</span><span class="sxs-lookup"><span data-stu-id="fb9c7-109">Project and Task Mapping</span></span>
- <span data-ttu-id="fb9c7-110">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="fb9c7-110">Included Transaction classes</span></span>
- <span data-ttu-id="fb9c7-111">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="fb9c7-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="fb9c7-112">Postavka naplativosti</span><span class="sxs-lookup"><span data-stu-id="fb9c7-112">Chargeability setup</span></span>
- <span data-ttu-id="fb9c7-113">Procjena s pomoću pojedinosti retka ponude</span><span class="sxs-lookup"><span data-stu-id="fb9c7-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="fb9c7-114">Klijenti retka ponude</span><span class="sxs-lookup"><span data-stu-id="fb9c7-114">Quote line Customers</span></span>

<span data-ttu-id="fb9c7-115">Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="fb9c7-116">Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="fb9c7-117">**Polje**</span><span class="sxs-lookup"><span data-stu-id="fb9c7-117">**Field**</span></span> | <span data-ttu-id="fb9c7-118">**Relevantnost, svrha i smjernice**</span><span class="sxs-lookup"><span data-stu-id="fb9c7-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="fb9c7-119">**Utjecaj prema dolje**</span><span class="sxs-lookup"><span data-stu-id="fb9c7-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fb9c7-120">Ime</span><span class="sxs-lookup"><span data-stu-id="fb9c7-120">Name</span></span> | <span data-ttu-id="fb9c7-121">Naziv retka ponude koji bi vam trebao pomoći pri prepoznavanju diskretne komponente ponude koja se procjenjuje.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="fb9c7-122">Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-123">Način naplate</span><span class="sxs-lookup"><span data-stu-id="fb9c7-123">Billing Method</span></span> | <span data-ttu-id="fb9c7-124">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="fb9c7-125">Ovo polje uključuje dva glavna načina ugovaranja koje podržava aplikacija Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="fb9c7-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="fb9c7-126">- Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="fb9c7-126">- Fixed price</span></span></br><span data-ttu-id="fb9c7-127">- Vrijeme i materijal.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-127">- Time and material.</span></span>| <span data-ttu-id="fb9c7-128">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-129">Project</span><span class="sxs-lookup"><span data-stu-id="fb9c7-129">Project</span></span> | <span data-ttu-id="fb9c7-130">Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="fb9c7-131">Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="fb9c7-132">Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="fb9c7-133">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="fb9c7-134">Uključeni zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-134">Included Tasks</span></span> | <span data-ttu-id="fb9c7-135">Označava upotrebljava li se ovaj redak ponude za sve ili samo neke projektne zadatke odabranog projekta.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="fb9c7-136">Polje ima sljedeće moguće vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="fb9c7-136">This field has the following possible values:</span></span></br><span data-ttu-id="fb9c7-137">- Svi projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-137">- All project tasks</span></span></br><span data-ttu-id="fb9c7-138">- Samo odabrani projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-138">- Selected project tasks only</span></span></br><span data-ttu-id="fb9c7-139">Nepostojanje vrijednosti u ovom polju jednako je mogućnosti **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="fb9c7-140">Kada se odabere mogućnost **Samo odabrani projektni zadaci** na stranici projekta, kartica **Postavljanje naplate zadataka** omogućuje vam odabir određenih zadataka kako biste ih povezali s ovim retkom ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="fb9c7-141">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-142">Uvrsti vrijeme</span><span class="sxs-lookup"><span data-stu-id="fb9c7-142">Include Time</span></span> | <span data-ttu-id="fb9c7-143">Zastavica **Da**/**Ne** označava hoće li vremenske transakcije ili troškovi rada na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb9c7-144">Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb9c7-145">Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fb9c7-146">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-147">Uvrsti trošak</span><span class="sxs-lookup"><span data-stu-id="fb9c7-147">Include Expense</span></span> | <span data-ttu-id="fb9c7-148">Zastavica **Da**/**Ne** označava hoće li troškovi izdataka na odabranom projektu biti uključeni u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb9c7-149">Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb9c7-150">Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fb9c7-151">Ta se vrijednost polja kopira preko retka ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-152">Uvrsti naknadu</span><span class="sxs-lookup"><span data-stu-id="fb9c7-152">Include Fee</span></span> | <span data-ttu-id="fb9c7-153">Zastavica **Da**/**Ne** označava hoće li naknade na odabranom projektu biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb9c7-154">Vrijednost **Ne** označava da naknade neće biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb9c7-155">Vrijednost **Da** označava da će naknade biti uključene u procjenu u ovom retku ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fb9c7-156">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-157">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="fb9c7-157">Quoted Amount</span></span> | <span data-ttu-id="fb9c7-158">To je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="fb9c7-159">U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="fb9c7-160">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="fb9c7-161">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-162">Procijenjeni porez</span><span class="sxs-lookup"><span data-stu-id="fb9c7-162">Estimated Tax</span></span> | <span data-ttu-id="fb9c7-163">Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="fb9c7-164">Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="fb9c7-165">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-166">Ponuđeni iznos nakon oporezivanja</span><span class="sxs-lookup"><span data-stu-id="fb9c7-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="fb9c7-167">Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="fb9c7-168">Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="fb9c7-169">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-170">Ograničenje koje se ne smije prekoračiti</span><span class="sxs-lookup"><span data-stu-id="fb9c7-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="fb9c7-171">Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="fb9c7-172">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb9c7-173">Proračun klijenta</span><span class="sxs-lookup"><span data-stu-id="fb9c7-173">Customer Budget</span></span> | <span data-ttu-id="fb9c7-174">Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="fb9c7-175">Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="fb9c7-176">Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="fb9c7-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="fb9c7-177">**Pravilo 1** : Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci** , projekt je uključen u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="fb9c7-178">**Pravilo 2** : Ako je polje **Uključeni zadaci** prazno ili je postavljeno na **Svi projektni zadaci** , projekt i određena klasa transakcija mogu se uključiti samo u jedan redak ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="fb9c7-179">**Pravilo 3** : Ako je polje **Uključeni zadaci** postavljeno na **Svi projektni zadaci** , projekt i određena klasa transakcija mogu se uključiti u više redaka ponude koji se temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="fb9c7-180">**Pravilo 4** : Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="fb9c7-181">**Pravilo 5** : Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="fb9c7-182">
                    <strong>Prilika</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="fb9c7-183">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fb9c7-184">
                    <strong>Redak ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fb9c7-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="fb9c7-186">
                    <strong>Uključeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fb9c7-187">
                    <strong>Uvrsti vrijeme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fb9c7-188">
                    <strong>Uvrsti trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fb9c7-189">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="fb9c7-190">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="fb9c7-191">
                    <strong>Valjan / nije valjan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="fb9c7-192">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb9c7-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-193">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-194">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-195">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-196">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-197">Prazno</span><span class="sxs-lookup"><span data-stu-id="fb9c7-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-198">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-199">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-200">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-201">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="fb9c7-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-202">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-202">Violation of Rule #2.</span></span> <span data-ttu-id="fb9c7-203">Vrijeme, trošak i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-204">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-205">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-206">QL2</span><span class="sxs-lookup"><span data-stu-id="fb9c7-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-207">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-208">Prazno</span><span class="sxs-lookup"><span data-stu-id="fb9c7-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-209">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-210">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-211">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-211">Yes</span></span> </p>
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
<span data-ttu-id="fb9c7-212">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-213">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-214">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-215">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-216">Prazno</span><span class="sxs-lookup"><span data-stu-id="fb9c7-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-217">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-218">No</span><span class="sxs-lookup"><span data-stu-id="fb9c7-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-219">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-220">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="fb9c7-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-221">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-221">Violation of Rule #2.</span></span> <span data-ttu-id="fb9c7-222">Vrijeme i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-223">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-224">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-225">QL2</span><span class="sxs-lookup"><span data-stu-id="fb9c7-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-226">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-227">Prazno</span><span class="sxs-lookup"><span data-stu-id="fb9c7-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-228">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-229">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-230">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-230">Yes</span></span> </p>
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
<span data-ttu-id="fb9c7-231">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-232">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-233">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-234">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="fb9c7-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-236">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-237">No</span><span class="sxs-lookup"><span data-stu-id="fb9c7-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-238">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-239">Valjano</span><span class="sxs-lookup"><span data-stu-id="fb9c7-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="fb9c7-240">Vrijeme i naknade za projekt P1 uključeni su u QL1.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="fb9c7-241">Trošak za projekt P1 uključen je u QL2.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="fb9c7-242">Nema preklapanja onoga što je uključeno u svaki redak ponude, a valjano je.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-243">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-244">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-245">QL2</span><span class="sxs-lookup"><span data-stu-id="fb9c7-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-246">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-247">Prazno</span><span class="sxs-lookup"><span data-stu-id="fb9c7-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-248">No</span><span class="sxs-lookup"><span data-stu-id="fb9c7-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-249">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-250">No</span><span class="sxs-lookup"><span data-stu-id="fb9c7-250">No</span></span> </p>
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
<span data-ttu-id="fb9c7-251">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-252">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-253">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-254">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-255">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-256">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-257">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-258">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-259">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="fb9c7-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-260">Kršenje gornjeg pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="fb9c7-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="fb9c7-261">Q1 uključuje vrijeme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fb9c7-262">QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i preklapa se s onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-263">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-264">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-265">QL2</span><span class="sxs-lookup"><span data-stu-id="fb9c7-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-266">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-267">Prazno</span><span class="sxs-lookup"><span data-stu-id="fb9c7-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-268">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-269">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-270">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-270">Yes</span></span> </p>
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
<span data-ttu-id="fb9c7-271">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-272">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-273">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-274">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-275">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-276">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-277">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-278">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-279">Valjano</span><span class="sxs-lookup"><span data-stu-id="fb9c7-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-280">Prema naprijed navedenom pravilu br. 3,</span><span class="sxs-lookup"><span data-stu-id="fb9c7-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="fb9c7-281">Q1 uključuje vrijeme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fb9c7-282">QL2 uključuje vrijeme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fb9c7-283">Jedina dodatna provjera valjanosti odnosi se na podskup zadataka na QL1 koji se razlikuju od podskupa zadataka na QL2.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="fb9c7-284">To osigurava da nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="fb9c7-285">To čini sustav kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-286">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-287">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-288">QL2</span><span class="sxs-lookup"><span data-stu-id="fb9c7-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-289">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-290">Samo odabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-291">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-292">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-293">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-293">Yes</span></span> </p>
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
<span data-ttu-id="fb9c7-294">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-295">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-296">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-297">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-298">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-299">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-300">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-301">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fb9c7-302">Valjano</span><span class="sxs-lookup"><span data-stu-id="fb9c7-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-303">Na temelju pravila br. 5, Q1 i Q2 dvije su ponude u istoj prilici, tako da obje mogu procijeniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-304">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-305">2. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-306">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-307">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-308">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-309">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-310">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-311">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-311">Yes</span></span> </p>
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
<span data-ttu-id="fb9c7-312">O1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-313">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-314">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-315">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-316">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-317">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-318">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-319">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fb9c7-320">Valjano</span><span class="sxs-lookup"><span data-stu-id="fb9c7-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb9c7-321">Na temelju pravila br. 4, Q1 i Q2 dvije su ponude u različitim prilikama, tako da ne mogu procijeniti iste komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb9c7-322">O2</span><span class="sxs-lookup"><span data-stu-id="fb9c7-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb9c7-323">1. tromj.</span><span class="sxs-lookup"><span data-stu-id="fb9c7-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-324">QL1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-325">P1</span><span class="sxs-lookup"><span data-stu-id="fb9c7-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="fb9c7-326">Svi ili prazni projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="fb9c7-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-327">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb9c7-328">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb9c7-329">Jest</span><span class="sxs-lookup"><span data-stu-id="fb9c7-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fb9c7-330">Nije valjan</span><span class="sxs-lookup"><span data-stu-id="fb9c7-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

