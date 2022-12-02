---
title: Novosti i izmjene u aplikaciji Project Operations u listopadu 2021. za scenarije koji se temelje na zalihama/proizvodnji
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Project Operations za listopad 2021. za scenarije koji se temelje na zalihama/proizvodnji.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029934"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novosti i izmjene u aplikaciji Project Operations u listopadu 2021. za scenarije koji se temelje na zalihama/proizvodnji

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Upravljanje projektima i računovodstvo u verziji 10.0.22 okruženja aplikacije Dynamics 365 Finance
 
## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
|--------------|------------------|----------------|
| Upravljanje projektom i računovodstvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projektni radovi u tijeku (WIP) i iznosi akumuliranog prihoda nisu pravilno poništeni kada se knjiži međukompanijska faktura klijenta. |
| Upravljanje projektom i računovodstvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkcija **Sprječavanje zatvaranja projekta ako postoje otvorene transakcije** ne radi. |
| Upravljanje projektom i računovodstvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikacija naplate na fakturi sa slobodnim tekstom ne popunjava automatski veličine iz projekata kada je ta funkcija omogućena. |
| Upravljanje projektom i računovodstvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | WIP i iznosi akumuliranog prihoda nisu pravilno poništeni kada se knjiži faktura projekta u međukompanijskim scenarijima. |
| Upravljanje projektom i računovodstvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Vrijednosti zaduženja i kredita mijenjaju se kada se Microsoft Excel dodatak koristi s dnevnikom troškova projekta i kad je polje **Vrsta računa za kompenzaciju** postavljeno na **Projekt**. |
| Upravljanje projektom i računovodstvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Iznos koji je knjižen u transakcijama projekta precijenjen je na narudžbenici projekta koja uključuje stavke na zalihama i koja ima iznose poreza koji se ne mogu odbiti kada je označena opcija **UseTax**. |
| Upravljanje projektom i računovodstvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sustav dijeli iznos između izvješća o dobiti i gubitku projekta i izvješća WIP projekta. |
| Upravljanje projektom i računovodstvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventar pri ruci netočan je nakon što se prilagodi zahtjev za djelomično vraćenu stavku. |
| Upravljanje projektom i računovodstvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nazivi resursa dupliciraju se u aplikaciji Project Operations kada se uređuju u aplikaciji Microsoft Project. |
| Upravljanje projektom i računovodstvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Izvješća o međukompanijskim troškovima koja imaju međukompanijske troškove faktura dobavljača na čekanju za dugovanja prvo se knjiže u vrstu knjiženja **Trošak WIP projekta**. Međutim, tijekom obrade, troškovi povezani s procjenom procjenu knjiže se u vrstu knjiženja **Trošak projekta** umjesto očekivanog **Međukompanijskog troška**. |
| Upravljanje projektom i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultati zadržavanja dobavljača u transakcijama troškova projekta nisu prikazani. |
| Upravljanje projektom i računovodstvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Vremenski list mora zaokružiti iznos transakcije u valuti transakcije na određeni broj decimalnih mjesta u svim računovodstvenim distribucijama i općenitim unosima dodjele u dnevniku. |
| Upravljanje projektom i računovodstvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Količine zahtjeva projektnih stavki automatski se ažuriraju kada se planirane narudžbe utvrde. |
| Upravljanje projektom i računovodstvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Broj vaučera, saldo dobavljača vrste transakcije i broj računa ne mogu se poništiti na fakturi za plaćanje unaprijed narudžbenice. |
| Upravljanje projektom i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Međukompanijska faktura dobavljača prekinuta je kada je uključena integracija fakture dobavljača. |
| Upravljanje projektom i računovodstvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Kada kreirate dnevnik troškova projekta, iznos troška prikazan je u polju **Kredit**. |
| Upravljanje projektom i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uvjeti plaćanja na projektnim fakturama ne funkcioniraju prema očekivanjima. |
| Upravljanje projektom i računovodstvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Vaučeri s vremenskim listovima mogu se ponovno upotrijebiti kada je niz brojeva postavljen kao neprekidan. |
| Upravljanje projektom i računovodstvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCUSKA: logika **Ručni iznos zadržavanja** nije usklađena s logikom **Automatski iznos zadržavanja** u prijedlogu fakture za ugovor o projektu. |
| Upravljanje projektom i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada se otpusti zadržavanje dobavljača, knjiženje vaučera ima dodatne retke koji su netočni. |
| Upravljanje projektom i računovodstvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Kada se polje **Datum fakture** na stranici **Stvori prijedlog fakture** promijeni, može se pojaviti sljedeća pogreška: "Referenca objekta nije postavljena na instancu objekta." |
| Upravljanje projektom i računovodstvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Dolazi do pogreške kada pokušate odobriti vremenski list iz tijeka rada **TSLine**, a postoji i pravilo vremenskog lista za subotu i nedjelju. |
| Upravljanje projektom i računovodstvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Vrsta stavke projekta početnog salda isključena je iz **Sažetaka transakcija prijedloga fakture** kada se izračuna ukupni iznos fakture prijedloga fakture. |
| Upravljanje projektom i računovodstvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ako je trošak potrošnje na proizvodnom nalogu projekta 0 (nula), sljedeća pogreška javlja se kada pokušate procijeniti: "Pokušaj dijeljenja s nulom." |
| Upravljanje projektom i računovodstvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilna aplikacija Project Timesheet za Android ne reagira. Problem je povezan s **TimeEntryDataManager ArgumentNullException**. |
| Upravljanje projektom i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Dnevnik integracije Project Operations nije uspio pri knjiženju jer račun nema veličine. Međutim, račun kojemu nedostaju veličine nije račun u koji knjižite. |
| Upravljanje projektom i računovodstvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filtar **ToDate** u pretraživanjima se ne briše kada se ukloni iz dijaloškog okivra **Odaberi** na stranici **Knjiži trošak**. |
| Upravljanje projektom i računovodstvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Resetiraj svu distribuciju** ne uspijeva i prikazuje pogrešku za vremenske listove koji su stvoreni za projekt vrste **Samo vrijeme**. |
| Upravljanje projektom i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **Project** ne može se uređivati na fakturi dobavljača na čekanju kada je kategorija nabave dodijeljena stavci. |
| Upravljanje projektom i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigacijsko okno nedostaje ako niste prijavljeni u Project Operations Dataverse. |
| Upravljanje projektom i računovodstvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Za transakcije prilagodbe međukompanijskog projekta postoje problemi u odredišnoj tvrtki. |
| Upravljanje projektom i računovodstvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Preuzeti troškovi za projekt izračunavaju pogrešnu količinu i cijenu koštanja ako je narudžbenica obrađena putem opcije **Postupak narudžbenice na kraju godine** u glavnoj knjizi. |
| Upravljanje projektom i računovodstvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kada se nalog za proizvodnju projekta koji ima naloge za kvalitetu prijavi kao završen, javlja se sljedeća pogreška: "Nijedna virtualna transakcija nije označena transakcijom inventara." |
| Upravljanje projektom i računovodstvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Kada se knjiži faktura za dugovanja povezana s projektom, pojavljuje se sljedeća pogreška: "Nabrojani tekst Projekt – trošak – stavka ne postoji." |
| Upravljanje projektom i računovodstvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Neizravni troškovi udvostručuju se kada ručno prikupljate prihod. |
| Upravljanje projektom i računovodstvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Prikupljanje prihoda i WIP knjiženje ne proizvode transakcije. |
| Upravljanje projektom i računovodstvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivacija cijene na čekanju ne uspijeva za stavku standardnog troška kada postoji primljena narudžbenica projekta. |
| Upravljanje projektom i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrnuta vrijednost WIP-a iz knjiženja fakture razlikuje se od izvorne knjižene vrijednosti WIP-a iz unosa vremena. |
| Upravljanje projektom i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Transakcije vaučera nisu uravnotežene zbog problema u knjiženju prihoda fakturiranih za projekt u primijenjenim slučajevima zadržavanja dijela plaćanja. |
| Upravljanje projektom i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Stvaranje procjene nakon knjiženja prijedloga fakture blokira uvoz redaka ispravaka u aplikaciji Project Operations. |
| Upravljanje projektom i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmjena potpuno fakturiranog ključnog zapisa ne bi trebala biti moguća. |
| Upravljanje projektom i računovodstvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Kada se koriste automatske naplate, međukompanijska faktura klijent za vremenski list ne može se knjižiti i prikazuje se poruka o pogrešci. |
| Upravljanje projektom i računovodstvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa na potprojektu nije ispravno ažurirana. |
| Upravljanje projektom i računovodstvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Cijena koštanja na zahtjevima stavki ažurira se nabavnom cijenom za konsolidirane narudžbenice. |
| Upravljanje projektom i računovodstvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Knjiženi trošak nije točan nakon ažuriranja nabavne cijene i omogućivanja parametra **Aktiviraj upravljanje promjenama**. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Svi troškovi korisnika vidljivi su kada tražite kategoriju u mobilnoj aplikaciji Expense. |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netočni iznosi transakcija dobavljača i transakcija poreza na promet koji su knjiženi iz troškova nastalih transakcijom kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Nevažno upozorenje pojavljuje se kada osvježite stranice izvješća o troškovima. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešan privremeni odobravatelj koristi se kada izbrišete privremenog odobravatelja i ponovno pošaljete kroz tijek rada. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Dolazi do pogreške knjiženja povezane s postavljanjem kilometraže. |
| Putovanje i trošak | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribucija ne ažurira pravni entitet kada se nepovezana transakcija ponovno doda u izvješće o troškovima u međukompanijskom trošku. |

### <a name="regulatory-updates"></a>Ažuriranja propisa

Za informacije o ažuriranjima propisa za aplikacije za financije i operacije pogledajte članak [Ažuriranja propisa](/dynamics365/finance/localizations/regulatory-updates). Također se možete prijaviti u Microsoft Dynamics Lifecycle Services (LCS) i upotrijebiti alat za pretraživanje problema da biste pregledali planirana ažuriranja propisa. Pretraživanje problema omogućuje vam pretraživanje po zemlji ili regiji, vrsti značajke i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
