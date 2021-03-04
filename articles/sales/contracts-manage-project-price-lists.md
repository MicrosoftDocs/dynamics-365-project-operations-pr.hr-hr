---
title: Upravljanje cjenicima za projekt u ugovorima o projektu
description: U ovoj temi nalaze se informacije o upravljanju cjenicima za projekt u ugovorima o projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133300"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Upravljanje cjenicima za projekt u ugovorima o projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Ugovori o projektu u aplikaciji Dynamics 365 Project Operations osmišljeni su tako da u ugovoru podržavaju prodajne cjenike mjerodavne na više datuma. U aplikaciji Project Operations postoji novi povezani entitet naziva **Cjenici za projekt**. Ovaj je entitet u odnosu jedan na više prema ugovoru o projektu.

Cjenici za projekt upotrebljavaju se za određivanje cijene transakcija vremena i troškova na projektu. Kada ugovor ima jedan ili više cjenika za projekt, ti se cjenici upotrebljavaju za određivanje cijene procijenjenih i stvarnih vremena i troškova za projekte koji su povezani s ugovorom putem retka ugovora.

Kada u ugovoru o projektu ne postoje cjenici za projekt, prikazat će se poruka upozorenja kako ne postoje cjenici za projekt, a vaše procjene, stvarni rad na projektu i troškovi neće imati određenu cijenu. Neće biti cijena za prodajne vrijednosti.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Povežite ili prekinite vezu cjenika za projekt s ugovorom o projektu

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Stvorite ili povežite određeni cjenik za procjenu rada i troškova koji se temelje na projektu

1. Na ugovoru o projektu odaberite karticu **Cjenici za projekt**.
2. U podrešetki odaberite **+ Dodaj novi cjenik za projekt**.
3. Na klizaču **Brzo stvaranje** odaberite cjenik. 

  Padajući popis prikazuje sve cjenike kojima je kontekst postavljen na **Prodaja**, pri čemu se valuta na cjeniku poklapa s valutom iz ugovora.
  
4. Unesite opis za povezivanje cjenika za projekt, odaberite **Spremi**, a zatim zatvorite klizač **Brzo stvaranje**.

   Stvoren je povezani cjenik projekta.
   
5. Ponovite korake 1 – 4 kako biste povezali više od jednog cjenika za projekt s ugovorom o projektu. Više cjenika za projekt stvorite samo ako imate različite datume stupanja na snagu na svakom povezanom cjeniku za projekt.

> [!NOTE]
> Project Operations ne podržava preklapanje datuma stupanja na snagu cjenika za projekt. Ako postoji više cjenika za projekt za transakciju s danim datumom, cijena te transakcije bit će zadana na nulu.

### <a name="remove-a-project-price-list-association"></a>Uklanjanje povezanosti cjenika za projekt

- Odaberite cjenik za projekt, a zatim na podrešetki odaberite **Izbriši cjenik ugovorna o projektu**. 

  Cjenik se uklanja iz cjenika za projekt na ugovoru. Sam cjenik neće se izbrisati. Izbrisat će se samo povezanost s ugovorom.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Postavljanje automatskog zadavanje cjenika za projekt na ugovor

Cjenik za projekt može se postaviti kao zadani popis na ugovoru o projektu. Ova postavka može vam osigurati da svi ugovori u vašoj tvrtki ili ustanovi uvijek započinju sa standardnim cjenikom za to cjenovno razdoblje.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Postavljanje organizacijski zadanih cjenika za projekt

1. Idite na **Postavke** > **Općenito**, a zatim odaberite **Parametri**.
2. Na stranici s popisom **Aktivni parametri** odaberite i dvaput kliknite zapis kako biste ga otvorili. Kada dvaput kliknete, pazite da ne kliknete na vrijednost polja koja je hiperveza. 
3. Na stranici **Aktivni parametri** odaberite karticu **Cjenik**. Podrešetka prikazuje popis zadanih cjenika. Ovo je popis cjenika standardnih troškova i prodajnih cijena. Postojanje cjenika **Prodaja** povezanog ovdje za svaku valutu u kojoj obavljate prodaju osigurava da je prodajni cjenik zadan za bilo koji ugovor koji stvarate za klijente koji obavljaju transakcije u toj valuti.

### <a name="set-up-a-customer-specific-project-price-list"></a>Postavljanje cjenika za projekt specifičnog za klijenta

Možete postaviti i cjenike za projekt specifične za klijenta kada ste sa svojim klijentima dogovorili glavni ugovor o cijenama.

1. Idite na **Prodaja** > **Klijenti**.
2. S popisa aktivnih računa odaberite klijenta za kojeg imate poseban cjenik.
3. Odaberite zapis o klijentu kako biste ga otvorili, a zatim odaberite karticu **Cjenici za projekt**. Podrešetka prikazuje popis cjenika za projekt specifičnih za tog klijenta. 
4. Ovdje stvorite vezu s novim cjenikom kako biste imali cjenik za projekt specifičan za ovog klijenta.

## <a name="custom-pricing-on-a-project-contract"></a>Prilagođeno određivanje cijena za ugovor o projektu

Nakon što ste dobili cjenike za projekt zadane organizacijski i za specifičnog klijenta, ugovori o projektu automatski će se stvoriti s tim vezama cjenika za projekt. Međutim, cjenici za projekt na ugovoru o projektu uvijek se kopiraju s datumom i nazivom ugovora koji im je dodan. Voditelji računa i projekata tada mogu početi uređivati cijene na tim kopijama. Ove izmijenjene cijene primjenjivat će se samo na ovaj ugovor o projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]