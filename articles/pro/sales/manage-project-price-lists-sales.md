---
title: Upravljanje cjenicima projekta u projektnim ponudama
description: U ovom se članku navode informacije o radu s cjenicima za projekt u ponudama.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af89996fcaca9823d32e84e10ce6d29ead4f3d6d
ms.sourcegitcommit: 95dacb0e74fa8970f56fdb1cbaa915d3fbec6e0f
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023604"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Upravljanje cjenicima projekta u projektnim ponudama 

_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_

Cjenici projekata osmišljeni su kako bi podržali prodajne cjenike koji su na snazi s višestrukim datumima. Uz Dynamics 365 Project Operations dodaje se novi povezani entitet pod nazivom **Cjenici za projekt**. Ovaj entitet u odnosu je 1 prema više s ponudom projekta.

Cjenici za projekte upotrebljavaju se za određivanje cijene vremena, materijala i transakcija troškova na projektu. Kada ponuda ima jedan ili više cjenika za projekt, ti se cjenici upotrebljavaju za cijenu procijenjenih vremena, materijala, troškova i stvarnih podataka na projektima koji su povezani s ponudom putem retka ponude.

Kada na ponudi projekta ne postoje cjenici za projekt, primit ćete poruku upozorenja. U poruci se navodi da, budući da ne postoje cjenici za projekt, vaš procijenjeni i stvarni rad na projektu i troškovi neće imati cijenu. Umjesto toga, imat će nultu (0) cijenu za vrijednosti prodaje.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Povezivanje ili prekidanje veze cjenika projekta na ponudi projekta

Kako biste stvorili ili odabrali određeni cjenik za procjenu rada i troškova koji se temelje na projektu, poduzmite sljedeće korake.

1. Na ponudi odaberite karticu **Cijena projekta** i u podrešetki odaberite mogućnost **+ Dodaj novi cjenik projekta**.
2. Na stranici Brzo stvaranje odaberite cjenik. Padajući popis prikazuje sve cjenike kojima je kontekst postavljen na **Prodaja**, a valuta odgovara valuti ponude.
4. Unesite opis povezanih cjenika projekta i odaberite **Spremi i zatvori**.

Stvoren je povezani cjenik projekta.

Ovaj postupak možete ponoviti ako trebate povezati više od jednog cjenika projekta ponudi projekta. Više cjenika za projekt stvorite samo ako imate različite datume stupanja na snagu na svakom povezanom cjeniku za projekt.

> [!NOTE]
> Project Operations ne podržava preklapanje datuma stupanja na snagu cjenika za projekt. Ako postoji više cjenika projekata za transakciju s danim datumom, cijena te transakcije bit će zadana na nulu (0).
Kako biste uklonili povezanost s cjenikom projekta, odaberite cjenik projekta, a zatim odaberite **Izbriši cjenik ponude projekta**. Cjenik se uklanja iz cjenika za projekt u ponudi, ali sam cjenik se ne briše. Briše se samo povezanost s ponudom.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Postavljanje zadanih cjenika za projekt na ponudu

Cjenici za projekt mogu se postaviti prema zadanim postavkama na ponudi projekta. Ova postavka osigurava da sve ponude u vašoj tvrtki ili ustanovi uvijek počinju sa standardnim cjenikom za to cjenovno razdoblje.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Postavljanje organizacijski zadanih cjenika za projekt

1. Idite na **Postavke** > **Općenito** > **Parametri**.
2. Na stranici s popisom **Aktivni parametri** pronađite zapis i dvaput pritisnite kako biste ga otvorili. 
3. Na stranici **Parametri** odaberite karticu **Cjenik**. Možete vidjeti da je prikazan popis zadanih cjenika. Ovo je popis standardnih troškova i prodajnih cjenika. Ako ovdje imate povezani prodajni cjenik za svaku valutu u kojoj prodajete, osigurat će se da je taj prodajni cjenik zadan za svaku ponudu koju stvarate za klijente koji obavljaju transakcije u toj valuti.

### <a name="set-up-customer-specific-project-price-lists"></a>Postavljanje cjenika za projekt specifičnog za klijenta

Cjenici za projekt specifični za klijenta mogu se postaviti i kada ste dogovorili glavni ugovor o cijenama sa svojim klijentima.

Kako biste postavili cjenik projekta specifičan za klijenta, poduzmite sljedeće korake.

1. U području **Prodaja** odaberite stavku **Klijenti**.
2. Na popisu svojih aktivnih računa odaberite i otvorite zapis o klijentu za kojeg imate poseban cjenik.
3. Na kartici **Cjenici za projekt** možete stvoriti nove povezane cjenike kako biste dobili cjenik za projekt koji je specifičan za ovog klijenta.

## <a name="create-custom-pricing-on-a-project-quote"></a>Stvaranje prilagođene cijene na ponudi projekta

Nakon što ste dobili cjenike za projekt zadane organizacijski i za specifičnog klijenta, ponude projekta automatski će se stvarati s tim povezanim cjenikom za projekt. Međutim, u određenim slučajevima možda ćete trebati stvoriti prilagođene cijene za određenu ponudu projekta. 

1. Na stavci **Ponuda projekta**, na kartici **Cjenik projekta**, provjerite u podrešetki da nije odabran posebni zapis cjenika.
2. Odaberite **Stvori prilagođene cijene**. Time će se napraviti kopije svih standardnih cjenika trenutačno povezanih s ponudom i povezati te primjerke s ponudom. Uklonit će se postojeća povezanost sa standardnim cjenicima. Tada prodajni predstavnik može započeti s uređivanjem cijena na tim primjercima. Promijenjene cijene primjenjivat će se samo na cijene ponude za ovaj projekt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
