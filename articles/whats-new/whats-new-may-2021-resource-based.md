---
title: Novosti u svibnju 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnimaa u izdanju aplikacije Project Operations za svibanj 2021. za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cc5e8104702951fd787d02407d26671e46d44f0c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029980"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u svibnju 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

- Project Operations u verziji 4.10.0.186 okruženja platforme Dynamics 365 Dataverse
- Upravljanje projektima i računovodstvo u okruženjima aplikacija za financije i operacije verzije 10.0.18

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- [Načini planiranja](../project-management/scheduling-modes.md): Voditelji projekata mogu definirati treba li projektom upravljati s pomoću fiksnog trajanja, fiksnog rada ili načina planiranja fiksnih jedinica.
- [Postavljanje kilometraže s pomoću cjenovnih razina kilometraže](../expense/set-up-mileage.md): Ažurirajte cjenovne razina kilometraže za izvješća o troškovima zaposlenika.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeći popis prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanje aplikacije Project Operations za svibanj 2021. godine.

| Karta entiteta | Ažurirana verzija | Komentari |
| --- | --- | --- |
| Izvor financiranja projekta (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sinkronizirajte uvjeta plaćanja prema ugovoru o projektu. |
| Prijedlog fakture za projekt V2 (fakture) | 1.0.0.3 | Sinkronizacija uvjeta plaćanja po predračunu. |
| Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Ažuriranja kvalitete |
| Projekti V2 (msdyn\_projects) | 1.0.0.2 | Ažuriranja kvalitete |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju aplikacija za financije i operacije. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2227635 | Vrijednosti u poljima **Grupa jedinica** i **Jedinica** zadaju proizvodi u rešetki **Procjene materijala**. |
| Naplata i određivanje cijene | 2234127 | Polje **ID zadatka** sada se ispravno integrira u stvarne podatke projekta na platformi Dataverse tijekom knjiženja fakture dobavljača. |
| Naplata i određivanje cijene | 2235564 | Spremanje retka dnevnika osigurava da se valuta prikazana u stavci retka dnevnika podudara sa zadanom valutom u retku nakon spremanja. |
| Naplata i određivanje cijene | 2246671 | Ako se tijekom fakturiranja transakcija učini nenaplativom, poništava se izvorni nefakturirani zapis o prodaji i stvara se novi nefakturirani zapis o prodaji kao nenaplativ. |
| Naplata i određivanje cijene | 2264042 | Valjani ispravak fakture ne smije se blokirati ako postoji pojedinost ispravka fakture koja nije valjana u okruženju. |
| Naplata i određivanje cijene | 2146367 | Mapiranje dvostrukog pisanja zaglavlja fakture za projekt prošireno je tako da obuhvaća uvjete plaćanja. |
|   Upravljanje prilikama | 2086888 | Nemojte dodavati uloge i kategorije koje su deaktivirane prije kopiranja ponude u uloge koje se naplaćuju i kategorije novokopirane ponude. |
|   Upravljanje prilikama | 2234376 | Polja samo za čitanje su zasivljena u rešetki **Procjene materijala**. |
|   Upravljanje prilikama | 2238337 | Ponuda koja se temelji na kontaktu može se spremiti čak i ako nije povezana s cjenikom za projekt. |
|   Upravljanje prilikama | 2239810 | Zatvaranje ponude kao izgubljene također zatvara povezani projekt i otkazuje sve rezervacije. |
| Planiranje i praćenje projekta | 2099559 | Dodane su dodatne provjere stanja sustava prije otvaranja rešetke **Projektni zadaci**. |
| Planiranje i praćenje projekta | 2178987 | Ispravljena je prijelazna pogreška koja se javlja pri odabiru mogućnosti **Sljedeća razina** na stranici **Projekt**. |
| Upravljanje resursima | 2224817 | Funkcija za proširenje rezervacija zadana je na točno stanje rezervacije. |
| Vremenski unos | 2202476 | Stranica **Vremenski unos** sada upotrebljava kontrolu reakcije rešetke i rješava probleme poput odstupanja rešetke. |
| Vremenski unos | 2223377 | Vremenski unos skriven je od odjeljka **Povezano** na stranici **Resursi koji se mogu rezervirati** kako bi se izbjegla zabuna s uporabljivošću. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations za scenarije koji se temelje na resursu: Ponudu nije moguće pretvoriti u dobivenu zbog pogreške integracije. |
| Upravljanje projektom i računovodstvo | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Prikazuje se pogreška kada pokušate povezati redak ugovora s ID-om projekta zbog provjere preklapanja redaka ugovora i vrsta transakcija. |
| Upravljanje projektom i računovodstvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** postavlja adresu fakture izvora financiranja od drugog klijenta. |
| Putovanje i trošak | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Može doći do pogreške knjiženja povezane s postavljanjem kilometraže. |
| Putovanje i trošak | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funkcija **Razdvoji na osobne** za transakcije deviznih troškova ne funkcionira. |
| Putovanje i trošak | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Vrijednosti padajućeg izbornika kategorije troškova prikazuju pogrešne kategorije za delegate bez obzira jesu li oni resurs. |
| Putovanje i trošak | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Ne možete spremiti izvješće o troškovima među poduzećima unutar tvrtke zbog pogreške pri **Provjeri valjanosti resursa/kategorije**. |
| Putovanje i trošak | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Pogrešan izračun cijene kilometraže u knjiženju izvješća o troškovima ima podijeljene retke. |
| Putovanje i trošak | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Ne možete knjižiti izvješće o troškovima među poduzećima unutar tvrtke kad je uključen porez na promet i kada je vrsta transakcijskog računa na načinu plaćanja **Radnik**. |
| Putovanje i trošak | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Vraćanje u prethodno stanje podatkovnog entiteta **TrvRequisitionLine** i jedinstveni indeks povezani su. |
| Putovanje i trošak | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Izvješće o troškovima podržava stvaranje i ažuriranje retka izvornog dokumenta. |
| Putovanje i trošak | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Prikazivao se neispravan dnevnik sporedne knjige u scenariju među poduzećima iste tvrtke ako je porez na promet knjižen u odredišnu pravnu osobu. |
| Putovanje i trošak | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Procjena troškova ne briše se iz aplikacije Financije kad je izbrisana s platforme Dataverse. |
| Putovanje i trošak | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kada je kategorija troškova kategorija koja nije projekt, financijske veličine koje su odabrane na stranici **Troškovi** ne kopiraju se u izvješće o troškovima. |
