---
title: Novosti i izmjene u aplikaciji Project Operations u rujnu 2021. za scenarije koji se temelje na zalihama/proizvodnji
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Project Operations za rujan 2021. za scenarije koji se temelje na zalihama/proizvodnji.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029843"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novosti i izmjene u aplikaciji Project Operations u rujnu 2021. za scenarije koji se temelje na zalihama/proizvodnji

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Upravljanje projektima i računovodstvo u verziji 10.0.21 okruženja aplikacije Dynamics 365 Finance
 
## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
|---|---|---|
| Upravljanje projektom i računovodstvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Omogućivanjem pristupa ulozi voditelja nabave jednoj pravnoj osobi omogućuje se i pristup svim projektima u svim pravnim osobama. |
| Upravljanje projektom i računovodstvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Do problema sa zaokruživanjem poreza na dodanu vrijednost (PDV) dolazi kad se kreditno odobrenje podmiruje prema izvornoj fakturi projekta. |
| Upravljanje projektom i računovodstvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Koristite alternativni proračun projekta za provjeru proračuna. |
| Upravljanje projektom i računovodstvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Cjenovna grupa **Prodajna cijena po satu** nije izračunata u strukturnoj analizi rada za ponude projekta. |
| Upravljanje projektom i računovodstvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Uklanjanje procjene ne uspijeva kada je omogućena značajka **Omogući valutu ugovora o projektu za izračun procjene**. |
| Upravljanje projektom i računovodstvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizacija poreza na promet prema količini dodaje se iznosu prodajne cijene kada se porez na korištenje koristi za grupu poreza na promet dnevnika troškova projekta. |
| Upravljanje projektom i računovodstvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Uvjetni porez nije pravilno izračunan za posljednju uplatu kada je zadržavanje dijela uplate dobavljaču i plaćanje unaprijed primijenjeno na fakturu na temelju narudžbenice. |
| Upravljanje projektom i računovodstvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Praćenje prilagodbe ne radi za dnevnike početnog stanja. |
| Upravljanje projektom i računovodstvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Raspodjela rebalansa proračuna projekta po razdobljima** podijeljena je na sva proračunska razdoblja. Kada se dodjela podnese, zapis se ne briše. |
| Upravljanje projektom i računovodstvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Knjiženja rada u tijeku (WIP) u glavnoj knjizi imaju netočan iznos. |
| Upravljanje projektom i računovodstvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Odobrenje dnevnika sati projekta ne funkcionira. |
| Upravljanje projektom i računovodstvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodajna cijena prilagodbe projekta ne ažurira se neizravnim troškovima kada ograničenje financiranja nije označeno. |
| Upravljanje projektom i računovodstvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Zahtjev stavke ne može se stvoriti kada je zaglavlje tablice Prodaja fakturirano, a prateća narudžbenica za postojeće retke dovršena. |
| Upravljanje projektom i računovodstvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Iznos zadržavanja za pravilo naplate koje ima ključnu točku za drugi projekt nije knjižen u odgovarajućem ID-u projekta koji je odabran za ključnu točku. Umjesto toga, knjiži se uz prvi projekt. |
| Upravljanje projektom i računovodstvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kada odaberete **Skup financijske dimenzije** na prijedlogu fakture pojavljuje se sljedeća pogreška: "Nije moguće pretvoriti objekt tipa 'Dynamics.AX .Application.FormIntControl' za upis 'Dynamics.AX .Application.FormStringControl'." |
| Upravljanje projektom i računovodstvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Izvješće o **Fakturi projekta** preskače retke. |
| Upravljanje projektom i računovodstvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Pogreška se javlja kada izračunavate kontrolu troškova za investicijski projekt. |
| Upravljanje projektom i računovodstvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metoda **ProjTable::InitFromCustTable - canDeletePostalAddress** uzrokuje problem s performansama. |
| Upravljanje projektom i računovodstvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Poruka o pogrešci trebala bi biti jasnija od "Neočekivana pogreška". |
| Upravljanje projektom i računovodstvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Skupno knjiženje Fakture projekte obrađuje i knjiži prijedlog fakture čak i ako reci fakture nisu generirani. |
| Upravljanje projektom i računovodstvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Do problema sa zaokruživanjem dolazi kada je ključ za konfiguraciju licence javnog sektora isključen. Netočan trošak ili prodajna cijena generira se na satima vremenskog lista za ugovore koji imaju više izvora osnivanja. |
| Upravljanje projektom i računovodstvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodajna cijena projekta na fakturiranoj narudžbenici projekta pogrešno je izračunata kada je model prodajne cijene **Omjer doprinosa**. |
| Upravljanje projektom i računovodstvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sustav ne uzima u obzir aktivne dane u međuvremenu kada izračunava efektivnu stopu rada za zaposlenika. |
| Upravljanje projektom i računovodstvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Pogreška u knjiženju javlja se u međukompanijskom vremenskom listu zbog sljedeće pogreške provjere valjanosti: "Nijedan trgovački partner nije konfiguriran za pravnu osobu." |
| Upravljanje projektom i računovodstvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis iz narudžbenice koja ima kategoriju troška nije dohvaćen na popisu knjiženih transakcija projekta. |
| Upravljanje projektom i računovodstvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Postoji netočna konverzija u dnevnicima stavki koje su knjižene u projektu. |
| Upravljanje projektom i računovodstvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Možete potvrditi narudžbenicu čak i ako je ograničenje financiranja premašeno. |
| Upravljanje projektom i računovodstvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Odjeljak **Ispravak/Poništenje računa** na fakturi sa slobodnim tekstom nestaje kada se odabere ID projekta. |
| Upravljanje projektom i računovodstvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Postoje problemi s performansama kada se prijedlog projektne fakture knjiži iz projektnog prodajnog naloga koji uključuje stavku na zalihama. |
| Upravljanje projektom i računovodstvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Fakture za kupnju projekta ne mogu se knjižiti jer se pojavljuje sljedeća pogreška: "Function AccDistProcessorProjectExtension.createForProjectRevenueLine nije ispravno pozvana." |
| Upravljanje projektom i računovodstvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Ažuriranje stvaranja skupnih poslova procjene projekta za podršku izvršenju više podzadataka. |
| Upravljanje projektom i računovodstvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status vremenskog lista ne može se ažurirati na **Nacrt** kada tijek rada zapne u stanju **Otkazano**. |
| Upravljanje projektom i računovodstvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Iznosi zadržavanja ne izračunavaju se u prijedlogu fakture kreditnog odobrenja ako postoji više redaka. |
| Upravljanje projektom i računovodstvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kada pokušate promijeniti iznos na generiranoj fakturi iz narudžbenice, javlja se sljedeća pogreška: "Transakcije na vaučeru nisu u ravnoteži prema XX/XX/XXXX. (računovodstvena valuta: 0,00 – izvještajna valuta: 0,01)” |
| Upravljanje projektom i računovodstvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Postoji problem s izvedbom kada se prijedlog fakture projekta knjiži u skupnom načinu rada zbog spajanja s **GeneralJournalAccountEntry**. |
| Upravljanje projektom i računovodstvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Postoje problemi s performansama kada se objavi vremenski list. |
| Upravljanje projektom i računovodstvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hijerarhija procjena troškova strukturne analize rada nije ispravno usklađena nakon što su svi zadaci prošireni ili nakon što je jedan zadatak ručno proširen. |
| Upravljanje projektom i računovodstvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excel predložak ponude projekta ne može se dodati u izbornik **Otvori u Excelu**. |
| Upravljanje projektom i računovodstvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Broj oslobođenja poreza za pravnu osobu nije uključen na ispisanoj fakturi za projekt. |
| Upravljanje projektom i računovodstvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Kada prilagodite projekt u odnosu na retke kredita, ne ažuriraju se financijski podaci u pogrešci jedinice zaliha. |
| Upravljanje projektom i računovodstvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Nakon što primijenite KB 461935, ne možete knjižiti procjene ako se prebacite na kontinuirane nizove brojeva. |
| Upravljanje projektom i računovodstvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** uzrokuje prestanak rada mobilne aplikacije Project timesheet za Android. |
| Upravljanje projektom i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrnuta vrijednost WIP-a iz knjiženja računa razlikuje se od izvorne knjižene vrijednosti WIP-a iz unosa vremena. |
| Upravljanje projektom i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Transakcije na vaučeru nisu uravnotežene kada se knjiži fakturirani prihod u primijenjenom slučaju zadržavanja dijela plaćanja. |
| Upravljanje projektom i računovodstvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Kada je omoguućena značajka **Poboljšanje performansi planiranja resursa projekta**, decimalne vrijednosti netočno su zaokružene za dostupnost resursa i kapacitet. |
| Upravljanje projektom i računovodstvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Kada je omogućena značajka **Izrada procjena projekta s pomoću više skupnih zadataka**, stvaranje procjena u skupini koja ima više podzadataka radi samo za trenutačno razdoblje. |
| Putovanje i trošak | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Pravila za putni nalog zanemaruju se kako bi se odobrio tijek rada bez pogrešaka. |
| Putovanje i trošak | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikacija Mobile Expense ne sprema sljedeće informacije u retku troškova:</p><ul><li>ID projekta</li><li>Je li trošak naplativ</li><li>Broj aktivnosti</li></ul> |
| Putovanje i trošak | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Polje **Priložena potvrda** postavljeno je na **Da** čak i ako redak troška nema priloženu potvrdu. |
| Putovanje i trošak | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Greška se javlja kada kategoriju troška promijenite u **Osobni**. |
| Putovanje i trošak | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Nakon što se transakcija kreditnom karticom podijeli na osobne troškove, ne možete priložiti potvrdu ni urediti nadređeni trošak. |
| Putovanje i trošak | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Pravila o trošku za transakcije među poduzećima s ID-om projekta ne rade ispravno. |
| Putovanje i trošak | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Nedostaje datum knjiženja za proknjižena izvješća o troškovima. |
| Putovanje i trošak | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | U mobilnoj aplikaciji Expense postoje problemi s načinom plaćanja. |
| Putovanje i trošak | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Putni nalog stvoren za jednog radnika može se upotrijebiti za izvješće o troškovima drugog radnika prije delegiranog datuma. |
| Putovanje i trošak | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kada se stvori trošak, promjena vrijednosti financijske veličine ne ažurira se ispravno na razini računovodstvene distribucije u radni prostor **Upravljanje troškovima**. |
| Putovanje i trošak | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status odobrenja glavnog retka troška nije sinkroniziran sa statusom odobrenja tijeka rada po pojedinom retku. |
| Putovanje i trošak | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Do pogreške dolazi ako knjižite izvješće o trošku, a povrat poreza je omogućen. |
| Putovanje i trošak | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegat ne može izbrisati dokumente o trošku za zaposlenika koji je dobio otkaz. |
| Putovanje i trošak | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Brisanje retka troškova traje dulje od očekivanog i utječe na performanse. |
| Putovanje i trošak | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** uzrokuje zaostali zapis **TaxUncommitted** zato što je izbrisan samo **SourceDocumentLine**. |
| Putovanje i trošak | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ne dozvoljava da **trvExpTrans.ReferenceDataAreaId** stvori novi slijed brojeva. |

## <a name="regulatory-updates"></a>Ažuriranja propisa

Za informacije o ažuriranjima propisa za aplikacije za financije i operacije pogledajte članak [Ažuriranja propisa](/dynamics365/finance/localizations/regulatory-updates). Također se možete prijaviti u Microsoft Dynamics Lifecycle Services (LCS) i upotrijebiti alat za pretraživanje problema da biste pregledali planirana ažuriranja propisa. Pretraživanje problema omogućuje vam pretraživanje po zemlji ili regiji, vrsti značajke i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
