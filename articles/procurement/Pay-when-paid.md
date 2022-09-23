---
title: Plaćanje prilikom plaćanja dobavljaču
description: Ova tema objašnjava kako koristiti scenarij plaćanja kada se plaća (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Plaćanje prilikom plaćanja dobavljaču

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ova tema objašnjava kako koristiti scenarij plaćanja kada se plaća (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Kreiranje narudžbenice s PWP uvjetima

Kada knjižite fakturu od dobavljača, ako dobavljač podliježe PWP uvjetima, ti se uvjeti prikazuju u recima narudžbenice (PO). Slijedite ove korake za stvaranje narudžbenice koja sadrži uvjete PWP-a.

1. U Microsoft Dynamics odjeljku Financije 365 slijedite jedan od sljedećih koraka:

    - Idite na **Nabava i dobavljanje** \> **Narudžbenice** \> **Sve narudžbenice**. U Oknu radnji odaberite **Novo**. **U dijaloškom okviru Kreiranje narudžbenice** odaberite dobavljača za kojeg su PWP pojmovi postavljeni na projektu, unesite druge potrebne podatke, a zatim odaberite **U redu**.
    - Idite na mogućnost **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**. U oknu akcije na **kartici Upravljanje** odaberite **Zadatak stavke**. Odaberite narudžbenicu. Odaberite dobavljača za kojeg su PWP pojmovi postavljeni na projektu, a zatim odaberite **U redu**.

2. Na stranici Narudžbenica **na** brzoj **kartici Reci narudžbenice** odaberite **Dodaj redak** da biste kreirali redak narudžbenice.
3. Odaberite broj artikla ili kategoriju nabave i unesite ostale potrebne detalje. Pregledajte detalje poštanskog reda za dobavljača.

    Mogućnost **Plati kad bude plaćeno** automatski se odabire, a vrijednost u polju **Postotak praga PWP-a** automatski se kopira iz polja **Postotak praga PWP-a** na stranicu **Projekti**.

4. Ako ne želite primijeniti uvjete PWP-a na dobavljača za redak narudžbe, očistite mogućnost **Plati kad bude plaćeno**. U tom će se slučaju polje postotka **praga** PWP-a za LINIJU PO vratiti na **0** (nula).
5. Na stranici Narudžbenica **u** oknu akcije na kartici Nabava **odaberite** **Potvrdi** da biste potvrdili narudžbenicu.
6. U oknu akcije na kartici Faktura **odaberite** **Faktura** da biste generirali fakturu za narudžbenicu.

## <a name="create-a-project-invoice-proposal"></a>Kreiranje prijedloga za fakturu za projekt

Prijedlozi faktura za projekt koriste se za kreiranje faktura projekta za kupca. U PWP scenariju plaćanja dobavljača ovise o plaćanjima kupaca prema PWP postavkama. Međutim, postoje opcije koje vam omogućuju oslobađanje plaćanja bez plaćanja kupaca kako vam je potrebno. Da biste kreirali fakturu projekta za kupca, slijedite ove korake.

1. U aplikacijama za angažiranje korisnika otvorite **Projekti** \> **i** odaberite projekt.
2. Na kartici **Stvarne** vrijednosti odaberite stvarni redak koji generira POŠTANSKI program koji ima **vrstu neobjavljene prodajne** transakcije. Zatim odaberite **Spremno za fakturu**.
3. Otvorite Ugovor o projektu **prodaje** \> **·**\> i odaberite ugovor o projektu.**·**
4. U oknu akcije odaberite **Faktura** da biste generirali fakturu kupcu.
5. U odjeljku Financije otvorite **Odjeljak Upravljanje projektima i računovodstvo** \> **Periodični** \> **uvoz iz pripremne tablice** i odaberite **U redu** da biste generirali temeljnicu integracije operacija projekta.
6. Otvorite Odjeljak **Upravljanje projektima i računovodstvo** \> **Fakture za projekt prijedlog fakture** \> **i** odaberite **Proknjiži** da biste proknjižili prijedlog fakture generiran za projekt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ažuriranje uplate klijenta i plaćanje dobavljaču

Kada dobavljač dovrši svoj rad na projektu i pošalje vam fakturu, morate pregledati status projekta i fakture kupca da biste utvrdili jesu li ispunjeni uvjeti PWP-a za projekt. Ako su ispunjeni uvjeti PWP-a za dobavljača, možete odrediti koje ćete retke na fakturi dobavljača platiti na temelju uplate klijenta za projekt. Ako odlučite platiti dobavljaču iako uvjeti PWP-a nisu ispunjeni, možete poništiti uvjete PWP-a na stranici **Račun dobavljača s načelom „plati kad bude plaćeno”**.

1. U financijama idite na **Projekti upravljanja i računovodstva** \> **Projekti** \> **Svi projekti** i odaberite projekt.
2. U oknu akcije odaberite **Kontrola**, a zatim odaberite **Fakture dobavljača da bi se prikazale** sve fakture dobavljača generirane za projekt.
3. U polje za pretraživanje na stranici **Račun dobavljača s načelom „plati kad bude plaćeno”**, unesite vrijednosti kako biste pronašli fakturu dobavljača koju želite pregledati, a zatim odaberite **Traži**.
4. **Odaberite mogućnost Plati prilikom plaćanja** da biste vidjeli samo PWP fakture.
5. Na brzoj **kartici Reci fakture** Dobavljač odaberite retke koje želite lansirati radi plaćanja.
6. Odaberite **Otpusti uplatu** dobavljača. Mogućnost **Plati kad bude plaćeno** je obrisana, a vrijednost polja **Spremno za plaćanje** mijenja se u **Da**.
