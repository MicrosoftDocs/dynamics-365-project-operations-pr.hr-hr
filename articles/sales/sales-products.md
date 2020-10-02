---
title: Proizvodi
description: U ovoj se temi nalaze informacije o katalogu proizvoda s pomoću kojeg kupcima pružate informacije o proizvodima i cijenama koje nudi vaša tvrtka ili ustanova.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898702"
---
# <a name="products"></a><span data-ttu-id="b3649-103">Proizvodi</span><span class="sxs-lookup"><span data-stu-id="b3649-103">Products</span></span>

<span data-ttu-id="b3649-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b3649-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b3649-105">Proizvodi su temelj vašeg poslovanja.</span><span class="sxs-lookup"><span data-stu-id="b3649-105">Products are the backbone of your business.</span></span> <span data-ttu-id="b3649-106">Katalog proizvoda u aplikaciji Dynamics 365 Sales Professional zbirka je proizvoda i informacija o cijenama.</span><span class="sxs-lookup"><span data-stu-id="b3649-106">The product catalog in Dynamics 365 Sales Professional is a collection of products and pricing information.</span></span> <span data-ttu-id="b3649-107">Brzo stvorite katalog proizvoda i olakšajte svojim prodajnim predstavnicima povećanje prodaje.</span><span class="sxs-lookup"><span data-stu-id="b3649-107">Make it easier for your sales reps to increase their sales by creating a product catalog quickly.</span></span>

## <a name="add-a-product"></a><span data-ttu-id="b3649-108">Dodavanje proizvoda</span><span class="sxs-lookup"><span data-stu-id="b3649-108">Add a product</span></span>

1.  <span data-ttu-id="b3649-109">Provjerite imate li ulogu stručnog voditelja prodaje ili administratora sustava kako biste dodali proizvode u aplikaciju Dynamics 365 Sales Professional.</span><span class="sxs-lookup"><span data-stu-id="b3649-109">Make sure you have the Sales Manager Professional or a System Administrator role so you can add products in Dynamics 365 Sales Professional.</span></span>
2.  <span data-ttu-id="b3649-110">U karti web-mjesta, pod stavkom **Postavljanje**, odaberite mogućnost **Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-110">In the site map, under **Setup**, select **Products**.</span></span>
3.  <span data-ttu-id="b3649-111">Odaberite **Dodaj proizvod** i popunite sljedeće podatke:</span><span class="sxs-lookup"><span data-stu-id="b3649-111">Select **Add Product** and fill in the following information:</span></span>

    -  <span data-ttu-id="b3649-112">**Ime**</span><span class="sxs-lookup"><span data-stu-id="b3649-112">**Name**</span></span>
    -  <span data-ttu-id="b3649-113">**ID proizvoda**</span><span class="sxs-lookup"><span data-stu-id="b3649-113">**Product ID**</span></span>
    -  <span data-ttu-id="b3649-114">**Nadređen**: Odaberite nadređenu skupinu proizvoda za proizvod.</span><span class="sxs-lookup"><span data-stu-id="b3649-114">**Parent**: Select a parent product family for the product.</span></span> <span data-ttu-id="b3649-115">Ako stvarate podređeni proizvod u skupini proizvoda, ovdje se unosi naziv skupine nadređenih proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b3649-115">If you're creating a child product in a product family, the name of the parent product family is populated here.</span></span> <span data-ttu-id="b3649-116">To se ne može promijeniti nakon što se zapis spremi.</span><span class="sxs-lookup"><span data-stu-id="b3649-116">This can't be changed after the record is saved.</span></span>
    -  <span data-ttu-id="b3649-117">**Valjan od**/**Valjan do**: Definirajte razdoblje tijekom kojeg je proizvod valjan tako da odaberete datum **Valjan od** i **Valjan do**.</span><span class="sxs-lookup"><span data-stu-id="b3649-117">**Valid From**/**Valid To**: Define the period the product is valid for by selecting a **Valid From** and **Valid To** date.</span></span>
    -  <span data-ttu-id="b3649-118">**Grupa jedinica**: odaberite grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="b3649-118">**Unit Group**: Select a unit group.</span></span> <span data-ttu-id="b3649-119">Grupa jedinica je skup različitih jedinica u kojima se prodaje proizvod i definira kako se pojedinačne stavke grupiraju u veće količine.</span><span class="sxs-lookup"><span data-stu-id="b3649-119">A unit group is a collection of various units a product is sold in and defines how individual items are grouped into larger quantities.</span></span> <span data-ttu-id="b3649-120">Na primjer, ako kao proizvod dodajete sjemenke, možda ste stvorili grupu jedinica pod nazivom „Sjemenke” i definirali njenu primarnu jedinicu kao „paket”.</span><span class="sxs-lookup"><span data-stu-id="b3649-120">For example, if you're adding seeds as a product, you might have created a unit group called "Seeds" and defined its primary unit as "packet."</span></span>
    -  <span data-ttu-id="b3649-121">**Zadana jedinica**: Odabir najčešće jedinice u kojoj će se proizvod prodavati.</span><span class="sxs-lookup"><span data-stu-id="b3649-121">**Default Unit**: Select the most common unit in which the product will be sold.</span></span> <span data-ttu-id="b3649-122">Jedinice su količine ili mjerne jedinice u kojima prodajete proizvode.</span><span class="sxs-lookup"><span data-stu-id="b3649-122">Units are the quantities or measurements that you sell your products in.</span></span> <span data-ttu-id="b3649-123">Na primjer, ako ste dodali sjemenke kao proizvod, možete ih prodavati u paketima, kutijama ili paletama.</span><span class="sxs-lookup"><span data-stu-id="b3649-123">For example, if you're adding seeds as a product, you can sell it in packets, boxes, or pallets.</span></span> <span data-ttu-id="b3649-124">Svaka od njih postaje jedinica proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b3649-124">Each of these becomes a unit of the product.</span></span> <span data-ttu-id="b3649-125">Ako se sjemenke većinom prodaju u paketima, odaberite to kao jedinicu.</span><span class="sxs-lookup"><span data-stu-id="b3649-125">If seeds are mostly sold in packets, select that as the unit.</span></span>
    -  <span data-ttu-id="b3649-126">**Zadani cjenik**: Ako je riječ o novom proizvodu, to je polje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="b3649-126">**Default Price List**: If this is a new product, this field is read-only.</span></span> <span data-ttu-id="b3649-127">Kako biste mogli odabrati zadani cjenik, morate ispuniti sva obavezna polja, a zatim spremiti zapis.</span><span class="sxs-lookup"><span data-stu-id="b3649-127">Before you can select a default price list, you must complete all the required fields and then save the record.</span></span> <span data-ttu-id="b3649-128">Iako zadani cjenik nije obavezan, nakon spremanja zapisa proizvoda dobro je postaviti zadani cjenik za svaki proizvod.</span><span class="sxs-lookup"><span data-stu-id="b3649-128">Although the default price list is not required, after you save the product record, it is a good idea to set a default price list for each product.</span></span> <span data-ttu-id="b3649-129">U tom slučaju, ako zapis klijenta ne sadrži cjenik, aplikacija Sales može koristiti zadani cjenik za generiranje ponuda, narudžbi i faktura.</span><span class="sxs-lookup"><span data-stu-id="b3649-129">Then, if a customer record does not contain a price list, Sales can use the default price list for generating quotes, orders, and invoices.</span></span>
    -  <span data-ttu-id="b3649-130">**Podržani decimalni brojevi**: Morate unijeti cijeli broj između 0 i 5.</span><span class="sxs-lookup"><span data-stu-id="b3649-130">**Decimals Supported**: Enter a whole number between 0 and 5.</span></span> <span data-ttu-id="b3649-131">Ako se proizvod ne može podijeliti na dijelove, unesite 0.</span><span class="sxs-lookup"><span data-stu-id="b3649-131">If the product can't be divided into fractional quantities, enter 0.</span></span> <span data-ttu-id="b3649-132">Ako proizvodu nije pridružen cjenik, točnost polja **Količina** u zapisu ponude, narudžbe ili proizvoda na fakturi provjerava se u odnosu na vrijednost u ovom polju.</span><span class="sxs-lookup"><span data-stu-id="b3649-132">The precision of the **Quantity** field in the quote, order, or invoice product record is validated against the value in this field if the product does not have an associated price list.</span></span>
    -  <span data-ttu-id="b3649-133">**Predmet**: Taj proizvod možete povezati s predmetom.</span><span class="sxs-lookup"><span data-stu-id="b3649-133">**Subject**: Associate this product with a subject.</span></span> <span data-ttu-id="b3649-134">Pomoću predmeta možete kategorizirati proizvode i filtrirati izvješća.</span><span class="sxs-lookup"><span data-stu-id="b3649-134">You can use subjects to categorize your products and to filter reports.</span></span>

4.  <span data-ttu-id="b3649-135">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-135">Select **Save**.</span></span>
5.  <span data-ttu-id="b3649-136">Na kartici **Dodatne pojedinosti**, u odjeljku **Stavke cjenika**, odaberite **Dodatne naredbe** i zatim odaberite mogućnost **Dodaj nove stavke cjenika**.</span><span class="sxs-lookup"><span data-stu-id="b3649-136">On the **Additional Details** tab, in the **Price List Items** section, select **More commands**, and then select **Add New Price List Item**.</span></span>
7.  <span data-ttu-id="b3649-137">Na kartici **Dodatne pojedinosti**, u odjeljku **Odnos proizvoda**, odaberite ikonu **Dodatne naredbe** i zatim odaberite mogućnost **Dodaj novi odnos proizvoda**.</span><span class="sxs-lookup"><span data-stu-id="b3649-137">On the **Additional Details** tab, in the **Product Relationship** section, select the **More commands** icon, and then select **Add New Product Relationship.**</span></span>
8.  <span data-ttu-id="b3649-138">U obrascu **Novi odnos proizvoda** unesite sljedeće pojedinosti, a na naredbenoj traci odaberite mogućnost **Spremi i zatvori**:</span><span class="sxs-lookup"><span data-stu-id="b3649-138">In the **New Product Relationship** form, enter the following details, and on the command bar, select **Save and Close**:</span></span>

    -   <span data-ttu-id="b3649-139">**Povezani proizvodi**: Odaberite proizvod koji želite dodati kao povezani proizvod u postojeći zapis o proizvodu na kojem radite.</span><span class="sxs-lookup"><span data-stu-id="b3649-139">**Related Product**: Select a product that you want to add as a related product to the existing product record you're working on.</span></span>
    -   <span data-ttu-id="b3649-140">**Vrsta prodajnog odnosa**: Odaberite želite li dodati proizvod kao napredniji proizvod, povezani proizvod, dodatak ili zamjenski proizvod.</span><span class="sxs-lookup"><span data-stu-id="b3649-140">**Sales Relation Type**: Select whether you want to add the product as an up-sell, cross-sell, accessory, or substitute product.</span></span>
    -   <span data-ttu-id="b3649-141">**Smjer**: Odaberite hoće li odnos između proizvoda biti jednosmjeran ili dvosmjeran.</span><span class="sxs-lookup"><span data-stu-id="b3649-141">**Direction**:Select whether the relationship between the products will be unidirectional or bidirectional.</span></span> <span data-ttu-id="b3649-142">Ako odaberete jednosmjeran, proizvod koji ste odabrali u stavci **Povezan proizvod** prikazat će se kao preporuka za postojeći proizvod, ali ne i obrnuto.</span><span class="sxs-lookup"><span data-stu-id="b3649-142">When you select unidirectional, the product that you select in **Related Product** will be shown as a recommendation for the existing product but not vice versa.</span></span>

9.  <span data-ttu-id="b3649-143">Na obrascu proizvoda odaberite mogućnost **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-143">On the Product form, select **Save**.</span></span>

## <a name="import-products"></a><span data-ttu-id="b3649-144">Uvoz proizvoda</span><span class="sxs-lookup"><span data-stu-id="b3649-144">Import products</span></span>

<span data-ttu-id="b3649-145">Možete upotrijebiti predloške za uvoz kako biste u aplikaciju Dynamics 365 Sales unijeli skupne podatke o proizvodu.</span><span class="sxs-lookup"><span data-stu-id="b3649-145">You can use import templates to bring bulk product data into Dynamics 365 Sales.</span></span>

## <a name="revise-a-product"></a><span data-ttu-id="b3649-146">Revizija proizvoda</span><span class="sxs-lookup"><span data-stu-id="b3649-146">Revise a product</span></span>

<span data-ttu-id="b3649-147">Redovito ažurirajte zalihe proizvoda tako da, prema potrebi, brzo revidirate svojstva proizvoda i ponovno objavite informacije kako bi vaši prodajni predstavnici mogli vidjeti najnovije promjene zaliha.</span><span class="sxs-lookup"><span data-stu-id="b3649-147">Keep the product inventory updated by quickly revising properties for the products, as required, and republishing the information so that your sales agents can see the latest changes to the inventory.</span></span>

1.  <span data-ttu-id="b3649-148">Provjerite imate li jednu od sljedećih sigurnosnih uloga ili ekvivalentnih dozvola: administrator sustava, osoba za prilagodbu sustava, upravitelj prodaje, potpredsjednik za prodaju, potpredsjednik za marketing, generalni ili poslovni direktor.</span><span class="sxs-lookup"><span data-stu-id="b3649-148">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="b3649-149">U karti web-mjesta odaberite opciju **Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-149">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b3649-150">Otvorite aktivni proizvod koji želite promijeniti i na naredbenoj traci odaberite mogućnost **Revizija**.</span><span class="sxs-lookup"><span data-stu-id="b3649-150">Open an active product that you want to change, and on the command bar, select **Revise**.</span></span>
4.  <span data-ttu-id="b3649-151">U dijaloškom okviru **Potvrda revizija** odaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-151">In the **Confirm Revise** dialog box, select **Confirm**.</span></span> <span data-ttu-id="b3649-152">To će promijeniti stanje proizvoda u **U reviziji**.</span><span class="sxs-lookup"><span data-stu-id="b3649-152">This will change the product status to **Under Revision**.</span></span>
5.  <span data-ttu-id="b3649-153">Nakon što završite s izmjenama, u naredbenoj traci odaberite mogućnost **Objavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="b3649-153">After you're done making changes, on the command bar, select **Publish**.</span></span>

    > [!TIP]
    > <span data-ttu-id="b3649-154">Kako biste vratili promjene i nastavili s posljednjom aktivnom verzijom proizvoda, odaberite mogućnost **Vraćanje**.</span><span class="sxs-lookup"><span data-stu-id="b3649-154">To revert the changes and continue with the last active version of the product, select **Revert**.</span></span> <span data-ttu-id="b3649-155">To mijenja stanje proizvoda natrag na **Aktivno**.</span><span class="sxs-lookup"><span data-stu-id="b3649-155">This changes the status of the product back to **Active**.</span></span>

## <a name="clone-a-product"></a><span data-ttu-id="b3649-156">Kloniranje proizvoda</span><span class="sxs-lookup"><span data-stu-id="b3649-156">Clone a product</span></span> 

<span data-ttu-id="b3649-157">Kada stvarate novi proizvod, uštedite vrijeme kloniranjem postojećeg.</span><span class="sxs-lookup"><span data-stu-id="b3649-157">When you're creating a new product, save time by cloning an existing one.</span></span> <span data-ttu-id="b3649-158">Tako se stvara kopija izvornog zapisa sa svim detaljima osim naziva i ID-a.</span><span class="sxs-lookup"><span data-stu-id="b3649-158">This creates a copy of the original record with all the details except for the name and ID.</span></span>

1.  <span data-ttu-id="b3649-159">Provjerite imate li jednu od sljedećih sigurnosnih uloga ili ekvivalentnih dozvola: administrator sustava, osoba za prilagodbu sustava, upravitelj prodaje, potpredsjednik za prodaju, potpredsjednik za marketing, generalni ili poslovni direktor.</span><span class="sxs-lookup"><span data-stu-id="b3649-159">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="b3649-160">U karti web-mjesta odaberite opciju **Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-160">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b3649-161">Odaberite zapis proizvoda koji želite klonirati i na naredbenoj traci odaberite **Kloniranje**.</span><span class="sxs-lookup"><span data-stu-id="b3649-161">Select a product record that you want to clone, and on the command bar, select **Clone**.</span></span> <span data-ttu-id="b3649-162">Prikazat će se dijaloški okvir za potvrdu.</span><span class="sxs-lookup"><span data-stu-id="b3649-162">A confirmation dialog box appears.</span></span>
4.  <span data-ttu-id="b3649-163">Odaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-163">Select **Confirm**.</span></span>

<span data-ttu-id="b3649-164">Novi zapis o proizvodu otvara se s istim pojedinostima kao što su u izvorniku, osim naziva i ID-a.</span><span class="sxs-lookup"><span data-stu-id="b3649-164">A new product record opens with the same details as the original one except for the name and ID.</span></span>

## <a name="retire-a-product"></a><span data-ttu-id="b3649-165">Opoziv proizvoda</span><span class="sxs-lookup"><span data-stu-id="b3649-165">Retire a product</span></span> 

<span data-ttu-id="b3649-166">Ako vaša tvrtka ili ustanova više ne prodaje proizvod, opozovite ga tako da više nije dostupan vašim prodajnim predstavnicima.</span><span class="sxs-lookup"><span data-stu-id="b3649-166">If your organization doesn't sell a product anymore, retire it so that the product is no longer available to your sales agents.</span></span>

1.  <span data-ttu-id="b3649-167">Provjerite imate li sigurnosnu ulogu administratora sustava ili voditelja Sales Professional ili jednakovrijedne dozvole.</span><span class="sxs-lookup"><span data-stu-id="b3649-167">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="b3649-168">U karti web-mjesta odaberite opciju **Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-168">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b3649-169">Otvorite aktivni proizvod koji želite opozvati i na naredbenoj traci odaberite mogućnost **Opoziv**.</span><span class="sxs-lookup"><span data-stu-id="b3649-169">Open an active product that you want to retire, and on the command bar, select **Retire**.</span></span>
4.  <span data-ttu-id="b3649-170">U dijaloškom okviru **Potvrda opoziva** odaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-170">In the **Confirm Retire** dialog box, select **Confirm**.</span></span>


## <a name="delete-a-product"></a><span data-ttu-id="b3649-171">Brisanje proizvoda</span><span class="sxs-lookup"><span data-stu-id="b3649-171">Delete a product</span></span>

<span data-ttu-id="b3649-172">Da biste zaustavili prodaju proizvoda, izbrišite je.</span><span class="sxs-lookup"><span data-stu-id="b3649-172">To stop selling a product, delete it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3649-173">Ne možete vratiti izbrisane zapise.</span><span class="sxs-lookup"><span data-stu-id="b3649-173">You can't recover a deleted record.</span></span>

1.  <span data-ttu-id="b3649-174">Provjerite imate li sigurnosnu ulogu administratora sustava ili voditelja Sales Professional ili jednakovrijedne dozvole.</span><span class="sxs-lookup"><span data-stu-id="b3649-174">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="b3649-175">U karti web-mjesta odaberite opciju **Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-175">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="b3649-176">Odaberite zapis proizvoda koji želite izbrisati i na naredbenoj traci odaberite mogućnost **Brisanje**.</span><span class="sxs-lookup"><span data-stu-id="b3649-176">Select a product record you want to delete, and on the command bar, select **Delete**.</span></span>
4.  <span data-ttu-id="b3649-177">U dijaloškom okviru **Potvrdi brisanje** odaberite mogućnost **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="b3649-177">In the **Confirm Deletion** dialog box, select **Continue**.</span></span>
 
 ## <a name="quantity-factors-for-products"></a><span data-ttu-id="b3649-178">Čimbenici količine za proizvode</span><span class="sxs-lookup"><span data-stu-id="b3649-178">Quantity factors for products</span></span>

<span data-ttu-id="b3649-179">Čimbenici količine podržavaju prodaju proizvoda temeljenih na pretplati.</span><span class="sxs-lookup"><span data-stu-id="b3649-179">Quantity factors support the sale of subscription-based products.</span></span> <span data-ttu-id="b3649-180">Za proizvode temeljene na pretplati količina u retku ponude ili ugovora o projektu izražena je kao broj korisničkih mjeseci.</span><span class="sxs-lookup"><span data-stu-id="b3649-180">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="b3649-181">Cijena softvera za pretplatu obično se pohranjuje u katalog kao mjesečna cijena po korisniku.</span><span class="sxs-lookup"><span data-stu-id="b3649-181">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="b3649-182">Međutim, umjesto toga možete koristiti druge vremenske opise.</span><span class="sxs-lookup"><span data-stu-id="b3649-182">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="b3649-183">Tijekom prodajnog postupka cijena u retku ponude obično je dogovorena mjesečna cijena cijena po korisniku uz popust IT prodajnog predstavnika.</span><span class="sxs-lookup"><span data-stu-id="b3649-183">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="b3649-184">Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="b3649-184">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="b3649-185">Količina koja se koristi za izračun iznosa retka ponude proizvod je broja korisnika i broja mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="b3649-185">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="b3649-186">Čimbenici količine oslanjaju se na atribute proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b3649-186">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="b3649-187">Kada konfigurirate određena svojstva za proizvod, možete označiti podskup tih svojstava ili svih svojstava kao čimbenika količine.</span><span class="sxs-lookup"><span data-stu-id="b3649-187">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="b3649-188">Sustav provjerava valjanost jesu li samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine.</span><span class="sxs-lookup"><span data-stu-id="b3649-188">The system validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="b3649-189">Kada se proizvod za koji su konfigurirani čimbenici količine doda u redak ponude, polje **Količina** u retku ponude postaje polje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="b3649-189">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="b3649-190">Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, izračunava se količina retka ponude.</span><span class="sxs-lookup"><span data-stu-id="b3649-190">After you enter values for product properties that are quantity factors, the quantity of the quote line is calculated.</span></span>

<span data-ttu-id="b3649-191">Na primjer, ako postoje sljedeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="b3649-191">For example, if there are the following properties:</span></span> 

- <span data-ttu-id="b3649-192">**Broj korisnika**: broj korisnika</span><span class="sxs-lookup"><span data-stu-id="b3649-192">**No of users**: The number of users</span></span> 
- <span data-ttu-id="b3649-193">**Broj mjeseci**: broj mjeseci pretplate</span><span class="sxs-lookup"><span data-stu-id="b3649-193">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="b3649-194">**SKU proizvoda**</span><span class="sxs-lookup"><span data-stu-id="b3649-194">**Product SKU**</span></span> 

<span data-ttu-id="b3649-195">Svojstva **Broj korisnika** i **Broj mjeseci** mogu se označiti kao čimbenici količine uređivanjem svojstava retka proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b3649-195">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 