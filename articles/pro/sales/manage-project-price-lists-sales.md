---
title: Upravljanje cjenicima projekta u ponudama projekta
description: U ovoj temi nalaze se informacije o radu s cjenicima projekta u ponudama. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966748"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Upravljanje cjenicima projekta u ponudama projekta (prodaja)

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Cjenici projekata osmišljeni su kako bi podržali prodajne cjenike koji su na snazi s višestrukim datumima. Uz Dynamics 365 Project Operations, dodaje se novi povezani entitet pod nazivom **Cjenici projekta**. Ovaj entitet u odnosu je 1 prema više s ponudom projekta.

Cjenici projekata upotrebljavaju se za određivanje cijene transakcijama vremena i troškova na projektu. Kada ponuda ima jedan ili više cjenika projekata, ti se cjenici upotrebljavaju za procjenu cijene vremena i troškova, kao i stvarnih podataka na projektima koji su povezani s ponudom preko retka ponude.

Kada na ponudi projekta ne postoje cjenici projekata, primit ćete poruku upozorenja. U poruci se navodi da, budući da ne postoje cjenici projekata, vaš procijenjeni i stvarni rad na projektu i troškovi neće imati cijenu. Umjesto toga, imat će nultu (0) cijenu za vrijednosti prodaje.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Povezivanje ili prekidanje veze cjenika projekta na ponudi projekta

Kako biste stvorili ili odabrali određeni cjenik za procjenu rada i troškova koji se temelje na projektu, poduzmite sljedeće korake.

1. Na ponudi odaberite karticu **Cijena projekta** i u podrešetki odaberite mogućnost **+ Dodaj novi cjenik projekta**.
2. Na stranici Brzo stvaranje odaberite cjenik. Padajući popis prikazuje sve cjenike kojima je kontekst postavljen na **Prodaja**, a valuta odgovara valuti ponude.
4. Unesite opis povezanih cjenika projekta i odaberite **Spremi i zatvori**.

Stvoren je povezani cjenik projekta.

Ovaj postupak možete ponoviti ako trebate povezati više od jednog cjenika projekta ponudi projekta. Više cjenika projekta stvorite samo ako imate različite datume stupanja na snagu na svakom povezanom cjeniku projekata.

> [!NOTE]
> Project Operations ne podržava preklapanje datuma stupanja na snagu cjenika projekata. Ako postoji više cjenika projekata za transakciju s danim datumom, cijena te transakcije bit će zadana na nulu (0).
Kako biste uklonili povezanost s cjenikom projekta, odaberite cjenik projekta, a zatim odaberite **Izbriši cjenik ponude projekta**. Cjenik se uklanja iz cjenika projekta u ponudi, ali sam cjenik se ne briše. Briše se samo povezanost s ponudom.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Postavljanje zadanih cjenika projekata na ponudu

Cjenici projekata mogu se postaviti prema zadanim postavkama na ponudi projekta. Ova postavka osigurava da sve ponude u vašoj tvrtki ili ustanovi uvijek počinju sa standardnim cjenikom za to cjenovno razdoblje.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Postavljanje organizacijski zadanih cjenika projekata

1. Idite na **Postavke** > **Općenito** > **Parametri**.
2. Na stranici s popisom **Aktivni parametri** pronađite zapis i dvaput pritisnite kako biste ga otvorili. 
3. Na stranici **Parametri** odaberite karticu **Cjenik**. Možete vidjeti da je prikazan popis zadanih cjenika. Ovo je popis standardnih troškova i prodajnih cjenika. Ako ovdje imate povezani prodajni cjenik za svaku valutu u kojoj prodajete, osigurat će se da je taj prodajni cjenik zadan za svaku ponudu koju stvarate za klijente koji obavljaju transakcije u toj valuti.

### <a name="set-up-customer-specific-project-price-lists"></a>Postavljanje cjenika projekata specifičnog za klijenta

Cjenici projekata specifični za klijenta mogu se postaviti i kada ste dogovorili glavni ugovor o cijenama sa svojim klijentima.

Kako biste postavili cjenik projekta specifičan za klijenta, poduzmite sljedeće korake.

1. U području **Prodaja** odaberite stavku **Klijenti**.
2. Na popisu svojih aktivnih računa odaberite i otvorite zapis o klijentu za kojeg imate poseban cjenik.
3. Na kartici **Cjenici projekata** možete stvoriti nove povezane cjenike kako biste dobili cjenik projekta koji je specifičan za ovog klijenta.

## <a name="create-custom-pricing-on-a-project-quote"></a>Stvaranje prilagođene cijene na ponudi projekta

Nakon što ste dobili cjenike projekata zadane organizacijski i za specifičnog klijenta, ponude projekata automatski će se stvarati s tim povezanim cjenikom projekata. Međutim, u određenim slučajevima možda ćete trebati stvoriti prilagođene cijene za određenu ponudu projekta. 

1. Na stavci **Ponuda projekta**, na kartici **Cjenik projekta**, provjerite u podrešetki da nije odabran posebni zapis cjenika.
2. Odaberite **Stvori prilagođene cijene**. Time će se napraviti kopije svih standardnih cjenika trenutačno povezanih s ponudom i povezati te primjerke s ponudom. Uklonit će se postojeća povezanost sa standardnim cjenicima. Tada prodajni predstavnik može započeti s uređivanjem cijena na tim primjercima. Promijenjene cijene primjenjivat će se samo na cijene ponude za ovaj projekt.
