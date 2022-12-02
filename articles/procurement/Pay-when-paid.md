---
title: Plaćanja dobavljača po načelu „plati kad bude plaćeno”
description: U ovoj temi je objašnjeno kako koristiti scenarij "plati kad bude plaćeno" (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525380"
---
# <a name="pay-when-paid-vendor-payments"></a>Plaćanja dobavljača po načelu „plati kad bude plaćeno”

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi je objašnjeno kako koristiti scenarij "plati kad bude plaćeno" (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Stvaranje narudžbenice koja ima uvjete PWP-a

Kada knjižite fakturu dobavljača, ako dobavljač podliježe uvjetima PWP-a, ti se uvjeti prikazuju na redcima narudžbenice. Slijedite ove korake za stvaranje narudžbenice koja sadrži uvjete PWP-a.

1. U sustavu Microsoft Dynamics 365 Finance slijedite jedan od ovih koraka:

    - Idite na **Nabava i dobavljanje** \> **Narudžbenice** \> **Sve narudžbenice**. U Oknu radnji odaberite **Novo**. U dijaloškom okviru **Stvaranje narudžbenice** odaberite dobavljača za kojeg su na projektu postavljeni PWP uvjeti, unesite druge potrebne podatke, a zatim odaberite **U redu**.
    - Idite na mogućnost **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**. U Oknu akcije, na kartici **Upravljanje**, odaberite **Zadatak stavke**. Odaberite narudžbenicu. Odaberite dobavljača za kojeg su na projektu postavljeni PWP uvjeti, a zatim odaberite **U redu**.

2. Na stranici **Narudžbenica**, na brzoj kartici **Redci narudžbenice**, odaberite **Dodaj redak** za stvaranje retka narudžbenice.
3. Odaberite broj stavke ili kategoriju nabave i unesite ostale potrebne podatke. Pregledajte pojedinosti retka narudžbenice za dobavljača.

    Mogućnost **Plati kad bude plaćeno** automatski se odabire, a vrijednost u polju **Postotak praga PWP-a** automatski se kopira iz polja **Postotak praga PWP-a** na stranicu **Projekti**.

4. Ako ne želite primijeniti uvjete PWP-a na dobavljača za redak narudžbe, očistite mogućnost **Plati kad bude plaćeno**. U ovom slučaju, polje **Postotak praga PWP-a** za redak narudžbenice vratit će se na **0** (nula).
5. Na stranici **Narudžbenica**, u Oknu akcije, na kartici **Kupnja**, odaberite **Potvrda** za potvrdu narudžbenice.
6. U Oknu akcije, na kartici **Faktura**, odaberite **Faktura** za stvaranje fakture za narudžbenicu.

## <a name="create-a-project-invoice-proposal"></a>Stvaranje prijedloga fakture za projekt

Prijedlozi projektnih faktura koriste se za izradu projektnih faktura za klijenta. U scenariju PWP, plaćanja dobavljača ovise o plaćanjima klijenta prema postavkama PWP-a. Međutim, postoje opcije koje vam omogućuju puštanje uplate bez plaćanja klijenta prema potrebi. Da biste izradili projektnu fakturu za klijenta, slijedite ove korake.

1. U aplikacijama za angažman klijenata idite na **Projekt** \> **Projekti** i odaberite projekt.
2. Na kartici **Stvarni podaci** odaberite redak stvarnih podataka koji generira narudžbenica koja ima vrstu transakcije **Nenaplaćena prodaja**. Zatim odaberite **Spremno za fakturu**.
3. Idite na **Prodaja** \> **Prodaja** \> **Projektni ugovor** i odaberite projektni ugovor.
4. U Oknu akcije odaberite **Faktura** za izradu fakture za klijenta.
5. U aplikaciji Finance idite na **Upravljanje projektima i računovodstvo** \> **Povremeno** \> **Uvoz iz pripremne tablice** pa odaberite **U redu** za izradu dnevnika integracije za Project Operations.
6. Idite na **Upravljanje projektima i računovodstvo** \> **Projektne fakture** \> **Prijedlog projektne fakture** i odaberite **Knjiži** za knjiženje prijedloga fakture koji je generiran za projekt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ažuriranje uplate klijenta i plaćanje dobavljaču

Kada dobavljač dovrši svoj posao na projektu i pošalje vam fakturu, morate pregledati status projekta i fakture klijenta kako biste utvrdili jesu li za projekt ispunjeni uvjeti PWP-a. Ako su ispunjeni uvjeti PWP-a za dobavljača, možete odrediti koje ćete retke na fakturi dobavljača platiti na temelju uplate klijenta za projekt. Ako odlučite platiti dobavljaču iako uvjeti PWP-a nisu ispunjeni, možete poništiti uvjete PWP-a na stranici **Račun dobavljača s načelom „plati kad bude plaćeno”**.

1. U aplikaciji Finance idite na **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti** i odaberite projekt.
2. U Oknu akcije odaberite **Kontrola**, a zatim odaberite **Fakture dobavljača** za prikaz svih faktura dobavljača koje su generirane za projekt.
3. U polje za pretraživanje na stranici **Račun dobavljača s načelom „plati kad bude plaćeno”**, unesite vrijednosti kako biste pronašli fakturu dobavljača koju želite pregledati, a zatim odaberite **Traži**.
4. Odaberite mogućnost **Plati kad bude plaćeno** za pregled samo PWP faktura.
5. Na Brzoj kartici **Redci fakture dobavljača** odaberite retke koje želite pustiti na naplatu.
6. Odaberite **Pusti uplatu dobavljaču**. Mogućnost **Plati kad bude plaćeno** je obrisana, a vrijednost polja **Spremno za plaćanje** mijenja se u **Da**.
