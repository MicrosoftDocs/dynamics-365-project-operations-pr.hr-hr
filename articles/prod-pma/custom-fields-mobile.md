---
title: Uvođenje prilagođenih polja za mobilnu aplikaciju Microsoft Dynamics 365 Project Timesheet na platformama iOS i Android
description: U ovoj temi nalaze se uobičajeni uzorci za uporabu nastavaka za uvođenje prilagođenih polja.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073442"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="d4c86-103">Uvođenje prilagođenih polja za mobilnu aplikaciju Microsoft Dynamics 365 Project Timesheet na platformama iOS i Android</span><span class="sxs-lookup"><span data-stu-id="d4c86-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4c86-104">U ovoj temi nalaze se uobičajeni uzorci za uporabu nastavaka za uvođenje prilagođenih polja.</span><span class="sxs-lookup"><span data-stu-id="d4c86-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="d4c86-105">Obuhvaćene su sljedeće teme:</span><span class="sxs-lookup"><span data-stu-id="d4c86-105">The following topics are covered:</span></span>

- <span data-ttu-id="d4c86-106">Razne vrste podataka koje podržava prilagođeni okvir polja</span><span class="sxs-lookup"><span data-stu-id="d4c86-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="d4c86-107">Način prikazivanja polja samo za čitanje ili uređivanje na unosima evidencije radnog vremena i spremanje vrijednosti koje su unijeli korisnici natrag u bazu podataka</span><span class="sxs-lookup"><span data-stu-id="d4c86-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="d4c86-108">Način prikazivanja polja samo za čitanje u zaglavlju evidencije radnog vremena</span><span class="sxs-lookup"><span data-stu-id="d4c86-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="d4c86-109">Način integriranja druge prilagođene poslovne logike za unos zadanih vrijednosti u polja i provođenje dodatne provjere valjanosti</span><span class="sxs-lookup"><span data-stu-id="d4c86-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="d4c86-110">Korisnici</span><span class="sxs-lookup"><span data-stu-id="d4c86-110">Audience</span></span>

<span data-ttu-id="d4c86-111">Ovaj tema namijenjena je razvojnim inženjerima koji integriraju prilagođena polja u mobilnu aplikaciju Microsoft Dynamics 365 Project Timesheet koja je dostupna za platforme Apple iOS i Google Android.</span><span class="sxs-lookup"><span data-stu-id="d4c86-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="d4c86-112">Pretpostavka je da su čitatelji upoznati s X++ razvojem i funkcionalnošću evidencije radnog vremena na projektu.</span><span class="sxs-lookup"><span data-stu-id="d4c86-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="d4c86-113">Ugovor o podacima – klasa TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="d4c86-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="d4c86-114">Klasa **TSTimesheetCustomField** klasa je ugovora podataka X++ koja predstavlja informacije o prilagođenom polju za funkcionalnost evidencije radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="d4c86-115">Popisi objekata prilagođenih polja prosljeđuju se na oba ugovora o podacima, i TSTimesheetDetails i TSTimesheetEntry, radi prikazivanja prilagođenih polja u mobilnoj aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="d4c86-116">**TSTimesheetDetails** – Ugovor o zaglavlju evidencije radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="d4c86-117">**TSTimesheetEntry** – Ugovor o transakciji evidencije radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="d4c86-118">Grupe ovih objekata koje imaju iste podatke o projektu i vrijednost **timesheetLineRecId** čine redak.</span><span class="sxs-lookup"><span data-stu-id="d4c86-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="d4c86-119">fieldBaseType (vrste)</span><span class="sxs-lookup"><span data-stu-id="d4c86-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="d4c86-120">Svojstvo **FieldBaseType** na objektu **TsTimesheetCustom** određuje vrstu polja koje se prikazuje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="d4c86-121">Podržane su sljedeće vrijednosti **Vrste**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="d4c86-122">Vrijednost vrsta</span><span class="sxs-lookup"><span data-stu-id="d4c86-122">Types value</span></span> | <span data-ttu-id="d4c86-123">Tip</span><span class="sxs-lookup"><span data-stu-id="d4c86-123">Type</span></span>              | <span data-ttu-id="d4c86-124">Bilješke</span><span class="sxs-lookup"><span data-stu-id="d4c86-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="d4c86-125">0</span><span class="sxs-lookup"><span data-stu-id="d4c86-125">0</span></span>           | <span data-ttu-id="d4c86-126">Niz (i nabrajanje)</span><span class="sxs-lookup"><span data-stu-id="d4c86-126">String (and Enum)</span></span> | <span data-ttu-id="d4c86-127">Polje se prikazuje kao tekstno polje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="d4c86-128">1</span><span class="sxs-lookup"><span data-stu-id="d4c86-128">1</span></span>           | <span data-ttu-id="d4c86-129">Integer</span><span class="sxs-lookup"><span data-stu-id="d4c86-129">Integer</span></span>           | <span data-ttu-id="d4c86-130">Vrijednost je prikazana kao broj bez decimalnih mjesta.</span><span class="sxs-lookup"><span data-stu-id="d4c86-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="d4c86-131">2</span><span class="sxs-lookup"><span data-stu-id="d4c86-131">2</span></span>           | <span data-ttu-id="d4c86-132">Stvaran</span><span class="sxs-lookup"><span data-stu-id="d4c86-132">Real</span></span>              | <span data-ttu-id="d4c86-133">Vrijednost je prikazana kao broj s decimalnim mjestima.</span><span class="sxs-lookup"><span data-stu-id="d4c86-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="d4c86-134">Kako biste prikazali stvarnu vrijednost kao valutu u aplikaciji, upotrijebite svojstvo **fieldExtensedType**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="d4c86-135">Možete upotrijebiti svojstvo **numberOfDecimals** za postavljanja broja decimalnih mjesta koji će se prikazati.</span><span class="sxs-lookup"><span data-stu-id="d4c86-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="d4c86-136">3</span><span class="sxs-lookup"><span data-stu-id="d4c86-136">3</span></span>           | <span data-ttu-id="d4c86-137">Datum</span><span class="sxs-lookup"><span data-stu-id="d4c86-137">Date</span></span>              | <span data-ttu-id="d4c86-138">Oblici datuma određeni su korisničkom postavkom **Datum, vrijeme i oblik broja** koja je navedena pod stavkom **Preferencije jezika i zemlje/regije** u mogućnosti **Korisničke mogućnosti**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="d4c86-139">4</span><span class="sxs-lookup"><span data-stu-id="d4c86-139">4</span></span>           | <span data-ttu-id="d4c86-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4c86-140">Boolean</span></span>           | |
| <span data-ttu-id="d4c86-141">15</span><span class="sxs-lookup"><span data-stu-id="d4c86-141">15</span></span>          | <span data-ttu-id="d4c86-142">GUID</span><span class="sxs-lookup"><span data-stu-id="d4c86-142">GUID</span></span>              | |
| <span data-ttu-id="d4c86-143">16</span><span class="sxs-lookup"><span data-stu-id="d4c86-143">16</span></span>          | <span data-ttu-id="d4c86-144">Int64</span><span class="sxs-lookup"><span data-stu-id="d4c86-144">Int64</span></span>             | |

- <span data-ttu-id="d4c86-145">Ako svojstvo **stringOptions** nije osigurano objektu **TSTimesheetCustomField** , korisniku se omogućuje polje slobodnog teksta.</span><span class="sxs-lookup"><span data-stu-id="d4c86-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="d4c86-146">Svojstvo **stringLength** može se upotrebljavati za postavljanje maksimalne duljine niza koju korisnici mogu unijeti.</span><span class="sxs-lookup"><span data-stu-id="d4c86-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="d4c86-147">Ako je svojstvo **stringOptions** osigurano objektu **TSTimesheetCustomField** , ti su elementi popisa jedine vrijednosti koje korisnici mogu odabrati s pomoću gumba s mogućnostima (gumbi za odabir).</span><span class="sxs-lookup"><span data-stu-id="d4c86-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="d4c86-148">U ovom slučaju polje niza može djelovati kao vrijednost nabrajanja u svrhu korisničkog unosa.</span><span class="sxs-lookup"><span data-stu-id="d4c86-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="d4c86-149">Kako biste vrijednost spremili u bazu podataka kao nabrajanje, ručno mapirajte vrijednost niza natrag u vrijednost nabrajanja prije spremanja u bazu podataka s pomoću lanca naredbi (kao primjer pogledajte odjeljak „Uporaba lanca naredbe na klasi TSTimesheetEntryService za spremanje unosa evidencije radnog vremena iz aplikacija natrag u bazu podataka” u nastavku ove teme).</span><span class="sxs-lookup"><span data-stu-id="d4c86-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="d4c86-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="d4c86-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="d4c86-151">Ovo svojstvo možete upotrebljavati za oblikovanje stvarnih vrijednosti kao valute.</span><span class="sxs-lookup"><span data-stu-id="d4c86-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="d4c86-152">Ovaj pristup primjenjiv je samo kada je vrijednost **fieldBaseType** **Stvarna**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="d4c86-153">**TSCustomFieldExtendedType: Nijedan** – Nije primijenjeno oblikovanje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="d4c86-154">**TSCustomFieldExtendedType::Valuta** – Formatiranje vrijednosti kao valute.</span><span class="sxs-lookup"><span data-stu-id="d4c86-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="d4c86-155">Kada je aktivno formatiranje valute, polje **stringValue** može se upotrebljavati za dodavanje koda valute koji bi se trebao prikazati u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="d4c86-156">Vrijednost je vrijednost samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-156">The value is a read-only value.</span></span>

    <span data-ttu-id="d4c86-157">Polje **realValue** sadrži iznos novca koji bi se trebao spremiti u bazu podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="d4c86-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="d4c86-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="d4c86-159">Ovo svojstvo možete upotrijebiti za određivanje mjesta u aplikaciji na kojem bi se prilagođeno polje trebalo prikazati.</span><span class="sxs-lookup"><span data-stu-id="d4c86-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="d4c86-160">**TSCustomFieldSection::Zaglavlje** – Polje će se prikazati u odjeljku **Pogledajte više pojedinosti** u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="d4c86-161">Ova polja uvijek su samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-161">These fields are always read-only.</span></span>
- <span data-ttu-id="d4c86-162">**TSCustomFieldSection::Redak** – Polje će se prikazati nakon svih polja s gotovim retkom u unosima evidencije radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="d4c86-163">Ta polja mogu se uređivati ili biti samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="d4c86-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="d4c86-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="d4c86-165">Ovo svojstvo identificira polje kada se vrijednosti koje daje aplikacija spremaju natrag u bazu podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="d4c86-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="d4c86-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="d4c86-167">Ovo svojstvo identificira polje kada se vrijednosti koje daje aplikacija spremaju natrag u bazu podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="d4c86-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="d4c86-168">isEditable (NoYes)</span></span>

<span data-ttu-id="d4c86-169">Postavite ovo svojstvo na **Da** kako biste odredili da polje u odjeljku za unos evidencije radnog vremena trebaju uređivati korisnici.</span><span class="sxs-lookup"><span data-stu-id="d4c86-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="d4c86-170">Postavite svojstvo na **Ne** kako bi polje bilo samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="d4c86-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="d4c86-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="d4c86-172">Postavite ovo svojstvo na **Da** kako biste odredili da je polje u odjeljku za unos evidencije radnog vremena obvezno.</span><span class="sxs-lookup"><span data-stu-id="d4c86-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="d4c86-173">oznaka (niz)</span><span class="sxs-lookup"><span data-stu-id="d4c86-173">label (str)</span></span>

<span data-ttu-id="d4c86-174">Ovo svojstvo navodi oznaku koja se prikazuje pokraj polja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="d4c86-175">stringOptions (Popis nizova)</span><span class="sxs-lookup"><span data-stu-id="d4c86-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="d4c86-176">Ovo je svojstvo primjenjivo samo kada je **fieldBaseType** postavljeno na **Niz**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="d4c86-177">Ako je stavka **stringOptions** postavljena, vrijednosti niza koje su dostupne za odabir putem gumba mogućnosti (gumb za odabir) određene su nizovima na popisu.</span><span class="sxs-lookup"><span data-stu-id="d4c86-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="d4c86-178">Ako nije osiguran nijedan niz, u polje niza dozvoljen je unos slobodnog teksta (kao primjer pogledajte odjeljak „Uporaba lanca naredbi na klasi TSTimesheetEntryService za spremanje unosa evidencije radnog vremena iz aplikacije natrag u bazu podataka” u nastavku ove teme).</span><span class="sxs-lookup"><span data-stu-id="d4c86-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="d4c86-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="d4c86-179">stringLength (int)</span></span>

<span data-ttu-id="d4c86-180">Ovo svojstvo određuje maksimalnu duljinu polja niza.</span><span class="sxs-lookup"><span data-stu-id="d4c86-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="d4c86-181">Primjenjivo je samo kada je **fieldBaseType** postavljeno na **Niz**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="d4c86-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="d4c86-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="d4c86-183">Ovo svojstvo navodi broj decimalnih mjesta koja se prikazuju za stvarno polje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="d4c86-184">Primjenjivo je samo kada je **fieldBaseType** postavljeno na **Stvarno**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="d4c86-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="d4c86-185">orderSequence (int)</span></span>

<span data-ttu-id="d4c86-186">Ovo svojstvo nadzire redoslijed prikazivanja prilagođenih polja u aplikaciji kada je navedeno više od jednog prilagođenog polja.</span><span class="sxs-lookup"><span data-stu-id="d4c86-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="d4c86-187">Prvo se prikazuju polja s manjim brojevima.</span><span class="sxs-lookup"><span data-stu-id="d4c86-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="d4c86-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="d4c86-188">booleanValue (boolean)</span></span>

<span data-ttu-id="d4c86-189">Za polja vrste **Boole** , ovo svojstvo prenosi Booleovu vrijednost polja između poslužitelja i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="d4c86-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="d4c86-190">guidValue (guid)</span></span>

<span data-ttu-id="d4c86-191">Za polja vrste **GUID** , ovo svojstvo prenosi vrijednost globalno jedinstvenog identifikatora (GUID) polja između poslužitelja i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="d4c86-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="d4c86-192">int64Value (int64)</span></span>

<span data-ttu-id="d4c86-193">Za polja vrste **Int64** , ovo svojstvo prenosi Int64 vrijednost polja između poslužitelja i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="d4c86-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="d4c86-194">intValue (int)</span></span>

<span data-ttu-id="d4c86-195">Za polja vrste **Int** , ovo svojstvo prenosi int vrijednost polja između poslužitelja i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="d4c86-196">realValue (stvarno)</span><span class="sxs-lookup"><span data-stu-id="d4c86-196">realValue (real)</span></span>

<span data-ttu-id="d4c86-197">Za polja vrste **Stvarno** , ovo svojstvo prenosi stvarnu vrijednost polja između poslužitelja i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="d4c86-198">stringValue (niz)</span><span class="sxs-lookup"><span data-stu-id="d4c86-198">stringValue (str)</span></span>

<span data-ttu-id="d4c86-199">Za polja vrste **Niz** , ovo svojstvo prenosi vrijednost niza u polju između poslužitelja i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="d4c86-200">Također se upotrebljava za polja vrste **Stvarno** koja su formatirana kao valuta.</span><span class="sxs-lookup"><span data-stu-id="d4c86-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="d4c86-201">Za ta polja svojstvo se upotrebljava za prosljeđivanje koda valute aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="d4c86-202">dateValue (datum)</span><span class="sxs-lookup"><span data-stu-id="d4c86-202">dateValue (date)</span></span>

<span data-ttu-id="d4c86-203">Za polja vrste **Datum** , ovo svojstvo prenosi vrijednost datuma u polju između poslužitelja i aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="d4c86-204">Prikaz i spremanje prilagođenog polja u odjeljku unosa evidencije radnog vremena</span><span class="sxs-lookup"><span data-stu-id="d4c86-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="d4c86-205">U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj se stvara unos evidencije radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="d4c86-206">Prikazuje gotova i prilagođena polja u odjeljku „Unos vremena” pod nazivom „Testni niz” s već postavljenom vrijednosti nabrajanja „Druga mogućnost”.</span><span class="sxs-lookup"><span data-stu-id="d4c86-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testni niz prilagođenog polja u aplikaciji](media/timesheet-entry.jpg)



<span data-ttu-id="d4c86-208">U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj korisnik odabire jednu od mogućnosti nabrajanja dostupnih za prilagođeno polje „Testni niz”.</span><span class="sxs-lookup"><span data-stu-id="d4c86-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="d4c86-209">Dvije mogućnosti, „Prva mogućnost” i „Druga mogućnost”, prikazane su kao gumbi za odabir.</span><span class="sxs-lookup"><span data-stu-id="d4c86-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="d4c86-210">Trenutačno je odabrana druga mogućnost.</span><span class="sxs-lookup"><span data-stu-id="d4c86-210">The second option is currently selected.</span></span>

![Gumbi mogućnosti (gumbi za odabir) za prilagođeno polje Testni niz](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="d4c86-212">Proširivanje tablice TSTimesheetLine tako da ima prilagođeno polje</span><span class="sxs-lookup"><span data-stu-id="d4c86-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="d4c86-213">U uobičajenim scenarijima vjerojatno će se podaci za prilagođeno polje u odjeljku unosa evidencije radnog vremena spremiti u tablicu TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="d4c86-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="d4c86-214">Međutim, druge se tablice mogu upotrebljavati ako se podaci mogu dohvatiti na temelju dostavljenog zapisa TSTimesheetTrans ili ako nema određenog konteksta zapisa (na primjer, ako je u parametrima projekta polje postavljeno kao samo za čitanje).</span><span class="sxs-lookup"><span data-stu-id="d4c86-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="d4c86-215">Imajte na umu da prilagođena polja ne moraju imati nikakve sigurnosne zapise baze podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="d4c86-216">Mogu se dinamički generirati na temelju X++ logike.</span><span class="sxs-lookup"><span data-stu-id="d4c86-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="d4c86-217">Ovaj pristup može biti koristan u scenarijima samo za čitanje (primjer dinamički generiranih vrijednosti prilagođenih polja potražite u odjeljku „Uporaba lanca naredbi na klasi TSTimesheetDetails, načina buildCustomFieldListForHeader za popunjavanje pojedinosti evidencije radnog vremena”.)</span><span class="sxs-lookup"><span data-stu-id="d4c86-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="d4c86-218">U nastavku se nalazi snimka zaslona aplikacije Visual Studio na kojem se nalazi stablo objekata aplikacije.</span><span class="sxs-lookup"><span data-stu-id="d4c86-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="d4c86-219">Ona prikazuje proširenje tablice TSTimesheetLine poljem TestLineString koje je dodano kao prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Niz retka](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="d4c86-221">Uporaba lanca naredbi u načinu buildCustomFieldList klase TSTimesheetSettings za prikaz polja u odjeljku unosa evidencije radnog vremena</span><span class="sxs-lookup"><span data-stu-id="d4c86-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="d4c86-222">Ovaj kôd regulira postavke zaslona za polje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="d4c86-223">Na primjer, regulira vrstu polja, oznaku, je li polje obavezno i u kojem se odjeljku polje prikazuje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="d4c86-224">Sljedeći primjer prikazuje polje niza za unose vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="d4c86-225">Ovo polje ima dvije mogućnosti, **Prva mogućnost** i **Druga mogućnost** , koje su dostupne putem gumba mogućnosti (gumbi za odabir).</span><span class="sxs-lookup"><span data-stu-id="d4c86-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="d4c86-226">Polje u aplikaciji povezano je s poljem **TestLineString** koje se dodaje tablici TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="d4c86-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="d4c86-227">Obratite pažnju na uporabu načina **TSTimesheetCustomField::newFromMetatdata()** za pojednostavljivanje inicijalizacije svojstava prilagođenog polja: **fieldBaseType** , **tableName** , **fieldname** , **oznaka** , **isEditable** , **isMandatory** , **stringLength** i **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="d4c86-228">Te parametre možete postaviti i ručno, ako želite.</span><span class="sxs-lookup"><span data-stu-id="d4c86-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="d4c86-229">Uporaba lanca naredbi u načinu buildCustomFieldListForEntry klase TSTimesheetEntry za unos vrijednosti u unos evidencije radnog vremena</span><span class="sxs-lookup"><span data-stu-id="d4c86-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="d4c86-230">Način **buildCustomFieldListForEntry** upotrebljava se za unos vrijednosti u spremljene retke evidencije radnog vremena u mobilnoj aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="d4c86-231">Kao parametar uzima se zapis TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="d4c86-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="d4c86-232">Polja iz tog zapisa mogu se upotrebljavati za popunjavanje vrijednosti prilagođenog polja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="d4c86-233">Uporaba lanca naredbi u klasi TSTimesheetEntryService za spremanje unosa evidencije radnog vremena iz aplikacije natrag u bazu podataka</span><span class="sxs-lookup"><span data-stu-id="d4c86-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="d4c86-234">Kako biste spremili prilagođeno polje natrag u bazu podataka uobičajenom uporabom, morate proširiti više načina:</span><span class="sxs-lookup"><span data-stu-id="d4c86-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="d4c86-235">Način **timesheetLineNeedsUdddating** upotrebljava se za utvrđivanje je li korisnik promijenio zapis retka u aplikaciji i mora li se spremiti u bazu podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="d4c86-236">Ako izvedba nije zabrinjavajuća, ovaj način možete pojednostaviti tako da on uvijek vrati vrijednost **točno**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="d4c86-237">Načini **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** mogu se proširiti tako da unose vrijednosti u zapis baze podataka TSTimesheetLine iz danog zapisa ugovornih podataka TSTimesheetEntry.</span><span class="sxs-lookup"><span data-stu-id="d4c86-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="d4c86-238">U primjeru koji slijedi vidjet ćete kako se ručno vrši mapiranje između polja baze podataka i polja unosa putem X++ koda.</span><span class="sxs-lookup"><span data-stu-id="d4c86-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="d4c86-239">Način **populateTimesheetWeekFromEntry** također se može proširiti ako se prilagođeno polje mapira na objekt **TSTimesheetEntry** mora upisati natrag u tablicu baze podataka TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="d4c86-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="d4c86-240">U sljedećem primjeru, vrijednost **firstOption** ili **secondOption** koju korisnik odabire sprema se u bazu podataka kao sirova vrijednost niza.</span><span class="sxs-lookup"><span data-stu-id="d4c86-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="d4c86-241">Ako je polje baze podataka polje vrste **Nabrajanje** , te se vrijednosti mogu ručno preslikati na vrijednost nabrajanja, a zatim spremiti u polje nabrajanja u tablici baze podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="d4c86-242">Prikaz prilagođenog polja u odjeljku zaglavlja evidencije radnog vremena</span><span class="sxs-lookup"><span data-stu-id="d4c86-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="d4c86-243">U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj korisnik pregledava evidenciju radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="d4c86-244">U gornjem desnom kutu odabran je gumb „Više informacija” za prikazivanje mogućnosti „Prikaži više pojedinosti”.</span><span class="sxs-lookup"><span data-stu-id="d4c86-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Naredba prikaz više pojedinosti](media/show-more.png)

<span data-ttu-id="d4c86-246">U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj se prikazuje odjeljak „Više” evidencije radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="d4c86-247">Prilagođeno polje pod nazivom „Stopa iskorištavanja ove evidencije radnog vremena (izračunano prilagođeno polje)” dodano je u odjeljak zaglavlja evidencije radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="d4c86-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="d4c86-248">U prilagođenom polju postavljena je vrijednost samo za čitanje „0.667”.</span><span class="sxs-lookup"><span data-stu-id="d4c86-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Više odjeljaka](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="d4c86-250">Proširivanje tablice TSTimesheetTable tako da ima prilagođeno polje</span><span class="sxs-lookup"><span data-stu-id="d4c86-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="d4c86-251">U uobičajenim scenarijima vjerojatno će se podaci za prilagođeno polje u odjeljku zaglavlja povući iz tablice TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="d4c86-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="d4c86-252">Međutim, druge se tablice mogu upotrebljavati ako se podaci mogu dohvatiti na temelju dostavljenog zapisa TSTimesheetTable ili ako nema određenog konteksta zapisa (na primjer, ako je u parametrima projekta polje postavljeno kao samo za čitanje).</span><span class="sxs-lookup"><span data-stu-id="d4c86-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="d4c86-253">Imajte na umu da prilagođena polja ne moraju imati nikakve sigurnosne zapise baze podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="d4c86-254">Mogu se dinamički generirati na temelju X++ logike.</span><span class="sxs-lookup"><span data-stu-id="d4c86-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="d4c86-255">Primjer koji slijedi pokazuje ovaj pristup.</span><span class="sxs-lookup"><span data-stu-id="d4c86-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="d4c86-256">Polja u odjeljku zaglavlja u aplikaciji su uvijek samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="d4c86-257">Uporaba lanca naredbi u načinu buildCustomFieldList klase TSTimesheetSettings za prikaz polja u odjeljku zaglavlja</span><span class="sxs-lookup"><span data-stu-id="d4c86-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="d4c86-258">Ovaj kôd regulira postavke zaslona za polje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="d4c86-259">Na primjer, regulira vrstu polja, oznaku, je li polje obavezno i u kojem se odjeljku polje prikazuje.</span><span class="sxs-lookup"><span data-stu-id="d4c86-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="d4c86-260">Sljedeći primjer prikazuje izračunanu vrijednost u odjeljku zaglavlja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="d4c86-261">Uporaba lanca naredbi u načinu buildCustomFieldListForHeader klase TSTimesheetDetails za popunjavanje pojedinosti evidencije radnog vremena</span><span class="sxs-lookup"><span data-stu-id="d4c86-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="d4c86-262">Način **buildCustomFieldListForHeader** upotrebljava se za popunjavanje pojedinosti zaglavlja evidencije radnog vremena u mobilnoj aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="d4c86-263">Kao parametar uzima se zapis TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="d4c86-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="d4c86-264">Polja iz tog zapisa mogu se upotrebljavati za popunjavanje vrijednosti prilagođenog polja u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="d4c86-265">Sljedeći primjer ne čita nikakve vrijednosti iz baze podataka.</span><span class="sxs-lookup"><span data-stu-id="d4c86-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="d4c86-266">Umjesto toga, upotrebljava logiku X++ za generiranje izračunane vrijednosti koja se zatim prikazuje u aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="d4c86-267">Ostale mogućnosti konfiguracije/proširivosti</span><span class="sxs-lookup"><span data-stu-id="d4c86-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="d4c86-268">Dodavanje dodatne provjere valjanosti za aplikaciju</span><span class="sxs-lookup"><span data-stu-id="d4c86-268">Adding additional validation for the app</span></span>

<span data-ttu-id="d4c86-269">Postojeća logika funkcionalnosti evidencije radnog vremena na razini baze podataka i dalje će raditi kako se očekivalo.</span><span class="sxs-lookup"><span data-stu-id="d4c86-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="d4c86-270">Kako biste prekinuli dovršavanje operacija spremanja ili slanja i prikazali određenu poruku o pogrešci, možete kôdu dodati **odbaci pogrešku („poruka korisniku”)** putem proširenja lanca naredbe.</span><span class="sxs-lookup"><span data-stu-id="d4c86-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="d4c86-271">Evo tri primjera korisnih proširivih načina:</span><span class="sxs-lookup"><span data-stu-id="d4c86-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="d4c86-272">Ako **validateWrite** u tablici TSTimesheetLine vraća vrijednost **netočno** tijekom operacije spremanja retka evidencije radnog vremena, u mobilnoj se aplikaciji prikazuje poruka o pogrešci.</span><span class="sxs-lookup"><span data-stu-id="d4c86-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="d4c86-273">Ako **validateSubmit** u tablici TSTimesheetTable vraća vrijednost **netočno** tijekom operacije slanja retka evidencije radnog vremena u aplikaciju, korisniku se prikazuje poruka o pogrešci.</span><span class="sxs-lookup"><span data-stu-id="d4c86-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="d4c86-274">Logika koja popunjava polja (na primjer, **Svojstvo retka** ) tijekom načina **umetni** na tablici TSTimesheetLine i dalje će se izvršavati.</span><span class="sxs-lookup"><span data-stu-id="d4c86-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="d4c86-275">Sakrivanje i označavanje gotovih polja kao polja samo za čitanje putem konfiguracije</span><span class="sxs-lookup"><span data-stu-id="d4c86-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="d4c86-276">Iz parametara projekta možete napraviti gotova polja samo za čitanje ili skrivena u mobilnoj aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="d4c86-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="d4c86-277">Postavite mogućnosti u odjeljak **Mobilne evidencije radnog vremena** na kartici **Evidencija radnog vremena** na stranici **Parametri upravljanja projektom i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametri projekta](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="d4c86-279">Promjena aktivnosti dostupnih za odabir putem proširenja</span><span class="sxs-lookup"><span data-stu-id="d4c86-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="d4c86-280">Aktivnosti dostupne za odabir za projekt popunjavaju se putem načina **getActivitiesForProject()** i **getActivityQuery()** u klasi **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="d4c86-281">Možete koristiti lanac naredbi kako biste promijenili ovo ponašanje tako da pristaje vašem poslovnom scenariju za aktivnosti koje su dostupne za odabir za određeni projekt.</span><span class="sxs-lookup"><span data-stu-id="d4c86-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="d4c86-282">Unos zadane kategorije projekta u unose evidencije radnog vremena</span><span class="sxs-lookup"><span data-stu-id="d4c86-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="d4c86-283">Unos zadane kategorije projekta u unose evidencije radnog vremena događa se na tri razine.</span><span class="sxs-lookup"><span data-stu-id="d4c86-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="d4c86-284">Možete upotrebljavati lanac naredbi kako biste proširili ponašanje na bilo kojoj ili svim ovim razinama radi postizanja željenog ponašanja.</span><span class="sxs-lookup"><span data-stu-id="d4c86-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="d4c86-285">Upotrebljava se sljedeća hijerarhija:</span><span class="sxs-lookup"><span data-stu-id="d4c86-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="d4c86-286">Aplikacija pokušava staviti zadanu kategoriju iz resursa projekta.</span><span class="sxs-lookup"><span data-stu-id="d4c86-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="d4c86-287">Ova zadana kategorija postavljena je u načine **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** u klasu **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="d4c86-288">Ako zadana kategorija nije navedena na razini resursa projekta, aplikacija je pokušava povući iz aktivnosti projekta.</span><span class="sxs-lookup"><span data-stu-id="d4c86-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="d4c86-289">Ova zadana kategorija postavljena je u način **getActivitiesForProject** u klasu **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="d4c86-290">Ako zadana kategorija nije navedena na razini aktivnosti projekta, aplikacija je pokušava uzeti iz parametara projekta.</span><span class="sxs-lookup"><span data-stu-id="d4c86-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="d4c86-291">Ova zadana kategorija postavljena je u način **getProjectDetailsbyRule** u klasu **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="d4c86-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
