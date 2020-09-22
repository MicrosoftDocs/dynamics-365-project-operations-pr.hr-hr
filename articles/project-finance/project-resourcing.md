---
title: Dodjela resursa projektu
description: U ovoj temi nalaze se informacije o dodjeli resursa projektu.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750061"
---
# <a name="project-resourcing"></a>Dodjela resursa projektu

[!include [banner](../includes/banner.md)]

U ovoj temi nalaze se informacije o dodjeli resursa projektu.

Dodjela resursa jedan je od izazova za voditelje projekata i voditelje resursa tijekom faze planiranja projekta, kada oni moraju odrediti i rezervirati ispravan resurs za rad na projektu. Mogućnosti resursa za projekte u aplikaciji Dynamics 365 Finance omogućuju vam definiranje uloga koje se tretiraju kao privremeni resursi koji se mogu rezervirati za određeni angažman ili dio angažmana. Ova vrsta dodijele resursa omogućuje voditeljima projekta i voditeljima resursa izvršenje sljedećih zadataka:

- Definiranje uloge koja ima potrebne kompetencije, tako da je lako podudariti resurse.
- Uporabu uloga za definiranje početnog rasporeda angažmana koji se temelji na rezerviranim resursima.
- Procjenu troškova i određivanje početnog proračuna na temelju dodijeljenih uloga i resursa za projekt.
- Uporabu uloga za procjenu broja rezervacija resursa potrebnih za svaki angažman.
- Procjenu broja resursa potrebnih za ukupni životni ciklus projekta.
- Skicirati strukturnu analizu rada (WBS) s pomoću početnih dodjela resursa.

[![Životni ciklus projekta](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Kako se planiranje projekta odvija, planirani resursi mogu se zamijeniti resursima osoblja. Voditelj projekta može se i vratiti te ažurirati rezervacije za dodjelu resursa tijekom bilo koje faze projekta.

## <a name="set-up-project-resources"></a>Postavljanje resursa projekta
Morate postaviti kalendar i povezati ga sa zaposlenikom ili radnikom. Kalendar se upotrebljava za planiranje projekta i radnog vremena resursa rezerviranih za projekt. Tijekom postavljanja kalendara, voditelji projekata mogu izvršiti ujednačavanje resursa kao dio optimizacije resursa. Na temelju kalendarskog rasporeda na resurse se mogu staviti ograničenja. Kalendar možete postaviti na stranicu **Kalendari**.

Kada radnika postavite kao resurs projekta, možete birati između radnika koji rade u tvrtki za koju postavljate resurse. Možete odabrati i radnike iz drugih tvrtki unutar svoje tvrtke ili ustanove. Ti su radnici poznati kao resursi unutar tvrtke.

U slijedećim se postupcima objašnjava način za postavljanje radnika kao resursa projekta u vašoj tvrtki i način za postavljanje resursa unutar tvrtke za projekt.

### <a name="set-up-a-worker-as-a-project-resource"></a>Postavljanje radnika kao resursa projekta

1. Na stranici **Radnici**, na popisu **Radnici**, odaberite radnika kojeg dodajete kao resurs projekta i otvorite zapis za radnika.
2. U oknu radnji odaberite **Projekt** &gt; **Postavljanje** &gt; **Postavljanje projekta**.
3. Odaberite kalendar, a zatim zatvorite stranicu.

Također možete odrediti zadane projekte za resurs kao vrstu prethodne dodjele. Prethodne dodjele mogu se upotrebljavati kada voditelj resursa ili voditelj projekata unaprijed zna na kojim će projektima resurs raditi. Prethodne dodjele također se mogu temeljiti na zahtjevu sponzora projekta ili klijenta. Kako biste unaprijed dodijelili projekt, odaberite odgovarajući projekt na stranici **Dodijeli projekte**, na kartici **Projekti** s popisa **Preostali projekti**.

### <a name="set-up-an-intercompany-resource"></a>Postavljanje resursa unutar tvrtke

Kada radnika postavite kao resurs unutar tvrtke, morate dovršiti postavljanje i u tvrtki davateljici posudbe i u tvrtki primateljici posudbe.

**U tvrtki davateljici posudbe**

1. U Financijama provjerite je li odabrana tvrtka davateljica posudbe, a zatim dovršite postupak iz prethodnog odjeljka „Postavljanje radnika kao resursa projekta”.
2. Na stranici **Računovodstvo unutar tvrtke** odaberite mogućnost **Novo**.
3. U polju **ID pravne osobe**, odaberite tvrtku davateljicu posudbe. Prema potrebi popunite preostala polja, a zatim odaberite **Spremi**.
4. Na stranici **Cijena prijenosa** odaberite **Novo**.
5. U polju **Pravna osoba koja prima posudbu** odaberite odgovarajuću tvrtku.
6. Kako biste posudili tvrtki primateljici posudbe samo one resurse koje ste stvorili na početku ovog odjeljka u polju **Resurs**, odaberite naziv resursa koji ste stvorili. Kako biste tvrtki primateljici posudbe omogućili sve resurse tvrtke davateljice posudbe, polje **Resurs** ostavite prazno.
7. Na stranici **Parametri upravljanja projektom i računovodstveni parametri**, na kartici **Unutar tvrtke**, postavite mogućnost **Omogući raspoređivanje resursa i evidencija radnog vremena unutar tvrtke** na **Da**.

**U tvrtki primateljici posudbe**

- U filtar za pretraživanje na stranici **Popis resursa** unesite naziv resursa koji ste stvorili za tvrtku primateljicu posudbe kako biste provjerili je li ime uključeno u popis resursa za tvrtku primateljicu posudbe.

## <a name="manage-resource-competencies"></a>Upravljanje kompetencijama resursa
Kompetencije resursa bitan su dio upravljanja resursima. Kompetencije se mogu upotrebljavati kao polazna osnova za određivanje resursa koji imaju pravu ravnotežu vještina, obrazovanja, ovlaštenja i projektnog iskustva. Te biste podatke trebali postaviti za svaki resurs i redovito ih ažurirati. Na taj način možete maksimizirati mogućnosti kada se odgovarajuće kompetencije resursa podudare tijekom dodjele resursa projekta.

[![Primjeri vještina, ovlaštenja, obrazovanja i projektnog iskustva](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

U slijedećim se postupcima objašnjava način postavljanja neke kompetencije za resurs.

Kako biste postavili kompetencije za radnika, možete upotrijebiti bilo stranicu s popisom **Radnici** u Ljudskim resursima ili stranicu s popisom **Resursi** u Upravljanju projektima i računovodstvu. Za sljedeće postupke upotrebljava se stranica s popisom **Radnici** u Ljudskim resursima.

### <a name="set-up-competencies-certificates"></a>Postavljanje kompetencija: Certifikati

1. Na stranici s popisom **Radnici** odaberite redak za radnika za kojeg želite dodati podatke o certifikatu.
2. U Oknu radnji na kartici **Radnik**, u grupi **Kompetencije**, kliknite mogućnost **Certifikati**.
3. Odaberite **Novo** i zatim u polju **Vrsta certifikata** odaberite **PMP**.
4. U polju **Datum početka** odaberite **1.10.2015.** i odaberite **Spremi**.

### <a name="set-up-competencies-skills"></a>Postavljanje kompetencija: Vještine

1. Na stranici s popisom **Radnici** provjerite je li radnik kojeg ste upotrebljavali u prethodnom postupku i dalje odabran. Zatim u Oknu radnji na kartici **Radnik**, u grupi **Kompetencije**, kliknite mogućnost **Vještine**.
2. Odaberite **Novo**.
3. U polju **Vještina** odaberite **Upravljanje projektom**.
4. U polju **Razina** odaberite **5 Stručnjak**.
5. U polju **Datum razine** odaberite **1.14.2014.**.
6. U polje **Godine iskustva** unesite **10**.
7. Odaberite **Spremi** i zatvorite stranicu.

## <a name="create-a-new-project"></a>Stvaranje novog projekta
1. Na stranici **Upravljanje projektom** odaberite **Novi projekt** i unesite sljedeće vrijednosti:

    - **Vrsta projekta:** Vrijeme i materijal
    - **Naziv projekta:** XYZ nadogradnja 2. faze
    - **Grupa projekata:** TM\_WIP
    - **ID ugovora projekta:** 00000002

2. Odaberite **Stvori projekt**.

### <a name="assign-a-resource-to-a-project"></a>Dodjela resursa projektu

1. Na stranici **Radnici**, na popisu **Radnici**, odaberite zapis za radnika za kojeg ste prethodno postavili kompetencije i otvorite zapis za radnika.
2. U Oknu radnji na kartici **Projekt** u grupi **Postavljanje**, kliknite mogućnost **Dodjeli projekte**.
3. Na stranici **Projektni zadaci za provjeru valjanosti resursa**, na kartici **Projekti** u polju **Dodajte projekt odabranim projektima**, filtrirajte na projekt **XYZ nadogradnja 2. faze**.
4. U oknu **Preostali projekti** odaberite projekt, a zatim odaberite gumb sa strelicom kako biste ga dodali u okno **Odabrani projekti**.

Prema potrebi možete dodijeliti i kategorije za resurs. Ta je vrsta kategorije ili **Trošak** ili **Prihod**. Vrstu kategorije određuje vaša tvrtka ili ustanova. Ako za resurs nisu dodijeljene kategorije, Financije pretražuju zadanu kategoriju cijena radnih sati za trošak i prihod.

### <a name="set-up-project-resource-and-role-characteristics"></a>Postavljanje svojstava resursa i uloga za projekt

Voditelj projekta može upotrijebiti funkcionalnost projektnih resursa za stvaranje uloga potrebnih za projekt. Uloge se mogu upotrebljavati ako su potvrđeni resursi i dalje nepoznati u vrijeme rezerviranja resursa. Uloge se mogu privremeno rezervirati kao planirani resursi, tako da možete nastaviti faze planiranja projekta.

[![Primjer uloge](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarij:** Contoso je angažiran da dovrši projekt Vrijeme i materijal koji ima odobren ugovor o projektu. Voditelj projekta nižeg ranga još uvijek dovršava djelokrug projekta. Voditelj resursa trenutačno identificira određene resurse koji će se rezervirati za rad na novom projektu. Zbog kritične naravi projekta, sponzor projekta zatražio je ulogu voditelja projekta višeg ranga kao jednu od uloga. Voditelj resursa mora nabaviti novi resurs i definirati ulogu u sustavu u slučaju da voditelj projekta nižeg ranga tijekom planiranja projekta zatraži podatke o resursima.

U sljedećim koracima pokazan je način na koji upravitelj resursa može postaviti ulogu voditelja projekta višeg ranga i s njom povezati svojstva resursa. Kasnije se uloga može upotrijebiti za traženje dostupnih resursa koji se podudaraju s potrebnim kompetencijama resursa.

1. Na stranici **Postavljanje uloga** odaberite **Novo** i unesite sljedeće vrijednosti:

    - **ID uloge:** Voditelj projekta višeg ranga
    - **ID uloge:** Voditelj projekta višeg ranga

2. Kliknite **Stvori**.
3. Odaberite ulogu **Voditelj projekta višeg ranga**, a zatim odaberite **Konfiguriraj svojstva**.
4. U polju **Vrste svojstava** odaberite **Vještina**.
5. U polju **Dostupna svojstva** unesite vještinu koja se traži.
6. U polju **Vrsta svojstva** odaberite **Certifikat**.
7. U polju **Dostupna svojstva** unesite vrstu certifikata koja se traži.

### <a name="assign-a-project-resource-to-a-project"></a>Dodjela projektu odgovarajućih resursa

1. Na stranici **Svi projekti** odaberite projekt **XYZ nadogradnja 2. faze**.
2. Na kartici **Projektni tim i planiranje** odaberite **Dodaj**.
3. U polju **Uloga** odaberite **Član tima**.
4. Odaberite **Rezerviraj iz kalendara**.
5. Na stranici **Dostupnost resursa** odaberite **Prikaz postavki**.
6. Na stranici **Prilagodi postavke prikaza** unesite sljedeće vrijednosti:

    - **Oblik prikaza raspona datuma:** Dan
    - **Prikaži dostupne opise:** Da
    - **Prikaži preostali kapacitet:** Da

7. S popisa resursa odaberite resurs.
8. Odaberite **Fiksna rezervacija** i **Puni kapacitet**.


### <a name="assign-a-resource-to-a-default-role"></a>Dodjela resursa zadanoj ulozi

Kako bi se pomoglo upraviteljima projekata ili resursa, mogu vršiti pretraživanje kroz razine naniže na resursima koji se mogu rezervirati za projekt. Zadanu ulogu možete povezati s postojećim ili novostečenim resursom. Primjerice, kad je Daniel zaposlen, imao je iskustva i vještine da ispuni ulogu poslovnog analitičara. Voditelj resursa dodijelio je ovu ulogu Danielu kao zadanu ulogu. Stoga je voditelj resursa dodao Daniela u skup poslovnih analitičara koji su dostupni za rad na projektima.

Tijekom rezervacije resursa, voditelji projekata mogu filtrirati uloge resursa koje su dostupne za rad na projektima. Te podatke mogu upotrebljavati kao jedan kriterij kada provode višekriterijsku analizu odluka tijekom realizacije resursa. U filtar mogu dodati i druga svojstva resursa za traženje resursa koji imaju određene vještine, obrazovanje i iskustvo za dani projekt.

**Scenarij:** Odobreni je projekt započeo, a uloga voditelja projekta višeg ranga rezervirana je tijekom faze planiranja projekta kao planirani resurs. Upravitelj resursa sada je nabavio resurs za ispunjavanje uloge voditelja projekta višeg ranga.

1. Na stranici **Popis resursa** odaberite **Daniel Petek**.
2. Na stranici **Uloga za resurs** odaberite **Novo** i unesite sljedeće vrijednosti:

    - **Na snazi:** Unesite trenutačni datum.
    - **Istek:** Unesite **Nikada**.
    - **Uloga:** Unesite **Voditelj projekta višeg ranga**.

3. Odaberite **Spremi** i zatvorite stranicu.
4. Na kartici **Kompetencije** dodajte vještinu **ProjectMgmt** i certifikat **PMP**.

## <a name="set-up-role-based-pricing"></a>Postavljanje cijene zasnovane na ulogama
Za uloge se mogu postaviti sve cijene troška, prodaje i prijenosa.

1. Na stranici **Prodajna cijena (sat)** odaberite **Novo** i unesite datum stupanja na snagu.
2. U stupcu **Uloga** odaberite ulogu.
3. U stupcu **Određivanje cijena** unesite cijenu za odabranu ulogu resursa.

## <a name="form-a-project-team"></a>Formiranje projektnog tima
Kako bi se upotrebljavale uloge koje su prethodno postavljene u projektu, voditelj projekta mora povezati uloge s projektom. Za projekt se može dodijeliti više uloga. Kako bi se spriječila zabuna, ove se uloge automatski označavaju tijekom rezervacije. Na primjer, ako voditelj projekta zahtijeva tri softverska inženjera, oznake tri uloge softverskog inženjera **softverski inženjer 1**, **softverski inženjer 2** i **softverski inženjer 3** automatski se generiraju. Ako su svojstva uloge prethodno postavljena za ulogu, ona se primjenjuju kao filtar tijekom pretraživanja resursa. Dodatna svojstva mogu se prema potrebi dodati za daljnje sužavanje pretraživanja.

Postavke prikaza također se mogu prilagoditi kako bi pružile bolji prikaz dostupnosti resursa. Postoje mogućnosti prikazivanja dostupnosti po satu, dnevno, tjedno, mjesečno, tromjesečno i godišnje. Također postoji mogućnost prikaza dostupnog i preostalog kapaciteta na resursima. Ova je mogućnost korisna za upravljanje vremenom kada procjenjujete dostupno vrijeme za aktivnosti ili dostupnost resursa.

Voditelj projekta može odabrati ulogu na stranici, a zatim, ako postoji dostupan resurs koji udovoljava zahtjevu, odabrati resurs kako bi ga rezervirao za popunjavanje uloge. Imajte na umu kako resurse u fazi planiranja u ovom trenutku nije potrebno rezervirati. Kada stvarate WBS uloge možete zamijeniti resursima osoblja za projekt. Ako se uloge u WBS-u zamijene resursima s osobljem, postavka resursa automatski ažurira popis i raspored projektnog tima.

[![Popis projektnog tima koji uključuje i uloge i stvarne resurse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Voditelj projekta ima razne mogućnosti za rezerviranje resursa za projekt, kao što su **Preostali kapacitet**, **Puni kapacitet**, **Postotak kapaciteta** i **Navođenje sati rada**. Ove mogućnosti rezervacije mogu se otkazati u bilo kojem trenutku ako se zadaci resursa promijene. Podržane su dvije vrste rezervacija:

- **Fiksna rezervacija** – Rezervacija resursa je odobrena i potvrđena za rad s određenim vremenom angažmana.
- **Uvjetna rezervacija** – Rezervacija resursa uvjetno je potvrđena za rad s određenim vremenom angažmana.

U sljedećem postupku objašnjava se način stvaranja projektnog tima.

### <a name="create-a-project-team"></a>Stvaranje projektnog tima

1. Na stranici s popisom **Svi projekti** odaberite projekt, a zatim odaberite **Uredi**.
2. Na kartici **Projektni tim i planiranje** u polju **Planiraj datum završetka** unesite datum koji nastupa mjesec dana nakon datuma početka rasporeda. Na primjer, ako je datum početka rasporeda 24. lipnja 2017. (24.6.2017.), unesite **24.07.2017.**.
3. Odaberite **Dodaj**.
4. U oknu **Dodaj uloge projektu** u polju **Uloga**, odaberite **Voditelj projekta višeg ranga**.
5. Odaberite **Potrebne kompetencije**.
6. Svojstva koja ste prethodno postavili za ulogu voditelja projekta višeg ranga , na stranici **Odaberi svojstva** odabiru se prema zadanim postavkama. Odaberite **U redu**.
7. Na stranici **Dodaj uloge projektu** u polje **Broj resursa** unesite **1**.
8. U polju **Resurs** pretraživanje prikazuje sve resurse koji imaju potrebne kompetencije. Odaberite **Daniel Petek**, a zatim odaberite **Stvori**.
9. Na stranici **Projekt** odaberite **Dodaj**.
10. U oknu **Dodaj uloge projektu** u polju **Uloga**, odaberite **Član tima**. U polje **Broj resursa** unesite **5**.
11. Kliknite **Stvori**.
12. Na stranici **Projekti** odaberite **Popuni resurs**.

## <a name="resource-capacity-synchronization"></a>Sinkronizacija kapaciteta resursa
Postupci sinkronizacije resursa pomažu kako bi se zajamčilo da se informacije za kalendar i osnovni kalendar slijevaju u planiranje resursa projekta. Ako se kalendar promijeni, postupci izvršavaju potrebna ažuriranja u planiranju projektnih resursa. Postupci također pomažu pri poboljšanju izvedbe jer se podaci o resursima kalendara unaprijed sinkroniziraju. Stoga se ažuriranja podataka o rasporedu resursa događaju brže. Preporučujemo da postupke planirate kao skupne, umjesto jednog po jednog. U suprotnom postoji opasnost da će netko zaboraviti uključene datume nakon posljednjeg sinkroniziranja podataka. Ako se ne upotrebljavaju uključeni datumi, može doći do praznina tijekom sinkronizacije datuma.

![Sinkronizacijski kalendara](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sinkronizacija skupnih vrijednosti kapaciteta resursa

Postupak sinkronizacije osmišljen je za sinkronizaciju svih podataka kalendara resursa. Te informacije uključuju osnovne podatke kalendara o svim promjenama u tablici kapaciteta kalendara resursa projekta. Ako se u projekt dodaju novi resursi, sinkronizacija pomaže zajamčiti dostupnost ažuriranih podataka kalendara. Ova se sinkronizacija može izvršiti u bilo kojem trenutku.

Preporučujemo da upotrijebite skupinu. Tijekom sinkronizacije rezervacija kapaciteta dostupne su mogućnosti.

1. Odaberite **Upravljanje projektima i računovodstvo** &gt; **Povremeno** &gt; **Sinkronizacija kapaciteta** &gt; **Sinkroniziraj skupnih vrijednosti kapaciteta resursa**.
2. Postavite mogućnosti u sljedeću tablicu.

    | Mogućnost      | Opis |
    |-------------|-------------|
    | Šifra razdoblja | Po želji odaberite šifru intervala datuma glavne knjige kako biste postavili datume početka i završetka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa. |
    | Datum početka  | Unesite datum početka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa. |
    | Datum završetka    | Unesite datum završetka postupka sinkronizacije skupnih vrijednosti kapaciteta resursa. |

[![Postupak sinkronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Postavljanje uloga na WBS predloške
Voditelji projekata mogu postaviti WBS predloške koje mogu primijeniti kada kreiraju WBS za nove projekte. Kada stvaraju predložak voditelji projekata mogu dodati uloge. Upotrijebite sljedeći postupak za dodjeljivanje uloge WBS predlošku.

1. Odaberite **Upravljanje projektima i računovodstvo** &gt; **Postavke** &gt; **Projekti** &gt; **Predlošci strukturne analize rada**.
2. Odaberite **Pojedinosti** za odabrani WBS predložak.
3. Na popisu odaberite zadatak, a zatim u polju **Uloga**, odaberite ulogu koju ćete dodijeliti zadatku.

### <a name="work-with-a-wbs"></a>Rad s WBS-om

Možete stvoriti novi WBS ili ga kopirati iz postojećeg WBS predloška. Voditelj projekta može lako upravljati resursima dodjeljivanjem uloga novim zadacima na WBS-u. Uloge se mogu zamijeniti, ili nakon stjecanja resursa ili nakon identificiranja potvrđenog resursa za rad na zadatku. Ova fleksibilnost omogućuje voditeljima projekata izvršavanje sljedećih zadataka:

- Određivanje broja resursa potrebnih za radne pakete WBS-a.
- Procjenu troškova projekta.
- Određivanje pripremnog proračuna.
- Procjenu trajanja aktivnosti na temelju uloga i resursa.
- Razvijanje nekih planova upravljanja projektom na temelju dostupnih informacija o projektu.

Dodatne mogućnosti dodane su u WBS radi bolje uporabe funkcionalnosti resursa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mogućnost</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dodjele resursa</td>
<td>Pregledajte dodijeljene resurse, datume, broj radnih sati i vrstu rezervacije za zadatke na WBS-u.</td>
</tr>
<tr class="even">
<td>Automatsko generiranje tima</td>
<td>Automatski dodajte planirane resurse s pomoću uloga povezanih sa zadatkom. Financije automatski predlažu planirane resurse s pomoću višekriterijske analize odluke koja se temelji na ulogama. Nakon što su uloge i rad (sati) postavljeni za zadatke u WBS-u i nakon što je objavljena struktura, odaberite mogućnost <strong>Automatski generiraj tim</strong>. Potreban broj planiranih resursa dodaje se WBS-u i kartici <strong>Planiranje projekata i tima</strong>.</td>
</tr>
<tr class="odd">
<td>Resurs (padajući popis)</td>
<td>Na stranici <strong>Pokretanje dodjele resursa</strong> možete odabrati resurse za fiksnu ili uvjetnu rezervaciju na temelju određenog trajanja. Možete prilagoditi postavke prikaza kako biste vidjeli i postavili trajanje aktivnosti resursa. Možete odabrati i dodijeliti resurse na razini radnog paketa s pomoću sljedećih mogućnosti:
<ul>
<li><strong>Prihvati</strong> – Potvrdite promjene resursa dodijeljenog zadatku.</li>
<li><strong>Odustani</strong> – Odustanite od promjena resursa dodijeljenog zadatku.</li>
<li><strong>Dodijeli automatski</strong> - Dostupni resurs osoblja koji ima podudarnu ulogu automatski se odabire i dodjeljuje odabranom zadatku.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stranici **Svi projekti** odaberite projekt **XYZ nadogradnja 2. faze**.
2. Odaberite **Planiraj** &gt; **Aktivnosti** &gt; **Strukturna analiza rada**.
3. Odaberite **Novo** kako biste WBS-u dodali sljedeće aktivnosti prve razine:

    - Pokretanje
    - Planiranje
    - Izvršavanje
    - Upravljanje i nadzor
    - Zatvaranje

4. Postavite datume i rad (sate) na način prikazan na sljedećoj slici.

    [![Postavljanje datuma i rada](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Odaberite redak zadatka **Pokretanje**, a zatim u polju **Uloga** odaberite **Voditelj projekta višeg ranga**.
6. Odaberite **Objavi**.
7. U istom retku, u polju **Resurs** odaberite **Daniel Petek**, a zatim odaberite **Prihvati**.
8. Odaberite redak zadatka **Planiranje**, a zatim u polju **Uloga** odaberite **Poslovni analitičar**.
9. Odaberite **Objavi**, a zatim odaberite **Automatski generiraj tim**.
10. U okviru poruke koji se prikazuje odaberite **Da**.
11. U polju **Resurs** provjerite postoji li vrijednost **Poslovni analitičar 1**.
12. Za resurs **Poslovni analitičar 1**, otvorite pretragu i odaberite **Pokreni dodjele resursa**. Zatim odaberite radnika za zadatak.
13. Odaberite **Uvjetna dodjela** &gt; **Puni kapacitet**.

    > [!NOTE] 
    > Nećete dobiti upozorenje da je navedeni resurs sada 2, jer broj resursa ostaje 1.

14. Na stranici **Strukturna analiza rada** potvrdite dodjelu resursa na WBS-u, a zatim odaberite **Spremi**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ispunjenje resursa za planirane resurse
Voditelj projekta može planirati potrebne uloge resursa za projekt. Voditelj resursa vidjet će ove planirane resurse kao zahtjeve na stranici **Ispunjenje resursa** i može dodijeliti stvarne resurse.

1. Na stranici **Svi projekti** odaberite projekt **XYZ nadogradnja 2. faze**.
2. Odaberite **Projekt** i zatim odaberite **Uredi**.
3. Na kartici **Projektni tim i planiranje** odaberite **Dodaj**.
4. U dijaloškom okviru **Dodaj uloge** odaberite ulogu **Razvojni inženjer softvera**.
5. Odaberite **Stvori** i zatvorite stranicu projekta.
6. Na stranici **Ispunjenje resursa** odaberite **Razvojni inženjer softvera 1** za projekt **2. faza nadogradnje projekta XYZ**.
7. Odaberite radnika, a zatim odaberite **Dodijeli**.
8. Provjerite je li redak za **Razvojni inženjer softvera 1** uklonjen za projekt **2. faza nadogradnje projekta**.
9. Na kartici **Projektni tim i planiranje** za projekt **2. faza nadogradnje XYZ**, provjerite je li radnik kojeg ste odabrali u prethodnom koraku dodan kao **Razvojni inženjer softvera**.

## <a name="requests-for-project-resources"></a>Zahtjevi za resurse projekta
Funkcionalnost za planiranje resursa projekata omogućuju voditeljima resursa samo da raspoređuju resurse osoblja na angažmanima ili projektima. Kako biste omogućili ovu funkciju, dovršite sljedeće zadatke ili provjerite jesu li dovršeni:

- Postavite nizove brojeva.
- Postavite tijekove upravljanja projektima i računovodstva.
- Omogućite tijekove zahtjeva za resursima.

Nakon dovršenja prethodnih zadataka, prema potrebi možete izvršiti sljedeće zadatke:

- Izraditi zahtjev za resursom iz uvjetnog resursa osoblja.
- Nadzirati zahtjeve za resursom.
- Ispuniti zahtjev za resurse.
- Zatražiti resurs osoblja iz WBS-a.
- Rezervirajte resurse za projekt bez zahtjeva za resursom osoblja.

## <a name="monitor-project-teams"></a>Nadzirite projektne timove
1. Na stranici **Svi projekti** odaberite vezu **Projekt ID** za projekt **2. faza nadogradnje XYZ**.
2. Na Brzoj kartici **Projektni tim i planiranje** provjerite jesu li navedeni resursi projekta točni.
