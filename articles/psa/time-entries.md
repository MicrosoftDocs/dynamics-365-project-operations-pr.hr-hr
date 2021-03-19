---
title: Stvaranje vremenskih unosa
description: Ova tema pruža informacije o tome kako izraditi vremenske unose.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 8f86f69090e869bf5e6a7505a4cb1ad1c69b475b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282144"
---
# <a name="create-time-entries"></a>Stvaranje vremenskih unosa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U ranijim verzijama programa Dynamics 365 Project Service Automation Unos vremenai su se unosili tjedno. U verziji 3 programa Project Service Automation Unos vremenai se unose svakodnevno. No, nakon izrade nekoliko unosa vremena možete ih skupno stvarati ili kopirati.

## <a name="create-a-time-entry"></a>Stvaranje unosa vremena

Slijedite ove korake da biste stvorili Unos vremena.

1. Na stranici **Unos vremenai** odaberite **Novo**.
2. U dijaloškom okviru **Brzo stvaranje: Unos vremena** unesite trajanje unosa vremena u minutama, satima ili danima. Trajanje se mora unijeti u sljedećem obliku: *x* minuta, *x* sati ili *x* dana. Dani i sati mogu se unijeti i pomoću decimalnih vrijednosti, primjerice *x,x* sati ili *x,x* dana.
3. Odaberite vrstu unosa vremena i projekt za koji unosite Unos vremena.
4. U polju **Projektni zadatak** pronađite zadatak za ovaj Unos vremena.

    > [!NOTE]
    > Ako stvarate Unos vremena za zadatak koji nije dodijeljen korisniku, u polju **Projektni zadatak** odaberite gumb **Pretraži**, **Promijeni prikaz**, a zatim odaberite **Svi aktivni zadaci projekta** za prikaz popisa svih zadataka.

5. Unesite opis ako je potreban opis, a zatim odaberite **Spremi i zatvori**.

Nakon stvaranja i spremanja unosa vremena možete ga urediti u rešetki vremenskih unosa. Rešetka vremenskih unosa podržava dva formata:

- U formatu **hh:mm** možete unositi vremenske unose. Ovaj se format zatim pretvara u sate i razlomke sata.
- Sate i razlomke sata možete unijeti izravno.

Imajte na umu da razlomci sata nisu minute. Stoga, 1,5 sati predstavlja 1 sat i 30 minuta. Isto se pravilo primjenjuje na razlomke dana. Jedan dan je 24 sata, a 0,5 dana predstavlja 12 sati.

## <a name="bulk-create-time-entries"></a>Skupno stvaranje vremenskih unosa

Nakon što ste stvorili nekoliko vremenskih unosa, možete ih kopirati da biste skupno stvorili dodatne vremenske unose.

1. Na stranici **Unos vremenai** odaberite **Kopiraj tjedan**.
2. U grupi polja **Razdoblje od** u poljima **Datum početka** i **Datum završetka** definirajte raspon datuma iz kojih ćete kopirati vremenske unose.
3. U grupi polja **Razdoblje do** u polju **Datum početka** navedite datum za koji stvarate vremenske unose.
4. Odaberite **Kopiraj** da biste stvorili kopiju vremenskih unosa koji odgovaraju danu u tjednu navedenom u grupi polja **Razdoblje do**. Na primjer, Unos vremena za ponedjeljak od prošlog tjedna kopira se u ponedjeljak u tjednu koji je naveden u grupi polja **Razdoblje do**.

## <a name="import-data-for-time-entries"></a>Uvoz podataka za vremenske unose

Možete uvesti podatke iz rezervacija i dodjela projekta. Kada uvezete podatke, možete navesti raspon datuma rezervacija koje želite uvesti, a zatim posebno odabrati rezervacije koje treba izraditi kao vremenske unose **Skica**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Mogućnosti grupiranja, sortiranja, pretraživanja i filtriranja

Vremenske unose možete grupirati i filtrirati po dimenzijama koje su navedene u stupcima. U polju **Grupiraj po** odaberite dimenziju koju želite upotrijebiti za filtriranje vremenskih unosa. Isto tako, zapise vremenskih unosa možete sortirati uzlaznim ili silazni redoslijedom pomoću strelice za sortiranje u naslovima stupaca. Osim toga, unose možete prikazati ili sakriti tako da odaberete gumb **Filtriraj** u naslovima stupaca, a zatim u okviru **Pretraživanje** unesete tekst koji treba koristiti za pretraživanje vremenskih unosa po nazivu projekta, projektnom zadatku, vremenskom unosu ili resursu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]