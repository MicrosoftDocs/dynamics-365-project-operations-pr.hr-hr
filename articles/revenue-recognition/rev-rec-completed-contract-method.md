---
title: Upravljanje procjenama prihoda
description: U ovoj temi nalaze se informacije o načinu rada s procjenama prihoda za projekte.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013838"
---
# <a name="manage-revenue-estimates"></a>Upravljanje procjenama prihoda

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Možete stvoriti, izračunati, knjižiti, stornirati ili ukloniti procjene prihoda. To možete učiniti ručno ili s pomoću periodičnog postupka. U ovoj temi nalaze se informacije o načinu rada s procjenama prihoda za projekte.

### <a name="manage-revenue-estimates-manually"></a>Ručno upravljanje procjenama prihoda

Na projektu s procjenom prihoda od fiksne cijene ili stranici **Upit za procjenu** (**Upravljanje projektima i računovodstvo** > **Izvješća i upiti** > **Upiti za procjenu i izvješća o procjeni**), odaberite **Procjene**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Upravljanje procjenama prihoda s pomoću periodičnog postupka

Idite na **Upravljanje projektima i računovodstvo** > **Periodički** > **Procjene** i odaberite odgovarajući postupak.

## <a name="create-a-revenue-estimate"></a>Stvaranje procjene prihoda

Kako biste ručno stvorili procjenu prihoda, poduzmite sljedeće korake. 

1. Idite na **Upravljanje projektima i računovodstvo** > **Periodički** > **Procjene**.
2. Odaberite **Novo**. Na stranici **Stvaranje procjene** odaberite sljedeće parametre:

   - **Kod razdoblja**: Ovaj kod određuje koliko se često procjene knjiže.
   - **Datum procjene**: Datum obrade procjene.
   - **Neprekidno**: Označite ovaj potvrdni okvir za stvaranje procjena samo ako su procjene knjižene u prethodnom razdoblju ili ako se radi o prvoj stvorenoj procjeni. Ako ovo nije odabrano, procjene se stvaraju čak i ako nisu knjižene u prethodnom razdoblju.
   - **Način troškova za završetak**: Definirajte način procjene preostalog posla na projektu. Dodatne informacija potražite u odjeljku [Načini troškova za završetak](cost-complete-methods.md).
   - **Način dovršenosti**: Odaberite način dovršenosti između sljedećih mogućnosti:
     - **Automatski**: Postotak dovršenosti izračunava se automatski i na temelju redaka troškova uključenih u izračun. Predložak troškova definira uključene retke troškova.
     - **Priručnik**: Postotak dovršenosti jednak je postotku dovršenosti posljednje procjene. Nakon stvaranja procjene, možete promijeniti **Ručni izračun** na stranici **Procjene**.
     - **Iz predloška troška**: Kombinacija automatskog i ručnog načina. Ova se mogućnost postavlja automatski ili ručno, ovisno o zadanoj vrijednosti u predlošku troška.
   - **Model predviđanja**: Odaberite model predviđanja za procjenu.
   - **Ispis popisa procjena**: Stvorite i prikažite popis procjena. Popis sadrži status trenutačne funkcije. Na izvješću možete ispisati sva upozorenja o procjeni. Sljedeći uvjeti uzrokuju prikazivanje upozorenja na popisu procjena:
     - Postotak dovršenosti veći od 100 posto.
     - Postotak dovršenosti manji od nula posto.
     - Negativni iznos u stupcu **Za završiti**.
     - Procjena bez odgovarajućeg ugovornog iznosa.
     - Procjena bez priložene procjene troškova.
   - **Prikaži zapis s informacijama**: Odaberite ovu mogućnost kako biste dobili poruku koja sadrži informacije o procjeni projekata koji su obrađeni tijekom izvođenja posla.


## <a name="post-wip-or-accruals"></a>Knjiženje WIP-a ili akumulacije

Nakon prosudbe procjene, one se održavaju, smanjuju ili povećavaju. Tada možete knjižiti WIP kada radite s načelom procjene **Završeni ugovor** ili knjižiti razgraničenja kada radite s načelom procjene **Završeni postotak**.
  
Status razdoblja procjene mijenja se iz **Stvoreno** u **Knjiženo**.

## <a name="reverse-wip-or-accruals"></a>Storno WIP-a ili akumulacije

Upotrijebite mogućnost storniranja knjiženja već objavljenog WIP-a ili akumulacije, a zatim stvorite procjene za to razdoblje.

> [!NOTE]
> Kako biste stornirali razdoblje koje se nalazi između ostalih razdoblja, stornirajte potrebna razdoblja procjene, a zatim ih ponovno proknjižite. Budući da sva sljedeća razdoblja ovise o procjenama iz prethodnog razdoblja, nemojte preskakati nijedno razdoblje.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Uklanjanje procjene projekta i završetak projekta

Posljednji je korak u postupku procjene uklanjanje procjene projekta i završetak projekta s fiksnom cijenom kada postotak dovršenosti dosegne 100 posto.

Kada pokrenete uklanjanje događa se sljedeće:

- Za izvršeni ugovor o projektu s fiksnom cijenom vrijednosti WIP-a brišu se s računa bilance i knjiže na račune dobiti i gubitka.
- Za projekt s fiksnom cijenom s ispunjenim postotkom, s računa dobiti i gubitka uklanja se akumulacija.

Procjena mijenja status u **Uklonjeno**.

> [!NOTE]
> U posebnim slučajevima, postotak se može proširiti i preko 100 posto. Kada se to dogodi, smanjite postotak dovršenosti s pomoću **Načina postavljanja troška za završetak na nulu** kako bi dosegli 100 posto.

## <a name="reverse-elimination"></a>Storniranje izmjena

1. Idite na **Upravljanje projektom i računovodstvo** > **Periodično** > **Procjene** > **Uklanjanje storniranja**. 
2. U oknu radnji, na kartici **Postupak**, u grupi **Održavanje**, odaberite **Procjena**. 
3. Odaberite **Uklanjanje storniranja**.

Ovu stranicu upotrijebite za storniranje svih uklanjanja s navedenim datumom procjene i statusom procjene **Uklonjeno**. Status transakcije mijenja se nakon što odaberete odgovarajuća polja.

Ovo također automatski mijenja status projekta u **U postupku** ako je faza projekta postavljena na završeno. Status procjene projektnog razdoblja vraća se na **Proknjiženo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]