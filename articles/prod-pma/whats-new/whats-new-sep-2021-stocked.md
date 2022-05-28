---
title: Što je novo ili promijenjeno u projektnim operacijama, rujan 2021. za scenarije koji se temelje na zalihama/proizvodnji
description: Ovaj tema pruža informacije o ažuriranjima kvalitete koja su dostupna u izdanju projektnih operacija u rujnu 2021. za scenarije koji se temelje na zalihama/proizvodnji.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582011"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Što je novo ili promijenjeno u projektnim operacijama, rujan 2021. za scenarije koji se temelje na zalihama/proizvodnji

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

Ovaj tema odnosi se na sljedeće microsoftove Dynamics 365 Project Operations komponente i verzije :

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.21
 
## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
|---|---|---|
| Upravljanje projektom i računovodstvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Ako uloga upravitelja nabave ima pristup jednoj pravnoj osobi, ona također dobiva pristup svim projektima u svim pravnim osobama. |
| Upravljanje projektom i računovodstvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Problem zaokruživanja poreza na dodanu vrijednost (PDV) pojavljuje se dok se kreditna bilješka podmiruje prema izvornoj fakturi projekta. |
| Upravljanje projektom i računovodstvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Upotrijebite zamjenski proračun projekta za provjeru proračuna. |
| Upravljanje projektom i računovodstvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Grupa cijena prodajnih **sati** ne izračunava se na strukturi raščlambe rada za navodnike projekta. |
| Upravljanje projektom i računovodstvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Uklanjanje procjene ne uspijeva kada je omogućena značajka Omogući valutu **ugovora o projektu za izračun** procjene. |
| Upravljanje projektom i računovodstvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizacija poreza na promet po količini dodaje se iznosu prodajne cijene kada se porez na korištenje koristi u grupi poreza na promet temeljnice troškova projekta. |
| Upravljanje projektom i računovodstvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Uvjetni porez ne izračunava se ispravno za posljednju uplatu kada se zadržavanje dobavljača i akontacija/pretplata primjenjuju na fakture narudžbenice. |
| Upravljanje projektom i računovodstvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Praćenje prilagođavanja ne funkcionira za početne temeljnice salda. |
| Upravljanje projektom i računovodstvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Dodjela revizije proračuna projekta po razdoblju** podijeljena je na sva proračunska razdoblja. Kada se alokacija pošalje, zapis se ne briše. |
| Upravljanje projektom i računovodstvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Knjiženja za rad u tijeku (PUT) u glavnu knjigu imaju netočan iznos. |
| Upravljanje projektom i računovodstvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Odobrenje temeljnice sati projekta ne funkcionira. |
| Upravljanje projektom i računovodstvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodajna cijena za prilagodbu projekta ne ažurira se neizravnim troškovima kada ograničenje financiranja nije zabilježeno. |
| Upravljanje projektom i računovodstvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Zahtjev za artiklom nije moguće kreirati kada je zaglavlje tablice Prodaja fakturirano, a rezervna narudžbenica za postojeće retke dovršena. |
| Upravljanje projektom i računovodstvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Iznos zadržavanja za pravilo naplate koje ima prekretnicu za drugi projekt nije objavljen u odgovarajućem ID-u projekta odabranom za prekretnicu. Umjesto toga, objavljeno je s prvim projektom. |
| Upravljanje projektom i računovodstvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kada odaberete **Financijska dimenzija postavljena** na prijedlogu fakture, pojavljuje se sljedeća pogreška: "Nije moguće baciti objekt vrste 'Dynamics.AX" Application.FormIntControl' za upisivanje 'Dynamics.AX. Aplikacija.FormStringControl'." |
| Upravljanje projektom i računovodstvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Izvješće o fakturi **projekta** preskače retke. |
| Upravljanje projektom i računovodstvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Pri izračunu kontrole troškova za investicijski projekt pojavljuje se pogreška. |
| Upravljanje projektom i računovodstvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metoda **ProjTable:: InitFromCustTable - canDeletePostalAddress** uzrokuje problem s performansama. |
| Upravljanje projektom i računovodstvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Poruka o pogrešci trebala bi biti jasnija od "Neočekivana pogreška". |
| Upravljanje projektom i računovodstvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Obrada Knjiženje fakture Projekta obrađuje i knjiži prijedlog fakture čak i ako reci fakture nisu generirani. |
| Upravljanje projektom i računovodstvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Problem s zaokruživanjem pojavljuje se kada je isključen ključ za konfiguriranje licence javnog sektora. Netočan trošak ili prodajna cijena generiraju se u satima vremenske tablice za ugovore koji imaju više izvora utemeljitelja. |
| Upravljanje projektom i računovodstvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodajna cijena projekta na fakturiranoj narudžbenici projekta pogrešno se izračunava kada je **model prodajne cijene omjer doprinosa**. |
| Upravljanje projektom i računovodstvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sustav ne uzima u obzir aktivne dane između kada izračunava efektivnu stopu rada za zaposlenika. |
| Upravljanje projektom i računovodstvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Na međukompanijskom vremenskom listu pojavljuje se pogreška pri knjiženju zbog sljedeće pogreške provjere valjanosti: "Nijedan trgovinski partner nije konfiguriran za pravnu osobu." |
| Upravljanje projektom i računovodstvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis iz narudžbenice koja ima kategoriju troškova ne dohvaća se na popisu proknjiženih projektnih transakcija. |
| Upravljanje projektom i računovodstvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Došlo je do pogrešne konverzije u temeljnicama artikla koje su proknjižene u projekt. |
| Upravljanje projektom i računovodstvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Narudžbenicu možete potvrditi čak i ako je prekoračeno ograničenje financiranja. |
| Upravljanje projektom i računovodstvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Odjeljak **Ispravak/Odustani od fakture** na besplatnoj tekstualnoj fakturi nestaje kada je odabran ID projekta. |
| Upravljanje projektom i računovodstvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Postoje problemi s performansama kada se prijedlog fakture za projekt knjiži iz naloga za prodaju projekta koji obuhvaća opskrbljeni artikl. |
| Upravljanje projektom i računovodstvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Ulazne fakture projekta nije moguće knjižiti jer se pojavljuje sljedeća pogreška: "Funkcija AccDistProcessorProjectExtension.createForProjectRevenueLine nije ispravno pozvana." |
| Upravljanje projektom i računovodstvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Ažurirajte na stvaranje obrada procjene projekta da biste podržali izvršavanje više podzadataka. |
| Upravljanje projektom i računovodstvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Stanje vremenske tablice ne može se ažurirati u Skica **kada** je tijek rada zaglavljen u otkazanom **stanju**. |
| Upravljanje projektom i računovodstvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Iznosi zadržavanja ne izračunavaju se u prijedlogu fakture za kreditnu bilješku ako postoji više redaka. |
| Upravljanje projektom i računovodstvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kada pokušate promijeniti iznos na generiranoj fakturi iz narudžbenice, pojavljuje se sljedeća pogreška: "Transakcije na vaučeru ne balansiraju prema XX/XX/XXXX. (računovodstvena valuta: 0,00 – izvještajna valuta: 0,01)” |
| Upravljanje projektom i računovodstvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Postoji problem s performansama kada se prijedlog fakture projekta proknjiži u skupnom načinu rada zbog pridruživanja **generaljournalAccountEntry**. |
| Upravljanje projektom i računovodstvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Postoje problemi s performansama prilikom knjiženja vremenske tablice. |
| Upravljanje projektom i računovodstvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hijerarhija procjena troškova strukture kvara rada nije ispravno poravnana nakon proširenja svih zadataka ili nakon ručnog proširenja jednog zadatka. |
| Upravljanje projektom i računovodstvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Predložak programa Excel s citatom projekta ne može se dodati na **izbornik Otvori u programu Excel**. |
| Upravljanje projektom i računovodstvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Broj oslobođenog poreza za pravnu osobu nije uključen u tiskani projektni račun. |
| Upravljanje projektom i računovodstvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | U pogrešci jedinice zaliha ne ažuriraju se financijski podaci kada se projekt prilagodi u odnosu na kreditne retke. |
| Upravljanje projektom i računovodstvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Nakon što primijenite KB 461935, ne možete knjižiti procjene ako prijeđete na neprekinute brojčane sekvence. |
| Upravljanje projektom i računovodstvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** uzrokuje prestanak reagiranja mobilne aplikacije Vremenska Android tablica projekta. |
| Upravljanje projektom i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Reverzirana vrijednost PUT-a iz knjiženja fakture razlikuje se od izvorno proknjižene vrijednosti PUT-a od stavke vremena. |
| Upravljanje projektom i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | U primijenjenim slučajevima akontacije transakcije na vaučeru ne saldiraju se prilikom knjiženja fakturiranog prihoda za projekt. |
| Upravljanje projektom i računovodstvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Kada je omogućena **značajka poboljšanja** performansi zakazivanja resursa programa Project, decimalne vrijednosti pogrešno se zaokružuju za dostupnost resursa i kapacitet. |
| Upravljanje projektom i računovodstvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Kada je omogućena **značajka Kreiraj procjene projekta pomoću više skupnih zadataka**, stvaranje procjena u seriji koja ima više podzadataka funkcionira samo za tekuće razdoblje. |
| Putovanje i trošak | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Pravilo zahtjevnice za putovanje se zanemaruje, a tijek rada se odobrava bez pogrešaka. |
| Putovanje i trošak | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikacija Mobilni trošak ne sprema sljedeće podatke u redak troška:</p><ul><li>ID projekta</li><li>Je li trošak naplativ</li><li>Broj aktivnosti</li></ul> |
| Putovanje i trošak | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Polje **Priložene primke** postavljeno je na **Da** čak i ako retku rashoda nije priložena primka. |
| Putovanje i trošak | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Pogreška se pojavljuje kada promijenite kategoriju troškova u **Osobno**. |
| Putovanje i trošak | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Ne možete priložiti potvrdu i urediti nadređeni trošak nakon što se transakcija kreditnom karticom podijeli s osobnim troškom. |
| Putovanje i trošak | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Politika troškova za međukompanijske transakcije koje imaju ID projekta ne funkcionira ispravno. |
| Putovanje i trošak | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Proknjiženi podaci o datumu nedostaju za proknjižena izvješća o troškovima. |
| Putovanje i trošak | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | U mobilnoj aplikaciji Expense postoje problemi s načinom plaćanja. |
| Putovanje i trošak | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Zahtjev za putovanje koji je stvoren za jednog radnika može se koristiti za izvješće o troškovima drugog radnika prije datuma delegata. |
| Putovanje i trošak | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kada kreirate trošak, promjene vrijednosti financijske dimenzije ne ažuriraju se ispravno na razini računovodstvene raspodjele u **radnom prostoru za upravljanje troškovima**. |
| Putovanje i trošak | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Stanje odobrenja retka glavnog troška nije sinkronizirano sa statusom odobrenja tijeka rada retka po stavkama. |
| Putovanje i trošak | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Pogreška se pojavljuje ako proknjižite izvješće o troškovima i ako je omogućen povrat poreza. |
| Putovanje i trošak | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegat ne može izbrisati dokumente o trošku za zaposlenika koji je dobio otkaz. |
| Putovanje i trošak | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Brisanje linije troškova traje dulje od očekivanog i utječe na performanse. |
| Putovanje i trošak | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** uzrokuje napušteni **zapis TaxUncommitted**, jer se briše samo **SourceDocumentLine**. |
| Putovanje i trošak | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ne poštuje **trvExpTrans.ReferenceDataAreaId** za stvaranje novog brojčanog slijeda. |

## <a name="regulatory-updates"></a>Ažuriranja propisa

Informacije o regulatornim ažuriranjima za aplikacije Financije i operacije potražite u članku [Regulatorna ažuriranja](/dynamics365/finance/localizations/regulatory-updates). Također se možete prijaviti Microsoft Dynamics u usluge životnog ciklusa (LCS) i pomoću alata za pretraživanje problema pregledati planirana regulatorna ažuriranja. Pretraživanje problema omogućuje vam pretraživanje po zemlji ili regiji, vrsti značajke i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
