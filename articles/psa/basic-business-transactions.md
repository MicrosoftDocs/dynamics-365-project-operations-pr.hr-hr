---
title: Poslovne transakcije
description: Ova tema pruža informacije o poslovnim transakcijama.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 68506142c5cd046806bc085f297ac928b0c94440
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291205"
---
# <a name="business-transactions"></a>Poslovne transakcije

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U Dynamics 365 Project Service Automation, *poslovna transakcija* je apstraktni koncept kojeg ne predstavlja entitet. Međutim, neka uobičajena polja i procesi na entitetima osmišljeni su za korištenje koncepta poslovnih transakcija. Sljedeći entiteti koriste ovu apstrakciju:

- Detalji retka ponude
- Detalji retka ugovora
- Reci procjene
- Reci u dnevniku
- Stvarne vrijednosti

Od tih entiteta, pojedinosti retka ponude, pojedinosti retka ugovora i reci procjene mapiraju se u fazu procjene u životnom ciklusu projekta. Reci u dnevniku i entiteti Stvarne vrijednosti mapiraju se u fazu izvršavanja u životnom ciklusu projekta.

PSA obrađuje zapise u tih pet entiteta kao poslovne transakcije. Jedina je razlika u tome što se zapisi u entitetima koji su mapirani u fazu procjene smatraju financijskim prognozama, dok se zapisi u entitetima koji su mapirani u fazu izvršenja smatraju financijskim činjenicama koje su se već dogodile.

Za dodatne informacije, pogledajte [Procjene](estimates.md) i [Stvarne vrijednosti](actuals.md)

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije
Sljedeći koncepti jedinstveni su za koncept poslovnih transakcija:

- Vrsta transakcije
- Razred transakcije
- Porijeklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Vrsta transakcije

Vrsta transakcije predstavlja vrijeme i kontekst financijskog učinka na projekt. Predstavljena je skupom mogućnosti koji ima sljedeće podržane vrijednosti u sustavu PSA:
- Trošak
- Ugovor projekta
- Nenaplaćena prodaja
- Naplaćena prodaja
- Međuorganizacijska prodaja
- Jedinična cijena resursa

### <a name="transaction-class"></a>Razred transakcije

Razred transakcije predstavlja različite vrste troškova nastalih na projektima. Predstavljena je skupom mogućnosti koji ima sljedeće podržane vrijednosti u sustavu PSA:

- Time
- Trošak
- Materijal
- Naknada
- Ključna točka
- Porez

Vrijednost **Ključna točka** obično se koristi za poslovnu logiku za naplatu fiksne cijene u sustavu PSA.

### <a name="transaction-origin"></a>Porijeklo transakcije

Izvor transakcije entitet je koji pohranjuje izvor svake poslovne transakcije. Kako se projekt izvršava, svaka poslovna transakcija stvorit će još jednu poslovnu transakciju koja će zauzvrat stvoriti sljedeću i tako dalje. Entitet koji je izvor transakcije dizajniran je za pohranjivanje podataka o izvoru svake transakcije kako bi se pomoglo izvješćivanje i mogućnost praćenja. 

### <a name="transaction-connection"></a>Veza transakcije

Veza transakcije entitet je koji pohranjuje odnos između dviju sličnih poslovnih transakcija, kao što su troškovi i povezane prodajne stvarne vrijednosti ili preokreti transakcija koje pokreću aktivnosti naplate kao što su potvrda fakture ili ispravci fakture.

Zajedno, entiteti Porijeklo transakcije i Veza transakcije pomažu vam da pratite odnose između poslovnih transakcija i radnji koje su rezultirale izradom određene poslovne transakcije.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Primjer: kako Porijeklo transakcije funkcionira s Vezom transakcije

Sljedeći primjer prikazuje tipičnu obradu unosa vremena u životnom ciklusu projekta sustava PSA.

> ![Vrijeme obrade u životnom ciklusu Project Service](media/basic-guide-17.png)
 
1. Slanje unosa vremena uzrokuje izradu dvaju redaka u dnevniku: jedan za trošak i jedan za nenaplaćene prodaje.
2. Eventualno odobrenje unosa vremena uzrokuje izradu dvaju stvarnih podataka: jedan za trošak i jedan za nenaplaćene prodaje.
3. Kada korisnik izradi projektnu fakturu, transakcija retka fakture izrađuje se s pomoću podataka iz nenaplaćenih prodajnih stvarnih podataka. 
4. Kada je faktura potvrđena, stvaraju se dva nova stvarna podatka: nenaplaćena stornirana prodaja i fakturirani prodajni stvarni podatak.

Svaki od tih događaja pokreće izradu zapisa u entitetima Porijeklo transakcije i Veza transakcije kako bi se pomoglo izgraditi trag odnosa između tih zapisa koji su izrađeni u unosu vremena, retku u dnevniku, stvarnim vrijednostima i pojedinostima retka fakture.

Sljedeća tablica prikazuje zapise u entitetu Porijeklo transakcije za prethodni tijek rada.

| Događaj                        | Porijeklo                   | Vrsta porijekla                       | Transakcija                       | Vrsta transakcije         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Slanje unosa vremena        | GUID zapis unosa vremena   | Unos vremena                        | GUID zapis retka u dnevniku (trošak)   | Redak u dnevniku             |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis retka u dnevniku (prodaja)  | Redak u dnevniku                      |                          |
| Odobrenje vremena                | GUID zapis retka u dnevniku | Redak u dnevniku                      | GUID zapis nenaplaćene prodaje        | Stvarna vrijednost                   |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis nenaplaćene prodaje        | Stvarna vrijednost                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID zapis stvarne vrijednosti troškova           | Stvarna vrijednost                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis stvarne vrijednosti troškova           | Stvarna vrijednost                            |                          |
| Izrada fakture             | GUID zapis unosa vremena   | Unos vremena                        | GUID transakcija retka fakture     | Transakcija retka fakture |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID transakcija retka fakture     | Transakcija retka fakture          |                          |
| Potvrda fakture         | GUID redak fakture        | Redak fakture                      | GUID zapis naplaćene prodaje          | Stvarni posao                   |
| GUID faktura                 | Faktura                  | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID detalji retka fakture     | Pojedinost retka fakture      | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID povrat nenaplaćene prodaje      | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID povrat nenaplaćene prodaje      | Stvarni posao                            |                          |
| Nacrt ispravka fakture     | Stari ILD GUID             | Transakcija retka fakture          | Ispravak ILD GUID               | Transakcija retka fakture |
| Stari IL GUID                  | Redak fakture             | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| Stara GUID faktura             | Faktura                  | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| GUID zapis unosa vremena       | Unos vremena               | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| Potvrđeni ispravak fakture | Stari ILD GUID             | Transakcija retka fakture          | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                   |
| Stari IL GUID                  | Redak fakture             | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| Stara GUID faktura             | Faktura                  | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| Stari ILD GUID                 | Transakcija retka fakture | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Stari IL GUID                  | Redak fakture             | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Stara GUID faktura             | Faktura                  | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Ispravak ILD GUID          | Transakcija retka fakture | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Ispravak IL GUID           | Redak fakture             | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Ispravak GUID faktura      | Faktura                  | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |

Sljedeća tablica prikazuje zapise u entitetu Transakcijska veza za prethodni tijek rada.

| Događaj                          | Transakcija 1                 | Uloga transakcije 1 | Vrsta transakcije 1           | Transakcija 2                | Uloga transakcije 2 | Vrsta transakcije 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Slanje unosa vremena          | redak u dnevniku (prodaja) GUID     | Nenaplaćena prodaja     | msdyn_journalline            | Redak u dnevniku (trošak) GUID     | Trošak               | msdyn_journalline  |
| Odobrenje vremena                  | Nenaplaćeni stvarni podaci (prodaja) GUID  | Nenaplaćena prodaja     | msdyn_actual                 | Stvarni podaci troška(trošak) GUID       | Trošak               | msdyn_actual       |
| Izrada fakture               | GUID detalji retka fakture      | Naplaćena prodaja       | msdyn_invoicelinetransaction | Nenaplaćena prodaja stvarni podaci GUID   | Nenaplaćena prodaja     | msdyn_actual       |
| Potvrda fakture           | Storniranje stvarnih podataka GUID         | Storniranje          | msdyn_actual                 | Izvorna nenaplaćena prodaja GUID | Izvorna           | msdyn_actual       |
| Naplaćena prodaja GUID              | Naplaćena prodaja                  | msdyn_actual       | Nenaplaćena prodaja stvarni podaci GUID   | Nenaplaćena prodaja               | msdyn_actual       |                    |
| Nacrt ispravka fakture       | GUID transakcija retka fakture | Zamjena          | msdyn_invoicelinetransaction | Naplaćena prodaja GUID            | Izvorna           | msdyn_actual       |
| Potvrdi ispravak fakture     | Storniranje naplaćene prodaje GUID    | Storniranje          | msdyn_actual                 | Naplaćena prodaja GUID            | Izvorna           | msdyn_actual       |
| Novi GUID stvarni podaci nenaplaćene prodaje | Zamjena                     | msdyn_actual       | Naplaćena prodaja GUID            | Izvorna                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]