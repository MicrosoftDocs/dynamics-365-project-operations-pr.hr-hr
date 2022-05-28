---
title: Novosti u ožujku 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom tema pružaju se informacije o ažuriranjima kvalitete koja su dostupna u izdanju projektnih operacija u ožujku 2022. za scenarije koji se temelje na resursima/nenaseljenim resursima.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600733"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u ožujku 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ovaj tema odnosi se na sljedeće microsoftove Dynamics 365 Project Operations komponente i verzije :

- Operacije projekta u verziji okruženja Dataverse 4.30.0.99
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.25

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

Dnevnice su sada podržane u novom i preoblikovanom modernom radnom prostoru troškova. Tvrtke koje koriste dnevnice mogu omogućiti ovoj značajki da korisnicima pruži jednostavan način podnošenja i povrata troškova dnevnica. Za više informacija pogledajte [troškove dnevnice](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeći popis prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanju Project Operations Ožujak 2022.

| **Karta entiteta** | **Ažurirana verzija** | **Komentari** |
| --- | --- | --- |
| Projekt Operations integracija projekt dobavljač faktura redak izvozni entitet msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Mapiranja su ažurirana da bi se poravnala sa entitetom retka fakture dobavljača u programu Dataverse. <br>Nemojte aktivirati 1.0.0.4 verzije mapiranja. Bit će spreman za upotrebu u kombinaciji s financijskom verzijom okruženja 10.0.26 u sljedećem mjesečnom ažuriranju. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Vrijeme i trošak | 2388011 | Prikažite komentare odbijanja podnositeljima unosa vremena tijekom masovnog odobrenja. |
| Planiranje i praćenje projekta | 2495294 | Pojedinosti o projektu ne smiju se moći uređivati na stranici Detalji o **zadatku**. |
| Naplata i određivanje cijene | 2499605 | Ključne etape ugovora stvorene iz ključnih etapa ponude pogrešno su označene samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promjene za spremanje. Skup je zatim lažno označen kao **Neuspješan**, dok bi ga trebalo odmah dovršiti. |
| Naplata i određivanje cijene | 2507401 | Zadane ugovorne jedinice pogrešno se unose u projekte zbog pogrešnog predmemoriranja. |
| Naplata i određivanje cijene | 2541660 | **Provjera valjanosti stvaranja naloga za** prodaju u dvostrukom pisanju trebala bi biti samo za narudžbe temeljene na projektima. |
| Naplata i određivanje cijene | 2552745 | Porez se ne dijeli između korisnika koji su postavili podijeljena pravila naplate. |
| Naplata i određivanje cijene | 2558859 | Poboljšane poruke o pogreškama prilikom postavljanja dimenzija određivanja cijena. |
| Naplata i određivanje cijene | 2558933 | **Uvoz iz procjena** projekta ne uspijeva kada **se msdyn\_ projekt** doda kao dimenzija određivanja cijena. |
| Naplata i određivanje cijene | 2559101 | Brisanje parametara projekta nije blokirano i uzrokuje probleme. |
|   Upravljanje prilikama | 2570390 | Dodatak s dvostrukim pisanjem prisiljava vrstu računa na ponude, narudžbe i prilike da bude **kupac**, čak i kada ta vrsta računa nije točna. |
| Naplata i određivanje cijene | 2586097 | Stvarni podijeljeni naplaćeni troškovi ne storniraju se kada se projekt ukloni iz retka ugovora o projektu. |
| Naplata i određivanje cijene | 2589619 | Porez na dopisni materijal prenosi se na neplaćene prodajne stvarne vrijednosti i račun. |
|   Upravljanje prilikama | 2594015 | Ponuda se ne može zatvoriti kao osvojena za korisnike koji imaju **Uvjete plaćanja Net60**. |
| Planiranje i praćenje projekta | 2595841 | U programu Project za web korisnici dobivaju poruku o pogrešci o stvarnom pokretanju **msdyna\_ koji nedostaje** prilikom stvaranja novog zahtjeva za resursom. |
| Vrijeme i trošak | 2602511 | Polje **Odbijeno po** za unose vremena prikazuje **Sustav** umjesto imenovanog korisnika kao odbijanje. |
| Vrijeme i trošak | 2602528 | Odobravatelj projekta može odobriti vrijeme na projektima u kojima nisu navedeni kao odobravatelj. |
| Naplata i određivanje cijene | 2608550 | Ispravak fakture može se potvrditi čak i ako nema promjena u izvorniku. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo na Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Postoji nepodudarnost između financija i projektnih operacija u dopuštenoj duljini polja ID **kategorije**. |
| Upravljanje projektom i računovodstvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekti s fiksnom cijenom ne mogu se eliminirati kada **je polje Fakturiranje** na računu postavljeno na **RUC i gubitak**, a **koristi se načelo Postotka** dovršenosti. |
| Upravljanje projektom i računovodstvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Neispravna zadana porezna grupa tržišta unosi se iz postave projekta u retke troškova u temeljnici Integracija operacija projekta. |
| Upravljanje projektom i računovodstvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Ne možete uređivati dimenzije zaglavlja prijedloga fakture projekta u integriranoj implementaciji s operacijama projekta. |
| Upravljanje projektom i računovodstvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Međukompanijske fakture dobavljača ne smiju se integrirati s programom Dataverse. |
| Upravljanje projektom i računovodstvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Postoji nepodudarnost u valuti salda klijenta i izvještajnoj valuti. |
| Upravljanje projektom i računovodstvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Proknjižiti fakturu projekta možete proknjižiti čak i ako je kupac na čekanju za sve fakture. |
| Upravljanje projektom i računovodstvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Gumb **Izbriši sve retke** nedostaje u prijedlozima faktura za projekte koji imaju prikaze **Zaglavlje** i **Reci**. |
| Upravljanje projektom i računovodstvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Kada proknjižite fakturu dobavljača, pojavljuje se sljedeća pogreška: "Datum obračuna za fakturu mora biti u istoj računovodstvenoj godini kao i povezana nabavljena narudžba. Pokrenite postupak na kraju godine narudžbenice ili promijenite datum u tekuću računovodstvenu godinu." |
| Putovanje i trošak | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Predani trošak projekta ne oslobađa se nakon što se oslobodi predani trošak zahtjevnice za putovanje. |
| Putovanje i trošak | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Prilikom slanja izvješća o troškovima pojavljuje se sljedeća pogreška: "Praćenje stoga: Tvrtka ne postoji." |
| Putovanje i trošak | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Zadani **ID** projekta ne unosi se u izvješća o troškovima kada **je u projektu odabran parametar Zatraži aktivnost za temeljnicu**. |
| Putovanje i trošak | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Gumb **Proknjiži troškove** ne radi ispravno u operacijama projekta za scenarije resursa/neutemeljenih resursa. |
| Putovanje i trošak | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Postoji problem sa stopom **po milji** za izvješće o troškovima kilometraže koje uključuje putnike. |
| Putovanje i trošak | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Stope kilometraže troškova za zaposlenike ne zbrajaju se ispravno kada se u **kategoriji troškova** stopa kilometraže koriste dvije različite vrste vozila. |
| Putovanje i trošak | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Pretraživanje polja Projekt **u** retku zahtjevnice za putovanje ne vraća točan popis projekata. |
| Putovanje i trošak | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraža u pregledu** pokazuje upozorenje o izvješćima o troškovima. |
| Putovanje i trošak | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Usluga optičkog prepoznavanja znakova (OCR) s potvrdom ne radi zbog problema s URL-om OCR usluge troškova. |
| Putovanje i trošak | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Kada je omogućena **značajka Mogućnost brzog** izdvajanja ponavljajućih troškova, iznosi u recima artikla u izvješćima o troškovima mijenjaju iznose svaki put kada **se otvori stranica Itemize**. |
| Putovanje i trošak | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Izvješće o troškovima ne možete izbrisati ako privremeni popis ima više odobravatelja. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarjele značajke

Uklonjene [ili zastarjele značajke u projektnim operacijama](removed-depreciated-features-project.md) tema opisuju značajke koje su uklonjene ili zastarjele za Dynamics 365 Project Operations.

- Značajka uklonjeno više nije dostupna u proizvodu.
- Zastarjela značajka nije u aktivnom razvoju i može se ukloniti u budućem ažuriranju.

Najava omalovažavanja pojavit će se u [značajkama Uklonjeno ili zastarjelo u projektnim operacijama](removed-depreciated-features-project.md) tema 12 mjeseci prije nego što se bilo koja značajka ukloni iz proizvoda.

Za razbijanje promjena koje utječu samo na vrijeme kompilacije, ali su binarno kompatibilne s sandboxom i proizvodnim okruženjima, vrijeme omalovažavanja bit će manje od 12 mjeseci. Obično su te promjene funkcionalna ažuriranja koja se moraju izvršiti na kompajleru.
