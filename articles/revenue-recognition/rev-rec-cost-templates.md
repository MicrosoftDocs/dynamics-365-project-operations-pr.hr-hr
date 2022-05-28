---
title: Postavljanje predložaka troškova
description: U ovoj temi nalaze se informacije o načinu stvaranja predložaka troškova i njihovoj uporabi u aplikaciji Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9e163dc3180d2b35ddf9b15aa0577bf51e3b72ce
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594201"
---
# <a name="set-up-cost-templates"></a>Postavljanje predložaka troškova

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


U ovoj temi nalaze se informacije o načinu stvaranja predložaka troškova i njihovoj uporabi u aplikaciji Project Operations. Predložak troškova određuje:

- Kategorije projekata za predviđanje i stvarne transakcije koje treba uključiti u postotak izračuna dovršenosti projekta. Tada se upotrebljava vrijednost ukupnog postotka za izračun iznosa prihoda koji se priznaje.
- Bilo da se postotak dovršenosti može mijenjati ako se automatski izračuna.
- Bilo da se postotak dovršenosti izračunava na temelju iznosa ili jedinica.

## <a name="cost-template-example"></a>Primjer predloška troškova

Radite na projektu dizajna web-mjesta za klijenta pri čemu naplaćujete paušalnu naknadu od 10.000 USD. Predviđate da će trebati 100 sati (5.000 USD) za dovršetak projekta. Također predviđate dvije avionske karte i četiri noćenja u hotelu za odlaske u mjesto klijenta (1.800 USD). To dovodi do ukupno predviđenih troškova od 6.800 USD.

Kada pokrenete postupak priznavanja prihoda s fiksnom cijenom kako biste na kraju mjeseca stvorili procjenu, ustanovit ćete da ste na projektu radili 35 sati. To još ne uključuje zrakoplovne letove ili hotelske troškove. Također ste imali pomoćnika koji je proveo pet sati u istraživanju za potrebe projekta po cijeni od 100 USD, što niste planirali.

Kada izračunate vrijednost postotka dovršenosti za ovaj projekt, trebate slijediti sljedeće mogućnosti:

- Želite li uključiti sve troškove (radno vrijeme i troškove) ili samo radno vrijeme?
- Želite li uključiti svo ili samo planirano radno vrijeme?
- Želite li izračunati postotak dovršenosti na temelju troška planiranog radnog vremena u dolarima (5.000 USD) ili samo na broju sati rada (100)?

Vaši odgovori na ova pitanja određuju mogućnosti koje postavljate na predlošku troškova i kategorije koje odaberete u redcima predloška troškova.

Sljedeća tablica prikazuje rezultate različitih načina za izračun vrijednosti ukupnog postotka za ovaj scenarij.

| Dovršenost na temelju | Troška ili jedinice u dolarima | Postotak dovršenosti | Izračun |
| --- | --- | --- | --- |
| Ukupno radno vrijeme, bez troškova | Trošak u dolarima | 37 % 35 x 50 USD + 100 USD= 1.850 USD 1.850 USD / 5.000 USD |
| Ukupno radno vrijeme, bez troškova | Jedinice | 40 % | 40 sati / 100 sati (uključujući pet neplaniranih sati) |
| Planirano radno vrijeme, bez troškova | Trošak ili jedinica u dolarima | 35 % | 35 / 100 sati ili 35 x 50 USD / 5.000 |
| Ukupno radno vrijeme i troškovi | Trošak u dolarima | 27,2 % | 1.850 USD / 6.800 USD |

Odluka o pristupu stvaranju predloška troškova može ovisiti o nekoliko razmatranja:

- Ako u obrazac troškova uvrstite neplanirano radno vrijeme, postoji mogućnost da ćete dosegnuti 100 posto dovršenosti prije završetka projekta. To je zato što će stvarni sati biti veći od planiranih. Ako upotrebljavate bilo koju od prva dva načina navedena u tablici, trebali biste promijeniti plan (predviđene jedinice) kad uočite odstupanja. U ovom biste slučaju trebali dodati ili oduzeti sate na temelju svog znanja o tome što je potrebno za završetak projekta. Ako će za dovršetak projekta trebati dodatnih 65 sati, planu biste trebali dodali pet sati na ukupno 105 sati. Ako znate da će vaš pomoćnik provesti još pet sati istraživanja, ukupno će to postati 110 sati.
- Ako upotrijebite način naveden u tablici kao treći, planirano vrijeme ažurirali biste samo za svoje vrijeme kako bi izračun ukupnog postotka ostao točan. Vaša će se profitabilnost promijeniti kada se zabilježe neplanirani sati, ali vi ćete ostati u poznatom pravcu kretanja ukupnog postotka.
- Ako upotrebljavate način koji je u tablici naveden kao četvrti, postoji opasnost da će se troškovi prikazati u nepravilnim vremenskim intervalima i možda se neće odraziti na napredak u dovršenju. Stoga, ako su troškovi uključeni, oni mogu uzrokovati da postotak dovršenosti varira više nego što je to poželjno. Primjerice, kako još niste letjeli, vaš je postotak dovršenosti iznosio je 27 posto, umjesto 35 ili 37 posto, koliko bi iznosio da ste proračun temeljili samo na radnom vremenu. Ako ste krenuli na jedno putovanje s dva noćenja i točno prognozirali troškove leta i hotela, postotak dovršenosti bio bi 40,4 posto (1.850 USD za rad i 900 USD za troškove = 2.750 USD / 6.800 USD = 40,4 posto). Stoga bi nastajanje troškova za samo jedno putovanje avionom promijenilo postotak dovršenosti sa 27 posto na 40 posto.

## <a name="create-cost-templates"></a>Stvaranje predložaka troškova
Kako biste stvorili predložak troška, poduzmite ove korake:

1. Da biste pristupili predlošcima troškova, u okruženju Dynamics 365 Finance otvorite **predložak Troškovi troškova upravljanja projektima i računovodstva** > **·** > **.** > **·**
2. Kako biste stvorili novi predložak, odaberite **Novo**. Unesite naziv i opis.
3. Navedite ID retka troška za svaku vrstu transakcije.
4. Odaberite zadani način dovršenja:

  - **Automatski**: Postotak dovršenosti izračunava se automatski na projektu. Dobivena vrijednost ne može se mijenjati.
  - **Ručno**: Postotak dovršenosti izračunava se automatski na projektu. Dobivena vrijednost može se mijenjati.

  > [!NOTE]
  > Za ručne izračune postotak dovršenosti održava se u stavci **Ručni izračun** na kartici **Općenito**, na stranici **Procjena**.

5. U stavci **Dovršenost na temelju** odaberite jednu od sljedećih vrijednosti:

  - **Iznos**: Iznos u računovodstvenoj valuti izračunava postotak dovršenosti.
  - **Jedinica**: Postotak dovršenosti izračunava se na temelju količine.
  - **Ravna crta**: Sustav proporcionalno izračunava postotak dovršenosti s pomoću datuma početka i završetka projekta kako bi odredio duljinu projekta.

6. Odaberite **Redci cijena** kako biste pregledali retke troškova u predlošku troškova. Za svaku vrstu transakcije potreban je barem jedan redak cijene. Međutim, možete stvoriti više redaka cijena za iste vrste transakcija i postaviti željene atribute za te retke.
7. Na kartici **Kategorije** odaberite kategorije projekata koje će biti uključene u redak predloška troškova.
8. Na kartici **Općenito** odaberite hoće li taj redak biti uključen u izračun postotka dovršenosti.
9. Odaberite način troškova do završetka koji će se upotrebljavati pri izračunu postotka dovršenosti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]