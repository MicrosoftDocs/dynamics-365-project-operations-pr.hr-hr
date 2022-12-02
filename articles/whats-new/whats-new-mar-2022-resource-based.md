---
title: Novosti u ožujku 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Project Operations za ožujak 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910897"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u ožujku 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.30.0.99
- Upravljanje projektima i računovodstvo u verziji 10.0.25 okruženja aplikacije Dynamics 365 Finance

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

Dnevnice su sada podržane u novom i preuređenom modernom radnom prostoru za troškove. Tvrtke koje koriste dnevnice mogu omogućiti ovu značajku kako bi korisnicima omogućile jednostavan način podnošenja i nadoknade troškova dnevnica. Dodatne informacije potražite u članku [Troškovi dnevnica](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeći popis prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanje aplikacije Project Operations za ožujak 2022.

| **Karta entiteta** | **Ažurirana verzija** | **Komentari** |
| --- | --- | --- |
| Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapiranja ažurirana radi usklađivanja s entitetom retka fakture dobavljača na platformi Dataverse. <br>Nemojte aktivirati verziju mapiranja 1.0.0.4. Bit će spremna za korištenje u kombinaciji s verzijom okruženja Finance 10.0.26 u sljedećem mjesečnom ažuriranju. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Vrijeme i trošak | 2388011 | Prikaži komentare odbijanja podnositeljima unosa vremena tijekom skupnog odobrenja. |
| Planiranje i praćenje projekta | 2495294 | Detalji projekta ne smiju se moći uređivati na stranici **Detalji zadatka**. |
| Naplata i određivanje cijene | 2499605 | Ključne točke ugovora koje su stvorene iz ključnih točaka ponude neispravno su označene kao samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promjena za spremanje. Skup je tada lažno označen kao **Neuspjeh** iako bi trebao biti dovršen odmah. |
| Naplata i određivanje cijene | 2507401 | Zadane ugovorne jedinice netočno su unesene u projekte zbog netočnog predmemoriranja. |
| Naplata i određivanje cijene | 2541660 | **Provjera valjanosti izrade prodajnog naloga** u dvostrukom pisanju treba biti samo za narudžbe temeljene na projektu. |
| Naplata i određivanje cijene | 2552745 | Porez se ne dijeli među kupcima koji su postavili pravila podijeljene naplate. |
| Naplata i određivanje cijene | 2558859 | Poboljšane poruke o pogrešci kada se postavljaju dimenzije cijena. |
| Naplata i određivanje cijene | 2558933 | **Uvoz iz procjena projekta** ne uspije kada se **msdyn\_project** dodaje kao dimenzija cijene. |
| Naplata i određivanje cijene | 2559101 | Brisanje parametara projekta nije blokirano i uzrokuje probleme. |
|   Upravljanje prilikama | 2570390 | Dodatak za dvostruko pisanje prisiljava vrstu računa za ponude, narudžbe i prilike da bude **Kupac**, čak i kada ta vrsta računa nije ispravna. |
| Naplata i određivanje cijene | 2586097 | Stvarne vrijednosti podijeljenog naplaćenog troška ne poništavaju se kada se projekt ukloni iz retka ugovora o projektu. |
| Naplata i određivanje cijene | 2589619 | Porez na upisani materijal prenosi se na stvarne vrijednosti nenaplaćene prodaje i fakturu. |
|   Upravljanje prilikama | 2594015 | Ponuda se ne može zatvoriti kao dobivena za kupce koji imaju uvjete plaćanja **Net60**. |
| Planiranje i praćenje projekta | 2595841 | U aplikaciji Project for the Web korisnici dobivaju poruku o pogrešci o nedostatku **msdyn\_actualstart** kada kreiraju novi zahtjev za resurs. |
| Vrijeme i trošak | 2602511 | Polje **Odbijen od strane** za unose vremena prikazuje **Sustav** umjesto imenovanog korisnika kao onog koji je odbio. |
| Vrijeme i trošak | 2602528 | Osoba koja odobrava projekte može odobriti vrijeme za projekte za koje nije navedena kao osoba koja odobrava. |
| Naplata i određivanje cijene | 2608550 | Ispravak računa može se potvrditi čak i ako nema promjena na izvorniku. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Postoji neusklađenost između Financija i Project Operations u dopuštenoj duljini polja **ID kategorije**. |
| Upravljanje projektom i računovodstvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekti s fiksnom cijenom ne mogu se eliminirati kada je polje **Fakturiranje po računu** postavljeno na **Dobit i gubitak** i koristi se načelo **Postotak dovršenosti**. |
| Upravljanje projektom i računovodstvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Netočna zadana grupa poreza na promet unesena je iz postavki projekta u recima troškova u dnevniku integracije Project Operations. |
| Upravljanje projektom i računovodstvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Ne možete uređivati dimenzije zaglavlja prijedloga fakture projekta u integriranoj implementaciji s aplikacijom Project Operations. |
| Upravljanje projektom i računovodstvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Međukompanijske fakture dobavljača ne smiju se integrirati s Dataverse. |
| Upravljanje projektom i računovodstvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Postoji neusklađenost u valuti stanja klijenta i valuti izvješća. |
| Upravljanje projektom i računovodstvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Možete knjižiti projektnu fakturu čak i ako je korisnik na čekanju za sve fakture. |
| Upravljanje projektom i računovodstvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Gumb **Izbriši sve retke** nedostaje u prijedlozima projektnih faktura koji imaju prikaze **Zaglavlje** i **Reci**. |
| Upravljanje projektom i računovodstvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Kada knjižite fakturu dobavljača, pojavljuje se sljedeća pogreška: "Računovodstveni datum za fakturu mora biti u istoj računovodstvenoj godini kao i povezana narudžba. Pokrenite proces završetka godine narudžbenice ili promijenite datum tekuće računovodstvene godine." |
| Putovanje i trošak | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Preuzeti trošak za projekt ne objavljuje se nakon zatvaranja putnog naloga s preuzetim troškom. |
| Putovanje i trošak | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Sljedeća se pogreška javlja kada predate izvješće o troškovima: "Stack Trace: tvrtka ne postoji." |
| Putovanje i trošak | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Zadana vrijednost **ID projekta** ne unosi se u izvješća o troškovima kada je parametar **Zahtijeva aktivnost za dnevnik** odabran u projektu. |
| Putovanje i trošak | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Gumb **Troškovi knjiženja** ne radi ispravno u aplikaciji Project Operations za scenarije resursa / bez zaliha. |
| Putovanje i trošak | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Postoji problem sa **Cijenom po kilometru** za izvješće o troškovima kilometraže koje uključuje putnike. |
| Putovanje i trošak | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Stope troškovne kilometraže za zaposlenike nisu točno zbrojene kada se koriste dvije različite vrste vozila u kategoriji troškova **Razine stope kilometraže**. |
| Putovanje i trošak | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Traženje za polje **Projekt** u retku zahtjeva za putovanje ne vraća točan popis projekata. |
| Putovanje i trošak | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraža na pregledu** prikazuje upozorenje u izvješćima o troškovima. |
| Putovanje i trošak | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Usluga optičkog prepoznavanja znakova (OCR) računa ne radi zbog problema s URL-om usluge OCR za troškove. |
| Putovanje i trošak | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Kada je omogućena značajka **Sposobnost brzog popisivanja tekućih troškova**, iznosi u recima stavki u izvješćima o troškovima mijenjaju iznose svaki put kada se otvori stranica **Stavke**. |
| Putovanje i trošak | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Ne možete izbrisati izvješće o troškovima ako privremeni popis ima više od jednog odobravatelja. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarjele značajke

Članak [Uklonjene ili zastarjele značajke u aplikaciji Project Operations](removed-depreciated-features-project.md) opisuje značajke koje su uklonjene ili zastarjele za aplikaciju Dynamics 365 Project Operations.

- Značajka uklonjeno više nije dostupna u proizvodu.
- Značajka zastarjelo ne nalazi se u aktivnom razvoju i u nekom budućem ažuriranju može biti uklonjena.

Obavijest o zastarjelosti pojavit će se u članku [Uklonjene ili zastarjele značajke u aplikaciji Project Operations](removed-depreciated-features-project.md) 12 mjeseci prije uklanjanja bilo koje značajke iz proizvoda.

Za prijelomne promjene koje utječu samo na vrijeme kompilacije, ali su binarno kompatibilne sa sigurnim testnim okruženjem i radnim okruženjima, vrijeme zastarjelosti bit će manje od 12 mjeseci. Obično su te promjene funkcionalna ažuriranja koja se moraju izvršiti na kompilatoru.
