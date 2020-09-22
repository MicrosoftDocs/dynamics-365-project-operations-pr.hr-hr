---
title: Fakturiranje unutar tvrtke
description: Ovaj članak sadrži podatke i primjere o fakturiranju projekata unutar tvrtke.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0385c796ca1ac02d6b8f66c04dad21bafe15ef8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750069"
---
# <a name="intercompany-invoicing"></a>Fakturiranje unutar tvrtke

[!include [banner](../includes/banner.md)]

Ovaj članak sadrži podatke i primjere o fakturiranju projekata unutar tvrtke.

Vaša tvrtka ili ustanova može imati više sektora, podružnica i drugih pravnih osoba koje međusobno prenose proizvode i usluge za projekte. Pravna osoba koja isporučuje uslugu ili proizvod naziva se *pravna osoba davatelj posudbe*, a pravna osoba koja prima uslugu ili proizvod naziva se *pravna osoba primatelj posudbe*. 

Na sljedećoj slici prikazan je uobičajen scenarij u kojem dvije pravne osobe, SI FR (pravna osoba primatelj posudbe) i SI USA (pravna osoba davatelj posudbe) dijele resurse kako bi isporučili projekt klijentu A. Za ovaj scenarij, SI FR ugovorom se obvezala isporučiti posao klijentu A. 

[![Primjer fakturiranja unutar tvrtke](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Cilj je kontrolu troškova, priznavanje prihoda, poreze i cijenu prijenosa za transakcije projekata unutar tvrtke učiniti fleksibilnijim i snažnijim. Osim toga, pružaju se sljedeće mogućnosti:

-   Stvorite fakture klijentima za projekt u pravnoj osobi primatelju posudbe uporabom evidencija radnog vremena, izdataka i faktura dobavljača unutar tvrtke u pravnoj osobi davatelju posudbe.
-   Podržite izračun poreza i posrednih troškova.
-   Odgodite priznavanje prihoda u pravnoj osobi davatelja posudbe i kada bi pravna osoba primatelja posudbe trebala priznati trošak.
-   Obračunajte prihode za djelomično izvršeni posao (WIP, work in process) u pravnoj osobi davatelja posudbe.
-   Postavite cijene prijenosa koje se mogu temeljiti na različitim modelima određivanja cijena. Evo nekoliko primjera:
    -   **Količina** – Iznos koji unesete u polje **Određivanje cijena** je stvarni trošak po količini ili jedinici.
    -   **Iznos naknade** – Cijena/trošak po transakciji uz iznos naknade koji ste unijeli u polje **Određivanje cijene**.
    -   **Postotak naplate** – Cijena prijenosa jest cijena/trošak po transakciji pomnožen s postotkom naknade koji unesete u polje **Određivanje cijene**.
    -   **Postotak prodajne cijene** – Postotak prodajne cijene koja se prenosi na pravnu osobu davatelja posudbe.
    -   **Iznos ispod prodajne cijene** – Iznos koji pravna osoba primatelj posudbe zadržava od prodajnih cijena prije prijenosa na pravnu osobu primatelja posudbe.
    -   **Omjer doprinosa** – Broj koji unesete u polje **Određivanje cijene** omjer je doprinosa, koji se izražava kao postotak prodajne cijene.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Primjer 1: Postavljanje parametara za fakturiranje unutar tvrtke
U ovom primjeru, USSI pravna je osoba davatelj posudbe i njezini resursi prijavljuju vrijeme koje tereti pravnu osobu primatelja posudbe FRSI, koja je vlasnik ugovora s krajnjim klijentom. Sati rada i izdaci koje prijavljuju zaposlenici tvrtke USSI mogu se uključiti u fakturu projekta koju generira tvrtka FRSI. Uz to, postoji i treći izvor transakcija koji može potjecati od pravne osobe davatelja posudbe (USSI u ovom primjeru) kada pruža usluge zajedničkih dobavljača podružnicama (kao što je FRSI), a zatim te troškove prosljeđuje na one troškove projekta unutar tih podružnica. Sve odgovarajuće dokumente faktura i izračuna poreza dovršava financijska služba. 

U ovom primjeru, FRSI mora biti klijent pravne osobe USSI, a USSI mora biti dobavljač pravne osobe FRSI. Tada možete uspostaviti međusobni odnos između dviju pravnih osoba. U sljedećem postupku prikazuje se način postavljanja parametara tako da obje pravne osobe mogu sudjelovati u fakturiranju unutar tvrtke.

1. Postavite FRSI kao klijenta u pravnoj osobi USSI i USSI postavite kao dobavljača u pravnoj osobi FRSI. Postoje tri ulazne točke za korake potrebne za ovaj zadatak.

   | Korak |                                                       Točka unosa                                                        |                                                                                                                                                                                               Opis                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | U USSI kliknite <strong>Potraživanja</strong> &gt; <strong>Klijenti</strong> &gt; <strong>Svi klijenti</strong>. |                                                                                                                                                                  Stvorite novi korisnički zapis za tvrtku FRSI i odaberite grupu klijenata.                                                                                                                                                                  |
   |  B   |    U tvrtki FRSI kliknite <strong>Dugovanja</strong> &gt; <strong>Dobavljači</strong> &gt; <strong>Svi dobavljači</strong>.     |                                                                                                                                                                    Stvorite zapis o novom dobavljaču za tvrtku USSI i odaberite grupu klijenata.                                                                                                                                                                    |
   |  C   |                                  U tvrtki FRSI otvorite zapis dobavljača koji ste upravo stvorili.                                  | U Oknu radnji, na kartici <strong>Općenito</strong>, u grupi <strong>Postavljanje</strong>, kliknite mogućnost <strong>Unutar tvrtke</strong>. Na stranici <strong>Unutar tvrtke</strong>, na kartici <strong>Trgovački odnos</strong>, postavite klizač <strong>Aktivan</strong> na <strong>Da</strong>. U polju <strong>Tvrtka klijent</strong>, odaberite zapis klijenta koji ste stvorili u koraku A. |


2. Kliknite **Upravljanje projektima i računovodstvo** &gt; **Postavljanje** &gt; **Računovodstveni parametri upravljanja projektom**, a zatim kliknite karticu **Unutar tvrtke**. Način postavljanja parametara ovisi o tome jeste li pravna osoba koja primatelj posudbe ili pravna osoba davatelj posudbe.
   -   Ako ste pravna osoba primatelj posudbe, odaberite kategoriju nabave koja će se upotrebljavati za podudaranje fakture dobavljača koji se automatski generiraju.
   -   Ako ste pravna osoba davatelj posudbe, za svaki pozajmljeni entitet odaberite zadanu kategoriju projekta za svaku vrstu transakcije. Kategorije projekata upotrebljavaju se za konfiguraciju poreza kada fakturirana kategorija u transakcijama unutar tvrtke postoji samo u pravnoj osobi primatelju posudbe. Možete odabrati obračun prihoda od transakcija unutar tvrtke. Ovo obračunavanje vrši se kada se transakcije knjiže, a zatim se stornira kada se knjiži faktura unutar tvrtke.

3. Kliknite **Upravljanje projektima i računovodstvo** &gt; **Postavljanje** &gt; **Cijene** &gt; **Cijena prijenosa**.
4. Odaberite valutu, vrstu transakcije i model cijene prijenosa. Valuta koja se upotrebljava na fakturi ona je koja je konfigurirana u zapisu klijenata za pravnu osobu primatelja posudbe u pravnoj osobi davatelja posudbe. Valuta se upotrebljava za podudaranje unosa u tablici cijena prijenosa.
5. Kliknite **Glavna knjiga** &gt; **Postavljanje knjiženja** &gt; **Računovodstvo unutar tvrtke** i postavite odnos za USSI i FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Primjer 2: Stvaranje i knjiženje evidenciju radnog vremena unutar tvrtke
USSI, pravna osoba davatelj posudbe, mora stvoriti i proknjižiti evidenciju radnog vremena za projekt od tvrtke FRSI, pravne osobe primatelja posudbe. Postoje dvije ulazne točke za korake potrebne za ovaj zadatak.

| Korak | Točka unosa                                                                       | Opis                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Upravljanje projektima i računovodstvo** &gt; **Evidencije radnog vremena** &gt; **Sve evidencije radnog vremena** | Stvorite novu evidenciju radnog vremena. U retku evidencije radnog vremena, u polju **Pravna osoba**, odaberite **FRSI**. U polju **ID projekta** odaberite projekt u tvrtki FRSI. Unesite sate rada za svaki dan u tjednu. |
| B    | Stranica **Evidencija radnog vremena**                                                                | Nakon što se tijek rada pokrene, proknjižite evidenciju radnog vremena i zabilježite broj kupona.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Primjer 3: Stvaranje i knjiženje fakture dobavljača unutar tvrtke
USSI, pravna osoba davatelj posudbe, mora stvoriti i proknjižiti fakturu dobavljača unutar tvrtke za projekt od tvrtke FRSI, pravne osobe primatelja posudbe. Ova faktura dobavljača predstavlja rad i izdatak prepušten vanjskim tvrtkama koje su izvršili dobavljači koje plaća tvrtka USSI. Postoje dvije ulazne točke za korake potrebne za ovaj zadatak.

| Korak | Točka unosa                                                                                      | Opis                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Dugovanja** &gt; **Fakture** &gt; **Otvori fakture dobavljača** &gt; **Nova faktura dobavljača** | Stvorite novu fakturu dobavljača i unesite usluge koje su nabavljene u ime projekta tvrtke FRSI.                                                                                                                                                                                  |
| B    | Stranica **Faktura dobavljača**                                                                      | Unesite retke koji predstavljaju usluge prepuštene vanjskim tvrtkama u ime tvrtke FRSI. Na Brzoj kartici **Pojedinosti redaka**, na kartici **Projekt** za redak fakture u polju **Projektna tvrtka**, unesite **FRSI**. Unesite projekt i odgovarajuće podatke. Zatim proknjižite fakturu dobavljača. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Primjer 4: Stvaranje i knjiženje fakture unutar tvrtke
USSI, pravna osoba davatelj posudbe, mora stvoriti i proknjižiti fakturu unutar tvrtke. Postoje dvije ulazne točke za korake potrebne za ovaj zadatak.

| Korak | Točka unosa                                                                                             | Opis                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Faktura za klijenta unutar tvrtke**  | Kliknite **Novo** kako biste otvorili stranicu **Stvori fakturu unutar tvrtke**.                                                                                  |
| B    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Fakture za klijenta unutar tvrtke** | Na stranici **Stvori fakturu unutar tvrtke** unesite pravnu osobu, navedite transakciju koju treba uključiti, a zatim kliknite **Traži**. |
| C    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Fakture za klijenta unutar tvrtke** | Odaberite transakcije za fakturiranje ili kliknite **Odaberi sve** kako biste fakturirali sve transakcije s popisa, a zatim kliknite **U redu**.                  |
| D    | Stranica **Faktura unutar tvrtke**                                                                       | Prikazuje se prijedlog fakture za klijente unutar tvrtke.                                                                                             |
| E    | Stranica **Faktura unutar tvrtke**                                                                       | Kliknite mogućnost **Knjiži**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Primjer 5: Knjiženje fakture dobavljača i fakturiranje klijentu
Kada pravna osoba davatelj posudbe, USSI, knjiži fakturu klijenta unutar tvrtke, u pravnoj osobi primatelja posudbe, FRSI, stvara se odgovarajuća faktura dobavljača na čekanju. Nakon knjiženja ove fakture dobavljača, FRSI također fakturira klijentu projekta za sate rada koje je unijela tvrtka USSI. Postoje tri ulazne točke za korake potrebne za ovaj zadatak.

| Korak | Točka unosa                                                                                        | Opis                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Dugovanja** &gt; **Fakture** &gt; **Fakture dobavljača na čekanju**                            | Pregledajte fakturu kako biste provjerili jesu li uključene vrijednosti evidencije radnog vremena, a zatim proknjižite fakturu dobavljača.                  |
| B    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Prijedlozi fakture projekta** | Stvorite novu fakturu projekta za projekt i provjerite pojavljuju li se proknjižene transakcije po satu.            |
| C    | Stranica **Faktura projekta**                                                                       | Odaberite fakturu projekta, a zatim kliknite **Pregledaj pojedinosti** kako biste pregledali trošak i iznos prodaje. Zatim fakturu proknjižite. |


Dodatne informacija potražite u odjeljku [Konfiguriranje fakturiranja projekta unutar tvrtke](tasks/configure-intercompany-project-invoicing.md).


