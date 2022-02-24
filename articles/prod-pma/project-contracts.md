---
title: Ugovori o projektu
description: U ovoj temi daju se primjeri ugovora o projektu koje možete stvoriti za razne vrste projekata i izvore financiranja, kao i način na koji možete upravljati ugovorima i fakturirati klijentima projekta.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073519"
---
# <a name="project-contracts"></a>Ugovori o projektu

[!include [banner](../includes/banner.md)]

U ovom članku daju se primjeri ugovora o projektu koje možete stvoriti za razne vrste projekata i izvore financiranja, kao i način na koji možete upravljati ugovorima i fakturirati klijentima projekta.

Vrsta projekta za koji stvarate ugovor o projektu određuje način fakturiranja projekta klijentima. Možete promijeniti ugovor o projektu i povezani projekt, ali ne možete promijeniti vrstu projekta. 

Uporabom ugovora o projektu istodobno možete fakturirati jedan ili više projekata. Ugovor o projektu također pomaže u jamčenju dosljednog postupka fakturiranja za svaki potprojekt u strukturi projekta. 

Svaki projekt koji će se fakturirati mora biti povezan s ugovorom o projektu. Postavke za ugovor o projektu primjenjuju se na sve projekte i potprojekte koji su povezani s tim ugovorom o projektu. 

U ugovoru o projektu može se navesti jedan ili više izvora financiranja. Stoga možete podijeliti naplatu između više davatelja sredstava, postaviti ograničenja financiranja tako da se izvorima financiranja ne naplaćuje više od određenog iznosa i konfigurirati pravila financiranja za naplatu izdataka.

## <a name="funding-for-project-contracts"></a>Financiranje ugovora o projektu
Neki projektni ugovori određuju da više strana dijeli odgovornost za financiranje troškova projekta. Evo nekoliko primjera:

-   Veliki klijent koji ima više sektora zahtijeva da se financiranje projekta podijeli po odjelima.
-   Vaša tvrtka dijeli troškove velikog projekta s vanjskom tvrtkom ili ustanovom.
-   Projekt ceste sufinanciraju dvije općine.
-   Projekt mosta financira se iz državne potpore i privatne korporacije.

U aplikaciji Dynamics 365 Finance možete podijeliti naplatu za jednu transakciju ili cijeli projekt između više klijenata, potpora te tvrtki ili ustanova. 

U projektima koji imaju više davatelja sredstava, sve strane koje pridonose financiranju naprednog projekta financiranja nazivaju se izvorima financiranja. Nakon što se klijent, tvrtka ili ustanova ili potpora definiraju kao izvor financiranja, mogu se dodijeliti jednom ili većem broju pravila financiranja. Pravila financiranja sadrže kriterije koji određuju način na koji se troškovi raspodjeljuju na različite izvore financiranja za projekt. 

Budući da se zalihe stavki, poput onih koje se pojavljuju u zahtjevima za kupnju i narudžbenicama, ne mogu podijeliti, iznos troškova ne može se podijeliti između više izvora financiranja u trenutku raspodjele. Stoga vrijednost izvora financiranja ostaje 0 (nula) dok se ne proknjiži izdavanje zaliha. Kada se proknjiži izdavanje zaliha, iznos troškova raspoređuje se prema pravilima raspodjele računa za projekt.

Evo nekoliko koraka koje možete poduzeti kako biste olakšali podjelu naplate između više izvora financiranja:

-   Navedite da sve transakcije koje se unose za projekt upotrebljavaju istu valutu prodaje kao i ugovor o projektu.
-   Postavite ograničenja financiranja tako da se izvoru financiranja ne fakturira više od određenog iznosa za projekt.
-   Konfigurirajte pravila financiranja i ograničenja financiranja za svakog radnika, stavku, kategoriju, grupu kategorija i vrstu transakcije (ili za sve vrste transakcija).
-   Odaberite neobavezne datume početka i završetka kako biste definirali razdoblje kada vrijedi svako pravilo financiranja.
-   Navedite postotak za koji je odgovoran svaki izvor financiranja.
-   Navedite koji je izvor financiranja odgovoran za zaokruživanje razlika uzrokovanih izračunima raspodjele sredstava.
-   Postavite pravila koja određuju kako se troškovi projekta fakturiraju vanjskim klijentima, a naplaćuju internim tvrtkama ili ustanovama.
-   Zabilježite transakcije na računu zadržanih sredstava dok se ne mogu dobiti dodatna sredstva ili dok ne odlučite snositi troškove interno.

Kako bi se utvrdilo koju poreznu skupinu treba pridružiti transakciji, pretražuje se projekt radi dodjele porezne grupe. Ako na razini projekta nije dodijeljena porezna grupa, pretražuje se ugovor o projektu.

### <a name="example-multiple-funding-sources-simple"></a>Primjer: Više izvora financiranja (jednostavno)

Sljedeća tablica daje scenarije za upravljanje raspodjelom sredstava između više izvora financiranja. Ti se scenariji temelje na sljedećim pretpostavkama:

-   Pri raspodjeli sredstava uzimaju se u obzir prioritetne postavke prije nego što se primijene drugi kriteriji pravila financiranja.
-   Nije naveden raspon datuma koji bi definirao razdoblje kada vrijedi pravilo financiranja.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenarij</strong></td>
<td><strong>Izvor financiranja</strong></td>
<td><strong>Postotak raspodjele</strong></td>
<td><strong>Prioritet raspodjele</strong></td>
</tr>
<tr class="even">
<td>Želite dodijeliti troškove jednom izvoru financiranja dok se njegova sredstva ne iscrpe, dodijeliti troškove drugom izvoru financiranja dok se njegova sredstva ne iscrpe i konačno dodijeliti preostale troškove trećem izvoru financiranja.</td>
<td><ul>
<li>Izvor　financiranja　1</li>
<li>Izvor　financiranja　2</li>
<li>Izvor　financiranja　3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Želite dodijeliti 75 posto troškova jednom izvoru financiranja, a 25 posto drugom izvoru financiranja. Kada se iscrpi bilo koji od tih izvora financiranja, preostale troškove želite platiti iz trećeg izvora financiranja.</td>
<td><ul>
<li>Izvor　financiranja　1</li>
<li>Izvor　financiranja　2</li>
<li>Izvor　financiranja　3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Želite dodijeliti 75 posto troškova jednom izvoru financiranja, a 25 posto drugom izvoru financiranja. Kada se iscrpi bilo koji od tih izvora financiranja, preostale troškove želite podijeliti između trećeg i četvrtog izvora financiranja.</td>
<td><ul>
<li>Izvor　financiranja　1</li>
<li>Izvor　financiranja　2</li>
<li>Izvor　financiranja　3</li>
<li>Izvor　financiranja　4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Želite dodijeliti prvih 25 posto troškova jednom izvoru financiranja, a ostatak drugom izvoru financiranja.</td>
<td><ul>
<li>Izvor　financiranja　1</li>
<li>Izvor　financiranja　2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Primjer: Više izvora financiranja (složeno)

Imate tri izvora financiranja koja želite upotrijebiti sljedećim redoslijedom:

1.  Upotrijebite izvor financiranja 2 i izvor financiranja 3 u jednakoj mjeri dok se izvor financiranja 2 ne iscrpi.
2.  Nastavite upotrebljavati izvor financiranja 3 dok se ne iscrpi.
3.  Upotrijebite izvor financiranja 1 nakon što se izvor financiranja 3 iscrpi.

Kako biste ispunili ovaj cilj, najprije morate učiniti sljedeće:

-   Postavite ograničenja financiranja za izvor financiranja 2 i izvor financiranja 3, za njihove odgovarajuće iznose.
-   Stvorite sljedeća pravila financiranja:
    -   Pravilo 1 (Prioritet 1): 50 posto transakcija dodijelite izvoru financiranja 2, a 50 posto izvoru financiranja 3.
    -   Pravilo 2 (Prioritet 2): Dodijelite 100 posto transakcija izvoru financiranja 3.
    -   Pravilo 3 (Prioritet 3): Dodijelite 100 posto transakcija izvoru financiranja 1.

Ova postavka funkcionira jer se provjeravaju transakcije u odnosu na pravila i ograničenja kako bi se utvrdilo primjenjuju li se neka od njih na transakciju. Ako se na transakciju ne primjenjuju posebna pravila ili ograničenja, primjenjuje se pravilo Sve transakcije. Pravilo Sve transakcije podudara se sa svim transakcijama. 

Ako se pronađe pravilo koje se podudara s transakcijom, najprije se primjenjuje postotak koji je dodijeljen tom pravilu, ali tek nakon što se podudaranja provjere u odnosu na postavljena ograničenja. Ako je dosegnuto ograničenje i ako su iscrpljena sredstva izvora financiranja, pravilo financiranja povezano s ograničenjem financiranja zanemaruje se, a program provjerava sljedeće pravilo koje se primjenjuje. 

U nekim se slučajevima prema pravilu može dodijeliti samo dio transakcije. To se može dogoditi jer je dosegnuto ograničenje kada se dodijelila transakcija. U ovom se slučaju prema tom pravilu dodjeljuje samo određeni iznos, poput 50 posto za svaki izvor financiranja. To je slučaj u pravilu 1, koje je opisano ranije u ovom odjeljku. Ostatak se dodjeljuje prema sljedećem pravilu u nizu. 

U slijedećoj se tablici podrobnije ispituje ovaj scenarij.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Pojedinosti</strong></td>
</tr>
<tr class="even">
<td>Pravila financiranja</td>
<td><ul>
<li>Pravilo 1 (Prioritet 1): Sve transakcije. Dodijelite 50 % izvoru 2 i 50 % izvoru 3.</li>
<li>Pravilo 2 (Prioritet 2): Sve transakcije. Dodijelite 100 % izvoru financiranja 3.</li>
<li>Pravilo 3 (Prioritet 2): Sve transakcije. Dodijelite 100 % izvoru financiranja 1.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ograničenja financiranja</td>
<td><ul>
<li>Ograničenje izvora financiranja 1 = 10.000,00</li>
<li>Ograničenje izvora financiranja 2 = 500,00</li>
<li>Ograničenje izvora financiranja 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakcija 1</td>
<td><strong>Iznos transakcije:</strong> 100,00<strong>Financiranje:</strong> Transakcija se plaća samo prema pravilu 1, jer se transakcija u potpunosti plaća nakon primjene pravila 1. Transakcija se financira jednako između izvora financiranja 2 i 3.
<ul>
<li>Izvor financiranja 2: 50,00</li>
<li>Izvor financiranja 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakcija 2</td>
<td><strong>Iznos transakcije:</strong> 5.000,00<strong>Financiranje:</strong> Transakcija se plaća prema sva tri pravila. <strong>Pravilo 1</strong>
<ul>
<li>Izvor financiranja 2: 450,00</li>
<li>Izvor financiranja 3: 450,00</li>
</ul>
<strong>2. pravilo</strong>
<ul>
<li>Izvor financiranja 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Pravilo 3</strong>
<ul>
<li>Izvor financiranja 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Ukupna sredstva koja se raspodjeljuju za svaki izvor financiranja</td>
<td><ul>
<li>Izvor financiranja 1: 3.850,00</li>
<li>Izvor financiranja 2: 500,00</li>
<li>Izvor financiranja 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Pravila naplate
Kada s klijentom pregovarate o ugovoru o projektu, definirate kako i kada možete klijentu fakturirati za rad na projektu. Nakon što utvrdite ugovor o projektu i projekt, možete postaviti pravila naplate za projekt. Pravila naplate temelje se na uvjetima projekta koji su navedeni u ugovoru o projektu. Pravila naplate koja možete stvoriti ovise o uvjetima ugovora o projektu i vrsti projekta, kao što su Vrijeme i materijal ili Fiksna cijena, koje povezujete s pravilom naplate. Za ugovor o projektu možete stvoriti više pravila za naplatu. Pravilo naplate možete dodijeliti i većem broju projekata koji su povezani s istim ugovorom o projektu i imaju slične uvjete naplate. 

Možete utvrditi sljedeće vrste pravila naplate:

-   **Jedinica isporuke** – Klijentu fakturirajte kada dovršite jedinicu isporuke. Jedinice isporuke definirate u ugovoru.
-   **Napredak** – Klijentu fakturirate kada dovršite određeni postotak projekta. Možete postaviti pravilo naplate na automatski izračun postotka dovršenog posla ili možete ručno izračunati postotak dovršenog posla i iznos za fakturiranje klijentu.
-   **Kontrolna točka** – Klijentu fakturirate puni iznos do kontrolne točke projekta, kada se ona postigne.
-   **Naknada** – Klijentu fakturirate svoje usluge uz naknadu za upravljanje, koja je obično postotak od troška usluge.
-   **Vrijeme i materijal** – Klijentu fakturirate vrijednost vremena i materijala koji su upotrijebljeni na projektu.

Za sve vrste pravila naplate možete odrediti postotak zadržavanja koji se klijentu oduzima od faktura dok projekt ne dosegne dogovorenu fazu. Postotak zadržavanja plaćanja naveden je u ugovoru o projektu. Iznos se izračunava na temelju ukupne vrijednosti redaka na fakturi za klijenta i oduzima se od te vrijednosti. 

Za pravila naplate **Vrijeme i materijal** i **Napredak**, možete dodijeliti naplative kategorije. Naplative kategorije označavaju transakcije koje bi trebale biti uključene u fakture za klijente. 

Kada ste spremni klijentu izdati fakturu, iznos fakture za projekt izračunava se na temelju pravila naplate i generira se prijedlog fakture za projekt. 

U slijedećim odjeljcima daju se primjeri koji pokazuju kako postaviti i upravljati pravilima naplate za projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Primjer: Stvaranje pravila naplate koje se temelji na broju isporučenih jedinica

Vaša tvrtka ili ustanova sklapa ugovor o pružanju ukupno pet treninga zaposlenicima klijenta po cijeni od 10.000 po treningu. Klijentu fakturirate nakon svakog treninga. 

Kada postavljate pravila naplate za ugovor, upotrijebite sljedeće vrijednosti:

-   Jedinica isporuke je jedan trening.
-   Jedinična cijena je 10.000 po treningu.
-   Ukupan broj jedinica je pet treninga.

Kada završite jedan trening, možete stvoriti račun na 10.000 za prvu isporučenu jedinicu i poslati račun klijentu.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Primjer: Stvaranje pravila naplate koje se temelji na određenom postotku završetka projekta (ručni izračun)

Vaša tvrtka ili ustanova, tvrtka za softversko savjetovanje, sklapa ugovor s klijentom o razvoju dijela proizvoda koji klijent razvija. Vaša se tvrtka ili ustanova slaže s isporukom softverskog koda u razdoblju od šest mjeseci. Klijent se slaže da će vašoj tvrtki ili ustanovi platiti ukupno 100.000 za posao. Stvarate pravilo naplate za fakturiranje klijentu na temelju postotka radova koji su dovršeni na projektu, kako je navedeno u ugovoru.

-   Na kraju prvog mjeseca sastajete se s klijentom kako biste utvrdili postotak dovršenog posla. Nakon što s klijentom pregledate projekt, odlučujete kako je dovršeno 15 posto projekta.
-   Stvorite fakturu na 15.000 (15 posto od 100.000) i pošaljite je klijentu.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Primjer: Stvaranje pravila naplate koje se temelji na određenom postotku završetka projekta (automatski izračun)

Vaša tvrtka ili ustanova, tvrtka za razvoj softvera, pristaje razviti paket obračuna plaća za klijenta za iznos od 30.000. Klijent se slaže da će vašoj tvrtki ili ustanovi plaćati na temelju postotka dovršenosti posla. Procjenjujete da troškovi projekta iznose 20.000. Ugovor o projektu navodi kategorije posla koje upotrebljavate u postupku naplate. Postavljate pravila naplate koja automatski izračunavaju iznose računa za postotak dovršenosti posla za svaku kategoriju. Postavljate proračun za svaku kategoriju:

-   **Razvoj** – Trošak od 15.000 i prihod od 20.000
-   **Instalacija** – Trošak od 5.000 i prihod od 10.000

Kada prvi put stvarate fakturu za klijenta, iznos fakture automatski se izračunava na temelju sljedećih podataka:

-   Nakon mjesec dana, radnik na projektu predaje evidenciju radnog vremena za projekt. Trošak sati rada radnika iznosi 5.000 za razvoj i 1.000 za ugradnju. Razvojni posao završen je 33 posto (5.000 stvarnog troška / 15.000 proračunskog troška), a instalacijski posao 20 posto (1.000 stvarnog troška / 5.000 proračunskog troška).
-   Iznos fakture od 8.667 automatski se izračunava (33 posto od 20.000 + 20 posto od 10.000).
-   Stvorite fakturu na 8.667 i pošaljite je klijentu.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Primjer: Stvaranje pravila naplate koje se temelji na dogovorenim kontrolnim točkama

Vaša tvrtka ili ustanova, tvrtka za savjetodavno upravljanje, pristaje provesti istraživanje tržišta za potrošački proizvod koji klijent planira prodati. Klijent se slaže da će vaše usluge koristiti tijekom razdoblja od tri mjeseca, počevši od ožujka, i pristaje vašoj tvrtki ili ustanovi platiti 50.000. Projekt ima tri kontrolne točke:

-   1. kontrolna točka: Prikupljanje podataka o potrošačima – 31. ožujka
-   2. kontrolna točka: Analiziranje potrošačkih podataka – 30. travnja
-   3. kontrolna točka: Predstavljanje prijedloga održivosti proizvoda – 31. svibnja

Klijent se slaže da će vašoj tvrtki ili ustanovi platiti 10.000 na prvoj kontrolnoj točki, 20.000 na drugoj i 20.000 na trećoj kontrolnoj točki. 

Kada postavljate ugovor o projektu, pristajete klijentu naplaćivati na temelju kontrolne točke koja je dovršena. Postavljanje pravila naplate uključuje sljedeće korake:

-   Definiranje kontrolnih točaka projekta.
-   Definiranje iznosa za fakturiranje klijentu kada se završi svaka kontrolna točka.

Kada se 31. ožujka dovrši prva kontrolna točka, označite je kao dovršenu, a zatim stvorite fakturu na 10.000 i pošaljite je klijentu. Ne možete stvoriti fakturu za kontrolnu točku dok je ne označite kao završenu.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Primjer: Stvaranje pravila naplate koje se temelji na uslugama uz dodatnu naknadu za upravljanje

Vaša tvrtka ili ustanova, tvrtka za savjetodavno upravljanje, pristaje provesti istraživanje tržišta kako bi se procijenila održivost proizvoda koju klijent, maloprodajna tvrtka, razvija. Uvjeti sporazuma određuju kako ćete osigurati usluge svoja tri najbolja savjetnika za upravljanje, koji će istraživanje provoditi na temelju vremena i materijala. Klijent pristaje platiti 100 po satu, uz dodatnih 10 posto naknade za upravljanje savjetničkim satima rada koji se naplaćuju projektu. 

Kada postavljate ugovor o projektu, stvorite pravilo naplate za dodavanje 10 posto naknade za upravljanje savjetničkim satima rada koji se naplaćuju projektu. 

Kada stvarate fakturu za klijenta, klijentu se naplaćuje 10-postotna naknada za upravljanje uvećana za trošak savjetničkog sata. Na primjer, ako su tri konzultanta na projektu radila ukupno 200 sati, faktura na 22.000 stvara se na temelju sljedećeg izračuna:

-   200 sati pri 100 za sat = 20.000
-   Naknada za upravljanje od 10 posto = 2.000
-   Ukupni iznos fakture = 22.000

Ako su naknade koje se zaračunavaju klijentu oporezive i u ugovoru o projektu odaberete grupu PDV-a, ona se automatski unosi u pravilo naplate naknada.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Primjer: Stvaranje pravila naplate za vrijednost vremena i materijala

Vaša tvrtka ili ustanova, tvrtka za softversko savjetovanje, pristaje osigurati pet tehničkih savjetnika koji će tijekom sljedećih šest mjeseci raditi na projektu razvoja softvera za klijenta. Klijent se obvezuje platiti 150 za svaki savjetnički sat rada, uvećan za troškove uredskog materijala. Vaša tvrtka ili ustanova šalje klijentu fakturu na kraju svakog mjeseca. 

Kada postavljate ugovor o projektu, suglasni ste da ćete klijentu svaki mjesec fakturirati vrijeme i materijale utrošene na projektu. Stvorite pravilo naplate koje uključuje sljedeće podatke:

-   Razdoblje ugovora je šest mjeseci.
-   Vrijeme savjetovanja izračunava se s cijenom od 150 na sat.
-   Uredski materijal fakturira se prema trošku, a ukupni trošak projekta ne smije prelaziti 10.000.
-   Fakturu za klijenta stvarate na kraju svakog kalendarskog mjeseca tijekom projekta.

Tijekom prvog mjeseca, savjetnici na projektu bilježe ukupno 800 sati. Cijena uredskog materijala koji se naplaćuje za projekt iznosi 2.000. Stoga na kraju mjeseca stvarate fakturu na 122.000, što je izračunano kao 800 sati pri 150 na sat, uz dodatnih 2.000 za uredski materijal.



