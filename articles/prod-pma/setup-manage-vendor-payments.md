---
title: Postavljanje i uporaba plaćanja dobavljača po načelu „plati kad bude plaćeno”
description: U ovoj temi objašnjava se način stvaranja uvjeta plaćanja „plati kad bude plaćeno” (PWP, pay-when-paid) tako da dobavljaču možete djelomična pustiti plaćanje na temelju uplate klijenta.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073367"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Postavljanje i uporaba plaćanja dobavljača po načelu „plati kad bude plaćeno”

[!include [banner](../includes/banner.md)]

Kada odobrite dobavljaču da radi kao podizvođač, možda ćete htjeti zadržati plaćanje dobavljaču sve dok vam klijent ne plati za projekt. Kako biste podržali ovaj scenarij, možete postaviti uvjete plaćanja „plati kad bude plaćeno” (PWP) kada s dobavljačem postavljate narudžbenicu (PO, purchase order).

Na primjer, kada klijent plati iznos fakture za projekt, možete dobavljaču pustiti dio ili cijeli iznos fakture. Samo postavite uvjete PWP-a koji određuju da će dobavljač biti plaćen nakon što od klijenta primite postotak pripadajuće uplate. Ako od klijenta primite djelomičnu uplatu, dobavljaču možete ručno pustiti uplate za neke povezane fakture.

Sljedeći primjer opisuje postupak kada se upotrebljavaju uvjeti PWP-a.

## <a name="example"></a>Primjer

Vaša se tvrtka ili ustanova slaže da će klijentu isporučiti 100 računala s instaliranim softverom po cijeni od 150,00 USD po računalu. Zatim unajmite dobavljača da vam osigura računala na kojima je instaliran softver. Prema ugovoru, klijent mora odobriti kvalitetu računala prije nego što plati vašoj tvrtki ili ustanovi. Pravila vaše tvrtke ili ustanove nalažu zadržavanje plaćanja dobavljačima dok vam klijent ne plati. Stoga ste projekt postavili tako da ima postotak PWP-a od 100 posto.

Dobavljač vam šalje 100 računala na kojima je instaliran softver, zajedno s računom na 10.000,00 USD. Budući da su za vaš projekt postavljeni uvjeti PWP-a, ne plaćate dobavljača po primitku računala. Umjesto toga, računala šaljete klijentu, zajedno s računom na 15.000,00. Klijent pregledava računala i odobrava puni iznos fakture projekta.

Nakon što od klijenta primite cijelu uplatu, dobavljaču plaćate 10.000,00, što je puni iznos fakture dobavljača.

## <a name="set-up-pwp-terms-for-a-project"></a>Postavljanje uvjeta PWP-a za projekt

Kada postavljate uvjete PWP-a za projekt, morate odrediti, u postocima, minimalni iznos koji vam klijent mora platiti za projekt prije nego što vi platite dobavljaču. Iznos praga automatski se izračunava na fakturama za projekt koje izdajete klijentu. Slijedite ove korake za postavljanje praga postotka za uvjete PWP-a.

1. Idite na mogućnost **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.
2. Pronađite i otvorite projekt za koji želite postaviti uvjete PWP-a.
3. Na Brzoj kartici **Ugovori s dobavljačima** odaberite **Dodaj redak**.
3. U polju **Kod računa** odaberite jednu od sljedećih mogućnosti:

    - **Tablica** – Uvjeti PWP-a primjenjuju se na pojedinog dobavljača.
    - **Grupa** – Uvjeti PWP-a primjenjuju se na sve dobavljače u grupi dobavljača.
    - **Svi** – Uvjete PWP-a primjenjuju se na sve dobavljače.

4. Ako ste u prethodnom koraku odabrali **Tablica** ili **Grupa** , u polju **Dobavljač / Grupa dobavljača** odaberite dobavljača ili grupu dobavljača na koje se primjenjuju uvjeti PWP-a. Ako ste u prethodnom koraku odabrali **Svi** , polje **Dobavljač / Grupa dobavljača** ne može se uređivati.
5. Ako su uvjeti zadržavanja plaćanja dobavljaču postavljeni za dobavljača u projektu, u polju **Uvjeti zadržavanja plaćanja dobavljaču** odaberite ID pravila za uvjete zadržavanja.
6. U polju **Postotak praga PWP-a** unesite postotak praga za projekt. Postotak koji unesete za projekt definira minimalni iznos koji vam kupac mora platiti prije nego što vi platite dobavljaču.

## <a name="create-a-po-that-has-pwp-terms"></a>Stvaranje narudžbenice koja sadrži uvjete PWP-a

Kada knjižite račun dobavljača, ako dobavljač podliježe uvjetima PWP-a, ti se uvjeti prikazuju na redcima narudžbenice. Slijedite ove korake za stvaranje narudžbenice koja sadrži uvjete PWP-a.

1. Idite na **Nabava i dobavljanje** \> **Narudžbenice** \> **Sve narudžbenice**.
2. U Oknu radnji odaberite **Novo**. Zatim, u dijaloški okvir **Stvori narudžbenicu** unesite potrebne podatke i odaberite **U redu**.

    Alternativno, otvorite postojeću narudžbenicu na stranici s popisom **Sve narudžbenice**.

4. Na stranici **Narudžbenica** , na Brzoj kartici **Redci narudžbenice** , pregledajte pojedinosti retka narudžbenice za dobavljača. Mogućnost **Plati kad bude plaćeno** automatski se odabire, a vrijednost u polju **Postotak praga PWP-a** automatski se kopira iz polja **Postotak praga PWP-a** na stranicu **Projekti**.
6. Ako ne želite primijeniti uvjete PWP-a na dobavljača za redak narudžbe, očistite mogućnost **Plati kad bude plaćeno**. U ovom slučaju, polje **Postotak praga PWP-a** za redak narudžbenice vratit će se na 0 (nula).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ažuriranje uplate klijenta i plaćanje dobavljaču

Kada dobavljač dovrši svoj posao na projektu i pošalje vam fakturu, morate pregledati status projekta i fakture klijenta kako biste utvrdili jesu li za projekt ispunjeni uvjeti PWP-a. Ako su ispunjeni uvjeti PWP-a za dobavljača, možete odrediti koje ćete retke na fakturi dobavljača platiti na temelju uplate klijenta za projekt. Ako odlučite platiti dobavljaču iako uvjeti PWP-a nisu ispunjeni, možete poništiti uvjete PWP-a na stranici **Račun dobavljača s načelom „plati kad bude plaćeno”**.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Upiti i izvješća** \> **Upiti za zadržavanje** \> **Račun dobavljača s načelom „plati kad bude plaćeno”**.
2. U polje za pretraživanje na stranici **Račun dobavljača s načelom „plati kad bude plaćeno”** , unesite vrijednosti kako biste pronašli fakturu dobavljača koju želite pregledati, a zatim odaberite **Traži**.
3. Na Brzoj kartici **Redci fakture dobavljača** odaberite retke koje želite promijeniti.
4. Ako se uvjeti **Plati kad bude plaćeno** za redak računa ispune, odaberite **Pusti uplatu dobavljaču**. Mogućnost **Plati kad bude plaćeno** je obrisana, a vrijednost polja **Spremno za plaćanje** mijenja se u **Da**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]