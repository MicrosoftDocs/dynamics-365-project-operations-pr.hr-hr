---
title: Novosti u srpnju 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha za srpanj 2021. godine.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 69507427521466335df9cbbaba79db1cfc7be91386b8b2ded5b1c384555946ee
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008037"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u srpnju 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

   - Project Operations u okruženju platforme Microsoft Dataverse verzije 4.12.0.148 ili 4.12.0.152.
   - Upravljanje projektima i računovodstvo u okruženju aplikacije Dynamics 365 Finance verzije 10.0.20.

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Omogućivanje administratorima da vide PSS zapisnike i zapisnike Operations Set iz izbornika postavki. Zapisnici se čuvaju 90 dana.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations.

Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane tablične karte dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti na stranici **Dvostruko pisanje** u stupcu **Verzija**. Aktivirajte novu verziju karte odabirom mogućnosti **Verzije tabličnih karata**, odabirom najnovije verzije, a zatim spremanjem odabrane verzije. Ako ste prilagodili gotovu kartu tablice, ponovite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem s nedostatkom stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke**              | **Broj reference** | **Ažuriranja kvalitete**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naplata i određivanje cijene           | 2224046              | Polje **Klasa transakcije** može se uređivati na kartici **Pojedinosti retka ponude**, ali je zaključano ako radite sa stranice **Pojedinosti ponude** stranica.                                                                     |
| Naplata i određivanje cijene           | 2224400              | Radnja **Zatvori ponudu kao dobivenu** ne uspijeva kada ponuda ne sadrži datumske kontrolne točke.                                                                                                                                    |
| Naplata i određivanje cijene           | 2234089              | Kada ručno unesete opis proizvoda, on se briše nakon što unesete količinu za procjenu materijala.                                                                                                                         |
| Naplata i određivanje cijene           | 2234100              | Rešetka **Postavljanje zadatka za naplatu** ne uključuje stupac **Materijal** i to je vrijednost na kartici projekta **Zadatak naplate**.                                                                                                       |
| Naplata i određivanje cijene           | 2277409              | ID proizvoda nije dostupan u pojedinostima retka ugovora za redak vrste materijala.                                                                                                                                        |
| Naplata i određivanje cijene           | 2281728              | Stvaranje retka ugovora nepotrebno preispituje stvarne podatke uzrokujući značajno povećanje količine podataka, što utječe na učinkovitost.                                                                                |
| Naplata i određivanje cijene           | 2298668              | Redci dnevnika povezani s opozvanim i izbrisanim troškom ne uklanjaju se.                                                                                                                                     |
| Naplata i određivanje cijene           | 2300192              | Kada više korisnika uređuje fakturu, moguće je stvoriti novu pojedinost retka fakture na potvrđenoj fakturi.                                                                                   |
| Naplata i određivanje cijene           | 2301569              | Računi se ne mogu ispraviti ako se primijeni akontacija u iznosu od \$0.                                                                                                                                        |
| Naplata i određivanje cijene           | 2307965              | Do pogreške dolazi ako se cijena kategorije stvara s vrijednostima koje nedostaju.                                                                                                                           |
| Naplata i određivanje cijene           | 2326870              | Do pogreške dolazi u **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** ako je **kôd vrste proizvoda** nula.                                                                            |
| Naplata i određivanje cijene           | 2332732              | Do pogreške dolazi ako se kontrolna točka u retku ugovora stvara bez retka narudžbe.                                                                                                                |
| Planiranje i praćenje projekta | 2181094              | API za planiranje projekata sada podržava PSS zapisnike i zapisnike Operacijskih skupova koji se pohranjuju 90 dana.                                                                                                                  |
| Planiranje i praćenje projekta | 2254201              | Oznaka **Način rasporeda** ažurira se pojedinostima koje opisuju logiku zadanih vrijednosti.                                                                                                                                      |
| Planiranje i praćenje projekta | 2300252              | Predmemorija odgovora **openProject** ažurira se i vlasnika tokena uključuje u ključ predmemorije, **osnovna URL-adresa**, i **URL-adresa segmenta** tako da se **URL-adresa zahtjeva** uvijek može ponovno stvoriti ako se **osnovna URL-adresa** promjeni. |
| Planiranje i praćenje projekta | 2301312              | **msdyn_membershipstatus** je uklonjen iz pregleda **Član projektnog tima**.                                                                                                                                        |
| Planiranje i praćenje projekta | 2302759              | Proizvodi se nepotrebno dohvaćaju na karticama **Dodjela resursa**, **Procjene** i **Procjene troškova**.                                                                                                        |
| Planiranje i praćenje projekta | 2308050              | **CopyProject** ne uspijeva uz pogrešku „Nije uspjelo dohvaćanje tokena za razgovor s udaljenom uslugom”.                                                                                                                           |
| Planiranje i praćenje projekta | 2322650              | Prikaz **Popis projektnih zadataka** ažuriran je tako da prema zadanim postavkama prikazuje datum zadatka.                                                                                                            |
| Planiranje i praćenje projekta | 2327266              | **CopyProject** generira pogrešku „Ključ nije pronađen u rječniku” tijekom kopiranja procjena.                                                                                                      |
| Planiranje i praćenje projekta | 2328123              | **CopyProject** generira pogrešku „Nije uspjelo dohvaćanje tokena za razgovor s udaljenom uslugom”.                                                                                                                          |
| Planiranje i praćenje projekta | 2336258              | **CopyProject** pogrešno kopira nazive položaja resursa.                                                                                                                                                 |
| Naplata i određivanje cijene           | 2224476              | Polje **Resursi koji se mogu rezervirati** nije ispravno zadano za prijavljenog korisnika na stranici **Uporaba materijala**.                                                                                                            |
| Upravljanje resursima           | 2277249              | Do pogreške dolazi kada se ažurira zahtjev za resursom koji se ne temelji na projektu.                                                                                                            |
| Upravljanje resursima           | 2323869              | Uporaba resursa ne prepoznaje ispravno filtrirane resurse.                                                                                                                                             |
| Vrijeme i trošak              | 2176538              | Pogrešni operatori filtra primjenjuju se na kontrolu **Vremenski unos**.                                                                                                                                                   |
| Vrijeme i trošak              | 2177462              | Brisanje vremenskog unosa u rešetki ne ažurira stanje gumba **Pošalji**, **Podsjeti**, **Izbriši** i **Uredi unos** prema očekivanjima.                                                                                        |
| Vrijeme i trošak              | 2299985              | **TimeEntriesImportFromResourceAssignment** ne održava vrijeme početka/završetka iz kontura dodjele.                                                                                                  |
| Vrijeme i trošak              | 2318426              | Nakon slanja vremenskog unosa, zaključana se polja i dalje mogu uređivati.                                                                                                                                   |
| Vrijeme i trošak              | 2323749              | Do pogreške dolazi kada se trošak stvara iz kartice **Povezano** resursa koji se može rezervirati.                                                                                                      |
| Vrijeme i trošak              | 2327678              | Kada vremenski unos stvarate iz kartice **Povezano** resursa koji se može rezervirati, nadređeni se resurs ne prosljeđuje kontroli vremenskog unosa.                                                                            |
| Općenito                       | 2296857              | Praćenje napretka za dugotrajne poslove.                                                                                                                                                                        |
| Općenito                       | 2253682              | Rješenje dvostrukog pisanja u aplikaciji Project Operations ne bi trebalo instalirati kada je jezgra dvostrukog pisanja instalirana u okruženje bez rješenja za organizaciju dvostrukog pisanja.                                                |
| Općenito                       | 2316420              | Priprema jezgre aplikacije Project Service ne uspijeva ako se promijeni poslovna jedinica korisnika aplikacije.                                                                                                                     |
| Općenito                       | 2376405              | Riješen je problem s ažuriranjem koje je proveo izdavač (ažuriranje kvalitete dostupno je u verziji 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke                      | Broj reference | Ažuriranja kvalitete                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upravljanje projektom i računovodstvo | 4620267          | Nije moguće prilagoditi obrasce za dodavanje polja **Svrha** stranicama **Proknjižena transakcija projekta**, **Stvaranje prijedloga fakture** i **Prijedlog fakture**.                                                                                                                                                                                         |
| Upravljanje projektom i računovodstvo | 4613449          | Kada u aplikaciji Financije odaberete ID ugovora o projektu, integrirano okruženje aplikacije Project Operations otvara stranicu za stvaranje novog zapisa, umjesto stranice za već stvorene ugovore o projektu.                                                                                                                                           |
| Upravljanje projektom i računovodstvo | 4614445          | U implementaciji scenarija integracije aplikacije Project Operations nije moguće uređivati polje **Grupa poreza na promet stavke** na prijedlogu fakture uvezenom iz faza. Grupu poreza na promet stavki treba uređivati za otvoreni prijedlog fakture svih vrsta transakcija, uključujući račun, radno vrijeme, troškove, naknade i stavke. |
| Upravljanje projektom i računovodstvo |                  | Nije moguće knjižiti prijedlog fakture što je rezultat ispravka negativne vremenske transakcije.                                                                                                                                                                                                                                              |
| Upravljanje projektom i računovodstvo |                  | Redci prijedloga fakture duplicirani su zbog višestrukih povremenih postupaka **Uvoz iz faza** koji se odvijaju istodobno.                                                                                                                                                                                                                |

