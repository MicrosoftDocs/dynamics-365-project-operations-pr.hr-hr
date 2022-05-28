---
title: Novosti u veljači 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom tema pružaju se informacije o ažuriranjima kvalitete koja su dostupna u izdanju projektnih operacija u veljači 2022. za scenarije koji se temelje na resursima/nenaseljenim resursima.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600825"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u veljači 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ovaj tema odnosi se na sljedeće microsoftove Dynamics 365 Project Operations komponente i verzije :

- Operacije projekta u verziji okruženja Dataverse 4.28.0.120
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance verziji okruženja 10.0.24

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

- Od ovog izdanja možete dodati do 300 članova tima u jedan projekt. Ranije je ograničenje broja članova tima bilo 150. Dodatne informacije potražite u članku [Ograničenja projekta](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Ažuriranja karte s dvostrukim pisanjem project operations

Sljedeći popis prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanju Project Operations veljače 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| --- | --- | --- |
| Izvozni subjekt troškova integracije projektnih troškova integracije projekta (msdyn\_ troškovi) | 1.0.0.3 | Prošireno za sinkronizaciju projektnih aktivnosti u Dataverse. |

Trenutni popis i verzije karata s dvostrukim pisanjem project operations potražite u članku [Verzije karte s dvostrukim pisanjem programa Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako prilikom pokretanja karte naiđete na problem, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2415109 | Zadana vrijednost u **polju Uvjeti** plaćanja Operacije moraju biti zapis kupca ugovora o projektu i zapis predračunske fakture. |
| Naplata i određivanje cijene | 2497369 | Korekcija materijala mora slijediti vrijednost datuma u parametrima **Ispravak**. |
| Naplata i određivanje cijene | 2498697 | Poboljšana je konfiguracija sigurnosti za **opoziv** unosa vremena. |
| Naplata i određivanje cijene | 2513824 | Za scenarije temeljene na resursima ID kategorije transakcije ne smije biti dulji od 28 znakova u operacijama projekta. |
| Naplata i određivanje cijene | 2517455 | Ne **smije se dopustiti da se akcija osvježavanja transakcija retka fakture** pokreće više puta istovremeno za istu fakturu. |
| Naplata i određivanje cijene | 2517465 | Akcija Deaktiviraj detalje retka **fakture** blokirana je jer nije podržana. |
| Naplata i određivanje cijene | 2556660 | Fiksna je provjera efektivnosti datuma izvršena na cjeniku koji je priložen zapisu parametara projekta. |
|   Upravljanje prilikama | 2369202 | Ispravljena je poslovna logika kojom se provjerava mogu li se cjenici koji imaju preklapajuće datume efektivnosti priložiti istom ugovoru o projektu. |
|   Upravljanje prilikama | 2385965 | Ispravljeno je ponašanje na kartici Kupci **na** stranici Ugovor **o** projektu kada odaberete **Spremi i zatvori**. |
| Vrijeme i trošak | 2538503 | Projektni zadatak mora biti dostupan u entitetu **Stvarni projekt nakon knjiženja izvješća o troškovima**. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo na Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Tijekom uvoza kreditnih bilješki dobavljača pojavljuje se pogreška. U poruci o pogrešci stoji: "Iznos zadržavanja ne može biti veći od preostalog neto iznosa." |
| Upravljanje projektom i računovodstvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ako prijedlog fakture uključuje transakcije s nultim iznosom naknade koje su neplaćene prodajne stvarne, fakturiranje se ne može dogoditi. |
| Upravljanje projektom i računovodstvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Proknjiženi trošak nije točan nakon ažuriranja nabavne cijene i **omogućeno je aktiviranje upravljanja** promjenama.|
| Upravljanje projektom i računovodstvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Procjena knjiženja za projekt s fiksnom cijenom koristi netočnu valutu i iznos u vrijednosnom kuponu za procjenu, čak i kada je omogućena značajka Omogući valutu **ugovora o projektu za izračun** procjene. |
| Upravljanje projektom i računovodstvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **Proširenje\_ ProjDMFDataPopulation** ne bi trebalo upućivati poziv kako bi se omogućilo praćenje promjena bez hvatanja iznimaka za entitete koji imaju konfiguracijske tipke koje nisu omogućene. |
| Upravljanje projektom i računovodstvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Obrada se fiksira kada se proknjiži više naprednih temeljnica i pojavi se pogreška. |
| Putovanje i trošak | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Zbog problema s nagodbom koji se odnosi na novčane predujmove na izvješćima o troškovima, iznos poreza nije pokriven kao dio gotovinskog predujma. |
| Putovanje i trošak | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Podaci o porezu na promet nisu obuhvaćeni izvješćem **Trošak - proknjižene transakcije**. |
| Putovanje i trošak | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Kršenje **pravila o obveznim** troškovima primki pogrešno prikazuje upozorenje o izvješćima o troškovima. |
| Putovanje i trošak | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projektna transakcija ne uključuje porez na promet koji se ne može nadoknaditi u ukupnom iznosu prodaje kada je transakcija rezultat troška kilometraže. |
| Putovanje i trošak | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kada redak po stavkama ima porez, ne možete promijeniti datum retka artikla i pojavljuje se pogreška stanja izvornog dokumenta. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarjele značajke

Uklonjene [ili zastarjele značajke u projektnim operacijama](removed-depreciated-features-project.md) tema opisuju značajke koje su uklonjene ili zastarjele za Dynamics 365 Project Operations.

- Značajka uklonjeno više nije dostupna u proizvodu.
- Zastarjela značajka nije u aktivnom razvoju i može se ukloniti u budućem ažuriranju.

Najava omalovažavanja pojavit će se u [značajkama Uklonjeno ili zastarjelo u projektnim operacijama](removed-depreciated-features-project.md) tema 12 mjeseci prije nego što se bilo koja značajka ukloni iz proizvoda.

Za razbijanje promjena koje utječu samo na vrijeme kompilacije, ali su binarno kompatibilne s sandboxom i proizvodnim okruženjima, vrijeme omalovažavanja bit će manje od 12 mjeseci. Obično su te promjene funkcionalna ažuriranja koja se moraju izvršiti na kompajleru.
