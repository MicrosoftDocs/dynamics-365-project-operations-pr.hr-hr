---
title: Izvedba API-ja rasporeda projekta
description: U ovom se članku navode informacije o referentnim vrijednostima performansi API-ja za raspored projekta i utvrđuju najbolje prakse za optimalnu uporabu.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911173"
---
# <a name="project-schedule-api-performance"></a>Izvedba API-ja rasporeda projekta

_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima/bez zaliha, osnovna implementacija – od sklapanja posla do predračuna, Project for the Web_

U ovom se članku navode informacije o mjerilima performansi sučelja za programiranje aplikacija za raspored projekta (API) i identificiraju se najbolji primjeri iz prakse za optimizaciju upotrebe.

## <a name="project-scheduling-service"></a>Usluga planiranja projekta
Usluga planiranja projekta usluga je s više klijenata koja radi na platformi Microsoft Azure. Dizajnirana je za poboljšanje interakcije pružanjem brzog i tečnog iskustva kada korisnici rade na projektima. Ovo se poboljšanje postiže prihvaćanjem zahtjeva za izmjenu, njihovom obradom, a zatim trenutačnim vraćanjem rezultata. Usluga asinkrono ustraje na aplikaciji Dataverse i ne blokira korisnike u izvođenju drugih operacija.

API-ji za planiranje projekta oslanjaju se na uslugu zakazivanja projekata za pokretanje zahtjeva koji su detaljnije opisani u kasnijim odjeljcima ovog članka.

API-ji rasporeda projekta dizajnirani su za rad sa sljedećim entitetima strukturne analize rada (WBS, engl. work breakdown structure):

  - Project
  - Zadatak projekta
  - Ovisnost projektnog zadatka
  - Članov projektnog tima
  - Dodjela resursa
  
Podržana su i gotova i prilagođena polja. Osim ako nije drugačije navedeno, podržane su sve uobičajene operacije, kao što su stvaranje, ažuriranje i brisanje. Dodatne informacija potražite u odjeljku [Uporaba API-ja rasporeda projekta za izvođenje operacija i entiteti planiranja](schedule-api-preview.md).

Kao dio API-ja rasporeda projekta, dodan je obrazac jedinice rada. Ovaj je uzorak poznat kao OperationSet i može se upotrebljavati kada se u jednoj transakciji mora obraditi nekoliko zahtjeva.

Primjer u nastavku prikazuje tijek koji će partner doživjeti kada se upotrijebi ova značajka.

![Dataverse i tijek usluge planiranja projekta.](./media/dataverse-project-scheduling-service-flow.png)

**Korak 1**: Klijent upućuje API poziv na krajnju točku protokola Open Data (OData) u aplikaciju Dataverse za stvaranje uzorka OperationSet.

**Korak 2**: Nakon stvaranja novog uzorka OperationSet, vraća se vrijednost **OperationSetId**.

**Korak 3**: Klijent upotrebljava vrijednost **OperationSetId** za izradu drugog zahtjeva API-ja rasporeda projekta. Rezultat je zahtjev za stvaranje, ažuriranje ili brisanje na entitetu za planiranje. Kada se uputi ovaj zahtjev, vrši se provjera valjanosti metapodataka. Ako provjera valjanosti ne uspije, zahtjev se prekida i vraća se pogreška.

**Koraci 4a – 4c**: Ovi koraci predstavljaju fazu PRIHVAĆANJE. Klijent zove API **ExecuteOperationSetV1**, koji šalje sve promjene usluzi planiranja projekta u jednom skupu. Usluga planiranja projekta izvodi vlastite provjere valjanosti zahtjeva u paketu. Svaki neuspjeh provjere valjanosti poništava skup i vraća iznimku pozivatelju. Ako usluga za planiranje projekta uspješno prihvati skup, status uzorka OperationSet ažurira se kako bi odražavao činjenicu da usluga planiranja projekta obrađuje uzorak OperationSet.

**Korak 5**: Ovaj korak predstavlja fazu USTRAJNOST. Usluga planiranja projekta asinkrono upisuje skup u aplikaciju Dataverse u transakciji. Ako je operacija upisivanja uspješna, OperationSet označuje se kao **Dovršen**. Sve pogreške vraćaju transakciju i skup, a OperationSet označuje se kao **Neuspio**.

## <a name="performance-methodology"></a>Metodologija izvedbe
Vrijeme izvršenja definira se kao vrijeme od poziva do API-ja **ExecuteOperationSetV1** dok usluga planiranja projekta ne završi upisivanje u aplikaciju Dataverse. Sve se operacije izvode zajedno 2.200 puta, a mjerenja vremena izvršenja P99 prijavljuju se. Mjere se operacije s jednim zapisom i masovne operacije.

Za operaciju s jednim zapisom, OperationSet sadrži jedan zahtjev. Za masovne operacije sadrži 20, 50 ili 100 zahtjeva. Veličina svake skupne navodi se zasebno.

Te se operacije izvode na osnovnoj implementaciji aplikacije UR 15 Project Operations u Sjevernoj Americi.

## <a name="results"></a>Rezultati
### <a name="create-operations"></a>Stvaranje operacija
#### <a name="single-record-create-operations"></a>Operacije stvaranja jednog zapisa
Tablica u nastavku prikazuje vremena izvršenja za stvaranje jednog zapisa. Vremena su navedena u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="2">Vrijeme</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obvezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodjela</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ovisnost</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operacije masovnog stvaranja
Tablica u nastavku prikazuje vremena izvršenja za stvaranje više zapisa. Točnije, Microsoft je izmjerio vrijeme izvršenja za stvaranje 20, 50 i 100 zapisa u jednom uzorku OperationSet. Vremena su navedena u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="6">Vrijeme</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 zapisa</th>
    <th class="tg-0lax" colspan="2">50 zapisa</th>
    <th class="tg-0lax" colspan="2">100 zapisa</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obvezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obvezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obvezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodjela</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ovisnost</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operacije masovnog stvaranja na entitetima **Projekt** i **Član tima** nisu uključeni u ovu tablicu, jer vrijeme izvođenja tih operacija nalikuje vremenu izvođenja kada se API za stvaranje jednog zapisa poziva više puta. Ovi se API-ji pokreću odmah u aplikaciji Dataverse.

Primjer u nastavku prikazuje dijagram vremena izvršenja za entitete **Zadatak**, **Dodjela** i **Ovisnost** kada se stvara 20, 50 i 100 zapisa i upotrebljavaju sva podržana polja.

![Stvorite grafikon vremena izvršenja zapisa.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operacije ažuriranja
#### <a name="single-record-update-operations"></a>Operacije ažuriranja jednog zapisa
Tablica u nastavku prikazuje vremena izvršenja za ažuriranja jednog zapisa. Vremena su navedena u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="2">Vrijeme</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obvezna polja </th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije ažuriranja u entitetima **Dodjele resursa** i **Ovisnost projektnog zadatka** nisu podržane.

#### <a name="bulk-update-operations"></a>Operacije masovnog ažuriranja
Tablica u nastavku prikazuje vremena izvršenja za ažuriranje više zapisa. Točnije, Microsoft je izmjerio vrijeme izvršenja za ažuriranje 20, 50 i 100 zapisa u jednom uzorku OperationSet. Vremena su navedena u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="6">Vrijeme</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 zapisa</th>
    <th class="tg-0lax" colspan="2">50 zapisa</th>
    <th class="tg-0lax" colspan="2">100 zapisa</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obvezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obvezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obvezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije ažuriranja u entitetima **Dodjele resursa** i **Ovisnost projektnog zadatka** nisu podržane.

Primjer u nastavku prikazuje dijagram vremena izvršenja za entitete Zadatak i Član tima kada se ažurira 20, 50 i 100 zapisa i upotrebljavaju sva podržana polja.

![Ažurirajte grafikon vremena izvršenja zapisa.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operacije brisanja
#### <a name="single-record-delete-operations"></a>Operacije brisanja jednog zapisa
Tablica u nastavku prikazuje vremena izvršenja za brisanje jednog zapisa. Vremena su navedena u sekundama.

| Vrsta zapisa | Vrijeme  |
|-------------|-------|
| Zadatak        | 20.12 |
| Dodjela  | 10.86 |
| Član tima | 12.52 |
| Ovisnost  | 20.89 |

> [!NOTE]
> Operacije brisanja u entitetu **Projekt** nisu podržane.

#### <a name="bulk-delete-operations"></a>Operacije masovnog brisanja
Tablica u nastavku prikazuje vremena izvršenja za brisanje više zapisa. Točnije, Microsoft je izmjerio vrijeme izvršenja za brisanje 20, 50 i 100 zapisa u jednom uzorku OperationSet. Vremena su navedena u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="3">Vrijeme</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 zapisa</th>
    <th class="tg-0lax">50 zapisa</th>
    <th class="tg-0lax">100 zapisa</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodjela</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ovisnost</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije brisanja u entitetu **Projekt** nisu podržane.

Primjer u nastavku prikazuje dijagram vremena izvršenja za entitete **Zadatak**, **Dodjela** i **Član tima** i **Ovisnost** kada se briše 20, 50 i 100 zapisa i upotrebljavaju sva podržana polja.

![Izbrišite grafikon vremena izvršenja zapisa.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Zapažanja
Za svaku operaciju snimanja, API-ju **ExecuteOperationSet** potrebno je oko 800 milisekundi za slanje zahtjeva Usluzi planiranja projekta. Usluzi planiranja projekta tada je potrebno oko pet sekundi za obradu podataka i poziv platformi Dataverse. Ostatak vremena izvršenja troši se na izvođenje poslovne logike i upisivanje podataka u bazu podataka platforme Dataverse.

Kada se stvori, ažurira ili obriše 100 zapisa, API-ju **ExecuteOperationSet** potrebno je oko tri sekunde da pošalje zahtjev Usluzi planiranja projekta. Usluzi planiranja projekta tada je potrebno oko pet sekundi za obradu zahtjeva i poziv platformi Dataverse. Masovne operacije jedanput moraju platiti **Porez na uslugu planiranja projekta**, za sve zapise u uzorku OperationSet. Stoga, masovne operacije imaju znatno kraće prosječno vrijeme izvršenja od operacija s jednim zapisom.

## <a name="scenarios"></a>Scenariji
Tablica u nastavku prikazuje vremena izvršenja kada se API-ji rasporeda projekta upotrebljavaju za postizanje određenih scenarija. Vremena su navedena u sekundama.

| Scenarij                                                                   | Vrijeme  |
|----------------------------------------------------------------------------|-------|
| Stvorite projekt koji ima 40 zadataka.                                      | 36.01 |
| Stvorite projekt koji ima 40 zadataka i 20 ovisnosti.                  | 38.11 |
| Stvorite projekt koji ima 40 zadataka i 30 dodjela.                   | 60.17 |
| Stvorite projekt koji ima 40 zadataka, 20 ovisnosti i 30 dodjela. | 60.27 |

## <a name="best-practices"></a>Najbolje prakse
Na temelju rezultata prethodnog scenarija, API-ji bolje rade u sljedećim uvjetima:

  - Grupirajte što više operacija zajedno. Prosječno vrijeme izvođenja masovnih operacije bolje je od prosječnog vremena izvođenja operacija s jednim zapisom. Što je manji broj uzoraka OperationSets u uporabi, prosječno vrijeme izvršenja bit će brže.
  - Postavite samo minimalne atribute koji su potrebni za ostvarenje vašeg scenarija. Budite selektivni u pogledu vrsta neobveznih polja uključenih u zahtjev uzorka OperationSet. Polja koja sadrže strane ključeve ili polja skupne vrijednosti negativno će utjecati na izvedbu.
