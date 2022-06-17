---
title: Što je novo ili promijenjeno u projektnim operacijama, listopad 2021. za scenarije koji se temelje na zalihama/proizvodnji
description: U ovom se članku nalaze informacije o ažuriranjima kvalitete koja su dostupna u izdanju projektnih operacija u listopadu 2021. za scenarije koji se temelje na zalihama/proizvodnji.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933667"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Što je novo ili promijenjeno u projektnim operacijama, listopad 2021. za scenarije koji se temelje na zalihama/proizvodnji

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.22
 
## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
|--------------|------------------|----------------|
| Upravljanje projektom i računovodstvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projektni rad u tijeku (PUT) i obračunati iznosi prihoda ne storniraju se ispravno kada se proknjiži međukompanijska faktura kupcu. |
| Upravljanje projektom i računovodstvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkcija **Spriječi zatvaranje projekta ako postoje** otvorene transakcije ne funkcionira. |
| Upravljanje projektom i računovodstvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikacija naplate na besplatnoj tekstualnoj fakturi ne ispunjava automatski dimenzije projekata kada je ta funkcija omogućena. |
| Upravljanje projektom i računovodstvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | U scenarijima koji nisu međukompanijski, iznosi PUT-a i obračunatog prihoda ne storniraju se ispravno prilikom knjiženja fakture projekta. |
| Upravljanje projektom i računovodstvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Dugovne i potražne vrijednosti mijenjaju se kada Microsoft Excel se dodatak koristi u temeljnici troškova projekta, a **polje Vrsta** offset računa postavljeno je na **Projekt**. |
| Upravljanje projektom i računovodstvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Iznos proknjižen u projektnim transakcijama precijenjen je na narudžbenici projekta koja uključuje zalihe artikala i koja ima iznose poreza koji se ne odbijaju kada **je označena UseTax**. |
| Upravljanje projektom i računovodstvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sustav dijeli iznos između izvješća o dobiti i gubitku projekta i izvješća o PUT-u projekta. |
| Upravljanje projektom i računovodstvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Zalihe na skladištu neispravne su nakon prilagodbe djelomično vraćenog zahtjeva za artiklom. |
| Upravljanje projektom i računovodstvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nazivi resursa dupliciraju se u operacijama projekta prilikom uređivanja u programu Microsoft Project. |
| Upravljanje projektom i računovodstvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Međukompanijska izvješća o troškovima koja imaju račune koji se plaćaju kao računi na čekanju troškova fakture dobavljača najprije se knjiže u **vrstu knjiženja troška** PUT-a projekta. Međutim, tijekom obrade troškovi povezani s procjenom knjiže se u **vrstu knjiženja troška** projekta umjesto u očekivanu **vrstu knjiženja međukompanijskih troškova**. |
| Upravljanje projektom i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultati zadržavanja dobavljača u transakcijama troškova projekta nisu prikazani. |
| Upravljanje projektom i računovodstvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Vremenska tablica mora zaokružiti iznos transakcije u valuti transakcije na određeni broj decimalnih mjesta na svim računovodstvenim distribucijama i stavkama alokacije opće temeljnice. |
| Upravljanje projektom i računovodstvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Količine zahtjeva za artiklom za projekt automatski se obnavljaju kada se planirani nalozi učvrste. |
| Upravljanje projektom i računovodstvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Broj vaučera, saldo dobavljača vrste transakcije i broj računa ne mogu se stornirati na fakturi akontacije/pretplate narudžbenice. |
| Upravljanje projektom i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Međukompanijska faktura dobavljača prekinuta je kada je uključena integracija fakture dobavljača. |
| Upravljanje projektom i računovodstvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Kada kreirate temeljnicu troškova projekta, iznos troška prikazuje se u polju **Potraživanje**. |
| Upravljanje projektom i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uvjeti plaćanja na računima projekta ne funkcioniraju kako se očekivalo. |
| Upravljanje projektom i računovodstvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Vaučeri vremenske tablice mogu se ponovno upotrijebiti kada je brojčani slijed postavljen kao kontinuiran. |
| Upravljanje projektom i računovodstvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCUSKA: logika ručnog iznosa **zadržavanja** ne odgovara logici automatskog iznosa **zadržavanja** u prijedlogu fakture za ugovor o projektu. |
| Upravljanje projektom i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada se oslobodi zadržavanje dobavljača, knjiženje vaučera ima netočne dodatne retke. |
| Upravljanje projektom i računovodstvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **Kada se promijeni polje datum** fakture na **stranici Stvaranje prijedloga** fakture, može se pojaviti sljedeća pogreška: "Referenca objekta nije postavljena na instancu objekta." |
| Upravljanje projektom i računovodstvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Pogreška se pojavljuje kada pokušate odobriti vremensku tablicu iz **tijeka rada TSLinea**, a postoji i pravilo vremenske tablice za subotu i nedjelju. |
| Upravljanje projektom i računovodstvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Vrsta stavke projekta početnog salda isključena je iz **sažetaka transakcije prijedloga fakture** prilikom izračuna ukupnog iznosa fakture prijedloga fakture. |
| Upravljanje projektom i računovodstvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ako je trošak potrošnje na radnom nalogu projekta 0 (nula), prilikom pokušaja procjene pojavljuje se sljedeća pogreška: "Pokušaj podjele s nulom." |
| Upravljanje projektom i računovodstvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikacija Project Timesheet Mobile za Android prestaje reagirati. Problem se odnosi na **TimeEntryDataManager ArgumentNullException**. |
| Upravljanje projektom i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Temeljnica integracije operacija projekta ne uspijeva kada je proknjižite jer računu nedostaju dimenzije. Međutim, račun kojem nedostaju dimenzije nije račun na koji knjižite. |
| Upravljanje projektom i računovodstvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filtar **ToDate** u pretraživanjima ne briše se kada se ukloni iz dijaloškog **okvira Odabir** na stranici Objava **troškova**. |
| Upravljanje projektom i računovodstvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Ponovno postavljanje svih distribucija** ne uspijeva i prikazuje pogrešku za vremenske tablice stvorene za projekt **vrste Samo** vrijeme. |
| Upravljanje projektom i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **Projekt** ne može se uređivati na fakturi dobavljača na čekanju kada je kategorija nabave dodijeljena artiklu. |
| Upravljanje projektom i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigacijsko okno nedostaje ako niste prijavljeni u projektne operacije Dataverse. |
| Upravljanje projektom i računovodstvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Za međukompanijske transakcije prilagodbe projekta postoje problemi u odredišnom poduzeću. |
| Upravljanje projektom i računovodstvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Predani troškovi za projekt izračunavaju pogrešnu količinu i cijenu troška ako je narudžbenica obrađena postupkom **narudžbenice** na kraju godine u glavnoj knjizi. |
| Upravljanje projektom i računovodstvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kada se radni nalog projekta koji ima kvalitetne naloge prijavi kao dovršen, pojavljuje se sljedeća pogreška: "Nema virtualne transakcije označene transakcijom zaliha." |
| Upravljanje projektom i računovodstvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Kada se proknjiži faktura za račune povezane s projektom, pojavljuje se sljedeća pogreška: "Nabrojeni tekst Projekt - trošak - artikl ne postoji." |
| Upravljanje projektom i računovodstvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Neizravni troškovi udvostručuju se kada ručno obračunate prihod. |
| Upravljanje projektom i računovodstvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Obračunavanje prihoda i knjiženje PUT-a ne proizvodi transakcije. |
| Upravljanje projektom i računovodstvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivacija cijene na čekanju ne uspijeva za stavku standardnog troška kada postoji zaprimljena narudžbenica projekta. |
| Upravljanje projektom i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Reverzirana vrijednost PUT-a iz knjiženja fakture razlikuje se od izvorne proknjižene vrijednosti PUT-a od vremenske stavke. |
| Upravljanje projektom i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Postoji problem s knjiženjem prihoda fakturiranog projekta u primijenjenim slučajevima akontacije u kojima transakcije na vaučeru ne saldiraju. |
| Upravljanje projektom i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kreiranje procjene nakon knjiženja prijedloga fakture blokira uvoz redaka ispravka u projektnim operacijama. |
| Upravljanje projektom i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmjena potpuno fakturiranog zapisa ključne etape ne bi trebala biti moguća. |
| Upravljanje projektom i računovodstvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Kada se koriste automatski troškovi, međukompanijska faktura kupca za vremensku tablicu ne može se proknjižiti i prikazuje se poruka o pogrešci. |
| Upravljanje projektom i računovodstvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa na potprojektu nije ispravno ažurirana. |
| Upravljanje projektom i računovodstvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Cijena troška za zahtjeve artikla obnavlja se nabavnom cijenom za konsolidirane narudžbenice. |
| Upravljanje projektom i računovodstvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Proknjiženi trošak nije ispravan nakon ažuriranja nabavne cijene i omogućavanja parametra **Aktiviraj upravljanje** promjenama. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Svi korisnički troškovi mogu se vidjeti kada tražite kategoriju u mobilnoj aplikaciji Expense. |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netočni iznosi transakcija dobavljača i transakcija poreza na promet knjiže se iz troška kreiranog iz transakcije kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Prilikom osvježavanja stranica izvješća o troškovima prikazuje se nevažna poruka upozorenja. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešan privremeni odobravatelj koristi se kada izbrišete privremenog odobravatelja, a zatim ponovno pošaljete putem tijeka rada. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojavljuje se pogreška pri knjiženju koja je povezana s postavljanjem kilometraže. |
| Putovanje i trošak | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribucija ne obnavlja pravnu osobu kada se nevezana transakcija ponovno doda u izvješće o troškovima na međukompanijski trošak. |

### <a name="regulatory-updates"></a>Ažuriranja propisa

Informacije o regulatornim ažuriranjima za aplikacije Financije i operacije potražite u članku [Regulatorna ažuriranja](/dynamics365/finance/localizations/regulatory-updates). Također se možete prijaviti Microsoft Dynamics u usluge životnog ciklusa (LCS) i pomoću alata za pretraživanje problema pregledati planirana regulatorna ažuriranja. Pretraživanje problema omogućuje vam pretraživanje po zemlji ili regiji, vrsti značajke i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
