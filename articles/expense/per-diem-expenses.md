---
title: Troškovi dnevnice
description: Ovaj tema pruža informacije o tome kako raditi s troškovima dnevnica.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596041"
---
# <a name="per-diem-expenses"></a>Troškovi dnevnice

> [!IMPORTANT] 
> Funkcionalnost opisana u ovom tema dostupna je ciljanim korisnicima kao dio izdanja pretpregleda.

Isplata dnevnica fiksna je, unaprijed određena dnevnica koju tvrtka isplaćuje svojim zaposlenicima za smještaj (hotele), obroke i slučajne troškove koje ti zaposlenici snose dok putuju na posao. Tvrtka isplaćuje ovu naknadu zaposlenicima umjesto da plaća stvarne putne troškove. Zaposlenici mogu koristiti svoju **naknadu za incidente / ostale** dnevnice za pokrivanje napojnica, posluga u sobu, pranja rublja ili usluga kemijskog čišćenja za važne poslovne sastanke. Stopa dnevnica može varirati, ovisno o tome hoće li poslodavac odlučiti nadoknaditi kombinirane troškove smještaja i obroka ili samo za troškove obroka i nezgoda.

Cijene dnevnica mogu se temeljiti na dobu godine, mjestu putovanja ili oboje. Kada stvorite pravilo dnevnice, možete odrediti da će postotak stope dnevnica biti zadržan ako zaposlenik primi besplatne obroke ili usluge. Također možete postaviti minimalni broj sati i maksimalan broj sati koje stopa dnevnica može primijeniti na putovanje zaposlenika.

Dnevnica se izračunava kao ukupna naknada koja se nudi dnevno umanjena za smanjenje obroka (trošak besplatnih obroka) koja se daje zaposleniku.

## <a name="configure-per-diems"></a>Konfiguriraj dnevnice

Da biste konfigurirali troškove dnevnice, slijedite ove korake.

1. Otvorite Parametri **upravljanja općim** \> **troškovima postave** \> **upravljanja** \> **troškovima.**
2. Na kartici **Dnevnica** u **polju Izračunaj smanjenje obroka po** poljima odaberite način izračuna dnevnica:

    - **Vrsta obroka po putovanju** - Izračunajte dnevnice na temelju vrste obroka koji se unosi (doručak, ručak ili večera) i na smanjenju obroka koje je navedeno za svaku vrstu obroka za dnevnice za vrijeme trajanja putovanja.
    - **Vrsta obroka po danu** - Izračunajte dnevnicu na temelju vrste obroka koji se unosi i smanjenja obroka koje je navedeno za svaku vrstu obroka za dnevnice dnevno.
    - **Broj obroka dnevno** – Izračunajte dnevnicu na temelju broja obroka koji se unose dnevno i smanjenja obroka za broj obroka koji se pružaju svaki dan.

3. Otvorite **Izračuni postave** \> **upravljanja troškovima** \> **i šifre** \> **Lokacije dnevnica.**
4. Dodajte mjesta na kojima se mogu koristiti dnevnice.
5. Za svaku lokaciju koju dodate **na** kartici Dnevnice odaberite stopu dnevnica i valutu koja vrijedi između određenih datuma početka i završetka smještaja, obroka i drugih troškova. Da biste konfigurirali stope dnevnica i valute, idite na **Izračuni postave** \> **upravljanja** \> **troškovima i šifre** \> **Dnevnice.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dnevnice u ponovno osmišljenom sučelju troškova

Značajka dnevnica podržana je u ponovno osmišljenom radnom prostoru upravljanja **troškovima** u Microsoft Dynamics 365 Finance verziji 10.0.25 i novijoj.

Da biste omogućili dnevnice, slijedite ove korake.

1. **U radnom prostoru za upravljanje** značajkama pronađite i odaberite **značajku Ponovno osmišljena** izvješća o troškovima na popisu, a zatim odaberite **Omogući odmah**.
2. Pronađite i odaberite značajku ponovno zamišljenog **sučelja** za izvješće o troškovima na popisu, a zatim odaberite **Omogući sada**.

## <a name="how-the-feature-works"></a>Kako značajka funkcionira

Ovaj odjeljak sadrži primjere za tri scenarija konfiguracije. Za svaki primjer polje **Izračunaj smanjenje obroka po postavljeno** je na drugu vrijednost. Za sva tri primjera, ukupan iznos koji se plaća je isti dok se ne primijeni smanjenje obroka. Nakon tog trenutka, ukupni iznos koji se plaća razlikuje se za svaki primjer.

Da biste stvorili trošak dnevnice koji se koristi za sva tri primjera, slijedite ove korake.

1. Otvorite Upravljanje **troškovima** radnih \>**prostora**.
2. Odaberite **Novo izvješće o troškovima** ili odaberite postojeće izvješće o troškovima.
3. Dodajte novi trošak. **U polju Kategorija** odaberite **Dnevnica**. Odaberite lokaciju te datume početka i završetka putovanja. Dnevnica za smještaj, obroke i slučajne troškove (ostali troškovi) izračunava se na temelju dnevne naknade koja je određena za odabranu lokaciju.

    Na primjer, kao lokaciju odabirete **Redmond (SAD**). Dnevnica za tu lokaciju iznosi 150 američkih dolara (150 USD) za smještaj, USD 75 za obroke i USD 5 za incidente. Datum početka je 10. siječnja, a datum završetka je 14. siječnja. Stoga je odabrano trajanje pet dana kada je odabrana konfiguracija kalendarski dani s vremenom, a odabrano vrijeme počinje i završava u 12:00 sati na datume početka i završetka. Evo izračuna:

    - Ukupan iznos koji se plaća = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Obrok i slučajni dio ukupnog iznosa = 5 × (75 + 5) = USD 400

Ako su tijekom putovanja osigurani doručak, ručak i večera, ti se obroci moraju uzeti u obzir kao smanjenje obroka.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Primjer 1: Dnevnica u kojoj se smanjenje obroka temelji na vrsti obroka po putovanju

U ovom primjeru smanjenje obroka je 30 posto za doručak, 30 posto za ručak i 40 posto za večeru. **Na stranici Parametri upravljanja troškovima** polje **Izračunaj smanjenje obroka po** poljem postavljeno je na **Vrsta obroka po putovanju**. Evo izračuna ako su zaposleniku osigurana tri doručka, dva ručka i nula večera:

- Redukcija obroka = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Obroci i incidenti = 400 – 112,50 = USD 287.50
- Ukupan iznos koji se plaća = Ukupna naknada – Smanjenje obroka = 1.150 – 112,50 = USD 1,037.50

![Trošak dnevnice gdje se smanjenje obroka temelji na vrsti obroka po putovanju.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Primjer 2: Dnevnica u kojoj se smanjenje obroka temelji na vrsti obroka dnevno

U ovom primjeru smanjenje obroka je 30 posto za doručak, 30 posto za ručak i 40 posto za večeru. Na stranici **Parametri upravljanja troškovima** polje Izračunaj smanjenje obroka po postavljeno **je na** Vrsta obroka po danu **.** U tom slučaju u **rešetki Obroci** u **dijaloškom okviru Uređivanje troškova** poništite potvrdne okvire kako biste naznačili koji su vam obroci dostavljeni tijekom putovanja.

Na primjer, evo izračuna ako je doručak bio osiguran za prva tri dana putovanja:

- Dnevno smanjenje obroka za svaki od prva tri dana = 75 × 30% = USD 22.50
- Ukupno smanjenje obroka = 3 × 22,50 = USD 67.50
- Obroci i incidenti za dane od 1 do 3 = 75 – 22,50 = USD 57.50
- Ukupni obroci i incidenti = Zbroj obroka i incidenata tijekom pet dana = 400 – 67,50 = USD 332.50
- Ukupan iznos koji se plaća = Ukupni iznos – Smanjenje obroka = 1.150 – 67,50 = USD 1,082.50

![Trošak dnevnice gdje se smanjenje obroka temelji na vrsti obroka dnevno.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Primjer 3:Dnevnica u kojoj se smanjenje obroka temelji na broju obroka dnevno

U ovom se primjeru smanjenje obroka izračunava na temelju broja obroka koji su se pružali dnevno (to jest, **polje Izračunaj smanjenje obroka po** broju na **stranici Parametri upravljanja troškovima** postavljeno je na **Broj obroka dnevno**). U rešetki **Obroci** u **dijaloškom okviru Uređivanje troškova** poništite potvrdne okvire kako biste naznačili koji su obroci osigurani.
U ovom slučaju, sniženje obroka temelji se samo na # dobivenih obroka, a ne na vrsti obroka ( Doručak/ručak/večera) koja se pruža.

Evo izračuna za dnevnice kada se dnevnica USD 150 za smještaj, USD 75 za obroke i USD 5 za slučajne slučajeve:

- **Ukupan iznos koji se** plaća = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Jedan obrok:** Smanjenje obroka = 20% = USD 15
- **Dva obroka:** Smanjenje obroka = 50% = USD 37.50
- **Tri obroka:** Smanjenje obroka = 100% = USD 75

Evo izračuna za naknadu za **obroke i slučajne slučajeve**, koja uključuje USD 5 za slučajne slučajeve:

- 1. dan - Dva obroka = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 2. dan - Dva obroka = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 3. dan - Jedan obrok osiguran = (75 – 15) + 5 = 60 + 5 = USD 65
- 4. dan - Nula obroka = (75-0) + 5 = 75 + 5 = USD 80
- 5. dan - Osigurana tri obroka = (75 – 75) + 5 = 0 + 5 = USD 5

- Ukupni obroci i incidenti = Obroci i incidenti za Dan 1+ Dan 2 +Dan 3+Dan 4+ Dan 5 = USD 235
- Ukupno sniženje obroka = Sniženje obroka za Dan 1+ Dan 2 +Dan 3+Dan 4+ Dan 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Ukupan iznos koji se plaća = Ukupna naknada – Ukupno smanjenje obroka = USD 1,150 - USD 165 = USD 985

![Trošak dnevnice gdje se smanjenje obroka temelji na broju obroka dnevno.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od financijske verzije 10.0.23, ako koristite ponovno osmišljeno sučelje troškova, ne možete stvoriti troškove dnevnica koji imaju datume preklapanja. Ako pokušate, primit ćete poruku o pogrešci.
