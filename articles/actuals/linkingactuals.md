---
title: Povezivanje stvarnih podataka s izvornim zapisima
description: U ovoj se temi objašnjava način povezivanja stvarnih podataka s izvornim zapisima, poput vremenskog unosa, unosa troškova ili zapisnika o uporabi materijala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991747"
---
# <a name="link-actuals-to-original-records"></a>Povezivanje stvarnih podataka s izvornim zapisima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


U aplikaciji Dynamics 365 Project Operations, *poslovna transakcija* apstraktni je koncept kojeg ne predstavlja entitet. Međutim, neka uobičajena polja i procesi na entitetima osmišljeni su za korištenje koncepta poslovnih transakcija. Ovaj koncept upotrebljavaju sljedeći entiteti:

- Detalji retka ponude
- Detalji retka ugovora
- Reci procjene
- Reci u dnevniku
- Stvarne vrijednosti

Od tih entiteta, **Pojedinosti retka ponude**, **Pojedinosti retka ugovora** i **Redci procjene** mapiraju se u fazu procjene u životnom ciklusu projekta. **Redci dnevnika** i **Entiteti stvarnih vrijednosti** mapiraju se u fazu izvršavanja u životnom ciklusu projekta.

Project Operations prepoznaje zapise u tih pet entiteta kao poslovne transakcije. Jedina je razlika u tome što se zapisi u entitetima koji su mapirani u fazu procjene smatraju financijskim prognozama, dok se zapisi u entitetima koji su mapirani u fazu izvršenja smatraju financijskim činjenicama koje su se već dogodile.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije
Sljedeći koncepti jedinstveni su za koncept poslovnih transakcija:

- Vrsta transakcije
- Razred transakcije
- Porijeklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Vrsta transakcije

Vrsta transakcije predstavlja vrijeme i kontekst financijskog učinka na projekt. To je predstavljeno skupom mogućnosti koji ima sljedeće podržane vrijednosti u sustavu Project Operations:

  - Cijena
  - Ugovor o projektu
  - Nenaplaćene prodaje
  - Naplaćene prodaje
  - Međuorganizacijska prodaja
  - Jedinična cijena resursa

### <a name="transaction-class"></a>Razred transakcije

Razred transakcije predstavlja različite vrste troškova nastalih na projektima. To je predstavljeno skupom mogućnosti koji ima sljedeće podržane vrijednosti u sustavu Project Operations:

  - Vrijeme
  - Izdatak
  - Materijal
  - Naknada
  - Kontrolna točka
  - Porez

**Kontrolnu točku** obično upotrebljava poslovna logika za naplatu fiksne cijene u sustavu Project Operations.

### <a name="transaction-origin"></a>Porijeklo transakcije

**Izvor transakcije** entitet je koji pohranjuje izvor svake poslovne transakcije. Kako se projekt odvija, svaka poslovna transakcija stvorit će drugu poslovnu transakciju koja će stvoriti novu i tako dalje. Entitet izvora transakcije dizajniran je za pohranu podataka o izvoru svake transakcije radi lakšeg izvješćivanja i mogućnosti praćenja. 

### <a name="transaction-connection"></a>Veza transakcije

**Veza transakcije** entitet je koji pohranjuje odnos između dviju sličnih poslovnih transakcija, kao što su troškovi i povezane prodajne stvarne vrijednosti ili preokreti transakcija koje pokreću aktivnosti naplate kao što su potvrda fakture ili ispravci fakture.

Zajedno, entiteti **Izvor transakcije** i **Veza transakcije** pomažu vam pri praćenju odnosa između poslovnih transakcija i radnji iz kojih su proizašle određene poslovne transakcije.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Primjer: kako Porijeklo transakcije funkcionira s Vezom transakcije

Sljedeći primjer prikazuje tipičnu obradu unosa vremena u životnom ciklusu projekta sustava Project Operations.

> ![Vrijeme obrade u životnom ciklusu Project Service.](media/basic-guide-17.png)
 
1. Slanje vremenskog unosa stvara dva retka dnevnika: jedan za trošak, a drugi za nenaplaćene prodaje.
2. Eventualno odobrenje vremenskog unosa stvara dva stvarna podataka: jedan stvarni podatak za trošak, a drugi za nenaplaćene prodaje.
3. Kada se stvori nova faktura za projekt, transakcija retka fakture stvara se s pomoću podataka iz stvarnih podataka o nenaplaćenoj prodaji. 
4. Kada je faktura potvrđena, stvaraju se dva nova stvarna podatka: stvarni podatak o storniranju nenaplaćene prodaje i stvarni podatak o naplaćenoj prodaji.

Svaki od ovih događaja stvara zapis u entitetima **Izvor transakcije** i **Veza transakcije**. Ovi novi zapisi pomažu pri stvaranju povijesti odnosa između zapisa stvorenih preko vremenskog unosa, retka dnevnika, stvarnih podataka i pojedinostima retka fakture.

Sljedeća tablica prikazuje zapise u entitetu **Izvor transakcije** za tijek rada.

| Događaj                        | Podrijetlo                   | Vrsta porijekla                       | Transakcija                       | Vrsta transakcije         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Slanje unosa vremena        | GUID zapis vremenskog unosa   | Vremenski unos                        | GUID zapis retka u dnevniku (trošak)   | Redak u dnevniku             |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis retka u dnevniku (prodaja)  | Redak u dnevniku                      |                          |
| Odobrenje vremena                | GUID zapis retka u dnevniku | Redak u dnevniku                      | GUID zapis nenaplaćene prodaje        | Stvarna vrijednost                   |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis nenaplaćene prodaje        | Stvarna vrijednost                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID zapis stvarne vrijednosti troškova           | Stvarna vrijednost                            |                          |
| GUID zapis unosa vremena       | Vremenski unos               | GUID zapis stvarne vrijednosti troškova           | Stvarno                            |                          |
| Izrada fakture             | GUID zapis vremenskog unosa   | Vremenski unos                        | GUID transakcija retka fakture     | Transakcija retka fakture |
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

Tablica u nastavku prikazuje zapise u entitetu **Veza transakcije** za tijek rada.

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
