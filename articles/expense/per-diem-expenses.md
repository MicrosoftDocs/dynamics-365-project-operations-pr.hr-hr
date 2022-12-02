---
title: Troškovi dnevnice
description: Ovaj članak sadrži informacije o radu s troškovima dnevnice.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923179"
---
# <a name="per-diem-expenses"></a>Troškovi dnevnice

> [!IMPORTANT] 
> Funkcionalnost koja je opisana u ovom članku dostupna je ciljanim korisnicima kao dio izdanja za pretpregled.

Isplaćeni iznos dnevnice fiksna je, unaprijed određena dnevna naknada koju tvrtka isplaćuje svojim zaposlenicima za smještaj (hoteli), obroke i usputne troškove koje ti zaposlenici imaju dok poslovno putuju. Tvrtka isplaćuje tu naknadu zaposlenicima umjesto plaćanja stvarnih putnih troškova. Zaposlenici mogu iskoristiti dnevnice za **usputne/ostale troškove** za pokrivanje napojnica, posluge u sobu, usluge pranja rubnja za važne poslovne sastanke. Iznos dnevnice može se razlikovati, ovisno o tome je li poslodavac odlučio nadoknaditi kombinirani trošak smještaja i obroka ili samo trošak obroka i usputnih troškova.

Cijene dnevnica mogu se temeljiti na dobu godine, mjestu putovanja ili oboje. Kada stvarate pravilo za dnevnice, možete odrediti da se od dnevnice odbija postotak ako zaposlenik prima besplatne obroke ili usluge. Također možete postaviti minimalni broj sati i maksimalni broj sati za koji se dnevnica može primijeniti kada je zaposlenik na putu.

Dnevnica se izračunava kao ukupna naknada koja se nudi po danu umanjena za trošak obroka (trošak besplatnik obroka) koja se daje zaposleniku.

## <a name="configure-per-diems"></a>Konfiguriranje dnevnica

Da biste konfigurirali dnevnice slijedite ove korake.

1. Otvorite **Upravljanje troškovima** \> **Postavljanje** \> **Općenito** \> **Parametri upravljanja troškovima**.
2. Na kartici **Dnevnica**, u polju **Izračunaj smanjenje obroka za** odaberite kako bi se dnevnica trabala izračunati:

    - **Vrsta obroka po putovanju** – izračunavajte dnevnice na temelju vrste obroka koji se unese (doručak, ručak ili večera) i prema umanjenju koje je navedeno za svaku vrstu obroka za iznos dnevnice za trajanje putovanja.
    - **Vrsta obroka po danu** – izračunavajte dnevnice na temelju vrste obroka koji se unese i prema umanjenju koje je navedeno za svaku vrstu obroka za iznos dnevnice po danu.
    - **Broj obroka po danu** – izračunajte dnevnicu na temelju broja obroka koji se unesu po danu i umenjenju obroka za broj obroka koji su osigurani svaki dan.

3. Idite na **Upravljanje troškovima** \> **Postavljanje** \> **Izračuni i šifre** \> **Lokacije za dnevnice**.
4. Dodajte lokacije na kojima se dnevnice mogu iskoristiti.
5. Za svaku lokaciju koju dodate na kartici **Dnevnice** odaberite cijenu dnevnice i valutu koji vrijede između određenog datuma početka i završetka za smještaj, obroke i ostale troškove. Za računanje stope dnevnica i valuta idite na **Upravljanje troškovima** \> **Postavljanje** \> **Izračuni i troškovi** \> **Dnevnice**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dnevnice u izmijenjenom sučelju za troškove

Funkcija dnevnica podržana je u izmijenjenom radnom prostoru **Upravljanje troškovima** u prograu Microsoft Dynamics 365 Finance, verzija 10.0.25 i novije.

Da biste omogućili dnevnice slijedite ove korake.

1. U radnom prostoru **Upravljanje značajkama** pronađite na popisu i odaberite značajku **Izmijenjena izvješća o troškovima**, a zatim odaberite **Omogući sada**.
2. Pronađite na popisu i omogućite značajku **Dnevnice za izmijenjeno sučelje izvješća o troškovima**, a zatim odaberite **Omogući sada**.

## <a name="how-the-feature-works"></a>Kako značajka funkcionira

U ovom su odjeljku navedeni primjeri za tri scenarija konfiguracije. U svakom primjeru polje **Izračunaj smanjenje obroka za** postavljeno je na drugačiju vrijednost. U svakom od tri primjera ukupni iznos za plaćanje jednak je dok se ne primijeni umanjenje obroka. Nakon toga ukupni iznos za plaćanje razlikuje se za svaki primjer.

Za stvaranje troška dnevnice koji je korišten u sva tri primjera pratite ove korake.

1. Idite na **Radni prostori** \> **Upravljanje troškovima**.
2. Odaberite **Novo izvješće o troškovima** ili odaberite postojeće izvješće o troškovima.
3. Dodajte novi trošak. U polju **Kategorija** odaberite **Dnevnica**. Odaberite lokaciju te datume početka i završetka vašeg putovanja. Dnevnice za smještaj, obroke i usputne troškove (druge troškove) računaju se na temelju denvne naknade koja je postavljena za odabranu lokaciju.

    Na primjer, kao lokaciju odaberite **Redmond (SAD)**. Dnevna naknada za tu lokaciju iznosi 150 USD za smještaj, 75 USD za obroke i 5 USD za usputne troškove. Datum početka je 10. siječnja, a datum završetka 14. siječnja. Prema tome odabrano trajanje iznosi pet dana kada odabrana konfiguracija predstavlja kalendarske dane s vremenom, a odabrano vrijeme započinje i završava u 12:00 sati na datume početka i završetka. Ovdje su prikazani izračuni:

    - Ukupni iznos za plaćanje = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
    - Udio obroka i usputni troškova u ukupnom iznosu = 5 × (75 + 5) = 400 USD

Ako su doručak, ručak i večera osigurani tijekom putovanja, ti se obroci moraju obračunati kao umanjenje obroka.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Primjer 1: dnevnica u kojoj se umanjenje obroka temelji na vrsti obroka po putovanju

U ovom primjeru umanjenje obroka iznosi 30% za doručak, 30% za ručak i 40% za večeru. Na stranici **Parametri upravljanja troškovima** polje **Izračunaj smanjenje obroka za** postavljeno je na **Vrsta obroka po putovanju**. Evo izračuna ako su za zaposlenika osigurana tri doručka, dva ručka i nula večera:

- Umanjenje obroka = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22.50) + (2 × 22.50) + 0 = 67.50 + 45 + 0 = 112,50 USD
- Obroci i popratni troškovi = 400 - 112.50 = 287,50 USD
- Ukupni iznos za plaćanje = ukupna naknada - umanjenje obroka = 1150 - 112,50 = 1037,50 USD

![Trošak dnevnice u kojoj se umanjenje obroka temelji na vrsti obroka po putovanju.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Primjer 2: dnevnica u kojoj se umanjenje obroka temelji na vrsti obroka po danu

U ovom primjeru umanjenje obroka iznosi 30% za doručak, 30% za ručak i 40% za večeru. Na stranici **Parametri upravljanja troškovima** polje **Izračunaj smanjenje obroka za** postavljeno je na **Vrsta obroka po danu**. U ovom slučaju u rešetki **Obroci** u dijaloškom okviru **Uredi troškove** izbrisat ćete potvrdne okvire da biste naveli koji su obroci osigurani tijekom putovanja.

Na primjer, ovdje su izračuni za slučaj kada je doručak osiguran za prva tri dana putovanja:

- Dnevno umanjenje obroka za prva tri dana = 75 × 30% = 22,50 USD
- Ukupno umanjenje obroka = 3 × 22,50 = 67,50 USD
- Obroci i popratni troškovi za dane 1 do 3 = 75 - 22,50 = 57,50 USD
- Ukupni obroci i popratni troškovi = zbroj obroka i popratnih troškova tijekom pet dana = 400 - 67,50 = 332,50 USD
- Ukupni iznos za plaćanje = ukupni iznos - umanjenje obroka = 1150 - 67,50 = 1082,50 USD

![Trošak dnevnice u kojoj se umanjenje obroka temelji na vrsti obroka po danu.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Primjer 3: dnevnica u kojoj se umanjenje obroka temelji na broju obroka po danu

U ovom primjeru umanjenje obroka izračunava se na temelju broja obroka koji su osigurani po danu (tj. polje **Izračunaj smanjenje obroka za** na stranici **Parametri upravljanja troškovima** posteljeno je na **Broj obroka po danu**). U rešetki **Obroci** u dijaloškom okviru **Uredi troškove** izbrisat ćete potvrdne okvire da biste naveli koji su obroci osigurani.
U ovom slučaju umanjenje obroka temelji se samo na broju osiguranih obroka, ne na vrsti osiguranog obroka (doručak/ručak/večera).

Ovdje su izračuni za dnevnice kada dnevna naknada iznosi 150 USD za smještaj, 75 USD za oborke i 5 USD za popratne troškove:

- **Ukupni iznos za plaćanje** = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
- **Jedan obrok:** smanjenje obroka = 20% = 15 USD
- **Dva obroka:** smanjenje obroka = 50% = 37,50 USD
- **Tri obroka:** smanjenje obroka = 100% = 75 USD

Ovdje su izračuni za **naknadu za obroke i popratne troškove**, što uključuje iznos od 5 USD za popratne troškove:

- Dan 1 – osigurana dva obroka = (75 - 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dan 2 – osigurana dva obroka = (75 - 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dan 3 – osiguran jedan obrok = (75 - 15) + 5 = 60 + 5 = 65 USD
- Dan 4 – osigurano nula obroka = (75 - 0) + 5 = 75 + 5 = 80 USD
- Dan 5 – osigurana trei obroka = (75 - 75) + 5 = 0 + 5 = 5 USD

- Ukupni obroci i popratni troškovi = obroci i popratni troškovi za Dan 1 + Dan 2 + Dan 3 + Dan 4 + Dan 5 = 235 USD
- Ukupno smanjenje obroka = smanjenje obroka za Dan 1 + Dan 2 + Dan 3 + Dan 4+ Dan 5 = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Ukupni iznos za plaćanje = ukupna naknada - ukupno umanjenje obroka = 1150 USD - 165 USD = 985 USD

![Trošak dnevnice u kojoj se umanjenje obroka temelji na broju obroka po danu.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od verzije Finance 10.0.23 ako koristite novoosmišljeno sučelje za troškove, ne možete stvarati troškove dnevnica koji imaju preklapajuće datume. Ako pokušate, dobit ćete poruku o pogrešci.
