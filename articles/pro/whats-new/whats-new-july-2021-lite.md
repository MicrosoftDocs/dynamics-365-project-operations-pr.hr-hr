---
title: Što je novo u srpnju 2021. – implementacija osnovne aplikacije Project Operations
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju implementacije osnovne aplikacije Project Operations u srpnju 2021. godine.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009207"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Što je novo u srpnju 2021. – implementacija osnovne aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations u okruženju platforme Dataverse verzije 4.12.0.148 ili 4.12.0.152.

## <a name="quality-updates"></a>Ažuriranja kvalitete
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
