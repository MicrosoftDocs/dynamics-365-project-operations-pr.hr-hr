---
title: Stvaranje vremenskih unosa
description: Ova tema pruža informacije o tome kako izraditi vremenske unose.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999257"
---
# <a name="create-time-entries"></a><span data-ttu-id="374ae-103">Stvaranje vremenskih unosa</span><span class="sxs-lookup"><span data-stu-id="374ae-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="374ae-104">U ranijim verzijama programa Dynamics 365 Project Service Automation Unos vremenai su se unosili tjedno.</span><span class="sxs-lookup"><span data-stu-id="374ae-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="374ae-105">U verziji 3 programa Project Service Automation Unos vremenai se unose svakodnevno.</span><span class="sxs-lookup"><span data-stu-id="374ae-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="374ae-106">No, nakon izrade nekoliko unosa vremena možete ih skupno stvarati ili kopirati.</span><span class="sxs-lookup"><span data-stu-id="374ae-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="374ae-107">Stvaranje unosa vremena</span><span class="sxs-lookup"><span data-stu-id="374ae-107">Create a time entry</span></span>

<span data-ttu-id="374ae-108">Slijedite ove korake da biste stvorili Unos vremena.</span><span class="sxs-lookup"><span data-stu-id="374ae-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="374ae-109">Na stranici **Unos vremenai** odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="374ae-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="374ae-110">U dijaloškom okviru **Brzo stvaranje: Unos vremena** unesite trajanje unosa vremena u minutama, satima ili danima.</span><span class="sxs-lookup"><span data-stu-id="374ae-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="374ae-111">Trajanje se mora unijeti u sljedećem obliku: *x* minuta, *x* sati ili *x* dana.</span><span class="sxs-lookup"><span data-stu-id="374ae-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="374ae-112">Dani i sati mogu se unijeti i pomoću decimalnih vrijednosti, primjerice *x,x* sati ili *x,x* dana.</span><span class="sxs-lookup"><span data-stu-id="374ae-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="374ae-113">Odaberite vrstu unosa vremena i projekt za koji unosite Unos vremena.</span><span class="sxs-lookup"><span data-stu-id="374ae-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="374ae-114">U polju **Projektni zadatak** pronađite zadatak za ovaj Unos vremena.</span><span class="sxs-lookup"><span data-stu-id="374ae-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="374ae-115">Ako stvarate Unos vremena za zadatak koji nije dodijeljen korisniku, u polju **Projektni zadatak** odaberite gumb **Pretraži**, **Promijeni prikaz**, a zatim odaberite **Svi aktivni zadaci projekta** za prikaz popisa svih zadataka.</span><span class="sxs-lookup"><span data-stu-id="374ae-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="374ae-116">Unesite opis ako je potreban opis, a zatim odaberite **Spremi i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="374ae-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="374ae-117">Nakon stvaranja i spremanja unosa vremena možete ga urediti u rešetki vremenskih unosa.</span><span class="sxs-lookup"><span data-stu-id="374ae-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="374ae-118">Rešetka vremenskih unosa podržava dva formata:</span><span class="sxs-lookup"><span data-stu-id="374ae-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="374ae-119">U formatu **hh:mm** možete unositi vremenske unose.</span><span class="sxs-lookup"><span data-stu-id="374ae-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="374ae-120">Ovaj se format zatim pretvara u sate i razlomke sata.</span><span class="sxs-lookup"><span data-stu-id="374ae-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="374ae-121">Sate i razlomke sata možete unijeti izravno.</span><span class="sxs-lookup"><span data-stu-id="374ae-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="374ae-122">Imajte na umu da razlomci sata nisu minute.</span><span class="sxs-lookup"><span data-stu-id="374ae-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="374ae-123">Stoga, 1,5 sati predstavlja 1 sat i 30 minuta.</span><span class="sxs-lookup"><span data-stu-id="374ae-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="374ae-124">Isto se pravilo primjenjuje na razlomke dana.</span><span class="sxs-lookup"><span data-stu-id="374ae-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="374ae-125">Jedan dan je 24 sata, a 0,5 dana predstavlja 12 sati.</span><span class="sxs-lookup"><span data-stu-id="374ae-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="374ae-126">Skupno stvaranje vremenskih unosa</span><span class="sxs-lookup"><span data-stu-id="374ae-126">Bulk create time entries</span></span>

<span data-ttu-id="374ae-127">Nakon što ste stvorili nekoliko vremenskih unosa, možete ih kopirati da biste skupno stvorili dodatne vremenske unose.</span><span class="sxs-lookup"><span data-stu-id="374ae-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="374ae-128">Na stranici **Unos vremenai** odaberite **Kopiraj tjedan**.</span><span class="sxs-lookup"><span data-stu-id="374ae-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="374ae-129">U grupi polja **Razdoblje od** u poljima **Datum početka** i **Datum završetka** definirajte raspon datuma iz kojih ćete kopirati vremenske unose.</span><span class="sxs-lookup"><span data-stu-id="374ae-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="374ae-130">U grupi polja **Razdoblje do** u polju **Datum početka** navedite datum za koji stvarate vremenske unose.</span><span class="sxs-lookup"><span data-stu-id="374ae-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="374ae-131">Odaberite **Kopiraj** da biste stvorili kopiju vremenskih unosa koji odgovaraju danu u tjednu navedenom u grupi polja **Razdoblje do**.</span><span class="sxs-lookup"><span data-stu-id="374ae-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="374ae-132">Na primjer, Unos vremena za ponedjeljak od prošlog tjedna kopira se u ponedjeljak u tjednu koji je naveden u grupi polja **Razdoblje do**.</span><span class="sxs-lookup"><span data-stu-id="374ae-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="374ae-133">Uvoz podataka za vremenske unose</span><span class="sxs-lookup"><span data-stu-id="374ae-133">Import data for time entries</span></span>

<span data-ttu-id="374ae-134">Možete uvesti podatke iz rezervacija i dodjela projekta.</span><span class="sxs-lookup"><span data-stu-id="374ae-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="374ae-135">Kada uvezete podatke, možete navesti raspon datuma rezervacija koje želite uvesti, a zatim posebno odabrati rezervacije koje treba izraditi kao vremenske unose **Skica**.</span><span class="sxs-lookup"><span data-stu-id="374ae-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="374ae-136">Mogućnosti grupiranja, sortiranja, pretraživanja i filtriranja</span><span class="sxs-lookup"><span data-stu-id="374ae-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="374ae-137">Vremenske unose možete grupirati i filtrirati po dimenzijama koje su navedene u stupcima.</span><span class="sxs-lookup"><span data-stu-id="374ae-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="374ae-138">U polju **Grupiraj po** odaberite dimenziju koju želite upotrijebiti za filtriranje vremenskih unosa.</span><span class="sxs-lookup"><span data-stu-id="374ae-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="374ae-139">Isto tako, zapise vremenskih unosa možete sortirati uzlaznim ili silazni redoslijedom pomoću strelice za sortiranje u naslovima stupaca.</span><span class="sxs-lookup"><span data-stu-id="374ae-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="374ae-140">Osim toga, unose možete prikazati ili sakriti tako da odaberete gumb **Filtriraj** u naslovima stupaca, a zatim u okviru **Pretraživanje** unesete tekst koji treba koristiti za pretraživanje vremenskih unosa po nazivu projekta, projektnom zadatku, vremenskom unosu ili resursu.</span><span class="sxs-lookup"><span data-stu-id="374ae-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]