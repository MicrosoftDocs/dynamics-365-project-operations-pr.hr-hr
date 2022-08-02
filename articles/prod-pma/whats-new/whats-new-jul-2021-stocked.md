---
title: Novosti ili izmjene u aplikaciji Project Operations u srpnju 2021., za scenarije koji se temelje na zalihama / proizvodnji
description: U ovom se članku nalaze informacije o ažuriranjima kvalitete dostupnima u izdanju projektnih operacija u srpnju 2021. za scenarije koji se temelje na zalihama/proizvodnji.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: c04d0465f5f7dd43ba50d4c0d2937b45fed6df86
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028831"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novosti ili izmjene u aplikaciji Project Operations u srpnju 2021., za scenarije koji se temelje na zalihama / proizvodnji

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

Ovaj se članak odnosi na sljedeće Dynamics 365 Project Operations komponente i verzije:

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.20
 
### <a name="quality-updates"></a>Ažuriranja kvalitete
                                                                                                                                                                                  
| Područje značajke                      | Broj reference| Ažuriranja kvalitete                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upravljanje projektom i računovodstvo | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Zbog problema u zahtjevu za kupnju, evidencija obveze za troškove iz zahtjeva za kupnju briše se čim se izda narudžbenica.                                                                           |
| Upravljanje projektom i računovodstvo | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Provjera valjanosti proračuna događa se dva puta na zahtjevu za kupnju. Ovo dupliciranje znači da se zahtjev ne može zatvoriti i da se nije stvorila odgovarajuća narudžbenica.                                                                                                                        |
| Upravljanje projektom i računovodstvo | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Pravilo naplate **Postotak za naplatu** nije se moglo dovršiti zbog problema sa zaokruživanjem.                                                                              |
| Upravljanje projektom i računovodstvo | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Kada prilagodite transakciju i postotak sadrži decimale, trošak i prodajna cijena ne prilagođavaju se ispravno.                                      |
| Upravljanje projektom i računovodstvo | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Alat za istraživanje računovodstvenog izvora prikazuje sate iz jednog retka tablice radnog vremena za više redaka iz te tablice s različitim aktivnostima.                                      |
| Upravljanje projektom i računovodstvo | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Spremljeni prikazi i prilagodba pojedinosti retka tablice radnog vremena uzrokuju da sustav uvijek pokušava otvoriti pojedinosti za prvu tablicu radnog vremena na popisu pri pokušaju otvaranja tablice radnog vremena.  |
| Upravljanje projektom i računovodstvo | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Korijenski čvor projekta nestaje, a zapisi strukturne analize rada brišu se nakon uvoza.                                                                                             |
| Upravljanje projektom i računovodstvo | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Kada se stavke iz zahtjeva za stavkom prime i izdaju djelomično, sustav ažurira pogrešan saldo potrošnje proračuna. |
| Upravljanje projektom i računovodstvo | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Narudžbenice za zadržavanje dijela iznosa plaćanja za projekt ne prikazuju ispravno ukupne vrijednosti u oknu **Ukupno** ili rešetki **Faktura na čekanju**.                                                                  |
| Upravljanje projektom i računovodstvo | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Pri zatvaranju zaliha, prilagodbe troškova projektnih stavki knjiže se na račun salda umjesto na račun dobiti i gubitka.                                                            |
| Upravljanje projektom i računovodstvo | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Vaučer za transakcije knjižene u projektu i vaučer za procjene upotrebljavaju USD kao računovodstvenu valutu, ali iznos pokazuje koliki bi bio ekvivalent u valuti CAD.              |
| Upravljanje projektom i računovodstvo | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Učinjeni troškovi sa zahtjevom za stavku i narudžbenicom pogrešni su u postupku fakturiranja narudžbenice s djelomičnim primitkom proizvoda i djelomičnim fakturiranjem.       |
| Upravljanje projektom i računovodstvo | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Prilagodba projekta ne ažurira ispravno iznos prodaje s neizravnim troškovima.                                                                                    |
| Upravljanje projektom i računovodstvo | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tablici **Tablica radnog vremena** nedostaje definirani odnos s prikazom **Radnik/Resurs**.                                                                                   |
| Upravljanje projektom i računovodstvo | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Nije moguće popuniti polje **Broj aktivnosti** kada ga odaberete s padajućeg izbornika za tablicu radnog vremena ostvarenog između poduzeća unutar iste tvrtke.                                                                 |
| Upravljanje projektom i računovodstvo | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Ne možete dodati prilagođeno polje **Svrha** ili **Opis aktivnosti** na sljedeće stranice: **Proknjižena transakcija projekta**, **Stvaranje prijedloga fakture** ili **Prijedlog fakture**.  |
| Upravljanje projektom i računovodstvo | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Pogrešna kontrola datuma isporuke daje se kada stvarate zahtjeve za stavkom s pomoću upravljanja podacima (**ProjSalesItemRequirementEntity**).                                              |
| Upravljanje projektom i računovodstvo | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Kada u aplikaciji Financije odaberete ID ugovora o projektu, integrirano okruženje aplikacije Project Operations otvara stranicu za stvaranje novog zapisa, umjesto otvaranja postojećeg ugovora o projektu.                                                                                                                 |
| Upravljanje projektom i računovodstvo | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Oznaka „@SYS4083080” („Nije moguće pronaći jedinstveni zapis o radniku koji se podudara s unesenim vrijednostima”) nije prevedena na danski jezik.                                |
| Upravljanje projektom i računovodstvo | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Polje **Grupa poreza na promet za stavku** ne može se uređivati na prijedlogu fakture.                                                                               |
| Upravljanje projektom i računovodstvo | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Učinjeni se troškovi preuveličavaju iznosima poreza koji se ne mogu otpisati.                                                                                                    |
| Upravljanje projektom i računovodstvo | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Knjiženje tablice radnog vremena ostvarenog među poduzećima iste tvrtke s više projekata i različitim financijskim veličinama generira neočekivane vrijednosti u glavnoj knjizi.                             |
| Upravljanje projektom i računovodstvo | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Redci prijedloga fakture duplicirani su zbog višestrukih instanci povremenih postupaka **Uvoz iz faza** koji se odvijaju istodobno.                                      |
| Upravljanje projektom i računovodstvo | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Došlo je do pogreške pri knjiženju prijedloga računa s kreditnom bilješkom, tako da se transakcije na vaučeru ne saldira.    |
| Upravljanje projektom i računovodstvo | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Troškovi učinjeni na projektu postaju netočni nakon što se izdaju fakture koje su na čekanju.                                                                             |
| Upravljanje projektom i računovodstvo | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Ne možete stvoriti kreditnu bilješku za narudžbu za prodaju projekta kada je porez u valuti koja se razlikuje od valute tvrtke.                                      |
| Upravljanje projektom i računovodstvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Brisanjem ugovora briše se i adresa povezana s klijentom.                                                                                     |
| Upravljanje projektom i računovodstvo | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Nije moguće knjižiti prijedlog fakture nastao iz ispravka negativne vremenske transakcije.                                                                    |
| Putovanje i trošak                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Porez se različito obračunava u izvješćima o troškovima.                                                                                                                  |
| Putovanje i trošak                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Ažuriranje izdanja **DB72_Expense.updateTrvExpTransProjTransId ()** ne dozvoljava da **trvExpTrans.Refer enceDataAreaId** stvara novi slijed brojeva.                    |
| Putovanje i trošak                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Polje s iznosom ne prikazuje se uz obvezno polje.                                                                                                             |
| Putovanje i trošak                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Poboljšanja u izvedbi pridruživanja troškova izvješću o troškovima s pomoću izmijenjenog korisničkog sučelja aplikacije Trošak.                                                            |
| Putovanje i trošak                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Možete izbrisati proknjižena izvješća o troškovima.                                                                                           |
| Putovanje i trošak                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Poruka Pravila o troškovima prikazuje se više puta.                                                                                                       |
| Putovanje i trošak                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Polje **Način plaćanja** uključeno je u okno **Novi trošak**.                                                                                                      |
| Putovanje i trošak                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Alat **Vrati stanje dokumenta o troškovima na zadano** trebao bi vratiti stanje izvješća o troškovima na **Skica** ako se ne pronađe tijek rada. 

### <a name="regulatory-updates"></a>Ažuriranja propisa
Informacije o regulatornim ažuriranjima za financijske i operativne aplikacije potražite u članku [Regulatorna ažuriranja](/dynamics365/finance/localizations/regulatory-updates). Također se možete prijaviti u aplikaciju Lifecycle Services (LCS) i pregledati planirana regulatorna ažuriranja s pomoću alata za pretraživanje problema. Pretraživanje izdanja omogućuje vam pretraživanje po zemlji, vrsti značajke i izdanju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
